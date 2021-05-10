---
title: Paden naar succes met de kerncomponenten
description: Hoe kan ik slagen wanneer u uw project implementeert met de Core Components
role: Architect, Developer, Administrator, Business Practitioner
exl-id: 1ea8cd1c-8435-4ded-82dc-5a7896c53e0c
translation-type: tm+mt
source-git-commit: 056c5bc15ac9e669c3bf6d5da7f060d6eef02608
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 0%

---

# Paden naar succes met de Core Components {#paths-to-success}

De kerncomponenten zijn krachtig, flexibel en gebruiksvriendelijk. Als u een aantal belangrijke richtlijnen volgt die in dit document worden beschreven, weet u zeker dat uw project met de kerncomponenten een succes is.

## Twee paden om te slagen {#two-paths}

Er zijn twee basisbenaderingen voor de implementatie van de kerncomponenten, die tot succes kunnen leiden maar hun eigen compromissen hebben die per project moeten worden bekeken.

1. Wijs uw ontwerpen toe aan de Componenten van de Kern en neem HTML die zij verstrekken. of
1. Als u moet voldoen aan reeds-bepaalde normen van HTML zult u meer inspanning nodig hebben en niet alle voordelen van de kerncomponenten krijgen.

## Veelvoorkomende valkuilen in componentimplementatie {#common-pitfalls}

Twee gemeenschappelijke kwesties die tot projecten leiden die niet met de Componenten van de Kern slagen zijn:

* **Afgeronde ontwerpen**  - Deze worden misschien wel op C-niveau goedgekeurd en worden overgedragen aan het ontwikkelingsteam om Pixel Perfect te implementeren zonder dat de onderliggende technologie daar zorgen over heeft.
* **Een HTML-stijlhulplijn**  voor het hele bedrijf: dergelijke hulplijnen moeten te vaak dogmatisch worden gevolgd door de componenten die stijlen vanuit een top-down perspectief toepassen.

In beide gevallen zijn de vereisten voor de onderdelen zo strak en specifiek dat het moeilijk is om de Core Components (Basiscomponenten) of een out-of-the-box component eraan te voldoen, wat leidt tot een enorme ontwikkeling van aangepaste componenten.

## Begin vroeg {#start-early}

In plaats van alleen de kerncomponenten in de implementatiefase van uw project te bekijken, begint u al met de kerncomponenten tijdens de draadframe- en ontwerpfase.

### De componentbibliotheek {#component-library} gebruiken

Verwijs [Component Library](https://adobe.com/go/aem_cmp_library) reeds in de ontwerpfase. De Core Components zijn krachtig en flexibel en kunnen u tot een uitgangspunt leiden. Voeg alleen aangepaste componenten toe wanneer er een echte zakelijke behoefte is die redelijkerwijs niet met een kerncomponent kan worden bereikt.

### De UI-kit voor Adobe XD gebruiken {#ui-kit}

Zodra er een aantoonbare behoefte aan een douanecomponent is, hefboomwerking de [UI uitrusting voor Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd) zodat de ontwerpers kunnen beginnen draadframes en de ontwerpen met de Componenten van de Kern als bouwstenen te bouwen.

## Laat krachtige functies {#powerful-features} niet over

De eigenschappen van AEM en de Componenten van de Kern kunnen zeer krachtig, maar ook zeer subtiel zijn en de mogelijkheden voor bepaalde functionaliteit zouden niet onmiddellijk duidelijk aan een ontwerper kunnen zijn.

### Contentfragmenten {#content-fragments}

[Met ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html) fragmentatie van inhoud kunt u kanaalneutrale inhoud maken, samen met (mogelijk kanaalspecifieke) variaties. Vervolgens kunt u deze fragmenten en de variaties ervan gebruiken bij het ontwerpen van de inhoudspagina&#39;s.

Samen met de bijgewerkte JSON-exportfunctie kunnen gestructureerde inhoudsfragmenten ook worden gebruikt om AEM inhoud via Content Services te leveren aan andere kanalen dan AEM pagina&#39;s.

### Ervaar fragmentsjablonen {#experience-fragment-templates}

Als een auteur onderdelen (een fragment van een ervaring) van een pagina opnieuw wil gebruiken. Zonder [Fragmenten ervaren,](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html) zou de auteur dat fragment moeten kopiëren en kleven. Het maken en onderhouden van deze kopiëren/plakken-ervaringen kost veel tijd en is vaak het gevolg van gebruikersfouten. De Fragmenten van de ervaring elimineren de behoefte aan exemplaar/deeg.

### De component Embed {#embed-component}

[Met de ](/help/components/embed.md) component Embed kunt u niet alleen eenvoudig externe bronnen, zoals YouTube-video-inhoud, opnemen, maar kunt u deze ook uitbreiden om inhoud die specifiek is voor de behoeften van een project, te kunnen bevatten.
