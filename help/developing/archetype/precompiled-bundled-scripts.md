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

AEM as a Cloud Service ondersteunt de implementatie van de [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) componentscripts als vooraf gecompileerde, gebundelde scripts. Dit staat ontwikkelaars toe om hun manuscripten in bouwstijl-tijd vooraf samen te stellen en hen als bundels te verpakken OSGi.

## Voordelen van het Opstellen van Vooraf gecompileerde Manuscripten via Bundels OSGi {#advantages}

Het opstellen van uw manuscripten als vooraf gecompileerde gebundelde manuscripten heeft de volgende voordelen:

+ Door scripts tijdens het samenstellen te compileren kunnen ontwikkelaars fouten vroeg in het ontwikkelingsproces opsporen.
+ Java API-scripteigenschappen worden expliciet gedefinieerd via de `Import-Package` en `Export-Package` bundelkoppen.
+ Overerving (via `sling:resourceSuperType`) en delegatie naar andere typen bronnen (via HTL&#39;s `data-sly-resource` blokelement of via `sling:include` JSP-tag, bijvoorbeeld) kan worden toegewezen via de metagegevens van de bundel.
+ Het versioning van het middeltype kan op een gelijkaardige manier als Java APIs worden afgedwongen.

## Vooraf compileren en Pakket importeren {#precompilation}

De [`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html) U kunt de syntaxis van HTML-scripts valideren, maar u kunt deze ook gebruiken om de HTML-scripts om te zetten in Java-klassen. Deze worden vervolgens toegevoegd aan de `generated-sources` en opgepakt door de `maven-compiler-plugin`.

De [`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin) kan worden toegevoegd om de metagegevens van de OSGi-bundel te genereren voor de invoer van Java API.

## Overerving en delegatie {#inheritance-delegation}

Het OSGi-kader biedt een krachtige manier om [vereisten en mogelijkheden](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies) overeenkomsten tussen verschillende componenten uit te drukken. Deze worden beschreven via meta-gegevens en tijdens runtime afgedwongen. Gebundelde scripts gebruiken dit mechanisme om hun overervingsrelaties uit te drukken (`sling:resourceSuperType`), alsmede delegeren (met inbegrip van andere typen bronnen in het renderingsproces).

De `bnd` insteekmodule van de [scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) kan worden gebruikt om de vereisten en mogelijkheden te extraheren die overeenkomen met de scripts die door de [`ui.apps`.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) inhoudspakket

## Ondersteuning voor projectarchetype AEM {#support}

Vanaf versie 31 worden de [Projectarchetype AEM](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html) kan aan correct opstelling worden gebruikt een AEM as a Cloud Service project om vooraf gecompileerde gebundelde manuscripten te gebruiken.

Bovendien vormt het AEM Project Archetype [AEM as a Cloud Service SDK Build Analyzer Maven Plugin](/help/developing/archetype/build-analyzer-maven-plugin.md) om de pakket-vlakke evenals manuscript-vlakke gebiedsdelen van Java te bevestigen.
