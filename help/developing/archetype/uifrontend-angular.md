---
title: Front-End Build for Angular SPAs
description: Een beschrijving van het front-end bouwt proces voor op hoekig-gebaseerde projecten van het KUUROORD
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Front-End Build for Angular SPAs {#frontend-angular}

Dit document verklaart de details van het gemaakte project wanneer het gebruiken van archetype om één enkele paginatoepassing (SPA) tot stand te brengen die op het Hoekkader wordt gebaseerd. Dat wil zeggen wanneer u de `frontendModule` optie instelt op `angular`.

## Overzicht {#overview}

Dit project werd opgestart met de [hoekige CLI](https://github.com/angular/angular-cli).

Deze toepassing is ontworpen om het AEM-model van een site te gebruiken. De lay-out wordt automatisch gegenereerd met behulp van de helpercomponenten uit het pakket [@adobe/cq-angular-editable-components](https://www.npmjs.com/package/@adobe/cq-angular-editable-components) .

## Scripts {#scripts}

In de projectfolder, kunt u de volgende bevelen in werking stellen.

### npm start {#npm-start}

```
npm start
```

Met deze opdracht voert u de toepassing uit in de ontwikkelingsmodus door het JSON-model te proxen vanuit een lokale AEM-instantie die wordt uitgevoerd op http://localhost:4502. Dit veronderstelt dat het volledige project aan AEM minstens eens (in de projectwortel) is opgesteld.`mvn clean install -PautoInstallPackage`

Nadat npm in werking stelt begin in de folder ui.frontend, zal uw app automatisch in uw browser (op weg http://localhost:4200/content/${appId}/${country} worden geopend/${language}/home.html). Als u bewerkingen uitvoert, wordt de pagina opnieuw geladen.

Als u fouten met betrekking tot CORS krijgt, zou u AEM als volgt kunnen willen vormen:

1. Navigeer aan de Manager van de Configuratie (http://localhost:4502/system/console/configMgr)
1. Open de configuratie voor &quot;Adobe Granite Cross-Origin Resource Sharing Policy&quot;
1. Maak een nieuwe configuratie met de volgende aanvullende waarden:
   * Toegestane oorsprong: http://localhost:4200
   * Ondersteunde kopteksten: Toestemming
   * Toegestane methoden: OPTIES

### npm-test {#npm-test}

```
npm test
```

Met deze opdracht start u de Karma-testruntime. Raadpleeg de documentatie bij [Hoeken over het uitvoeren van tests](https://angular.io/guide/testing) voor meer informatie.

### npm run test:foutopsporing {#npm-run-test-debug}

```
npm run test:debug
```

Met deze opdracht start u de Karma-testruntime in de interactieve controlemodus.

### npm-run-build {#npm-run-build}

```
npm run build
```

Met deze opdracht wordt de app voor productie naar de map build gemaakt. De toepassing bundelt hoekig in de productiemodus en optimaliseert de build voor de beste prestaties. Zie de documentatie van [Hoeken over plaatsing](https://angular.io/guide/deployment) voor meer informatie.

Bovendien wordt uit de app een AEM ClientLib gegenereerd met behulp van het [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator) -pakket.

Zie de algemene [ui.frontend moduledocumentatie](uifrontend.md#clientlibs) voor verdere informatie over hoe AEM ClientLibs door het projectarchetype wordt gebruikt.

## Browserondersteuning {#browser-support}

Standaard gebruikt dit project de standaardinstellingen van [Browser](https://github.com/browserslist/browserslist)om doelbrowsers te identificeren. Bovendien bevat het programma polyvullingen voor functies in moderne talen om oudere browsers (bijvoorbeeld Internet Explorer 11) te ondersteunen. Als het steunen van dergelijke browsers geen vereiste is, kunnen de polyfill gebiedsdelen en de invoer worden verwijderd.
