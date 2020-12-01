---
title: Front-end build voor hoekige SPA
description: Een beschrijving van het proces van de front-end bouwstijl voor Hoekgebaseerde SPA projecten
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---


# Front-end build voor hoekige SPA {#frontend-angular}

In dit document worden de details uitgelegd van het project dat is gemaakt wanneer u het archetype gebruikt om een toepassing van één pagina (SPA) te maken op basis van het hoekframework. D.w.z. wanneer u de optie `frontendModule` op `angular` plaatst.

## Overzicht {#overview}

Dit project is opgestart met de [Hoekige CLI](https://github.com/angular/angular-cli).

Deze toepassing is ontworpen om het AEM van een site te gebruiken. De lay-out wordt automatisch gegenereerd met behulp van de helpercomponenten uit het [@adobe/cq-angular-editable-components](https://www.npmjs.com/package/@adobe/cq-angular-editable-components)-pakket.

## Scripts {#scripts}

In de projectfolder, kunt u de volgende bevelen in werking stellen.

### npm start {#npm-start}

```
npm start
```

Met deze opdracht voert u de toepassing uit in de ontwikkelingsmodus door het JSON-model te proxen vanuit een lokale AEM-instantie die wordt uitgevoerd op http://localhost:4502. Dit veronderstelt dat het volledige project aan AEM minstens eens (`mvn clean install -PautoInstallPackage` in de projectwortel) is opgesteld.

Nadat npm in werking stelt begin in de folder ui.frontend, zal uw app automatisch in uw browser (op weg http://localhost:4200/content/${appId}/${country} worden geopend/${language}/home.html). Als u bewerkingen uitvoert, wordt de pagina opnieuw geladen.

Als u fouten met betrekking tot CORS krijgt, zou u AEM als volgt kunnen willen vormen:

1. Navigeer aan de Manager van de Configuratie (http://localhost:4502/system/console/configMgr)
1. Open de configuratie voor &quot;Adobe Granite Cross-Origin Resource Sharing Policy&quot;
1. Maak een nieuwe configuratie met de volgende aanvullende waarden:
   * Toegestane oorsprong: http://localhost:4200
   * Ondersteunde kopteksten: Toestemming
   * Toegestane methoden: OPTIONS

### npm-test {#npm-test}

```
npm test
```

Met deze opdracht start u de Karma-testruntime. Zie de [Hoekdocumentatie over het uitvoeren van tests](https://angular.io/guide/testing) voor meer informatie.

### npm run test:debug {#npm-run-test-debug}

```
npm run test:debug
```

Met deze opdracht start u de Karma-testruntime in de interactieve controlemodus.

### npm run build {#npm-run-build}

```
npm run build
```

Met deze opdracht wordt de app voor productie naar de map build gemaakt. De toepassing bundelt hoekig in de productiemodus en optimaliseert de build voor de beste prestaties. Zie de [Hoekige documentatie over implementatie](https://angular.io/guide/deployment) voor meer informatie.

Bovendien wordt uit de toepassing een AEM ClientLib gegenereerd met behulp van het [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator)-pakket.

Zie de algemene [ui.frontend moduledocumentatie](uifrontend.md#clientlibs) voor meer informatie over hoe AEM ClientLibs door het projectarchetype worden gebruikt.

## Browserondersteuning {#browser-support}

Standaard gebruikt dit project de standaardinstelling [Browserslist](https://github.com/browserslist/browserslist) om doelbrowsers te identificeren. Bovendien bevat het programma polyvullingen voor functies in moderne talen om oudere browsers (bijvoorbeeld Internet Explorer 11) te ondersteunen. Als het steunen van dergelijke browsers geen vereiste is, kunnen de polyfill gebiedsdelen en de invoer worden verwijderd.
