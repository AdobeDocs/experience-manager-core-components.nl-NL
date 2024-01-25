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
>Het nieuwste AEM Projectarchetype en de bijbehorende technische documentatie [kan op GitHub worden gevonden.](https://github.com/adobe/aem-project-archetype)

## Aan de slag {#getting-started}

Het project archetype maakt het gemakkelijk om zich op AEM te beginnen ontwikkelen. U kunt uw eerste stappen met archetype op een aantal manieren nemen.

* **WKND-zelfstudie** - Voor een grote inleiding bij het ontwikkelen van AEM, met inbegrip van hoe te om het archetype te gebruiken zie [Aan de slag met AEM Sites - WKND-zelfstudie](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) voor een praktisch voorbeeld dat u door het gebruiken van archetype loopt om een eenvoudig project uit te voeren.
* **Zelfstudie over WKND-gebeurtenissen** - Als u bijzonder geïnteresseerd bent in de ontwikkeling van één pagina voor toepassingen (SPA) op AEM, moet u de speciale [Zelfstudie over WKND-gebeurtenissen.](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)
* **Eigen beginnen!** - U kunt de [huidig projectarchetype beschikbaar op GitHub](https://github.com/adobe/aem-project-archetype) en maak uw eerste project zelf.

## Het gebruiken van Archetype {#how-to-use-the-archetype}

De eerste stap die archetype gebruikt moet een project tot stand brengen, dat produceert [de modules](#what-you-get) in een lokale bestandsstructuur. Als deel van projectgeneratie, kan een aantal eigenschappen voor uw project worden bepaald zoals projectnaam, versie, toelatend diverse opties, enz.

>[!TIP]
>
>Wanneer u het archetype bouwt, zal het ook een reeks lezingen produceren, die u van de technische details en het gebruik van elke module voorzien zoals [is hieronder gekoppeld.](#what-you-get)

Het bouwen van het project met Maven leidt tot de artefacten (pakketten en bundels OSGi), die aan AEM kunnen worden opgesteld. De extra Gemaakt bevelen en de profielen kunnen worden gebruikt om de projectartefacten aan een AEM instantie op te stellen.

## Wat u krijgt met Archetype {#what-you-get}

Het archetype bestaat uit modules, die allen automatisch worden gecreeerd wanneer het gebruiken van archetype.

* **[kern](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** is een bundel van Java die alle kernfunctionaliteit zoals de diensten OSGi, luisteraars, en planners, evenals component-verwante code van Java zoals servlets en verzoekfilters bevat.
* **[it.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** zijn op Java gebaseerde integratietests.
* **[ui.apps](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.apps)** bevat de `/apps` en `/etc` delen van het project, d.w.z. JS en CSS clientlibs, componenten, en malplaatjes.
* **[ui.content](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.content)** bevat voorbeeldinhoud met behulp van de componenten uit de module ui.apps.
* **[ui.config](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.config)** bevat runtime-specifieke OSGi vormen voor het project.
* **[ui.frontend.general](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.general)** bevat de artefacten die worden vereist om de algemene Web-pack-gebaseerde voorste bouwstijlmodule (facultatief) te gebruiken.
* **[ui.frontend.response](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.react)** **(optioneel)** bevat de artefacten die wanneer het gebruiken van archetype worden vereist om SPA tot stand te brengen die op React (facultatief, hangt van bouwstijlparameters af) worden gebaseerd.
* **[ui.frontend.angular](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.angular)** **(optioneel)** bevat de artefacten die wanneer het gebruiken van archetype worden vereist om een SPA tot stand te brengen die op Angular (facultatief, hangt van bouwstijlparameters af) worden gebaseerd.
* **[ui.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** bevat op selenium gebaseerde UI-tests.
* **[alles](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/all)** is één enkel inhoudspakket dat alle gecompileerde modules (bundels en inhoudspakketten) met inbegrip van om het even welke verkopersgebiedsdelen inbedt.
* **[dispatcher.ams](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.ams)** bevat de basisconfiguraties van de verzender voor projecten AMS/on-prem (facultatief, hangt van bouwstijlparameters af).
* **[dispatcher.cloud](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.cloud)** bevat de basisconfiguraties van de verzender voor projecten AEMaaCS (facultatief, hangt van bouwstijlparameters af).

![Inhoudspakketorganisatie](/help/assets/content-package-organization.png)

De modules van archetype in Maven worden vertegenwoordigd opgesteld aan AEM als inhoudspakketten die de toepassing, de inhoud, en de noodzakelijke bundels OSGi vertegenwoordigen.

## Bovenliggende POM {#parent-pom}

De `pom.xml` aan de basis van het project (`<src-directory>/<project>/pom.xml`) staat bekend als de bovenliggende POM en drijft de structuur van het project en beheert afhankelijkheden en bepaalde algemene eigenschappen van het project.

### Algemene projecteigenschappen {#global-properties}

De `<properties>` sectie van ouderPOM bepaalt verscheidene globale eigenschappen die voor de plaatsing van uw project op een AEM instantie zoals gebruikersnaam/wachtwoord, gastheernaam/haven, enz. belangrijk zijn.

Deze eigenschappen worden opstelling om aan een lokale AEM instantie op te stellen, aangezien dit de gemeenschappelijkste bouwstijl is die de ontwikkelaars zullen doen. Er zijn eigenschappen die in een auteurinstantie en een publicatieinstantie moeten worden geïmplementeerd. Dit is ook waar de geloofsbrieven worden geplaatst om met de AEM instantie voor authentiek te verklaren. De standaardwaarde `admin:admin` referenties worden gebruikt.

Deze eigenschappen zijn opstelling zodat zij kunnen worden met voeten getreden wanneer het opstellen aan hogere niveaumilieu&#39;s. Op deze manier hoeven de POM-bestanden niet te worden gewijzigd, maar variabelen zoals `aem.host` en `sling.password` kan worden overschreven via opdrachtregelargumenten:

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Modulestructuur {#module-structure}

De `<modules>` de sectie van ouderPOM bepaalt de modules die het project zal bouwen. Standaard wordt het project gebouwd [de eerder gedefinieerde standaardmodules.](#what-you-get) Meer modules kunnen altijd worden toegevoegd aangezien een project evolueert.

### Afhankelijkheden {#dependencies}

De `<dependencyManagement>` sectie van ouderPOM bepaalt alle gebiedsdelen en versies van APIs die in het project worden gebruikt. Versies moeten worden beheerd in de bovenliggende POM. Submodules mogen geen versiegegevens bevatten.

#### Uber-Jar {#uber-jar}

Een van de belangrijkste afhankelijkheden is de [AEM Java API Jar.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) Dit omvat alle AEM APIs met enkel één enkele gebiedsdeelingang voor de versie van AEM.

>[!NOTE]
>
>Als beste praktijken zou u de uber-jar versie moeten bijwerken om de doelversie van AEM aan te passen. Als u bijvoorbeeld wilt implementeren op AEM 6.5, moet u de versie van de uber-jar bijwerken naar 6.5.X, waar `X` is het recentste de dienstpak.

#### Kernonderdelen {#core-components}

Het archetype maakt natuurlijk gebruik van de [Core Components.](/help/introduction.md) Daarom is het, om de Componenten van de Kern in alle plaatsingen te gebruiken, een beste praktijk om hen als deel van het Maven project te omvatten.

core.wcm.components.examples zijn een reeks steekproefpagina&#39;s die voorbeelden van de Componenten van de Kern illustreren. Als beste praktijken, wanneer het opstellen van een project voor productiegebruik zou u deze gebiedsdeel en subpackage opneming moeten verwijderen.

>[!NOTE]
>
>De Componenten van de Kern en het archetype worden gehandhaafd als afzonderlijke projecten GitHub en als dusdanig verschillen hun versies.
>
>Elke versie van het archetype zal de recentste versie van de Componenten van de Kern gebruiken beschikbaar op het tijdstip van de versie. U kunt de afhankelijkheid van de kerncomponenten echter handmatig bijwerken.

## Testen {#testing}

Het project bevat drie testniveaus en omdat het verschillende typen tests zijn, worden deze op verschillende manieren of op verschillende plaatsen uitgevoerd.

* **[Eenheidstests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** - Klassieke eenheidstests van de code in de bundel
* **[Integratietests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** - integratietests aan de serverzijde die eenheidstests in de AEM-omgeving, d.w.z. op de AEM server in werking stellen
* **[UI-tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** - Op selenium gebaseerde browserzijtests die browsergedrag controleren
