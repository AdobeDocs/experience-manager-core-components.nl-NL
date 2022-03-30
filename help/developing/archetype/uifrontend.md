---
title: AEM project archetype front-end build
description: Een projectmalplaatje voor op AEM gebaseerde toepassingen
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
source-git-commit: 0e8082b0c5db1f2efc7db51f13123b5264a3a608
workflow-type: tm+mt
source-wordcount: '1621'
ht-degree: 0%

---

# ui.frontend Module van het Archetype van het AEM Project {#uifrontend-module}

Het AEM Project Archetype omvat een facultatief, specifiek front-end bouwstijlmechanisme dat op Webpack wordt gebaseerd. De module ui.frontend wordt dus de centrale locatie voor alle front-end bronnen van het project, waaronder JavaScript- en CSS-bestanden. Om volledig gebruik te maken van deze nuttige en flexibele functie, is het belangrijk om te begrijpen hoe front-end ontwikkeling past in een AEM project.

## AEM en front-end ontwikkeling {#aem-and-front-end-development}

In sterk vereenvoudigde termen kunnen AEM projecten worden beschouwd als bestaande uit twee afzonderlijke maar verwante delen:

* De ontwikkeling van het achterste deel die de logica van AEM drijft en Java bibliotheken, de diensten OSGi, enz. produceert
* Front-end ontwikkeling die de presentatie en het gedrag van de resulterende website aandrijft en JavaScript en CSS bibliotheken produceert

Omdat deze twee ontwikkelingsprocessen zich richten op verschillende delen van het project, kan de achterkant en front-end ontwikkeling parallel plaatsvinden.

![front end workflowdiagram](/help/assets/front-end-flow.png)

Voor elk project moet echter gebruik worden gemaakt van de resultaten van beide ontwikkelingsinspanningen, d.w.z. zowel back-end als front-end.

Wordt uitgevoerd `npm run dev` start het front-end constructieproces dat de JavaScript- en CSS-bestanden verzamelt die zijn opgeslagen in de module ui.frontend en dat twee geminificeerde clientbibliotheken of ClientLibs genereert die `clientlib-site` en `clientlib-dependencies` en zet ze neer in de module ui.apps. ClientLibs kan worden geïmplementeerd om te AEM en u kunt uw code aan de clientzijde opslaan in de opslagplaats.

Wanneer het volledige AEM project archetype in werking wordt gesteld `mvn clean install -PautoInstallPackage` alle projectartefacten met inbegrip van ClientLibs worden dan geduwd aan de AEM instantie.

>[!TIP]
>
>Meer informatie over hoe AEM ClientLibs in de [AEM ontwikkelingsdocumentatie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html), hoe [opnemen](/help/developing/including-clientlibs.md)of zie hieronder [hoe de ui.frontend module hen gebruikt.](#clientlib-generation)

## Overzicht van ClientLibs {#clientlibs}

De voorste module is beschikbaar via een [AEM ClientLib](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html). Wanneer het uitvoeren van NPM bouwt manuscript, wordt app gebouwd en het aem-client-generator-generatorpakket neemt de resulterende bouwstijloutput en transformeert het in zulk een ClientLib.

Een ClientLib bestaat uit de volgende bestanden en mappen:

* `css/`: CSS-bestanden die kunnen worden aangevraagd in de HTML
* `css.txt`: Hiermee AEM u de volgorde en namen van bestanden in `css/` zodat ze kunnen worden samengevoegd
* `js/`: JavaScript-bestanden die kunnen worden aangevraagd in de HTML
* `js.txt` Hiermee AEM u de volgorde en namen van bestanden in `js/` zodat ze kunnen worden samengevoegd
* `resources/`: Bronkaarten, niet-invoerpuntcodeschunks (als gevolg van code splitsen), statische elementen (bijvoorbeeld pictogrammen) enz.

## Mogelijke front-end ontwikkelingsworkflows {#possible-workflows}

De bouwstijlmodule aan de voorzijde is een nuttig en zeer flexibel instrument, maar stelt geen specifieke mening over hoe deze moet worden gebruikt. Hieronder volgen twee voorbeelden: *mogelijk* gebruik, maar uw individuele projectbehoeften kunnen andere gebruiksmodellen dicteren.

### Statische ontwikkelingsserver van Webpack gebruiken {#using-webpack}

Met Webpack kunt u stijl en ontwikkeling toepassen op basis van de statische uitvoer van AEM webpagina&#39;s in de module ui.frontend.

1. Pagina voorvertonen in AEM met de modus Voorvertoning van pagina of doorgeven in `wcmmode=disabled` in de URL
1. Paginabron weergeven en opslaan als statische HTML in de module ui.frontend
1. [Webpack starten](#webpack-dev-server) en beginnen met opmaken en de benodigde JavaScript en CSS genereren
1. Uitvoeren `npm run dev` om de ClientLibs te genereren

In deze stroom, kan een AEM ontwikkelaar stappen één en twee uitvoeren en statische HTML van de tot de front-end ontwikkelaar overgaan die zich op de output van AEM HTML baseert.

>[!TIP]
>
>Je zou ook de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library) om voorbeelden van de prijsverhogingsoutput van elke component te vangen om op componentenniveau eerder dan op paginaniveau te werken.

### Winybook gebruiken {#using-storybook}

Gebruiken [Winkelboek](https://storybook.js.org) u kunt meer atomische front-end ontwikkeling uitvoeren. Hoewel Storybook niet is opgenomen in het AEM Project Archetype, kunt u het installeren en uw objecten uit het Storybook opslaan in de module ui.frontend. Als ze klaar zijn om te worden getest binnen AEM, kunnen ze worden geïmplementeerd als ClientLibs door ze uit te voeren `npm run dev`.

>[!NOTE]
>
>[Winkelboek](https://storybook.js.org) is niet opgenomen in het AEM Projectarchetype. Als u ervoor kiest om het te gebruiken, moet u het afzonderlijk installeren.

### De markering bepalen {#determining-markup}

Welke ontwikkelworkflow op de voorgrond u ook wilt implementeren voor uw project, de back-end ontwikkelaars en front-end ontwikkelaars moeten het eerst eens worden over de markering. AEM definieert doorgaans de markering, die wordt geleverd door de kerncomponenten. [Dit kan echter zo nodig worden aangepast](/help/developing/customizing.md#customizing-the-markup).

## De module ui.frontend {#ui-frontend-module}

Het AEM Project Archetype omvat een facultatief specifiek front-end bouwstijlmechanisme dat op Webpack met de volgende eigenschappen wordt gebaseerd.

* Volledige ondersteuning voor TypeScript, ES6 en ES5 (met de toepasselijke webpack-wrappers)
* TypeScript- en JavaScript-koppelingen met behulp van een TSLint-regelset
* ES5-uitvoer, voor ondersteuning van oudere browsers
* Globalisering
   * Geen noodzaak om overal import toe te voegen
   * Alle JS- en CSS-bestanden kunnen nu aan elke component worden toegevoegd.
      * Beste praktijken zijn onder `/clientlib/js`, `/clientlib/css`, of `/clientlib/scss`
   * Nee `.content.xml` of `js.txt`/`css.txt` bestanden zijn nodig omdat alles via Webpack wordt uitgevoerd.
   * De globber trekt in alle JS- dossiers onder `/component/` map.
      * Met Webpack kunnen CSS-/SCSS-bestanden via JS-bestanden in een keten worden geplaatst.
      * Ze worden door de twee ingangspunten naar binnen getrokken. `sites.js` en `vendors.js`.
   * Het enige bestand dat AEM gebruikt, zijn de uitvoerbestanden `site.js` en `site.css` in `/clientlib-site` alsmede `dependencies.js` en `dependencies.css` in `/clientlib-dependencies`
* Chunks
   * Hoofd (site-js/css)
   * Leveranciers (afhankelijkheden js/css)
* Volledige ondersteuning voor klasse/scss (de klasse wordt gecompileerd naar CSS via Webpack)
* Statische webpack-ontwikkelingsserver met ingebouwde proxy naar een lokale instantie van AEM

>[!NOTE]
>
>Voor meer technische informatie over de module ui.frontend raadpleegt u de [documentatie over GitHub](https://github.com/adobe/aem-project-archetype/blob/master/src/main/archetype/ui.frontend.general/README.md).

## Installatie {#installation}

1. Installeren [NodeJS](https://nodejs.org/en/download/) (v10+), globaal. Hierdoor wordt ook npm geïnstalleerd.
1. Navigeer naar ui.frontend in uw project en voer deze uit `npm install`.

>[!NOTE]
>
>U moet [Voer het archetype uit](overview.md) met de optie `-DoptionIncludeFrontendModule=y` om de map ui.frontend te vullen.

## Gebruik {#usage}

De volgende npm manuscripten drijven de frontend werkschema:

* `npm run dev` - Volledige build met JS-optimalisatie uitgeschakeld (schudden van boomstructuur, enz.) en bronkaarten ingeschakeld en CSS-optimalisatie uitgeschakeld.
* `npm run prod` - volledige build met JS-optimalisatie ingeschakeld (schudden van structuren, enz.), brontoewijzingen uitgeschakeld en CSS-optimalisatie ingeschakeld.
* `npm run start` - Start een statische webpack ontwikkelingsserver voor lokale ontwikkeling met minimale afhankelijkheid van AEM.

## Uitvoer {#output}

De module ui.frontend compileert de code onder de `ui.frontend/src` en geeft de gecompileerde CSS en JS en alle bronnen onder een map met de naam `ui.frontend/dist`.

* **Site** - `site.js`, `site.css` en `resources/` map voor lay-outafhankelijke afbeeldingen en lettertypen worden gemaakt in een `dist/`clientlib-site map.
* **Afhankelijkheden** - `dependencies.js` en `dependencies.css` worden gemaakt in een `dist/clientlib-dependencies` map.

### JavaScript {#javascript}

* Optimalisatie - Voor productiebuilds wordt alle JS verwijderd die niet wordt gebruikt of aangeroepen.

### CSS {#css}

* Automatisch voormaken - Alle CSS wordt uitgevoerd via een voorvoegsel en alle eigenschappen die voorfixeren vereisen, worden automatisch toegevoegd aan de CSS.
* Optimalisatie - Alle CSS wordt na de publicatie uitgevoerd via een optimalisator (cssnano) die de standaard instelt op de volgende regels:
   * Vermindert CSS calc uitdrukking waar mogelijk, die zowel browser verenigbaarheid als compressie verzekeren zet tussen gelijkwaardige lengte, tijd en hoekwaarden om. De lengtewaarden worden standaard niet omgezet.
   * Hiermee verwijdert u opmerkingen in en rondom regels, kiezers en declaraties
   * Hiermee worden dubbele regels, at-rules en declaraties verwijderd
      * Dit werkt alleen voor exacte duplicaten.
   * Verwijdert lege regels, mediaquery&#39;s en regels met lege kiezers, omdat deze geen invloed hebben op de uitvoer
   * Voegt aangrenzende regels samen door kiezers en overlappende eigenschap/waardeparen
   * Zorgt ervoor dat het CSS-bestand slechts één @charset bevat en verplaatst het naar de bovenkant van het document
   * Hiermee vervangt u het oorspronkelijke CSS-trefwoord door de werkelijke waarde wanneer de resulterende uitvoer kleiner is
   * Hiermee worden inline SVG-definities gecomprimeerd met SVGO
* Schoonmaken - Omvat expliciete schone taak voor het wissen van de geproduceerde CSS, JS en Kaart dossiers op bestelling.
* Brontoewijzing - alleen ontwikkelingsbuild

>[!NOTE]
>
>De voorkant bouwt optie gebruikt dev-slechts en prod-enige webpack configuratiedossiers die een gemeenschappelijk configuratiedossier delen. Op deze manier kunnen de ontwikkelings- en productiemontages onafhankelijk worden gewijzigd.

### Client Library Generation {#clientlib-generation}

De ui.frontend module bouwt proces hefboomwerkingen de [aem-clientlib-generator](https://www.npmjs.com/package/aem-clientlib-generator) om de gecompileerde CSS, JS en alle bronnen naar de module ui.apps te verplaatsen. De aem-clientlib-generator configuratie wordt bepaald in `clientlib.config.js`. De volgende clientbibliotheken worden gegenereerd:

* **clientlib-site** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-site`
* **clientlib-afhankelijkheden** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-dependencies`

### Inclusief clientbibliotheken op pagina&#39;s {#clientlib-inclusion}

`clientlib-site` en `clientlib-dependencies` categorieën worden op pagina&#39;s opgenomen via de [Configuratie van paginabeleid](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html#template-definitions) als onderdeel van de standaardsjabloon. Als u het beleid wilt weergeven, bewerkt u de **Content Page Template > Page Information > Page Policy**.

De uiteindelijke opname van clientbibliotheken op de sitepagina ziet er als volgt uit:

```html
<HTML>
    <head>
        <link rel="stylesheet" href="clientlib-base.css" type="text/css">
        <script type="text/javascript" src="clientlib-dependencies.js"></script>
        <link rel="stylesheet" href="clientlib-dependencies.css" type="text/css">
        <link rel="stylesheet" href="clientlib-site.css" type="text/css">
    </head>
    <body>
        ....
        <script type="text/javascript" src="clientlib-site.js"></script>
        <script type="text/javascript" src="clientlib-base.js"></script>
    </body>
</HTML>
```

Bovenstaande opname kan natuurlijk worden gewijzigd door het paginabeleid bij te werken en/of de categorieën en insluiteigenschappen van de respectievelijke clientbibliotheken te wijzigen.

### Statische WebPack Development Server {#webpack-dev-server}

In de module ui.frontend is een webpack-dev-server inbegrepen die levende herlading voor snelle front-end ontwikkeling buiten AEM verstrekt. De setup gebruikt de html-webpack-plug-in om CSS en JS die uit de module ui.frontend zijn gecompileerd, automatisch te injecteren in een statische HTML-sjabloon.

#### Belangrijke bestanden {#important-files}

* `ui.frontend/webpack.dev.js`
   * Dit bevat de configuratie voor webpack-dev-serve en wijst naar de HTML-sjabloon die moet worden gebruikt.
   * Het bevat ook een volmachtsconfiguratie aan een AEM instantie die op localhost:4502 loopt.
* `ui.frontend/src/main/webpack/static/index.html`
   * Dit is de statische HTML waarop de server wordt uitgevoerd.
   * Op deze manier kan een ontwikkelaar CSS/JS-wijzigingen aanbrengen en deze direct in de opmaak weergeven.
   * Aangenomen wordt dat de markering die in dit bestand is geplaatst, de gegenereerde opmaak van AEM componenten correct weerspiegelt.
   * Opmaak in dit bestand wordt niet automatisch gesynchroniseerd met AEM componentmarkeringen.
   * Dit bestand bevat ook verwijzingen naar clientbibliotheken die zijn opgeslagen in AEM, zoals de CSS van de kerncomponent en de CSS van het responsieve raster.
   * De webpack-ontwikkelingsserver is ingesteld op proxy die deze CSS/JS bevat van een lokale actieve AEM-instantie op basis van de configuratie in `ui.frontend/webpack.dev.js`.

#### Gebruiken {#using-webpack-server}

1. Van binnen de wortel van het project stelt het bevel in werking `mvn -PautoInstallSinglePackage clean install` om het volledige project aan een AEM instantie te installeren die bij loopt `localhost:4502`.
1. Navigeren in het deelvenster `ui.frontend` map.
1. Voer de volgende opdracht uit `npm run start` om de webpack-ontwikkelserver te starten. Als de functie eenmaal is gestart, wordt een browser geopend (`localhost:8080` of de volgende beschikbare poort).

U kunt nu CSS-, JS-, SCSS- en TS-bestanden wijzigen en de wijzigingen direct bekijken die worden weerspiegeld in de webpack-ontwikkelserver.
