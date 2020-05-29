---
title: De gegevenslaag van de Adobe-client gebruiken met de kerncomponenten
description: De gegevenslaag van de Adobe-client gebruiken met de kerncomponenten
translation-type: tm+mt
source-git-commit: 539a4250c954ac830731a9ecf010e129b2cf9c3a
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---


# Using the Adobe Client Data Layer with the Core Components {#data-layer-core-components}

Het doel van de gegevenslaag van de Cliënt van Adobe is de inspanning aan instrumentwebsites te verminderen door een gestandaardiseerde methode te verstrekken om om het even welk soort gegevens voor om het even welk manuscript bloot te stellen en toegang te hebben.

The Adobe Client Data Layer is platform agnostic, but is fully integrated into the Core Components for use with AEM.

Like the Core Components, the code for the Adobe Client Data Layer is available on GitHub along with its developer documentation. Dit document geeft een overzicht van hoe de Componenten van de Kern met de Laag van Gegevens in wisselwerking staan, maar de volledige technische details worden uitgesteld aan de documentatie GitHub.

>[!TIP]
>
>Voor meer informatie over de Laag van Gegevens van de Cliënt van Adobe, [verwijs naar de middelen in zijn bewaarplaats GitHub.](https://github.com/adobe/adobe-client-data-layer)
>
>Zie het [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) bestand in de opslagplaats voor kerncomponenten voor meer technische details over de integratie van de Adobe Client Data Layer met de Core Components.


## Installatie en activering {#installation-activation}

Vanaf versie 2.9.0 van de Componenten van de Kern, wordt de Laag van Gegevens gedistribueerd met de Componenten van de Kern als cliëntlib. Installatie is niet nodig.

However the Data Layer is not activated by default. To activate the Data Layer

1. Create the following structure below the `/conf` node:
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
1. Add a boolean property called `enabled` and set it to `true`.
1. Add a `sling:configRef` property to the `jcr:content` node of your site below `/content` (e.g. `/content/<mySite>/jcr:content`) and set it to `/conf/<mySite>`.

Once enabled, you can verify the activation by loading a page of the site outside of the editor. When you inspect the page you will see that the Adobe Client Data Layer is loaded.

## Core Components Data Schemas {#data-schemas}

Het volgende is een lijst van schema&#39;s die de Componenten van de Kern met de Laag van Gegevens gebruiken.

### Component/Container Item Schema {#item}

Het schema Component/Container Item wordt gebruikt in de volgende componenten:

* [Broodkruimel](/help/components/breadcrumb.md)
* [Knop](/help/components/button.md)
* [Taalnavigatie](/help/components/language-navigation.md)
* [Lijst](/help/components/list.md)
* [Navigatie](/help/components/navigation.md)
* [Teaser](/help/components/teaser.md)
* [Tekst](/help/components/text.md)
* [Titel](/help/components/title.md)

Het schema Component/Container Item is als volgt gedefinieerd.

```
id: {                   // component ID
    @type               // resource type
    repo:modifyDate     // last modified date
    dc:title            // title
    dc:description      // description
    xdm:text            // text
    xdm:linkURL         // link URL
    parentId            // parent component ID
}
```


### Paginaschema {#page}

Het paginaschema wordt gebruikt door de volgende component:

* [Pagina](/help/components/page.md)

Het paginaschema wordt als volgt gedefinieerd.

```
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    xdm:tags            // page tags
    repo:path           // page path
    xdm:template        // page template
    xdm:language        // page language
}
```

### Containerschema {#container}

The Container schema is used by the following components:

* [Accordeon](/help/components/accordion.md)
* [Tabs](/help/components/tabs.md)
* [Carousel](/help/components/carousel.md)

Het containerschema wordt als volgt gedefinieerd.

```
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    shownItems          // array of the displayed item IDs
}
```

### Afbeeldingsschema {#image}

Het schema van het Beeld wordt gebruikt door de volgende component:

* [Afbeelding](/help/components/image.md)

Het afbeeldingsschema wordt als volgt gedefinieerd.

```
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    image               // asset detail (see below section)
}
```

### Elementschema {#asset}

Het schema Elementen wordt gebruikt binnen de component [Afbeelding.](/help/components/image.md)

Het schema Asset wordt als volgt gedefinieerd.

```
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```

