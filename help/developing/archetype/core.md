---
title: De Module van de kern van het AEM Project Archetype
description: De Module van de kern van het AEM Project Archetype
translation-type: tm+mt
source-git-commit: 6f7166c46940ed451721e0760d565d58efe412ab
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---


# De Module van de kern van het AEM Archetype van het Project {#core-module}

De kernmodule (`<src-directory>/<project>/core`) bevat alle Java-code die nodig is voor de implementatie. De module zal alle code van Java verpakken en aan de AEM instantie als Bundel OSGi opstellen.

De in `<src-directory>/<project>/core/pom.xml` gedefinieerde bundelinsteekmodule Geweven is verantwoordelijk voor het compileren van de Java-code in een OSGi-bundel die door AEM OSGi-container kan worden herkend. Hier wordt de locatie van verkoopmodellen gedefinieerd.

Hoewel het zeldzaam is dat de kernbundel onafhankelijk van de module ui.apps in hogere niveaumilieu&#39;s moet worden opgesteld, is het direct opstellen van de kernbundel nuttig tijdens lokale ontwikkeling/het testen. Met de plug-in Maven Sling kan de kernbundel worden geïmplementeerd om het profiel `autoInstallBundle` rechtstreeks te AEM, zoals gedefinieerd in de [bovenliggende POM](/help/developing/archetype/using.md#parent-pom).

```
mvn -PautoInstallBundle clean install
```

Nadat de uitvoering is voltooid, kunt u de bundelconsole weergeven op `http://<host>:<port>/system/console/bundles`.
