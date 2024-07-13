---
title: Paden naar succes met de kerncomponenten
description: Hoe kan ik slagen wanneer u uw project implementeert met de Core Components
role: Architect, Developer, Admin, User
exl-id: 1ea8cd1c-8435-4ded-82dc-5a7896c53e0c
source-git-commit: b1d38310a3f05e2dd2a68de1574a278bac2c78e7
workflow-type: tm+mt
source-wordcount: '541'
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

* **Afgeronde ontwerpen** - deze zouden kunnen worden goedgekeurd C-Vlak en worden overgeleverd aan het ontwikkelingsteam om pixel-perfect zonder zorg voor de onderliggende technologie worden uitgevoerd.
* **een bedrijf-brede HTML stijl-gids** - Dergelijke gidsen moeten te vaak dogmatisch door de componenten worden gevolgd die stijlen van een top-down perspectief toepassen.

In beide gevallen zijn de vereisten voor de onderdelen zo strak en specifiek dat het moeilijk is om de Core Components (Basiscomponenten) of een out-of-the-box component eraan te voldoen, wat leidt tot een enorme ontwikkeling van aangepaste componenten.

## Begin vroeg {#start-early}

In plaats van alleen de kerncomponenten in de implementatiefase van uw project te bekijken, begint u al met de kerncomponenten tijdens de draadframe- en ontwerpfase.

### De componentbibliotheek gebruiken {#component-library}

Verwijzing de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library) reeds in de ontwerpfase. De Core Components zijn krachtig en flexibel en kunnen u tot een beginpunt leiden. Voeg alleen aangepaste componenten toe wanneer er een echte zakelijke behoefte is die redelijkerwijs niet met een kerncomponent kan worden bereikt.

### De UI-kit voor Adobe XD gebruiken {#ui-kit}

Zodra er een bewezen behoefte aan een douanecomponent is, hefboomwerking de uitrusting UI voor Adobe XD, [ die hier kan worden gedownload, ](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd) zodat de ontwerpers kunnen beginnen draadframes en de ontwerpen met de Componenten van de Kern te bouwen als bouwstenen.

## Laat krachtige functies onverlet {#powerful-features}

De eigenschappen van AEM en de Componenten van de Kern kunnen zeer krachtig, maar ook zeer subtiel zijn en de mogelijkheden voor bepaalde functionaliteit zouden niet onmiddellijk duidelijk aan een ontwerper kunnen zijn.

### Inhoudsfragmenten {#content-fragments}

[ de Fragmenten van de Inhoud ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html) staan u toe om kanaal-neutrale inhoud, samen met (misschien kanaal-specifieke) variaties tot stand te brengen. Vervolgens kunt u deze fragmenten en de variaties ervan gebruiken bij het ontwerpen van de inhoudspagina&#39;s.

Samen met de bijgewerkte JSON-exportfunctie kunnen gestructureerde inhoudsfragmenten ook worden gebruikt om AEM inhoud via Content Services te leveren aan andere kanalen dan AEM pagina&#39;s.

### Fragmentsjablonen ervaren {#experience-fragment-templates}

Als een auteur onderdelen (een fragment van een ervaring) van een pagina opnieuw wil gebruiken. Zonder [ Fragmenten van de Ervaring, ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html) zou de auteur dat fragment moeten kopiëren en kleven. Het maken en onderhouden van deze kopiëren/plakken-ervaringen kost veel tijd en is vaak het gevolg van gebruikersfouten. De Fragmenten van de ervaring elimineren de behoefte aan exemplaar/deeg.

### De component Embed {#embed-component}

[ de Embed Component ](/help/components/embed.md) staat niet alleen voor eenvoudige opneming van externe middelen zoals de videoinhoud van YouTube toe, maar is ook verlengbaar om het toe te staan om inhoud aan te passen specifiek voor de behoeften van een project.
