---
title: De Module van de kern van het AEM Project Archetype
description: De Module van de kern van het AEM Project Archetype
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---


# De Module van de kern van het AEM Archetype van het Project {#core-module}

De kernmodule (`<src-directory>/<project>/core`) bevat alle Java-code die nodig is voor de implementatie. De module zal alle code van Java verpakken en aan de AEM instantie als Bundel OSGi opstellen.

De in `<src-directory>/<project>/core/pom.xml` gedefinieerde bundelinsteekmodule Geweven is verantwoordelijk voor het compileren van de Java-code in een OSGi-bundel die door AEM OSGi-container kan worden herkend. Hier wordt de locatie van verkoopmodellen gedefinieerd.

Hoewel het zeldzaam is dat de kernbundel onafhankelijk van de module ui.apps in hogere niveaumilieu&#39;s moet worden opgesteld, is het direct opstellen van de kernbundel nuttig tijdens lokale ontwikkeling/het testen. Met de plug-in Maven Sling kan de kernbundel worden geïmplementeerd om het profiel `autoInstallBundle` rechtstreeks te AEM, zoals gedefinieerd in de [bovenliggende POM](/help/developing/archetype/using.md#parent-pom).

```shell
mvn -PautoInstallBundle clean install
```

Nadat de uitvoering is voltooid, kunt u de bundelconsole weergeven op `http://<host>:<port>/system/console/bundles`.

##  Eenheidstests {#unit-tests}

De eenheidstest in de kernmodule toont de klassieke eenheidstests van de code in de bundel. Om te testen, voer uit:

```shell
mvn clean test
```
