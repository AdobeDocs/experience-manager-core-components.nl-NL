---
title: Kernmodule van het AEM Project Archetype
description: Kernmodule van het AEM Project Archetype
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Kernmodule van het AEM Project Archetype {#core-module}

De kernmodule (`<src-directory>/<project>/core`) bevat alle Java-code die nodig is voor de implementatie. De module zal alle code van Java verpakken en aan de instantie AEM als Bundel OSGi opstellen.

De in de `<src-directory>/<project>/core/pom.xml` definitie gedefinieerde bundelinsteekmodule Geweven is verantwoordelijk voor het compileren van de Java-code in een OSGi-bundel die door de OSGi-container van AEM kan worden herkend. Hier wordt de locatie van verkoopmodellen gedefinieerd.

Hoewel het zeldzaam is dat de kernbundel onafhankelijk van de module ui.apps in hogere niveaumilieu&#39;s moet worden opgesteld, is het direct opstellen van de kernbundel nuttig tijdens lokale ontwikkeling/het testen. Met de plug-in Maven Sling kan de kernbundel worden geïmplementeerd in AEM door rechtstreeks gebruik te maken van het `autoInstallBundle` profiel zoals gedefinieerd in de [bovenliggende POM](overview.md#parent-pom).

```
mvn -PautoInstallBundle clean install
```

Als de uitvoering is voltooid, kunt u de bundelconsole weergeven op `http://<host>:<port>/system/console/bundles`.
