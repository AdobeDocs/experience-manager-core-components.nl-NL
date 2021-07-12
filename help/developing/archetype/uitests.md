---
title: ui.tests Module van AEM Project Archetype
description: Hoe te om de Tests UI van de Archetype van het Project van de AEM te gebruiken
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: eb3c9b34-f10e-410f-bcf3-34f94f124c7c
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# ui.tests Module van het Archetype van het AEM Project {#uitests-module}

Het project bevat drie testniveaus:

* [Eenheidstests](core.md#unit-tests)
* [Integratietests](ittests.md)
* UI-tests

Dit artikel beschrijft de tests UI beschikbaar als deel van de module ui.tests.

## UI-tests uitvoeren {#running-tests}

Om te testen, voer uit:

```shell
mvn verify -Pui-tests-local-execution
```

Na uitvoering zijn rapporten en logbestanden beschikbaar in de map `target/reports`.

## Aanvullende opties {#additional-options}

De tests UI kunnen met vele verschillende opties worden in werking gesteld met inbegrip van voor hoofdloze het testen tegen lokale browser en als beeld van het Dokker. Zie het [README.md- dossier van ui.tests module](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests) voor verdere informatie.
