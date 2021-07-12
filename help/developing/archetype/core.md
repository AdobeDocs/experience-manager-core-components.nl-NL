---
title: De Module van de kern van het AEM Project Archetype
description: De Module van de kern van het AEM Project Archetype
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 49e80d8c-2b41-4c42-b45e-c2e3b4b16a59
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# De Module van de kern van het AEM Project Archetype {#core-module}

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
