---
title: Vooraf gecompileerde, gecompileerde scripts
description: Leer hoe te om uw componentenmanuscripten via bundels OSGi aan de Cloud Service van Adobe Experience Manager op te stellen.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 3edc388f-01b2-45cc-bd56-f22e5a5a8624
source-git-commit: 554be9539428cd75462a38fc45f1bece04baf066
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---


# Vooraf gecompileerde, gecompileerde scripts {#precompiled-bundled-scripts}

AEM as a Cloud Service steunt de plaatsing van de [`ui.apps` ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) componentenmanuscripten als vooraf gecompileerde gebundelde manuscripten. Dit staat ontwikkelaars toe om hun manuscripten in bouwstijl-tijd vooraf samen te stellen en hen als bundels te verpakken OSGi.

## Voordelen van het Opstellen van Vooraf gecompileerde Manuscripten via Bundels OSGi {#advantages}

Het opstellen van uw manuscripten als vooraf gecompileerde gebundelde manuscripten heeft de volgende voordelen:

+ Door scripts tijdens het samenstellen te compileren kunnen ontwikkelaars fouten vroeg in het ontwikkelingsproces opsporen.
+ Java API-scripteigenschappen worden expliciet gedefinieerd via de `Import-Package` - en `Export-Package` -bundelkoppen.
+ Overerving (via `sling:resourceSuperType` ) en delegatie naar andere typen bronnen (via het blokelement `data-sly-resource` van HTML of via de JSP-tag `sling:include` bijvoorbeeld) kunnen worden toegewezen via de metagegevens van de bundel.
+ Het versioning van het middeltype kan op een gelijkaardige manier als Java APIs worden afgedwongen.

## Vooraf compileren en Pakket importeren {#precompilation}

[`htl-maven-plugin` ](https://sling.apache.org/components/htl-maven-plugin/index.html) kan de syntaxis van manuscripten van HTML bevestigen, maar het kan ook worden gebruikt om de manuscripten van HTML in klassen van Java te transpileren. Deze worden vervolgens toegevoegd aan de map `generated-sources` van het Maven-project en vervolgens opgehaald door `maven-compiler-plugin` .

[`bnd-maven-plugin` ](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin) kan worden toegevoegd om de meta-gegevens van de bundel OSGi voor de invoer van Java API te produceren.

## Overerving en delegatie {#inheritance-delegation}

Het kader OSGi verstrekt een krachtige manier om [ vereisten en mogelijkheden ](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies) te bepalen om contracten tussen diverse componenten uit te drukken. Deze worden beschreven via meta-gegevens en tijdens runtime afgedwongen. Gebundelde manuscripten gebruiken dit mechanisme om zowel hun overervingsverhoudingen (`sling:resourceSuperType`) uit te drukken, als delegatie (met inbegrip van andere middeltypes in het teruggevende proces).

De `bnd` insteekmodule van het [ scriptingbundle-maven-plugin ](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) project kan worden gebruikt om de vereisten en de mogelijkheden te halen die aan de manuscripten beantwoorden die door [`ui.apps` worden verstrekt.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) inhoudspakket

## Ondersteuning voor projectarchetype AEM {#support}

Beginnend met versie 31, kan het [ AEM Archetype van het Project ](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html) worden gebruikt aan correct opstelling een project van AEM as a Cloud Service om vooraf gecompileerde gebundelde manuscripten te gebruiken.

Bovendien vormt het AEM Archieftype van het Project de [ SDK van AEM as a Cloud Service bouwt Analysator Gemaakte Insteekmodule ](/help/developing/archetype/build-analyzer-maven-plugin.md) om Java pakket-niveau evenals manuscript-vlakke gebiedsdelen te bevestigen.
