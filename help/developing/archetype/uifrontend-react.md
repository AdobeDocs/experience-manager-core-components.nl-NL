---
title: Front-End bouwt voor React SPAs
description: Een beschrijving van het front-end bouwt proces voor React-based projecten van het KUUROORD
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Front-End bouwt voor React SPAs {#frontend-react}

Dit document verklaart de details van het gemaakte project wanneer het gebruiken van archetype om één enkele paginatoepassing (SPA) tot stand te brengen die op het kader van de Reactie wordt gebaseerd. Dat wil zeggen wanneer u de `frontendModule` optie instelt op `react`.

## Overzicht {#overview}

Dit project is opgestart met [create-response-app](https://github.com/facebook/create-react-app).

Deze toepassing is ontworpen om het AEM-model van een site te gebruiken. De lay-out wordt automatisch gegenereerd met behulp van de helpercomponenten uit het pakket [@adobe/cq-response-editable-components](https://www.npmjs.com/package/@adobe/cq-react-editable-components) .

## Scripts {#scripts}

In de projectfolder, kunt u de volgende bevelen in werking stellen:

### npm start {#npm-start}

```
npm start
```

Met deze opdracht voert u de toepassing uit in de ontwikkelingsmodus door het JSON-model te proxen vanuit een lokale AEM-instantie die wordt uitgevoerd op http://localhost:4502. Dit veronderstelt dat het volledige project aan AEM minstens eens (in de projectwortel) is opgesteld.`mvn clean install -PautoInstallPackage`

Nadat de app is uitgevoerd `npm start` in de map [ui.frontend](uifrontend.md) , wordt deze automatisch geopend in uw browser (op pad `http://localhost:3000/content/<appId>/<country>/<language>/home.html`). Als u bewerkingen uitvoert, wordt de pagina opnieuw geladen.

Als u fouten met betrekking tot CORS krijgt, zou u AEM als volgt kunnen willen vormen:

1. Navigeer aan de Manager van de Configuratie (http://localhost:4502/system/console/configMgr)
1. Open de configuratie voor &quot;Adobe Granite Cross-Origin Resource Sharing Policy&quot;
1. Maak een nieuwe configuratie met de volgende aanvullende waarden:
   * Toegestane oorsprong: http://localhost:3000
   * Ondersteunde kopteksten: Toestemming
   * Toegestane methoden: OPTIES

### npm-test {#npm-test}

```
npm test
```

Met deze opdracht start u de testruntime in de interactieve controlemodus. Raadpleeg de documentatie bij [Reageren over het uitvoeren van tests](https://facebook.github.io/create-react-app/docs/running-tests) voor meer informatie.

### npm-run-build {#npm-run-build}

```
npm run build
```

Met deze opdracht wordt de app voor productie naar de map build gemaakt. Het bundelt React op productiemodus en optimaliseert de bouwstijl voor de beste prestaties. Zie de documentatie van [React over plaatsing](https://facebook.github.io/create-react-app/docs/deployment) voor meer informatie.

Bovendien wordt uit de app een AEM ClientLib gegenereerd met behulp van het [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator) -pakket.

## Browserondersteuning {#browser-support}

Standaard gebruikt dit project de standaardinstellingen van [Browser](https://github.com/browserslist/browserslist)om doelbrowsers te identificeren. Bovendien bevat het programma polyvullingen voor functies in moderne talen om oudere browsers (bijvoorbeeld Internet Explorer 11) te ondersteunen. Als het steunen van dergelijke browsers geen vereiste is, kunnen de polyfill gebiedsdelen en de invoer worden verwijderd.

## Codesplitsing {#code-splitting}

De React-app is geconfigureerd om standaard gebruik te maken van [code splitsen](https://webpack.js.org/guides/code-splitting) . Wanneer u de app voor productie maakt, wordt de code in verschillende delen uitgevoerd:

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

Om deze functie te kunnen gebruiken met AEM, moet de app kunnen bepalen welke JS- en CSS-bestanden moeten worden aangevraagd vanuit de door AEM gegenereerde HTML. Dit kan worden bereikt met behulp van de &quot;entrypoints&quot;-sleutel in het bestand asset-manifest.json. Het bestand wordt geparseerd in clientlib.config.js en alleen de entrypoint-bestanden worden gebundeld in de ClientLib. De resterende bestanden worden in de bronnenmap van ClientLib geplaatst en worden dynamisch aangevraagd en daarom alleen geladen wanneer ze echt nodig zijn.

Zie de algemene [ui.frontend moduledocumentatie](uifrontend.md#clientlibs) voor verdere informatie over hoe AEM ClientLibs door het projectarchetype wordt gebruikt.
