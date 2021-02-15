---
title: Het gebruiken van de Laag van de Gegevens van de Cliënt van Adobe met de Componenten van de Kern
description: Het gebruiken van de Laag van de Gegevens van de Cliënt van Adobe met de Componenten van de Kern
translation-type: tm+mt
source-git-commit: 57582c5c938e0f345b27785bd6fd6d5ed5454bd0
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 1%

---


# De gegevenslaag van de Adobe-client gebruiken met de kerncomponenten {#data-layer-core-components}

Het doel van de de Gegevens van de Cliënt van Adobe is de inspanning aan instrumentwebsites te verminderen door een gestandaardiseerde methode te verstrekken om om het even welk soort gegevens voor om het even welk manuscript bloot te stellen en toegang te hebben.

De gegevenslaag van de Cliënt van Adobe is platform agnostic, maar is volledig geïntegreerd in de Componenten van de Kern voor gebruik met AEM.

Als de Componenten van de Kern, is de code voor de Laag van Gegevens van de Cliënt van Adobe beschikbaar op GitHub samen met zijn ontwikkelaardocumentatie. Dit document geeft een overzicht van hoe de Componenten van de Kern met de Laag van Gegevens in wisselwerking staan, maar de volledige technische details worden uitgesteld aan de documentatie GitHub.

>[!TIP]
>
>Voor meer informatie over de Laag van Gegevens van de Cliënt van Adobe, [verwijs naar de middelen in zijn bewaarplaats GitHub.](https://github.com/adobe/adobe-client-data-layer)
>
>Voor verdere technische details over de integratie van de de Gegevens van de Cliënt van Adobe met de Componenten van de Kern, zie [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) dossier in de bewaarplaats van de Componenten van de Kern.

## Installatie en activering {#installation-activation}

Vanaf versie 2.9.0 van de Componenten van de Kern, wordt de Laag van Gegevens gedistribueerd met de Componenten van de Kern als AEM Bibliotheek van de Cliënt en geen installatie is noodzakelijk. Alle projecten die door [AEM Project Archetype v. 24+](/help/developing/archetype/overview.md) worden geproduceerd omvatten standaard een geactiveerde Laag van Gegevens.

Om de Laag van Gegevens manueel te activeren moet u een [context-bewuste configuratie](/help/developing/context-aware-configs.md) voor het tot stand brengen:

1. Maak de volgende structuur onder de map `/conf/<mySite>`, waarbij `<mySite>` de naam van het project van uw site is:
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * Waar elk knooppunt een `jcr:primaryType` heeft ingesteld op `nt:unstructured`.
1. Voeg een booleaanse eigenschap met de naam `enabled` toe en stel deze in op `true`.

   ![Locatie van DataLayerConfig in WKND Reference Site](/help/assets/datalayer-contextaware-sling-config.png)

   *Locatie van DataLayerConfig in WKND Reference Site*

1. Voeg een eigenschap `sling:configRef` toe aan het `jcr:content`-knooppunt van uw site onder `/content` (bijvoorbeeld `/content/<mySite>/jcr:content`) en stel deze in op `/conf/<mySite>` uit de vorige stap.

1. Zodra toegelaten, kunt u de activering verifiëren door een pagina van de plaats buiten de redacteur te laden, bijvoorbeeld door **Mening te gebruiken zoals Gepubliceerd** optie in de redacteur. Inspect de paginabron en de tag `<body>` moeten een kenmerk `data-cmp-data-layer-enabled` bevatten

   ```html
   <body class="page basicpage" id="page-id" data-cmp-data-layer-enabled>
       <script>
         window.adobeDataLayer = window.adobeDataLayer || [];
         adobeDataLayer.push({
             page: JSON.parse("{\x22page\u002D6c5d4b9fdd\x22:{\x22xdm:language\x22:\x22en\x22,\x22repo:path\x22:\x22\/content\/wknd\/language\u002Dmasters\/en.html\x22,\x22xdm:tags\x22:[],\x22xdm:template\x22:\x22\/conf\/wknd\/settings\/wcm\/templates\/landing\u002Dpage\u002Dtemplate\x22,\x22@type\x22:\x22wknd\/components\/page\x22,\x22dc:description\x22:\x22WKND is a collective of outdoors, music, crafts, adventure sports, and travel enthusiasts that want to share our experiences, connections, and expertise with the world.\x22,\x22dc:title\x22:\x22WKND Adventures and Travel\x22,\x22repo:modifyDate\x22:\x222020\u002D09\u002D29T07:50:13Z\x22}}"),
             event:'cmp:show',
             eventInfo: {
                 path: 'page.page\u002D6c5d4b9fdd'
             }
         });
       </script>
   ```

1. U kunt ook de ontwikkelaarsgereedschappen van uw browser openen en in de console moet het JavaScript-object `adobeDataLayer` beschikbaar zijn. Ga het volgende bevel in om de staat van de Laag van Gegevens van uw huidige pagina te krijgen:

   ```javascript
   window.adobeDataLayer.getState();
   ```

## Ondersteunde componenten {#supported-components}

De volgende componenten steunen de Laag van Gegevens.

* [Accordeon](/help/components/accordion.md)
* [Broodkruimel](/help/components/breadcrumb.md)
* [Knop](/help/components/button.md)
* [Carousel](/help/components/carousel.md)
* [Inhoudsfragment](/help/components/content-fragment-component.md)
* [Afbeelding](/help/components/image.md)
* [Taalnavigatie](/help/components/language-navigation.md)
* [Lijst](/help/components/list.md)
* [Navigatie](/help/components/navigation.md)
* [Pagina](/help/components/page.md)
* [Voortgangsbalk](/help/components/progress-bar.md)
* [Tabs](/help/components/tabs.md)
* [Teaser](/help/components/teaser.md)
* [Tekst](/help/components/text.md)
* [Titel](/help/components/title.md)

Verwijs ook naar [gebeurtenissen die door de componenten worden teweeggebracht.](#events-components)

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

```javascript
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

De volgende [gebeurtenis](#events) is relevant voor het schema Component/Container-item:

* `cmp:click`

### Paginaschema {#page}

Het paginaschema wordt gebruikt door de volgende component:

* [Pagina](/help/components/page.md)

Het paginaschema wordt als volgt gedefinieerd.

```javascript
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

Bij het laden van de pagina wordt een gebeurtenis `cmp:show` geactiveerd. Deze gebeurtenis wordt verzonden vanuit inline JavaScript direct onder de openingstag `<body>`, waardoor deze de oudste gebeurtenis in de wachtrij met gegevenslaaggebeurtenissen is.

### Containerschema {#container}

Het containerschema wordt gebruikt door de volgende componenten:

* [Accordeon](/help/components/accordion.md)
* [Tabs](/help/components/tabs.md)
* [Carousel](/help/components/carousel.md)

Het containerschema wordt als volgt gedefinieerd.

```javascript
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

De volgende [gebeurtenissen](#events) zijn relevant voor het containerschema:

* `cmp:click`
* `cmp:show`
* `cmp:hide`

### Afbeeldingsschema {#image}

Het schema van het Beeld wordt gebruikt door de volgende component:

* [Afbeelding](/help/components/image.md)

Het afbeeldingsschema wordt als volgt gedefinieerd.

```javascript
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

De volgende [gebeurtenis](#events) is relevant voor het beeldschema:

* `cmp:click`

### Middelenschema {#asset}

Het schema Asset wordt gebruikt in de [Afbeeldingscomponent.](/help/components/image.md)

Het schema Asset wordt als volgt gedefinieerd.

```javascript
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```

De volgende [gebeurtenis](#events) is relevant voor het schema Asset:

* `cmp:click`

### Inhoudsfragmentatieschema {#content-fragment}

Het inhoudsfragmentschema wordt gebruikt door de [Inhoudsfragmentcomponent.](/help/components/content-fragment-component.md)

Het inhoudsfragmentschema wordt als volgt gedefinieerd.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    elements            // array of the Content Fragment elements
}
```

Het schema dat voor het element Inhoudsfragment wordt gebruikt, ziet er als volgt uit.

```javascript
{
    xdm:title           // title
    xdm:text            // text
}
```

## Gebeurtenissen kerncomponent {#events}

Er zijn een aantal gebeurtenissen die de Componenten van de Kern via de Laag van Gegevens teweegbrengen. De beste manier om met de Laag van Gegevens in wisselwerking te staan is een gebeurtenisluisteraar [te registreren ](https://github.com/adobe/adobe-client-data-layer/wiki#addeventlistener) en *dan een actie te voeren die op het gebeurtenistype en/of de component wordt gebaseerd die de gebeurtenis teweegbracht.* Dit zal potentiële rassenvoorwaarden met asynchrone manuscripten vermijden.

Hieronder vindt u de gebeurtenissen uit de box die worden geleverd door AEM Core Components:

* **`cmp:click`** - Als u op een klikbaar element (een element met een  `data-cmp-clickable` kenmerk) klikt, activeert de gegevenslaag een  `cmp:click` gebeurtenis.
* **`cmp:show`** en  **`cmp:hide`** - Door het manipuleren van de accordeon (uitvouwen/samenvouwen), de carrousel (volgende/vorige knoppen) en de tabs (geselecteerde tabbladen) worden respectievelijk de gegevenslaag geactiveerd  `cmp:show` en een  `cmp:hide` gebeurtenis. Er wordt ook een `cmp:show`-gebeurtenis verzonden bij het laden van de pagina en dit is naar verwachting de eerste gebeurtenis.
* **`cmp:loaded`** - Zodra de Laag van Gegevens met de Componenten van de Kern op de pagina wordt bevolkt, teweegbrengt de Laag van Gegevens een  `cmp:loaded` gebeurtenis.

### Gebeurtenissen geactiveerd door component {#events-components}

In de volgende tabellen worden de standaard Core Components weergegeven die gebeurtenissen met deze gebeurtenissen activeert.

| Component | Gebeurtenis(sen) |
|---|---|
| [Accordeon](/help/components/accordion.md) | `cmp:show` and `cmp:hide` |
| [Knop](/help/components/button.md) | `cmp:click` |
| [Broodkruimel](/help/components/breadcrumb.md) | `cmp:click` |
| [Carousel](/help/components/carousel.md) | `cmp:show` en  `cmp:hide` |
| [Taalnavigatie](/help/components/language-navigation.md) | `cmp:click` |
| [Navigatie](/help/components/navigation.md) | `cmp:click` |
| [Pagina](/help/components/page.md) | `cmp:show` |
| [Tabs](/help/components/tabs.md) | `cmp:show` en  `cmp:hide` |
| [Teaser](/help/components/teaser.md) | `cmp:click` |

### Informatie over gebeurtenispad {#event-path-info}

Elke gebeurtenis van de Laag van Gegevens die door een AEM Component van de Kern wordt teweeggebracht zal een lading met het volgende voorwerp JSON omvatten:

```json
eventInfo: {
    path: '<component-path>'
}
```

Hierbij is `<component-path>` het JSON-pad naar de component in de gegevenslaag die de gebeurtenis heeft geactiveerd.  De waarde, beschikbaar via `event.eventInfo.path`, is belangrijk aangezien het als parameter aan `adobeDataLayer.getState(<component-path>)` kan worden gebruikt die de huidige staat van de component terugwint die de gebeurtenis teweegbracht, toestaand douanecode om tot extra gegevens toegang te hebben en het toe te voegen aan de Laag van Gegevens.

Bijvoorbeeld:

```javascript
function logEventObject(event) {
    if(event.hasOwnProperty("eventInfo") && event.eventInfo.hasOwnProperty("path")) {
        var dataObject = window.adobeDataLayer.getState(event.eventInfo.path);
        console.debug("The component that triggered this event: ");
        console.log(dataObject);
    }
}

window.adobeDataLayer = window.adobeDataLayer || [];
window.adobeDataLayer.push(function (dl) {
     dl.addEventListener("cmp:show", logEventObject);
});
```

## Zelfstudie

Wilt u de componenten van de Laag en van de Kern van Gegevens meer in detail onderzoeken? [Bekijk deze praktische zelfstudie](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/adobe-client-data-layer/data-layer-overview.html).

>[!TIP]
>
>Om de flexibiliteit van de Laag van Gegevens verder te onderzoeken, herzie over de integratieopties met inbegrip van hoe te om de Laag van Gegevens voor uw douanecomponenten toe te laten.
