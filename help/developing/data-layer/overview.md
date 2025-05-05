---
title: Het gebruiken van de Laag van de Gegevens van de Cliënt van de Adobe met de Componenten van de Kern
description: Het gebruiken van de Laag van de Gegevens van de Cliënt van de Adobe met de Componenten van de Kern
feature: Core Components, Adobe Client Data Layer
role: Architect, Developer, Admin
exl-id: 55c984d3-deb7-4eda-a81d-7768791d2b46
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: tm+mt
source-wordcount: '952'
ht-degree: 0%

---

# Het gebruiken van de Laag van de Gegevens van de Cliënt van de Adobe met de Componenten van de Kern {#data-layer-core-components}

Het doel van de Laag van Gegevens van de Cliënt van de Adobe is de inspanning aan instrumentwebsites te verminderen door een gestandaardiseerde methode te verstrekken om om het even welk soort gegevens voor om het even welk manuscript bloot te stellen en toegang te hebben.

De gegevenslaag van de Cliënt van de Adobe is platform agnostic, maar is volledig geïntegreerd in de Componenten van de Kern voor gebruik met AEM.

Als de Componenten van de Kern, is de code voor de Laag van de Gegevens van de Cliënt van de Adobe beschikbaar op GitHub samen met zijn ontwikkelaardocumentatie. Dit document geeft een overzicht van hoe de Componenten van de Kern met de Laag van Gegevens in wisselwerking staan, maar de volledige technische details worden uitgesteld aan de documentatie GitHub.

>[!TIP]
>
>Voor verdere informatie over de Laag van de Gegevens van de Cliënt van de Adobe, [ verwijs naar de middelen in zijn bewaarplaats GitHub.](https://github.com/adobe/adobe-client-data-layer)
>
>Voor verdere technische details over de integratie van de Laag van Gegevens van de Cliënt van de Adobe met de Componenten van de Kern, zie het [`DATA_LAYER_INTEGRATION.md` ](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) dossier in de bewaarplaats van de Componenten van de Kern.

## Installatie en activering {#installation-activation}

Vanaf versie 2.9.0 van de Componenten van de Kern, wordt de Laag van Gegevens gedistribueerd met de Componenten van de Kern als AEM Bibliotheek van de Cliënt en geen installatie is noodzakelijk. Alle projecten die door [ worden geproduceerd AEM Archetype van het Project v. 24+ ](/help/developing/archetype/overview.md) omvatten een geactiveerde Laag van Gegevens door gebrek.

Om de Laag van Gegevens manueel te activeren moet u a [ context-bewuste configuratie ](/help/developing/context-aware-configs.md) voor het creëren:

1. Maak de volgende structuur onder de map `/conf/<mySite>` , waarbij `<mySite>` de naam van het project van uw site is:
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * Waar voor elk knooppunt een `jcr:primaryType` is ingesteld op `nt:unstructured` .
1. Voeg een Booleaanse eigenschap met de naam `enabled` toe en stel deze in op `true` .

   ![ Plaats van DataLayerConfig in de Plaats van de Verwijzing WKND ](/help/assets/datalayer-contextaware-sling-config.png)

   *Plaats van DataLayerConfig in de Plaats van de Verwijzing WKND*

1. Voeg een eigenschap `sling:configRef` toe aan het knooppunt `jcr:content` van de onderstaande site `/content` (bijvoorbeeld `/content/<mySite>/jcr:content` ) en stel deze in op `/conf/<mySite>` uit de vorige stap.

1. Zodra toegelaten, kunt u de activering verifiëren door een pagina van de plaats buiten de redacteur te laden, bijvoorbeeld door de **Mening als Gepubliceerde** optie in de redacteur te gebruiken. Inspect: de paginabron en de tag `<body>` moeten een kenmerk bevatten `data-cmp-data-layer-enabled`

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

1. U kunt ook de ontwikkelaarsgereedschappen van uw browser openen en in de console moet het JavaScript-object van `adobeDataLayer` beschikbaar zijn. Ga het volgende bevel in om de staat van de Laag van Gegevens van uw huidige pagina te krijgen:

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

Verwijs ook naar de [ gebeurtenissen die door de componenten worden teweeggebracht.](#events-components)

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

De volgende [ gebeurtenis ](#events) is relevant voor het schema van het Punt van de Component/van de Container:

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

Er wordt een `cmp:show` -gebeurtenis geactiveerd bij het laden van de pagina. Deze gebeurtenis wordt verzonden vanuit een inline JavaScript direct onder de openingstag `<body>` , waardoor deze de oudste gebeurtenis in de gebeurteniswachtrij voor gegevenslagen is.

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

De volgende [ gebeurtenissen ](#events) zijn relevant voor het schema van de Container:

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

De volgende [ gebeurtenis ](#events) is relevant voor het schema van het Beeld:

* `cmp:click`

### Middelenschema {#asset}

Het schema van Activa wordt gebruikt binnen de [ component van het Beeld.](/help/components/image.md)

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

De volgende [ gebeurtenis ](#events) is relevant voor het schema van Activa:

* `cmp:click`

### Inhoudsfragmentschema {#content-fragment}

Het schema van het Fragment van de Inhoud wordt gebruikt door de [ component van het Fragment van de Inhoud.](/help/components/content-fragment-component.md)

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

## Gebeurtenissen van de kerncomponent {#events}

Er zijn een aantal gebeurtenissen die de Componenten van de Kern via de Laag van Gegevens teweegbrengen. De beste praktijken voor het in wisselwerking staan met de Laag van Gegevens moeten [ een gebeurtenisluisteraar ](https://github.com/adobe/adobe-client-data-layer/wiki#addeventlistener) registreren en *dan* een actie nemen die op het gebeurtenistype en/of de component wordt gebaseerd die de gebeurtenis teweegbracht. Dit zal potentiële rassenvoorwaarden met asynchrone manuscripten vermijden.

Hieronder vindt u de gebeurtenissen uit de box die worden geleverd door AEM Core Components:

* **`cmp:click`** - Als u op een klikbaar element klikt (een element met een `data-cmp-clickable` -kenmerk), activeert de gegevenslaag de gebeurtenis `cmp:click` .
* **`cmp:show`** en **`cmp:hide`** - De componenten van de accordeon (uit-/samenvouwen), carrousel (uit-/samenvouwen) en tabbladen (selecteren) zorgen ervoor dat de gegevenslaag gebeurtenissen `cmp:show` respectievelijk `cmp:hide` activeert. Er wordt ook een `cmp:show` -gebeurtenis verzonden tijdens het laden van de pagina. Dit is naar verwachting de eerste gebeurtenis.
* **`cmp:loaded`** - Zodra de gegevenslaag is gevuld met de kerncomponenten op de pagina, wordt een gebeurtenis `cmp:loaded` geactiveerd door de gegevenslaag.

### Gebeurtenissen geactiveerd door component {#events-components}

In de volgende tabellen worden de standaard Core Components weergegeven die gebeurtenissen met deze gebeurtenissen activeert.

| Component | Gebeurtenis(sen) |
|---|---|
| [ Accordeon ](/help/components/accordion.md) | `cmp:show` en `cmp:hide` |
| [ Knoop ](/help/components/button.md) | `cmp:click` |
| [ Breadcrumb ](/help/components/breadcrumb.md) | `cmp:click` |
| [ Carousel ](/help/components/carousel.md) | `cmp:show` en `cmp:hide` |
| [ Navigatie van de Taal ](/help/components/language-navigation.md) | `cmp:click` |
| [ Navigatie ](/help/components/navigation.md) | `cmp:click` |
| [ Pagina ](/help/components/page.md) | `cmp:show` |
| [ Lusjes ](/help/components/tabs.md) | `cmp:show` en `cmp:hide` |
| [ Taser ](/help/components/teaser.md) | `cmp:click` |

### Info van gebeurtenispad {#event-path-info}

Elke gebeurtenis van de Laag van Gegevens die door een AEM Component van de Kern wordt teweeggebracht zal een lading met het volgende voorwerp JSON omvatten:

```json
eventInfo: {
    path: '<component-path>'
}
```

Waar `<component-path>` het JSON-pad is naar de component in de gegevenslaag die de gebeurtenis heeft geactiveerd.  De waarde, beschikbaar via `event.eventInfo.path` , is belangrijk omdat deze kan worden gebruikt als parameter voor `adobeDataLayer.getState(<component-path>)` die de huidige status ophaalt van de component die de gebeurtenis heeft geactiveerd, zodat aangepaste code toegang heeft tot aanvullende gegevens en deze aan de gegevenslaag kan toevoegen.

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

Wilt u de componenten van de Laag en van de Kern van Gegevens meer in detail onderzoeken? [ Controle uit dit hands-on leerprogramma ](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/adobe-client-data-layer/data-layer-overview.html?lang=nl-NL).

>[!TIP]
>
>Om de flexibiliteit van de Laag van Gegevens verder te onderzoeken, herzie over de integratieopties met inbegrip van hoe te om de Laag van Gegevens voor uw douanecomponenten toe te laten.
