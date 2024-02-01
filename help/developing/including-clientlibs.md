---
title: Clientbibliotheken en de kerncomponenten
description: De componenten van de Kern komen met een aantal cliëntbibliotheken en bieden de capaciteit aan om uw te omvatten.
role: Architect, Developer, Admin
exl-id: 84e7c178-247b-42a2-99bf-6d1699ecee14
source-git-commit: d39fe0084522f67664203a026340b23d325c1883
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# Clientbibliotheken en de kerncomponenten {#client-libraries}

De componenten van de Kern komen met een aantal cliëntbibliotheken en bieden de capaciteit aan om uw te omvatten.

## Aangeleverde clientbibliotheken {#provided}

De componenten van de Kern verstrekken de volgende cliëntbibliotheken uit-van-de-doos.

* De **site** clientlibs bieden het minimale functionele gedrag van de onderdelen die op de site moeten worden toegepast.
   * Zij dienen als uitgangspunt voor het versnellen van projecten, waarbij implementaties worden aangemoedigd om uit te breiden en [aanpassen](/help/developing/customizing.md) om de gewenste weergave en functionaliteit te verkrijgen.
* De **editor** clientlibs worden toegepast op het ontwerpdialoogvenster om de verwachte functionaliteit en vormgeving ervan te garanderen.
* De **editorhaak** clientlibs worden toegepast op de site wanneer ze in de bewerkingsmodus worden geladen.
   * Ze bevatten JavaScript-code die wordt uitgevoerd op gebeurtenissen die door de editor worden geactiveerd, waardoor de initialisatie van dynamische functionaliteit wordt vergemakkelijkt.
* Sommige componenten kunnen specifieke extra clientlibs hebben die voor gebruik in bijzondere situaties worden ontworpen zoals wanneer gebruikt naast [Dynamic Media](/help/components/image.md#dynamic-media) bijvoorbeeld.

## Inclusief clientbibliotheken {#including}

Er zijn verschillende manieren om op te nemen [clientbibliotheken](/help/developing/archetype/front-end.md#clientlibs) afhankelijk van uw gebruiksgeval. Hier volgen voorbeelden van voorbeelden [HTML-fragmenten](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html) voor elk.

### Aanbevolen standaardgebruik {#recommended-default-usage}

Als u geen tijd hebt om te onderzoeken wat in uw situatie het beste is, dan omvat uw cliëntbibliotheken door de volgende lijnen van HTML binnen uw pagina te plaatsen `head` element:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Dit omvat zowel de CSS als de JS in uw pagina `head`, maar de `defer` attribuut aan uw JS `script` bevat, zodat de browsers wachten totdat de DOM gereed is voordat ze de scripts uitvoeren en de laadsnelheid van de pagina daarom optimaliseren.

### Standaardgebruik {#basic-usage}

De basissyntaxis om zowel JS als CSS van een categorie van de cliëntbibliotheek te omvatten, die al overeenkomstige CSS zal produceren `link` elementen en/of JS `script` de elementen zijn als volgt:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Als u hetzelfde wilt doen voor meerdere clientbibliotheekcategorieën tegelijk, kan een array met tekenreeksen worden doorgegeven aan de `categories` parameter:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

### Alleen CSS of JS {#css-js-only}

Vaak wilt u de CSS-include-bestanden in de HTML plaatsen `head` en het JS omvat net vóór de sluiting van het `body` element.

In de `head`, alleen de CSS, en niet de JS, gebruiken `cssIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

Voor de `body` sluiten, alleen de JS en niet de CSS opnemen, gebruik `jsIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

### Attributen {#attributes}

Kenmerken toepassen op de gegenereerde CSS `link` elementen en/of JS `script` elementen zijn een aantal parameters mogelijk:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base',
    media='print',
    async=true,
    defer=true,
    onload='console.log(\'loaded: \' + this.src)',
    crossorigin='anonymous'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

CSS `link` kenmerken die kunnen worden doorgegeven aan `jsAndCssIncludes` en `cssIncludes`:

* `media`: tekenreeks JS `script` kenmerken die kunnen worden doorgegeven aan `jsAndCssIncludes` en `jsIncludes`:
* `async`: boolean
* `defer`: boolean
* `onload`: string
* `crossorigin`: string

### Invoering {#inlining}

In sommige gevallen, voor optimalisatie of voor e-mail of [AMP,](amp.md) mogelijk moet u de CSS of JS inline zetten in de uitvoer van de HTML.

De CSS inline plaatsen, `cssInline` kan worden gebruikt, in welk geval u de omringende `style` element:

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

Evenzo, om het JS te inline te zetten, `jsInline` kan worden gebruikt, in welk geval u de omringende `script` element:

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```

### CSS en JavaScript met behoud van context laden {#context-aware-loading}

De [Pagina-component](/help/components/page.md) Het laden van door ontwikkelaars gedefinieerde contextgevoelige CSS-, JavaScript- of metatags wordt ook ondersteund.

Dit doet u door een [contextbewuste resource](context-aware-configs.md) for `com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig` de volgende structuur gebruiken:

```text
com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig
    - prefixPath="/some/path"
    + item01
        - element=["link"|"script"|"meta"]
        - location=["header"|"footer"]
        + attributes
            - attributeName01="attributeValue01"
            - attributeName02="attributeValue02"
            ...
    + item02
        ...
    ...
```

[Zie de technische documentatie voor de Component van de Pagina voor meer informatie.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page#loading-of-context-aware-cssjs)
