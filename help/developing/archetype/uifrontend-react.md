---
title: Front-end build voor React SPA
description: Een beschrijving van het front-end bouwstijlproces voor React-based SPA projecten
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---


# Front-End Build for React SPA {#frontend-react}

In dit document worden de details van het gemaakte project uitgelegd wanneer u het archetype gebruikt om een toepassing van één pagina (SPA) te maken die is gebaseerd op het React-framework. D.w.z. wanneer u de optie `frontendModule` op `react` plaatst.

## Overzicht {#overview}

Dit project is opgestart met [create-response-app](https://github.com/facebook/create-react-app).

Deze toepassing is ontworpen om het AEM van een site te gebruiken. De lay-out wordt automatisch gegenereerd met behulp van de helpercomponenten uit het [@adobe/cq-response-editable-components](https://www.npmjs.com/package/@adobe/cq-react-editable-components)-pakket.

## Scripts {#scripts}

In de projectfolder, kunt u de volgende bevelen in werking stellen:

### npm start {#npm-start}

```
npm start
```

Met deze opdracht voert u de toepassing uit in de ontwikkelingsmodus door het JSON-model te proxen vanuit een lokale AEM-instantie die wordt uitgevoerd op http://localhost:4502. Dit veronderstelt dat het volledige project aan AEM minstens eens (`mvn clean install -PautoInstallPackage` in de projectwortel) is opgesteld.

Nadat u `npm start` in de map [ui.frontend](uifrontend.md) hebt uitgevoerd, wordt uw app automatisch geopend in uw browser (op pad `http://localhost:3000/content/<appId>/<country>/<language>/home.html`). Als u bewerkingen uitvoert, wordt de pagina opnieuw geladen.

Als u fouten met betrekking tot CORS krijgt, zou u AEM als volgt kunnen willen vormen:

1. Navigeer aan de Manager van de Configuratie (http://localhost:4502/system/console/configMgr)
1. Open de configuratie voor &quot;Adobe Granite Cross-Origin Resource Sharing Policy&quot;
1. Maak een nieuwe configuratie met de volgende aanvullende waarden:
   * Toegestane oorsprong: http://localhost:3000
   * Ondersteunde kopteksten: Toestemming
   * Toegestane methoden: OPTIONS

### npm-test {#npm-test}

```
npm test
```

Met deze opdracht start u de testruntime in de interactieve controlemodus. Zie [Documentatie van de Reactie over het runnen van tests](https://facebook.github.io/create-react-app/docs/running-tests) voor meer informatie.

### npm run build {#npm-run-build}

```
npm run build
```

Met deze opdracht wordt de app voor productie naar de map build gemaakt. Het bundelt React op productiemodus en optimaliseert de bouwstijl voor de beste prestaties. Zie de [Reageer documentatie over plaatsing](https://facebook.github.io/create-react-app/docs/deployment) voor meer informatie.

Bovendien wordt uit de toepassing een AEM ClientLib gegenereerd met behulp van het [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator)-pakket.

## Browserondersteuning {#browser-support}

Standaard gebruikt dit project de standaardinstelling [Browserslist](https://github.com/browserslist/browserslist) om doelbrowsers te identificeren. Bovendien bevat het programma polyvullingen voor functies in moderne talen om oudere browsers (bijvoorbeeld Internet Explorer 11) te ondersteunen. Als het steunen van dergelijke browsers geen vereiste is, kunnen de polyfill gebiedsdelen en de invoer worden verwijderd.

## Codesplitsing {#code-splitting}

De React app wordt gevormd om gebruik te maken van [code het splitsen](https://webpack.js.org/guides/code-splitting) door gebrek. Wanneer u de app voor productie maakt, wordt de code in verschillende delen uitgevoerd:

```
$ ls build/static/js
2.5b77f553.chunk.js
2.5b77f553.chunk.js.map
main.cff1a559.chunk.js
main.cff1a559.chunk.js.map
runtime~main.a8a9905a.js
runtime~main.a8a9905a.js.map
```

Als u alleen taken laadt wanneer deze vereist zijn, kunnen de prestaties van de app aanzienlijk worden verbeterd.

Deze functie werkt alleen met AEM als de app kan bepalen welke JS- en CSS-bestanden moeten worden aangevraagd vanuit de HTML die door AEM wordt gegenereerd. Dit kan worden bereikt met behulp van de &quot;entrypoints&quot;-sleutel in het bestand asset-manifest.json. Het bestand wordt geparseerd in clientlib.config.js en alleen de entrypoint-bestanden worden gebundeld in de ClientLib. De resterende bestanden worden in de bronnenmap van ClientLib geplaatst en worden dynamisch aangevraagd en daarom alleen geladen wanneer ze echt nodig zijn.

Zie de algemene [ui.frontend moduledocumentatie](uifrontend.md#clientlibs) voor meer informatie over hoe AEM ClientLibs door het projectarchetype worden gebruikt.
