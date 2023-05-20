---
title: Inclusief clientbibliotheken
description: Afhankelijk van uw gebruiksscenario zijn er verschillende manieren om clientbibliotheken op te nemen.
role: Architect, Developer, Admin
exl-id: 84e7c178-247b-42a2-99bf-6d1699ecee14
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 0%

---

# Inclusief clientbibliotheken {#including-client-libraries}

Er zijn een aantal verschillende manieren om op te nemen [clientbibliotheken](/help/developing/archetype/uifrontend.md#clientlibs) afhankelijk van uw gebruiksgeval. Dit document bevat voorbeelden en voorbeelden [HTML-fragmenten](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html) voor elk.

## Aanbevolen standaardgebruik {#recommended-default-usage}

Als u geen tijd hebt om te onderzoeken wat in uw situatie het beste is, dan omvat uw cliëntbibliotheken door de volgende lijnen van HTML binnen uw pagina te plaatsen `head` element:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Dit omvat zowel de CSS als de JS in uw pagina `head`, maar het toevoegen van `defer` attribuut aan uw JS `script` bevat, zodat de browsers wachten totdat de DOM gereed is voordat ze de scripts uitvoeren. Hierdoor wordt de laadsnelheid van de pagina geoptimaliseerd.

## Standaardgebruik {#basic-usage}

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

## Alleen CSS of JS {#css-js-only}

Vaak wilt u de CSS-include-bestanden in de HTML plaatsen `head` en het JS omvat net vóór de sluiting van het `body` element.

In de `head`gebruikt u `cssIncludes`:

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

## Attributen {#attributes}

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

* `media`: string JS `script` kenmerken die kunnen worden doorgegeven aan `jsAndCssIncludes` en `jsIncludes`:
* `async`: boolean
* `defer`: boolean
* `onload`: string
* `crossorigin`: string

## Invoering {#inlining}

In sommige gevallen, voor optimalisatie of voor e-mail of [AMP](amp.md) mogelijk moet u de CSS of JS inline zetten in de uitvoer van de HTML.

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

## CSS en JavaScript met behoud van context laden {#context-aware-loading}

De [Pagina-component](/help/components/page.md) Het laden van door ontwikkelaars gedefinieerde contextgevoelige CSS-, JavaScript- of metatags wordt ook ondersteund.

Dit doet u door een [contextbewuste resource](context-aware-configs.md) for `com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig` met behulp van de volgende structuur:

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
