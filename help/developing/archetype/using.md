---
title: Het gebruiken van het AEM Project Archetype
description: Leer hoe u het AEM Project Archetype kunt gebruiken om een minimaal Adobe Experience Manager-project op basis van best practices te maken als startpunt voor uw eigen AEM.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
source-git-commit: bd92a5d1884056ca7b44ea28e5817d8bde10a4d9
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---


# Het gebruiken van het AEM Project Archetype {#using-the-archetype}

In dit document wordt uitgelegd hoe u het AEM Project Archetype kunt gebruiken om een minimaal Adobe Experience Manager-project op basis van best practices te maken als startpunt voor uw eigen AEM projecten.

Het richt zich op algemene gebruikspatronen en wat het archetype voor u doet. Voor gedetailleerde bouwstijlopties en technische instructies, te zien gelieve de documentatie in de bewaarplaats GitHub van archetype.

>[!TIP]
>
>Het recentste AEM Archetype van het Project en bijbehorende technische documentatie [ kunnen op GitHub worden gevonden.](https://github.com/adobe/aem-project-archetype)

## Aan de slag {#getting-started}

Het project archetype maakt het gemakkelijk om zich op AEM te beginnen ontwikkelen. U kunt uw eerste stappen met archetype op een aantal manieren nemen.

* **WKND Leerprogramma** - voor een grote inleiding aan het ontwikkelen op AEM met inbegrip van hoe te hefboomwerking het archetype zien [ Begonnen het WKND Leerprogramma ](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=nl-NL) voor een praktisch voorbeeld dat u door het gebruiken van archetype loopt om een eenvoudig project uit te voeren.
* **het Leerprogramma van de Gebeurtenissen van WKND** - als u bijzonder in de ontwikkeling van één enkele paginatoepassing (SPA) op AEM geinteresseerd bent, ben zeker om het specifieke [ WKND leerprogramma van Gebeurtenissen te controleren.](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)
* **Begin alleen!** - U kunt het [ huidige project archetype gemakkelijk downloaden beschikbaar op GitHub ](https://github.com/adobe/aem-project-archetype) en uw eerste project op uw tot stand brengen.

## Het gebruiken van Archetype {#how-to-use-the-archetype}

De eerste stap die archetype gebruikt moet een project tot stand brengen, dat [ de modules ](#what-you-get) in een lokale dossierstructuur produceert. Als deel van projectgeneratie, kan een aantal eigenschappen voor uw project worden bepaald zoals projectnaam, versie, toelatend diverse opties, enz.

>[!TIP]
>
>Wanneer u het archetype bouwt, zal het ook een reeks lezingen produceren, die u van de technische details en het gebruik van elke module voorzien zoals [ hieronder verbonden.](#what-you-get)

Het bouwen van het project met Maven leidt tot de artefacten (pakketten en bundels OSGi), die aan AEM kunnen worden opgesteld. De extra Gemaakt bevelen en de profielen kunnen worden gebruikt om de projectartefacten aan een AEM instantie op te stellen.

## Wat u krijgt met Archetype {#what-you-get}

Het archetype bestaat uit modules, die allen automatisch worden gecreeerd wanneer het gebruiken van archetype.

* **[kern ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** is een bundel van Java die alle kernfunctionaliteit zoals diensten OSGi, luisteraars, en planners, evenals op component betrekking hebbende code van Java zoals servlets en verzoekfilters bevatten.
* **[it.tests ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** zijn op Java-Gebaseerde integratietests.
* **[ui.apps ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.apps)** bevat de `/apps` en `/etc` delen van het project, d.w.z. JS en CSS clientlibs, componenten, en malplaatjes.
* **[ui.content ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.content)** bevat steekproefinhoud gebruikend de componenten van de module ui.apps.
* **[ui.config ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.config)** bevat runtime-specifieke OSGi vormt voor het project.
* **[ui.frontend.general ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.general)** bevat de artefacten die worden vereist om de algemene Web-pack-Gebaseerde voorste bouwstijlmodule (facultatief) te gebruiken.
* **[ui.frontend.response ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.react)** **(facultatief)** bevat de artefacten die wanneer het gebruiken van archetype worden vereist om SPA projecten tot stand te brengen die op React (facultatief, afhangt van bouwstijlparameters) worden gebaseerd.
* **[ui.frontend.angular ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.angular)** **(facultatief)** bevat de artefacten die wanneer het gebruiken van archetype worden vereist om tot SPA projecten te leiden die op Angular (facultatief, afhangt van bouwstijlparameters) worden gebaseerd.
* **[ui.tests ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** bevat op selenium-Gebaseerde tests UI.
* **[allen ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/all)** is één enkel inhoudspakket dat alle gecompileerde modules (bundels en inhoudspakketten) met inbegrip van om het even welke verkopersgebiedsdelen inbedt.
* **[dispatcher.ams ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.ams)** bevat de basisberichtcherconfiguraties voor AMS/op-prem projecten (facultatief, hangt van bouwstijlparameters af).
* **[dispatcher.cloud ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.cloud)** bevat de basis verzender configuraties voor projecten AEMaaCS (facultatief, hangt van bouwstijlparameters af).

![ het pakketorganisatie van de Inhoud ](/help/assets/content-package-organization.png)

De modules van archetype in Maven worden vertegenwoordigd opgesteld aan AEM als inhoudspakketten die de toepassing, de inhoud, en de noodzakelijke bundels OSGi vertegenwoordigen.

## Bovenliggende POM {#parent-pom}

`pom.xml` bij de wortel van het project (`<src-directory>/<project>/pom.xml`) is gekend als ouder POM en drijft de structuur van het project evenals beheert gebiedsdelen en bepaalde globale eigenschappen van het project.

### Algemene projecteigenschappen {#global-properties}

Het gedeelte `<properties>` van de bovenliggende POM definieert verschillende algemene eigenschappen die belangrijk zijn voor de implementatie van uw project op een AEM instantie, zoals gebruikersnaam/wachtwoord, hostnaam/poort, enz.

Deze eigenschappen worden opstelling om aan een lokale AEM instantie op te stellen, aangezien dit de gemeenschappelijkste bouwstijl is die de ontwikkelaars zullen doen. Er zijn eigenschappen die in een auteurinstantie en een publicatieinstantie moeten worden geïmplementeerd. Dit is ook waar de geloofsbrieven worden geplaatst om met de AEM instantie voor authentiek te verklaren. De standaardreferenties `admin:admin` worden gebruikt.

Deze eigenschappen zijn opstelling zodat zij kunnen worden met voeten getreden wanneer het opstellen aan hogere niveaumilieu&#39;s. Op deze manier hoeven de POM-bestanden niet te worden gewijzigd, maar variabelen zoals `aem.host` en `sling.password` kunnen worden overschreven via opdrachtregelargumenten:

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Modulestructuur {#module-structure}

De `<modules>` sectie van ouderPOM bepaalt de modules die het project zal bouwen. Door gebrek bouwt het project [ de eerder bepaalde standaardmodules.](#what-you-get) Er kunnen altijd meer modules worden toegevoegd terwijl een project evolueert.

### Afhankelijkheden {#dependencies}

De `<dependencyManagement>` sectie van ouderPOM bepaalt alle gebiedsdelen en versies van APIs die in het project worden gebruikt. Versies moeten worden beheerd in de bovenliggende POM. Submodules mogen geen versiegegevens bevatten.

#### Uber-Jar {#uber-jar}

Één van de belangrijkste gebiedsdelen is [AEM Java API Jar.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html?lang=nl-NL) Dit omvat alle AEM API&#39;s met slechts één afhankelijkheidsitem voor de versie van AEM.

>[!NOTE]
>
>Als beste praktijken zou u de uber-jar versie moeten bijwerken om de doelversie van AEM aan te passen. Als u bijvoorbeeld wilt implementeren op AEM 6.5, moet u de versie van de uber-jar bijwerken naar 6.5.X, waarbij `X` het meest recente servicepack is.

#### Kernonderdelen {#core-components}

Het archetype van cursus hefboomwerkingen de [ Componenten van de Kern.](/help/introduction.md) Daarom is het raadzaam om deze componenten op te nemen in het Maven-project, zodat ze bij alle implementaties kunnen worden gebruikt.

core.wcm.components.examples zijn een reeks steekproefpagina&#39;s die voorbeelden van de Componenten van de Kern illustreren. Als beste praktijken, wanneer het opstellen van een project voor productiegebruik zou u deze gebiedsdeel en subpackage opneming moeten verwijderen.

>[!NOTE]
>
>De Componenten van de Kern en het archetype worden gehandhaafd als afzonderlijke projecten GitHub en als dusdanig verschillen hun versies.
>
>Elke versie van het archetype zal de recentste versie van de Componenten van de Kern gebruiken beschikbaar op het tijdstip van de versie. U kunt de afhankelijkheid van de kerncomponenten echter handmatig bijwerken.

## Testen {#testing}

Het project bevat drie testniveaus en omdat het verschillende typen tests zijn, worden deze op verschillende manieren of op verschillende plaatsen uitgevoerd.

* **[Tests van de Eenheid ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** - Klassieke eenheidstests van de code bevat in de bundel
* **[Tests van de Integratie ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** - server-zijintegratietests die eenheid-als tests in werking stellen in het AEM-milieu, d.w.z. op de AEM server
* **[Tests UI ](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** - Op selenium-Gebaseerde browser-zijtests die browser-zijgedrag verifiëren
