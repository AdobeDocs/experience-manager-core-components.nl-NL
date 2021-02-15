---
title: ui.tests Module van AEM Project Archetype
description: Hoe te om de Tests UI van de Archetype van het Project van de AEM te gebruiken
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '112'
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
