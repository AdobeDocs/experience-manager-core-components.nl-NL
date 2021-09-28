---
title: Vooraf gecompileerde, gecompileerde scripts
description: Leer hoe te om uw componentenmanuscripten via bundels OSGi aan de Cloud Service van Adobe Experience Manager op te stellen.
source-git-commit: 56464decc8d6ae3cef68d62bfe459bceda0539ef
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# Vooraf gecompileerde, gecompileerde scripts

AEM als Cloud Service steunt de plaatsing van [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) componentenmanuscripten als vooraf gecompileerde gebundelde manuscripten. Dit staat ontwikkelaars toe om hun manuscripten in bouwstijl-tijd vooraf samen te stellen en hen als bundels te verpakken OSGi.

## De voordelen om vooraf gecompileerde manuscripten via bundels op te stellen OSGi

Het opstellen van uw manuscripten als vooraf gecompileerde gebundelde manuscripten heeft de volgende voordelen:

+ het compileren van manuscripten bij bouwstijltijd staat ontwikkelaars toe om fouten vroeg in het ontwikkelingsproces te ontdekken
+ Java API-scriptafhankelijkheden worden expliciet gedefinieerd via de bundelkoppen `Import-Package` en `Export-Package`
+ overerving (via `sling:resourceSuperType`) en delegatie naar andere middeltypes (via het blokelement `data-sly-resource` van HTML of via `sling:include` JSP markering, bijvoorbeeld) kunnen via de meta-gegevens van de bundel worden in kaart gebracht
+ versioning van bronnen kan op vergelijkbare wijze worden afgedwongen als de Java API&#39;s

## Vooraf samengestelde en uit te voeren pakketten

Met [`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html) kunt u de syntaxis van HTML-scripts valideren, maar u kunt deze ook gebruiken om de HTML-scripts om te zetten in Java-klassen. Deze worden dan toegevoegd aan de `generated-sources` omslag van uw Geweven project en opgepikt door `maven-compiler-plugin`.

[`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin) kan worden toegevoegd om de meta-gegevens van de bundel OSGi voor de invoer van Java API te produceren.

## Overerving en delegatie

Het OSGi-framework biedt een krachtige manier om [Vereisten en Capabilities](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies) te definiëren om contracten tussen verschillende componenten uit te drukken. Deze worden beschreven via meta-gegevens en tijdens runtime afgedwongen. Gebundelde scripts gebruiken dit mechanisme om zowel hun overervingsrelaties (`sling:resourceSuperType`) als delegatie (inclusief andere typen bronnen in het renderingsproces) uit te drukken.

De `bnd`-plug-in van het [scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html)-project kan worden gebruikt om de vereisten en mogelijkheden te extraheren die overeenkomen met de scripts die worden geleverd door het [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles)-inhoudspakket.

## Ondersteuning voor Project Archetype AEM

Beginnend met versie 31, kan [AEM Project Archetype](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html) worden gebruikt aan correcte opstelling AEM als project van de Cloud Service om vooraf gecompileerde gebundelde manuscripten te gebruiken. Daarnaast configureert het AEM Project Archetype [AEM als Cloud Service SDK Build Analyzer Maven Plugin](/help/developing/archetype/build-analyzer-maven-plugin.md) om het pakket-niveau Java evenals manuscript-vlakke gebiedsdelen te bevestigen.
