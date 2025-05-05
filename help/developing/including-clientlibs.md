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

* De **plaats** clientlibs verstrekken het minimalistische functionele gedrag van de componenten die op de plaats moeten worden toegepast.
   * Zij dienen als uitgangspunt om projecten te versnellen, met implementaties die worden aangemoedigd om uit te breiden en [ hen ](/help/developing/customizing.md) aan te passen om de gewenste verschijning en de functionaliteit te bereiken.
* De **redacteur** clientlibs worden toegepast op de auteursdialoog om zijn verwachte functionaliteit en verschijning te verzekeren.
* De **editorhaak** clientlibs worden toegepast op de plaats wanneer geladen op geef wijze uit.
   * Ze bevatten JavaScript-code die wordt uitgevoerd op gebeurtenissen die door de editor worden geactiveerd, waardoor de initialisatie van dynamische functionaliteit wordt vergemakkelijkt.
* Sommige componenten kunnen specifieke extra clientlibs hebben die voor gebruik in bepaalde situaties worden ontworpen, zoals wanneer tewerkgesteld naast [ Dynamic Media ](/help/components/image.md#dynamic-media) bijvoorbeeld.

## Inclusief clientbibliotheken {#including}

Er zijn een aantal verschillende manieren om [ cliëntbibliotheken ](/help/developing/archetype/front-end.md#clientlibs) afhankelijk van uw gebruiksgeval te omvatten. Het volgende is voorbeelden met steekproef [ HTML fragmenten ](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=nl-NL) voor elk.

### Aanbevolen standaardgebruik {#recommended-default-usage}

Als u geen tijd hebt om te onderzoeken wat in uw situatie het beste is, dan omvat uw cliëntbibliotheken door de volgende lijnen van HTML binnen uw pagina `head` element te plaatsen:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Dit omvat zowel de CSS als de JS op de pagina `head` , maar het toevoegen van het `defer` -kenmerk aan uw JS `script` -include-bestanden, zodat de browsers wachten totdat de DOM gereed is voordat ze de scripts uitvoeren. Hierdoor wordt de laadsnelheid van de pagina geoptimaliseerd.

### Standaardgebruik {#basic-usage}

De basissyntaxis voor het opnemen van zowel JS als CSS van een categorie in de clientbibliotheek, die alle bijbehorende CSS `link` -elementen en/of JS `script` -elementen genereert, ziet er als volgt uit:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Als u hetzelfde wilt doen voor meerdere clientbibliotheekcategorieën tegelijk, kan een array met tekenreeksen worden doorgegeven aan de parameter `categories` :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

### Alleen CSS of JS {#css-js-only}

Vaak wilt u de CSS-include-bestanden in het element HTML `head` plaatsen en de JS-code wordt net vóór het sluiten van het element `body` opgenomen.

Als u in `head` alleen de CSS en niet de JS wilt opnemen, gebruikt u `cssIncludes` :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

Gebruik `jsIncludes` vóór het sluiten van `body` om alleen de JS en niet de CSS op te nemen:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

### Attributen {#attributes}

Om kenmerken toe te passen op de gegenereerde CSS `link` -elementen en/of JS `script` -elementen, is een aantal parameters mogelijk:

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

CSS `link` -kenmerken die kunnen worden doorgegeven aan `jsAndCssIncludes` en `cssIncludes` :

* `media`: tekenreeks JS `script` -kenmerken die kunnen worden doorgegeven aan `jsAndCssIncludes` en `jsIncludes` :
* `async` : Boolean
* `defer` : Boolean
* `onload` : tekenreeks
* `crossorigin` : tekenreeks

### Invoering {#inlining}

In sommige gevallen, of voor optimalisering, of voor e-mail of [ AMP, ](amp.md) zou het kunnen worden vereist om CSS of JS in de output van HTML te inline.

Als u de CSS wilt inline, kunt u `cssInline` gebruiken. In dat geval moet u het omringende `style` -element schrijven:

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

Op dezelfde manier kunt u `jsInline` gebruiken om de JS in te line te plaatsen. In dat geval moet u het omringende `script` -element schrijven:

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```

### CSS en JavaScript met behoud van context laden {#context-aware-loading}

De [ Component van de Pagina ](/help/components/page.md) steunt ook ladend ontwikkelaar-bepaalde context-bewuste CSS, JavaScript, of meta markeringen.

Dit wordt gedaan door a [ context-bewuste middel ](context-aware-configs.md) voor `com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig` het gebruiken van de volgende structuur te creëren:

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

[ zie de technische documentatie voor de Component van de Pagina voor meer informatie.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page#loading-of-context-aware-cssjs)
