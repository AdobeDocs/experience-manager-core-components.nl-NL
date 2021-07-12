---
title: AEM project archetype front-end build
description: Een projectmalplaatje voor op AEM gebaseerde toepassingen
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '1625'
ht-degree: 0%

---

# ui.frontend Module van het Archetype van het AEM Project {#uifrontend-module}

Het AEM Project Archetype omvat een facultatief, specifiek front-end bouwstijlmechanisme dat op Webpack wordt gebaseerd. De module ui.frontend wordt dus de centrale locatie voor alle front-end bronnen van het project, waaronder JavaScript- en CSS-bestanden. Om volledig gebruik te maken van deze nuttige en flexibele functie, is het belangrijk om te begrijpen hoe front-end ontwikkeling past in een AEM project.

## AEM projecten en front-end ontwikkeling {#aem-and-front-end-development}

In sterk vereenvoudigde termen kunnen AEM projecten worden beschouwd als bestaande uit twee afzonderlijke maar verwante delen:

* De ontwikkeling van het achterste deel die de logica van AEM drijft en Java bibliotheken, de diensten OSGi, enz. produceert
* Front-end ontwikkeling die de presentatie en het gedrag van de resulterende website aandrijft en JavaScript en CSS bibliotheken produceert

Omdat deze twee ontwikkelingsprocessen zich richten op verschillende delen van het project, kan de achterkant en front-end ontwikkeling parallel plaatsvinden.

![front end workflowdiagram](/help/assets/front-end-flow.png)

Voor elk project moet echter gebruik worden gemaakt van de resultaten van beide ontwikkelingsinspanningen, d.w.z. zowel back-end als front-end.

Als u `npm run dev` uitvoert, wordt het &#39;front-end&#39; ontwikkelproces gestart dat de JavaScript- en CSS-bestanden verzamelt die zijn opgeslagen in de module ui.frontend en twee geminificeerde clientbibliotheken of ClientLibs met de namen `clientlib-site` en `clientlib-dependencies` produceert, en deze opslaat in de module ui.apps. ClientLibs kan worden geïmplementeerd om te AEM en u kunt uw code aan de clientzijde opslaan in de opslagplaats.

Wanneer het volledige AEM projectarchetype in werking wordt gesteld gebruikend `mvn clean install -PautoInstallPackage` worden alle projectartefacten met inbegrip van ClientLibs dan geduwd aan de AEM instantie.

>[!TIP]
>
>Meer informatie over hoe AEM ClientLibs verwerkt in de [AEM ontwikkelingsdocumentatie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html), hoe u deze [opneemt](/help/developing/including-clientlibs.md), of zie hieronder [hoe de module ui.frontend deze gebruikt.](#clientlib-generation)

## Overzicht van ClientLibs {#clientlibs}

De frontend module wordt ter beschikking gesteld gebruikend [AEM ClientLib](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html). Wanneer het uitvoeren van NPM bouwt manuscript, wordt app gebouwd en het aem-client-generator-generatorpakket neemt de resulterende bouwstijloutput en transformeert het in zulk een ClientLib.

Een ClientLib bestaat uit de volgende bestanden en mappen:

* `css/`: CSS-bestanden die kunnen worden aangevraagd in de HTML
* `css.txt`: Hiermee AEM u de volgorde en namen van bestanden,  `css/` zodat deze kunnen worden samengevoegd
* `js/`: JavaScript-bestanden die kunnen worden aangevraagd in de HTML
* `js.txt` Hiermee AEM u de volgorde en namen van bestanden,  `js/` zodat deze kunnen worden samengevoegd
* `resources/`: Bronkaarten, niet-invoerpuntcodeschunks (als gevolg van code splitsen), statische elementen (bijvoorbeeld pictogrammen) enz.

## Mogelijke front-end ontwikkelingsworkflows {#possible-workflows}

De bouwstijlmodule aan de voorzijde is een nuttig en zeer flexibel instrument, maar stelt geen specifieke mening over hoe deze moet worden gebruikt. Het volgende is twee voorbeelden van *mogelijk* gebruik, maar uw individuele projectbehoeften kunnen andere gebruiksmodellen dicteren.

### Statische ontwikkelingsserver van Webpack gebruiken {#using-webpack}

Met Webpack kunt u stijl en ontwikkeling toepassen op basis van de statische uitvoer van AEM webpagina&#39;s in de module ui.frontend.

1. Pagina voorvertonen in AEM met de modus Paginavoorvertoning of doorgeven in `wcmmode=disabled` in de URL
1. Paginabron weergeven en opslaan als statische HTML in de module ui.frontend
1. [Webpakket starten en ](#webpack-dev-server) opmaak beginnen en de benodigde JavaScript en CSS genereren
1. `npm run dev` uitvoeren om de ClientLibs te genereren

In deze flow kan een AEM ontwikkelaar stappen 1 en 2 uitvoeren en de statische HTML doorgeven aan de front-end ontwikkelaar die zich ontwikkelt op basis van de AEM HTML-uitvoer.

>[!TIP]
>
>U kunt ook de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library) gebruiken om voorbeelden van de opmaakuitvoer van elke component vast te leggen om op componentniveau te werken in plaats van op paginaniveau.

### Winybook gebruiken {#using-storybook}

Met [Storybook](https://storybook.js.org) kunt u meer atomische front-end ontwikkeling uitvoeren. Hoewel Storybook niet is opgenomen in het AEM Project Archetype, kunt u het installeren en uw objecten uit het Storybook opslaan in de module ui.frontend. Als ze klaar zijn om te worden getest binnen AEM, kunnen ze worden geïmplementeerd als ClientLibs door `npm run dev` uit te voeren.

>[!NOTE]
>
>[](https://storybook.js.org) Storybookis niet inbegrepen in het AEM Project Archetype. Als u ervoor kiest om het te gebruiken, moet u het afzonderlijk installeren.

### De markering bepalen {#determining-markup}

Welke ontwikkelworkflow op de voorgrond u ook wilt implementeren voor uw project, de back-end ontwikkelaars en front-end ontwikkelaars moeten het eerst eens worden over de markering. AEM definieert doorgaans de markering, die wordt geleverd door de kerncomponenten. [Dit kan echter zo nodig](/help/developing/customizing.md#customizing-the-markup) worden aangepast.

## De module ui.frontend {#ui-frontend-module}

Het AEM Project Archetype omvat een facultatief specifiek front-end bouwstijlmechanisme dat op Webpack met de volgende eigenschappen wordt gebaseerd.

* Volledige ondersteuning voor TypeScript, ES6 en ES5 (met de toepasselijke webpack-wrappers)
* TypeScript- en JavaScript-koppelingen met behulp van een TSLint-regelset
* ES5-uitvoer, voor ondersteuning van oudere browsers
* Globalisering
   * Geen noodzaak om overal import toe te voegen
   * Alle JS- en CSS-bestanden kunnen nu aan elke component worden toegevoegd.
      * De beste praktijken zijn onder `/clientlib/js`, `/clientlib/css`, of `/clientlib/scss`
   * Er zijn geen `.content.xml`- of `js.txt`/`css.txt`-bestanden nodig omdat alles via Webpack wordt uitgevoerd.
   * De globber trekt in alle JS- dossiers onder de `/component/` omslag.
      * Met Webpack kunnen CSS-/SCSS-bestanden via JS-bestanden in een keten worden geplaatst.
      * Zij worden binnen getrokken door de twee ingangspunten, `sites.js` en `vendors.js`.
   * Het enige bestand dat AEM gebruikt, zijn de uitvoerbestanden `site.js` en `site.css` in `/clientlib-site`, alsook `dependencies.js` en `dependencies.css` in `/clientlib-dependencies`
* Chunks
   * Hoofd (site-js/css)
   * Leveranciers (afhankelijkheden js/css)
* Volledige ondersteuning voor klasse/scss (de klasse wordt gecompileerd naar CSS via Webpack)
* Statische webpack-ontwikkelingsserver met ingebouwde proxy naar een lokale instantie van AEM

>[!NOTE]
>
>Voor meer technische informatie betreffende de module ui.frontend, te zien gelieve de [documentatie op GitHub](https://github.com/adobe/aem-project-archetype/blob/master/src/main/archetype/ui.frontend.general/README.md).

## Installatie {#installation}

1. Installeer [NodeJS](https://nodejs.org/en/download/) (v10+), globaal. Hierdoor wordt ook npm geïnstalleerd.
1. Navigeer naar ui.frontend in uw project en voer `npm install` uit.

>[!NOTE]
>
>U moet [in werking stellen archetype](overview.md) met de optie `-DoptionIncludeFrontendModule=y` hebben om de omslag ui.frontend te bevolken.

## Gebruik {#usage}

De volgende npm manuscripten drijven de frontend werkschema:

* `npm run dev` - Volledige build met JS-optimalisatie uitgeschakeld (schudden van boomstructuur, enz.) en bronkaarten ingeschakeld en CSS-optimalisatie uitgeschakeld.
* `npm run prod` - volledige build met JS-optimalisatie ingeschakeld (schudden van structuren, enz.), brontoewijzingen uitgeschakeld en CSS-optimalisatie ingeschakeld.
* `npm run start` - Start een statische webpack ontwikkelingsserver voor lokale ontwikkeling met minimale afhankelijkheid van AEM.

## Uitvoer {#output}

De module ui.frontend compileert de code onder de `ui.frontend/src` omslag en output gecompileerde CSS en JS, en om het even welke middelen onder een omslag genoemd `ui.frontend/dist`.

* **Site** -  `site.js`en een  `site.css` map voor lay-outafhankelijke afbeeldingen en lettertypen worden gemaakt in een map op de  `resources/`   `dist/`clientlib-site.
* **Afhankelijkheden** -  `dependencies.js` en  `dependencies.css` worden gemaakt in een  `dist/clientlib-dependencies` map.

### JavaScript {#javascript}

* Optimalisatie - Voor productiebuilds wordt alle JS verwijderd die niet wordt gebruikt of aangeroepen.

### CSS {#css}

* Automatisch voormaken - Alle CSS wordt uitgevoerd via een voorvoegsel en alle eigenschappen die voorfixeren vereisen, worden automatisch toegevoegd aan de CSS.
* Optimalisatie - Alle CSS wordt na de publicatie uitgevoerd via een optimalisator (cssnano) die de standaard instelt op de volgende regels:
   * Vermindert CSS calc uitdrukking waar mogelijk, die zowel browser verenigbaarheid als compressie verzekert
Hiermee wordt een waarde tussen equivalente lengte, tijd en hoek omgezet. De lengtewaarden worden standaard niet omgezet.
   * Hiermee verwijdert u opmerkingen in en rondom regels, kiezers en declaraties
   * Hiermee worden dubbele regels, at-rules en declaraties verwijderd
      * Dit werkt alleen voor exacte duplicaten.
   * Verwijdert lege regels, mediaquery&#39;s en regels met lege kiezers, omdat deze geen invloed hebben op de uitvoer
   * Voegt aangrenzende regels samen door kiezers en overlappende eigenschap/waardeparen
   * Zorgt ervoor dat het CSS-bestand slechts één @charset bevat en verplaatst het naar de bovenkant van het document
   * Hiermee vervangt u het oorspronkelijke CSS-trefwoord door de werkelijke waarde wanneer de resulterende uitvoer kleiner is
   * Hiermee comprimeert u inline SVG-definities met SVGO
* Schoonmaken - Omvat expliciete schone taak voor het wissen van de geproduceerde CSS, JS en Kaart dossiers op bestelling.
* Brontoewijzing - alleen ontwikkelingsbuild

>[!NOTE]
>
>De voorkant bouwt optie gebruikt dev-slechts en prod-enige webpack configuratiedossiers die een gemeenschappelijk configuratiedossier delen. Op deze manier kunnen de ontwikkelings- en productiemontages onafhankelijk worden gewijzigd.

### Client Library Generation {#clientlib-generation}

Het ui.frontend module bouwproces gebruikt [aem-clientlib-generator](https://www.npmjs.com/package/aem-clientlib-generator) plugin om gecompileerde CSS, JS en om het even welke middelen in de module ui.apps te bewegen. De aem-clientlib-generatorconfiguratie wordt bepaald in `clientlib.config.js`. De volgende clientbibliotheken worden gegenereerd:

* **clientlib-site** -  `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-site`
* **clientlib-afhankelijkheden** -  `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-dependencies`

### Inclusief clientbibliotheken op pagina&#39;s {#clientlib-inclusion}

`clientlib-site` en  `clientlib-dependencies` categorieën worden op pagina&#39;s opgenomen via de configuratie  [ ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html#template-definitions) Paginabeleid als onderdeel van de standaardsjabloon. Als u het beleid wilt weergeven, bewerkt u **Sjabloon voor inhoudspagina > Pagina-informatie > Paginabeleid**.

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
   * Dit is de statische HTML waartegen de server zal lopen.
   * Op deze manier kan een ontwikkelaar CSS/JS-wijzigingen aanbrengen en deze direct in de opmaak weergeven.
   * Aangenomen wordt dat de markering die in dit bestand is geplaatst, de gegenereerde opmaak van AEM componenten correct weerspiegelt.
   * Opmaak in dit bestand wordt niet automatisch gesynchroniseerd met AEM componentmarkeringen.
   * Dit bestand bevat ook verwijzingen naar clientbibliotheken die zijn opgeslagen in AEM, zoals de CSS van de kerncomponent en de CSS van het responsieve raster.
   * De webpack-ontwikkelingsserver is ingesteld op proxy die door deze CSS/JS wordt opgenomen vanuit een lokale actieve AEM-instantie op basis van de configuratie in `ui.frontend/webpack.dev.js`.

#### Gebruiken {#using-webpack-server}

1. Van binnen de wortel van het project stel het bevel `mvn -PautoInstallSinglePackage clean install` in werking om het volledige project aan een AEM instantie te installeren die bij `localhost:4502` loopt.
1. Navigeer in de map `ui.frontend`.
1. Voer de volgende opdracht `npm run start` uit om de webpack-ontwikkelserver te starten. Als de toepassing eenmaal is gestart, moet deze een browser (`localhost:8080` of de volgende beschikbare poort) openen.

U kunt nu CSS-, JS-, SCSS- en TS-bestanden wijzigen en de wijzigingen direct bekijken die worden weerspiegeld in de webpack-ontwikkelserver.
