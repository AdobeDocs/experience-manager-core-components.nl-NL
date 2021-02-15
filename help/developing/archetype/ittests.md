---
title: it.tests Module van AEM Project Archetype
description: Hoe te om de Tests van de Integratie van de Archetype van het AEM te gebruiken
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---


# it.tests Module van het AEM Project Archetype {#ittests-module}

Het project bevat drie testniveaus:

* [Eenheidstests](core.md#unit-tests)
* Integratietests
* [UI-tests](uitests.md)

In dit artikel worden de integratietests beschreven die beschikbaar zijn als onderdeel van de module it.tests.

## Integratietests uitvoeren {#running-tests}

Met de integratietests aan de serverzijde kunnen eenheidstests worden uitgevoerd in de AEM-omgeving, d.w.z. op de AEM server. Om te testen, voer uit:

```
mvn clean verify -PintegrationTests
```
