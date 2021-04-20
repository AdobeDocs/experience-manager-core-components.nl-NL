---
title: ui.tests Module van AEM Project Archetype
description: Hoe te om de Tests UI van de Archetype van het Project van de AEM te gebruiken
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# ui.tests Module van het Archetype van het AEM Project {#uitests-module}

Het project bevat drie testniveaus:

* [Eenheidstests](core.md#unit-tests)
* [Integratietests](ittests.md)
* UI-tests

Dit artikel beschrijft de tests UI beschikbaar als deel van de module ui.tests.

## UI-tests {#running-tests} uitvoeren

Om te testen, voer uit:

```shell
mvn verify -Pui-tests-local-execution
```

Na uitvoering zijn rapporten en logbestanden beschikbaar in de map `target/reports`.

## Aanvullende opties {#additional-options}

De tests UI kunnen met vele verschillende opties worden in werking gesteld met inbegrip van voor hoofdloze het testen tegen lokale browser en als beeld van het Dokker. Zie het [README.md- dossier van ui.tests module](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests) voor verdere informatie.
