---
title: Het gebruiken van de Laag van de Gegevens van de Cliënt van Adobe met de Componenten van de Kern
description: Het gebruiken van de Laag van de Gegevens van de Cliënt van Adobe met de Componenten van de Kern
translation-type: tm+mt
source-git-commit: 24a810ff634f8846881dfa0095e879476d0f16f0
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---


# Het gebruiken van de Laag van de Gegevens van de Cliënt van Adobe met de Componenten van de Kern {#data-layer-core-components}

Het doel van de de Gegevens van de Cliënt van Adobe is de inspanning aan instrumentwebsites te verminderen door een gestandaardiseerde methode te verstrekken om om het even welk soort gegevens voor om het even welk manuscript bloot te stellen en toegang te hebben.

De gegevenslaag van de Cliënt van Adobe is platform agnostic, maar is volledig geïntegreerd in de Componenten van de Kern voor gebruik met AEM.

Als de Componenten van de Kern, is de code voor de Laag van Gegevens van de Cliënt van Adobe beschikbaar op GitHub samen met zijn ontwikkelaardocumentatie. Dit document geeft een overzicht van hoe de Componenten van de Kern met de Laag van Gegevens in wisselwerking staan, maar de volledige technische details worden uitgesteld aan de documentatie GitHub.

>[!TIP]
>
>Voor verdere informatie over de Laag van Gegevens van de Cliënt van Adobe, [verwijs naar de middelen in zijn bewaarplaats GitHub.](https://github.com/adobe/adobe-client-data-layer)
>
>Voor verdere technische details over de integratie van de de Gegevens van de Cliënt van Adobe met de Componenten van de Kern, zie het [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) dossier in de bewaarplaats van de Componenten van de Kern.

## Installatie en activering {#installation-activation}

Vanaf versie 2.9.0 van de Componenten van de Kern, wordt de Laag van Gegevens gedistribueerd met de Componenten van de Kern als cliëntlib. Installatie is niet nodig.

De gegevenslaag wordt echter niet standaard geactiveerd. Om de Laag van Gegevens te activeren moet u een [context-bewuste configuratie](/help/developing/context-aware-configs.md) voor het tot stand brengen:

1. Maak de volgende structuur onder het `/conf` knooppunt:
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * Type knooppunt: `nt:unstructured`
1. Voeg een booleaanse eigenschap met de naam toe `enabled` en stel deze in op `true`.
1. Voeg hieronder een `sling:configRef` eigenschap toe aan het `jcr:content` knooppunt van uw site `/content` (bijvoorbeeld `/content/<mySite>/jcr:content`) en instellen op `/conf/<mySite>`.

Zodra toegelaten, kunt u de activering verifiëren door een pagina van de plaats buiten de redacteur te laden. Wanneer u de pagina inspecteert zult u zien dat de Laag van Gegevens van de Cliënt van Adobe wordt geladen.

## Gegevensschema&#39;s voor kerncomponenten {#data-schemas}

Het volgende is een lijst van schema&#39;s die de Componenten van de Kern met de Laag van Gegevens gebruiken.

### Component-/containeritemschema {#item}

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

Het containerschema wordt gebruikt door de volgende componenten:

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

