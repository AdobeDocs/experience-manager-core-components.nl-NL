---
title: AEM-projectarchetype front-end build
description: Een projectmalplaatje voor op AEM-Gebaseerde toepassingen
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# ui.frontend Module van het Archetype van het Project AEM {#uifrontend-module}

Het AEM Project Archetype omvat een facultatief, specifiek front-end bouwstijlmechanisme dat op Webpack wordt gebaseerd. De module ui.frontend wordt dus de centrale locatie voor alle front-end bronnen van het project, waaronder JavaScript- en CSS-bestanden. Om ten volle gebruik te maken van deze nuttige en flexibele functie, is het belangrijk te begrijpen hoe front-end ontwikkeling past in een AEM-project.

## AEM-projecten en front-endontwikkeling {#aem-and-front-end-development}

In sterk vereenvoudigde termen kunnen AEM-projecten worden beschouwd als bestaande uit twee afzonderlijke, maar verwante onderdelen:

* De ontwikkeling van het achterste deel die de logica van AEM drijft en Java bibliotheken, de diensten OSGi, enz. produceert
* Front-end ontwikkeling die de presentatie en het gedrag van de resulterende website aandrijft en JavaScript en CSS bibliotheken produceert

Omdat deze twee ontwikkelingsprocessen zich richten op verschillende delen van het project, kan de achterkant en front-end ontwikkeling parallel plaatsvinden.

![front end workflowdiagram](/help/assets/front-end-flow.png)

Voor elk project moet echter gebruik worden gemaakt van de resultaten van beide ontwikkelingsinspanningen, d.w.z. zowel back-end als front-end.

Als u deze functie uitvoert, `npm run dev` wordt het constructieproces op de voorgrond gestart dat de JavaScript- en CSS-bestanden verzamelt die zijn opgeslagen in de module ui.frontend en dat twee geminificeerde clientbibliotheken of ClientLibs genereert die worden aangeroepen `clientlib-site` en `clientlib-dependencies` en in de module ui.apps worden opgeslagen. ClientLibs kan worden geïmplementeerd op AEM en biedt u de mogelijkheid om uw clientcode op te slaan in de opslagplaats.

Wanneer het volledige AEM projectarchetype gebruikend `mvn clean install -PautoInstallPackage` alle projectartefacten met inbegrip van ClientLibs dan aan de instantie AEM wordt geduwd.

>[!TIP]
>Meer informatie over ClientLibs vindt u in de [AEM-ontwikkelingsdocumentatie](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/clientlibs.html) en [hoe de module ui.frontend deze hieronder](#clientlib-generation)gebruikt.

## Overzicht van ClientLibs {#clientlibs}

De frontend module wordt ter beschikking gesteld gebruikend een [AEM ClientLib](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html). Wanneer het uitvoeren van NPM bouwt manuscript, wordt app gebouwd en het aem-client-generator-generatorpakket neemt de resulterende bouwstijloutput en transformeert het in zulk een ClientLib.

Een ClientLib bestaat uit de volgende bestanden en mappen:

* `css/`: CSS-bestanden die kunnen worden aangevraagd in de HTML
* `css.txt`: Vertelt AEM de orde en de namen van dossiers in `css/` zodat zij kunnen samenvoegen
* `js/`: JavaScript-bestanden die kunnen worden aangevraagd in de HTML
* `js.txt` Vertelt AEM de orde en de namen van dossiers in `js/` zodat zij kunnen samenvoegen
* `resources/`: Bronkaarten, niet-invoerpuntcodeschunks (als gevolg van code splitsen), statische elementen (bijvoorbeeld pictogrammen) enz.

## Mogelijke front-end ontwikkelingsworkflows {#possible-workflows}

De bouwstijlmodule aan de voorzijde is een nuttig en zeer flexibel instrument, maar stelt geen specifieke mening over hoe deze moet worden gebruikt. Het volgende is twee voorbeelden van *mogelijk* gebruik, maar uw individuele projectbehoeften kunnen andere gebruiksmodellen dicteren.

### Statische ontwikkelingsserver van Webpack gebruiken {#using-webpack}

Met Webpack kunt u stijl en ontwikkeling toepassen op basis van statische uitvoer van AEM-webpagina&#39;s in de module ui.frontend.

1. Voorvertoning van pagina weergeven in AEM met de modus Voorvertoning van pagina of door `wcmmode=disabled` te geven in de URL
1. Paginabron weergeven en opslaan als statische HTML in de module ui.frontend
1. [Webpack](#webpack-dev-server) starten en opmaak beginnen en de benodigde JavaScript en CSS genereren
1. Uitvoeren `npm run dev` om de ClientLibs te genereren

In deze flow kan een AEM-ontwikkelaar stappen 1 en 2 uitvoeren en de statische HTML doorgeven aan de front-end ontwikkelaar die zich ontwikkelt op basis van de AEM HTML-uitvoer.

>[!TIP]
>
>U kunt de [componentbibliotheek](https://adobe.com/go/aem_cmp_library) ook gebruiken om voorbeelden van de opmaakuitvoer van elke component vast te leggen, zodat u op componentniveau kunt werken in plaats van op paginaniveau.

### Winybook gebruiken {#using-storybook}

Met [Storybook](https://storybook.js.org) kunt u meer atomische front-end ontwikkeling uitvoeren. Hoewel Storybook niet is opgenomen in het AEM Project Archetype, kunt u het installeren en uw Storybook artefacten opslaan binnen de module ui.frontend. Als ze klaar zijn om te worden getest in AEM, kunnen ze worden geïmplementeerd als ClientLibs door te werken `npm run dev`.

>[!NOTE]
>
>[Storybook](https://storybook.js.org) is niet opgenomen in het AEM Project Archetype. Als u ervoor kiest om het te gebruiken, moet u het afzonderlijk installeren.

### De markering bepalen {#determining-markup}

Welke ontwikkelworkflow op de voorgrond u ook wilt implementeren voor uw project, de back-end ontwikkelaars en front-end ontwikkelaars moeten het eerst eens worden over de markering. AEM definieert doorgaans de opmaak, die wordt geleverd door de kerncomponenten. [Dit kan echter zo nodig](/help/developing/customizing.md#customizing-the-markup)worden aangepast.

## De module ui.frontend {#ui-frontend-module}

Het AEM Project Archetype omvat een facultatief specifiek front-end bouwstijlmechanisme dat op Webpack met de volgende eigenschappen wordt gebaseerd.

* Volledige ondersteuning voor TypeScript, ES6 en ES5 (met de toepasselijke webpack-wrappers)
* TypeScript- en JavaScript-koppelingen met behulp van een TSLint-regelset
* ES5-uitvoer, voor ondersteuning van oudere browsers
* Globalisering
   * Geen noodzaak om overal import toe te voegen
   * Alle JS- en CSS-bestanden kunnen nu aan elke component worden toegevoegd.
      * Beste praktijken zijn onder `/clientlib/js`, `/clientlib/css`of `/clientlib/scss`
   * Er zijn geen `.content.xml` of `js.txt`/`css.txt` bestanden nodig omdat alles via Webpack wordt uitgevoerd.
   * De globber trekt in alle JS- dossiers onder de `/component/` omslag.
      * Met Webpack kunnen CSS-/SCSS-bestanden via JS-bestanden in een keten worden geplaatst.
      * Ze worden door de twee ingangspunten naar binnen getrokken, `sites.js` en `vendors.js`.
   * Het enige bestand dat door AEM wordt gebruikt, zijn de uitvoerbestanden `site.js` en `site.css` in `/clientlib-site` , `dependencies.js` en `dependencies.css` in `/clientlib-dependencies`
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
1. Navigeer naar ui.frontend in uw project en voer dit uit `npm install`.

>[!NOTE]
>
>U moet het archetype [met de optie in](overview.md) werking hebben gesteld `-DoptionIncludeFrontendModule=y` om de omslag te bevolken ui.frontend.

## Gebruik {#usage}

De volgende npm manuscripten drijven de frontend werkschema:

* `npm run dev` - Volledige build met JS-optimalisatie uitgeschakeld (schudden van boomstructuur, enz.) en bronkaarten ingeschakeld en CSS-optimalisatie uitgeschakeld.
* `npm run prod` - volledige build met JS-optimalisatie ingeschakeld (schudden van structuren, enz.), brontoewijzingen uitgeschakeld en CSS-optimalisatie ingeschakeld.
* `npm run start` - Start een statische webpack ontwikkelingsserver voor lokale ontwikkeling met minimale afhankelijkheid van AEM.

## Output {#output}

De module ui.frontend compileert de code onder de `ui.frontend/src` omslag en output gecompileerde CSS en JS, en om het even welke middelen onder een omslag genoemd `ui.frontend/dist`.

* **Site** - `site.js`en `site.css` een `resources/` map voor lay-outafhankelijke afbeeldingen en lettertypen worden gemaakt in een map op de `dist/`clientlib-site.
* **Afhankelijkheden** - `dependencies.js` en `dependencies.css` worden gemaakt in een `dist/clientlib-dependencies` map.

### JavaScript {#javascript}

* Optimalisatie - Voor productiebuilds wordt alle JS verwijderd die niet wordt gebruikt of aangeroepen.

### CSS {#css}

* Automatisch voormaken - Alle CSS wordt uitgevoerd via een voorvoegsel en alle eigenschappen die voorfixeren vereisen, worden automatisch toegevoegd aan de CSS.
* Optimalisatie - Alle CSS wordt na de publicatie uitgevoerd via een optimalisator (cssnano) die de standaard instelt op de volgende regels:
   * Vermindert CSS calc uitdrukking waar mogelijk, die zowel browser verenigbaarheid als compressieConverteert tussen gelijkwaardige lengte, tijd en hoekwaarden verzekert. De lengtewaarden worden standaard niet omgezet.
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
>De voorkant bouwt optie gebruikt dev-slechts en prod-enige webpack configuratiedossiers die een gemeenschappelijk configuratiedossier delen. Op deze manier kunnen de ontwikkelings- en productiemontages onafhankelijk worden gewijzigd.

### Client Library Generation {#clientlib-generation}

Het ui.frontend module bouwproces gebruikt de [aem-clientlib-generator](https://www.npmjs.com/package/aem-clientlib-generator) stop in om gecompileerde CSS, JS en om het even welke middelen in de module ui.apps te bewegen. De aem-clientlib-generatorconfiguratie wordt bepaald in `clientlib.config.js`. De volgende clientbibliotheken worden gegenereerd:

* **clientlib-site** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-site`
* **clientlib-afhankelijkheden** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-dependencies`

### Inclusief clientbibliotheken op pagina&#39;s {#clientlib-inclusion}

`clientlib-site` en `clientlib-dependencies` categorieën worden op pagina&#39;s opgenomen via de configuratie [van het Beleid van de](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/page-templates-editable.html#template-definitions) Pagina als deel van het standaardmalplaatje. Als u het beleid wilt weergeven, bewerkt u Sjabloon voor **inhoudspagina > Pagina-informatie > Paginabeleid**.

De uiteindelijke opname van clientbibliotheken op de sitepagina ziet er als volgt uit:

```
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
   * Het bevat ook een proxyconfiguratie voor een AEM-instantie die wordt uitgevoerd op localhost:4502.
* `ui.frontend/src/main/webpack/static/index.html`
   * Dit is de statische HTML waartegen de server zal lopen.
   * Op deze manier kan een ontwikkelaar CSS/JS-wijzigingen aanbrengen en deze direct in de opmaak weergeven.
   * Aangenomen wordt dat de markering die in dit bestand is geplaatst, de gegenereerde opmaak van AEM-componenten correct weerspiegelt.
   * Opmaak in dit bestand wordt niet automatisch gesynchroniseerd met opmaakcodes voor AEM-componenten.
   * Dit bestand bevat ook verwijzingen naar clientbibliotheken die zijn opgeslagen in AEM, zoals de CSS van de Core Component en de CSS van het responsieve raster.
   * De webpack-ontwikkelingsserver is ingesteld op proxy die door deze CSS/JS wordt opgenomen vanuit een lokale actieve AEM-instantie op basis van de configuratie in `ui.frontend/webpack.dev.js`.

#### Gebruiken {#using-webpack-server}

1. Van binnen de wortel van het project stel het bevel in werking `mvn -PautoInstallSinglePackage clean install` om het volledige project aan een instantie te installeren AEM die bij loopt `localhost:4502`.
1. Navigeer in de `ui.frontend` map.
1. Voer de volgende opdracht uit `npm run start` om de webpack-ontwikkelserver te starten. Nadat u de toepassing hebt gestart, opent u een browser (`localhost:8080` of de volgende beschikbare poort).

U kunt nu CSS-, JS-, SCSS- en TS-bestanden wijzigen en de wijzigingen direct bekijken die worden weerspiegeld in de webpack-ontwikkelserver.
