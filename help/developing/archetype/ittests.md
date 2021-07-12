---
title: it.tests Module van AEM Project Archetype
description: Hoe te om de Tests van de Integratie van de Archetype van het AEM te gebruiken
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 0abc0265-3a3f-4323-97e6-3af0c62299ef
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '80'
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
