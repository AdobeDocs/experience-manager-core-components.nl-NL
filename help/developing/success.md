---
title: Paden naar succes met de kerncomponenten
description: Hoe kan ik slagen wanneer u uw project implementeert met de Core Components
role: Architect, Developer, Admin, User
exl-id: 1ea8cd1c-8435-4ded-82dc-5a7896c53e0c
source-git-commit: 888719359f9a1d1c9dccff97fb639b332f2be54c
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 0%

---

# Paden naar succes met de kerncomponenten {#paths-to-success}

De kerncomponenten zijn krachtig, flexibel en gebruiksvriendelijk. Als u een aantal belangrijke richtlijnen volgt die in dit document worden beschreven, weet u zeker dat uw project met de kerncomponenten een succes is.

## Twee paden om te slagen {#two-paths}

Er zijn twee basisbenaderingen voor de implementatie van de kerncomponenten, die tot succes kunnen leiden maar hun eigen compromissen hebben die per project moeten worden bekeken.

1. Breng uw ontwerpen in kaart aan de Componenten van de Kern en neem de HTML die zij verstrekken. of
1. Als u aan reeds-bepaalde normen van de HTML moet voldoen zult u meer inspanning nodig hebben en niet alle voordelen van de kerncomponenten krijgen.

## Veelvoorkomende fouten in componentimplementatie {#common-pitfalls}

Twee gemeenschappelijke kwesties die tot projecten leiden die niet met de Componenten van de Kern slagen zijn:

* **Voltooide ontwerpen** - Deze zouden zelfs op C-niveau kunnen worden goedgekeurd en worden overgedragen aan het ontwikkelingsteam om pixelvolmaakt te worden geïmplementeerd zonder dat de onderliggende technologie daarbij betrokken is.
* **Een HTML stijlgids voor het hele bedrijf** - Dergelijke gidsen moeten te vaak dogmatisch worden gevolgd door de componenten die stijlen toepassen vanuit een top-down perspectief.

In beide gevallen zijn de vereisten voor de onderdelen zo strak en specifiek dat het moeilijk is om de Core Components (Basiscomponenten) of een out-of-the-box component eraan te voldoen, wat leidt tot een enorme ontwikkeling van aangepaste componenten.

## Begin vroeg {#start-early}

In plaats van alleen de kerncomponenten in de implementatiefase van uw project te bekijken, begint u al met de kerncomponenten tijdens de draadframe- en ontwerpfase.

### De componentbibliotheek gebruiken {#component-library}

Verwijs naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library) reeds in de ontwerpfase. De Core Components zijn krachtig en flexibel en kunnen u tot een uitgangspunt leiden. Voeg alleen aangepaste componenten toe wanneer er een echte zakelijke behoefte is die redelijkerwijs niet met een kerncomponent kan worden bereikt.

### De UI-kit voor Adobe XD gebruiken {#ui-kit}

Zodra er een aantoonbare behoefte aan een aangepaste component is, kunt u de opdracht [UI-kit voor Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd)  zodat de ontwerpers de draadframes en de ontwerpen kunnen beginnen te bouwen met de Componenten van de Kern als bouwstenen.

## Laat krachtige functies niet over het hoofd zien {#powerful-features}

De eigenschappen van AEM en de Componenten van de Kern kunnen zeer krachtig, maar ook zeer subtiel zijn en de mogelijkheden voor bepaalde functionaliteit zouden niet onmiddellijk duidelijk aan een ontwerper kunnen zijn.

### Contentfragmenten {#content-fragments}

[Inhoudsfragmenten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html) kunt u kanaalneutrale inhoud maken, samen met (mogelijk kanaalspecifieke) variaties. Vervolgens kunt u deze fragmenten en de variaties ervan gebruiken bij het ontwerpen van de inhoudspagina&#39;s.

Samen met de bijgewerkte JSON-exportfunctie kunnen gestructureerde inhoudsfragmenten ook worden gebruikt om AEM inhoud via Content Services te leveren aan andere kanalen dan AEM pagina&#39;s.

### Fragmentsjablonen ervaren {#experience-fragment-templates}

Als een auteur onderdelen (een fragment van een ervaring) van een pagina opnieuw wil gebruiken. Zonder [ervaringsfragmenten,](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html) de auteur moet dat fragment kopiëren en plakken. Het maken en onderhouden van deze kopiëren/plakken-ervaringen kost veel tijd en is vaak het gevolg van gebruikersfouten. De Fragmenten van de ervaring elimineren de behoefte aan exemplaar/deeg.

### De component Embed {#embed-component}

[De component Embed](/help/components/embed.md) staat niet alleen voor eenvoudige opneming van externe middelen zoals de video-inhoud van YouTube toe, maar is ook verlengbaar om het toe te staan om inhoud aan te passen specifiek aan de behoeften van een project.
