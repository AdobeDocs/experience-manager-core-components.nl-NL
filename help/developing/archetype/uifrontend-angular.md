---
title: Front-end build voor SPA Angular
description: Een beschrijving van het front-end bouwstijlproces voor op Angular-gebaseerde SPA projecten
feature: Core Components, AEM Project Archetype
role: Architect, ontwikkelaar, beheerder
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---


# Front-End Build for Angular SPA {#frontend-angular}

In dit document worden de details uitgelegd van het project dat is gemaakt wanneer u het archetype gebruikt om een toepassing van één pagina (SPA) te maken die is gebaseerd op het raamwerk van de Angular. D.w.z. wanneer u de optie `frontendModule` op `angular` plaatst.

## Overzicht {#overview}

Dit project is opgestart met de [Angular CLI](https://github.com/angular/angular-cli).

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

```shell
npm test
```

Met deze opdracht start u de Karma-testruntime. Zie de [documentatie van de Angular over het runnen van tests](https://angular.io/guide/testing) voor meer informatie.

### npm run test:debug {#npm-run-test-debug}

```shell
npm run test:debug
```

Met deze opdracht start u de Karma-testruntime in de interactieve controlemodus.

### npm run build {#npm-run-build}

```shell
npm run build
```

Met deze opdracht wordt de app voor productie naar de map build gemaakt. Het bundelt Angular in productiemodus en optimaliseert de build voor de beste prestaties. Zie de [documentatie van de Angular over plaatsing](https://angular.io/guide/deployment) voor meer informatie.

Bovendien wordt uit de toepassing een AEM ClientLib gegenereerd met behulp van het [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator)-pakket.

Zie de algemene [ui.frontend moduledocumentatie](uifrontend.md#clientlibs) voor meer informatie over hoe AEM ClientLibs door het projectarchetype worden gebruikt.

## Browserondersteuning {#browser-support}

Standaard gebruikt dit project de standaardinstelling [Browserslist](https://github.com/browserslist/browserslist) om doelbrowsers te identificeren. Bovendien bevat het programma polyvullingen voor functies in moderne talen om oudere browsers (bijvoorbeeld Internet Explorer 11) te ondersteunen. Als het steunen van dergelijke browsers geen vereiste is, kunnen de polyfill gebiedsdelen en de invoer worden verwijderd.
