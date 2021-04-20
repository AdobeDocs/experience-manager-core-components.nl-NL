---
title: Inclusief clientbibliotheken
description: Afhankelijk van uw gebruiksscenario zijn er verschillende manieren om clientbibliotheken op te nemen.
role: Architect, Developer, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 2%

---


# Inclusief clientbibliotheken {#including-client-libraries}

Er zijn een aantal verschillende manieren om [cliëntbibliotheken](/help/developing/archetype/uifrontend.md#clientlibs) afhankelijk van uw gebruiksgeval op te nemen. Dit document bevat voorbeelden en voorbeelden [HTL-fragmenten](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) voor beide.

## Aanbevolen standaardgebruik {#recommended-default-usage}

Als u geen tijd hebt om te onderzoeken wat het beste in uw situatie is, dan omvat uw cliëntbibliotheken door de volgende lijnen van HTML binnen uw pagina `head` element te plaatsen:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Dit omvat zowel het CSS als JS in uw pagina `head`, maar het toevoegen van `defer` attribuut aan uw JS `script` omvat, zodat browsers op DOM wachten alvorens uw manuscripten uit te voeren, en daarom optimaliserend de snelheid van de paginading.

## Standaardgebruik {#basic-usage}

De basissyntaxis voor zowel JS als CSS van een categorie van de cliëntbibliotheek, die alle overeenkomstige CSS `link` elementen en/of JS `script` elementen zal produceren, is als volgt:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Als u hetzelfde wilt doen voor meerdere clientbibliotheekcategorieën tegelijk, kan een array van tekenreeksen worden doorgegeven aan de parameter `categories`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

## Alleen CSS of JS {#css-js-only}

Vaak wilt u de CSS-include-bestanden in het element HTML `head` plaatsen en de JS-code net vóór het sluiten van het element `body`.

Als u in `head` alleen de CSS en niet de JS wilt opnemen, gebruikt u `cssIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

Gebruik `jsIncludes` voordat u `body` sluit om alleen de JS en niet de CSS op te nemen:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

## Kenmerken {#attributes}

Als u kenmerken wilt toepassen op de gegenereerde CSS `link`-elementen en/of JS `script`-elementen, is een aantal parameters mogelijk:

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

CSS `link`-kenmerken die kunnen worden doorgegeven aan `jsAndCssIncludes` en `cssIncludes`:

* `media`: tekenreeks-JS- `script` kenmerken die kunnen worden doorgegeven aan  `jsAndCssIncludes` en  `jsIncludes`:
* `async`: boolean
* `defer`: boolean
* `onload`: string
* `crossorigin`: string

## {#inlining} onderstrepen

In sommige gevallen, voor optimalisatie, of voor e-mail of [AMP, ](amp.md) zou het kunnen worden vereist om CSS of JS in de output van HTML te inline.

Als u de CSS wilt inline, kunt u `cssInline` gebruiken. In dat geval moet u het omringende `style`-element schrijven:

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

Op dezelfde manier kunt u `jsInline` gebruiken om JS in te line, in welk geval u het omringende `script` element moet schrijven:

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```

## CSS en JavaScript {#context-aware-loading} laden met behoud van context

De [Paginacomponent](/help/components/page.md) ondersteunt ook het laden van door ontwikkelaars gedefinieerde contextgevoelige CSS-, JavaScript- of metatags.

Dit wordt gedaan door een [context-bewuste middel](context-aware-configs.md) voor `com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig` te creëren gebruikend de volgende structuur:

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
