---
title: ui.tests Module van AEM Project Archetype
description: JUnit-tests voor AEM projectontwerp gebruiken
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# ui.tests Module van het Archetype van het AEM Project {#uitests-module}

Het project bevat drie testniveaus:

## Eenheidstests {#unit-tests}

De eenheidstest in [kernmodule](core.md) toont klassieke eenheidstests van de code in de bundel. Om te testen, voer uit:

```
mvn clean test
```

## Integratietests {#integration-tests}

Met de integratietests aan de serverzijde kunnen eenheidstests worden uitgevoerd in de AEM-omgeving, d.w.z. op de AEM server. Om te testen, voer uit:

```
mvn clean verify -PintegrationTests
```

## Client-Side Tests {#client-side-tests}

De tests `client-side Hobbes.js` zijn op JavaScript gebaseerde browser-zijtests die browser-zijgedrag verifiëren.

Als u wilt testen, opent u de pagina in **Developer mode** door het linkervenster te openen en over te schakelen op het tabblad **Tests** en de gegenereerde **MyName Tests** te zoeken en uit te voeren.
