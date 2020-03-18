---
title: ui.tests Module van AEM Project Archetype
description: JUnit-tests voor AEM-projectarchitectuur gebruiken
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# ui.tests Module van het AEM Project Archetype {#uitests-module}

Het project bevat drie testniveaus:

## Eenheidstests {#unit-tests}

Bij de eenheidstest in de [kernmodule](core.md) worden klassieke eenheidstests van de code in de bundel weergegeven. U test als volgt:

```
mvn clean test
```

## Integratietests {#integration-tests}

Met de integratietests aan de serverzijde kunnen eenheidstests worden uitgevoerd in de AEM-omgeving, d.w.z. op de AEM-server. U test als volgt:

```
mvn clean verify -PintegrationTests
```

## Client-Side Tests {#client-side-tests}

De `client-side Hobbes.js` tests zijn op JavaScript gebaseerde browsertests die gedrag aan de browserzijde controleren.

Als u wilt testen, wanneer u een AEM-pagina weergeeft die u in de browser wilt testen, opent u de pagina in de modus **** Ontwikkelaar door het linkerdeelvenster te openen en over te schakelen naar het tabblad **Tests** . Vervolgens zoekt u de gegenereerde **MyName-tests** en voert u deze uit.
