---
title: Inclusief clientbibliotheken
description: Afhankelijk van uw gebruiksscenario zijn er verschillende manieren om clientbibliotheken op te nemen.
translation-type: tm+mt
source-git-commit: 87e39566617f64b91bd8e98b3779b9b5c426c31c
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 3%

---


# Inclusief clientbibliotheken {#including-client-libraries}

Afhankelijk van uw gebruiksscenario zijn er verschillende manieren om [clientbibliotheken](/help/developing/archetype/uifrontend.md#clientlibs) op te nemen. Dit document bevat voorbeelden en voorbeelden van [HTML-fragmenten](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) voor beide.

## Aanbevolen standaardgebruik {#recommended-default-usage}

Als u geen tijd hebt om te onderzoeken wat in uw situatie het beste is, dan omvat uw cliëntbibliotheken door de volgende lijnen van HTML binnen uw paginalement te plaatsen `head` :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Dit omvat zowel de CSS als JS in uw pagina `head`, maar het toevoegen van het `defer` attribuut aan uw JS `script` omvat, zodat browsers op DOM wachten klaar te zijn alvorens uw manuscripten uit te voeren, en daarom optimaliserend de snelheid van de paginading.

## Standaardgebruik {#basic-usage}

De basissyntaxis voor zowel JS als CSS van een categorie van de cliëntbibliotheek, die alle overeenkomstige CSS `link` elementen en/of JS `script` elementen zal produceren, is als volgt:

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

Vaak wilt u de CSS-include-bestanden in het HTML- `head` element plaatsen en de JS-code net vóór het sluiten van het `body` element.

Als u in het `head`gedeelte alleen de CSS en niet de JS wilt opnemen, gebruikt u `cssIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

Gebruik vóór het `body` sluiten de volgende opties om alleen de JS en niet de CSS op te nemen `jsIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

## Attributen {#attributes}

Voor het toepassen van kenmerken op de gegenereerde CSS- `link` elementen en/of JS- `script` elementen is een aantal parameters mogelijk:

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

CSS- `link` kenmerken die kunnen worden doorgegeven aan `jsAndCssIncludes` en `cssIncludes`:

* `media`: string

JS- `script` kenmerken die kunnen worden doorgegeven aan `jsAndCssIncludes` en `jsIncludes`:

* `async`: boolean
* `defer`: boolean
* `onload`: string
* `crossorigin`: string

## Invoering {#inlining}

In sommige gevallen, voor optimalisatie, of voor e-mail of [AMP,](amp.md) zou het kunnen worden vereist om CSS of JS in de output van HTML in te line.

Als u de CSS wilt inline, `cssInline` kunt u deze gebruiken. In dat geval moet u het omringende `style` element schrijven:

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

Op dezelfde manier om JS in te zetten, `jsInline` kan worden gebruikt, in welk geval u het omringende `script` element moet schrijven:

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```
