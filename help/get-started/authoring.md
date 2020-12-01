---
title: Ontwerpen met kerncomponenten
description: In AEM, zijn de componenten de structurele elementen die de inhoud van de pagina's vormen die worden ontworpen - de Componenten van de Kern bieden flexibele en eigenschap-rijke auteursfunctionaliteit aan.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---


# Auteur met kerncomponenten

In Adobe Experience Manager zijn componenten de structuurelementen die de inhoud vormen van de pagina&#39;s die worden gemaakt.

De componenten van de Kern bieden flexibele en eigenschap-rijke auteursfunctionaliteit aan. De [WKND-referentiesite](https://wknd.site) en de bijbehorende illustratie laten zien hoe de kerncomponenten kunnen worden gebruikt om een rijke ervaring op websites te implementeren.

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library) om de Core Components te ervaren en voorbeelden van hun configuratieopties en HTML- en JSON-uitvoer te bekijken.

Voor een meer diepgaande, ontwikkelaar-georiënteerde inleiding aan het uitvoeren van de Componenten van de Kern op een AEM project door [AEM Project Archetype](/help/developing/archetype/overview.md) controle [uit de WKND zelfstudie te gebruiken.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

>[!NOTE]
>
>De Componenten van de kern zijn niet onmiddellijk beschikbaar aan auteurs, [ontwikkelingsteam moet hen eerst aan uw milieu integreren](/help/get-started/using.md). Zodra geïntegreerd, kunnen zij via [malplaatjeredacteur](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) ter beschikking worden gesteld en worden gevormd.

>[!CAUTION]
>
>Core Components [vereisen AEM 6.4 of hoger](/help/versions.md) en vereisen het gebruik van [bewerkbare sjablonen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html). Zij werken niet met Klassieke UI noch met statische malplaatjes.

## Ontwerpen met kerncomponenten {#authoring-with-core-components}

Als auteur zult u verscheidene voordelen van de Componenten van de Kern opmerken, die omvatten:

* Eenvoudig te gebruiken en goed geïntegreerd met [paginaredacteur](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html)

* Functiemogelijkheden die veel ruimte bieden voor veel gebruiksgevallen, zoals wordt geïllustreerd door de [WKND-referentiesite](https://wknd.site) en in de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library)

* [Pre-configureerbaar ](#pre-configuring-core-components) om te bepalen welke eigenschappen aan paginaauteurs via de  [malplaatjeredacteur beschikbaar zijn](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

* Gebaseerd op [toegankelijkheidsrichtlijnen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

* Gemaakt voor ondersteuning van [responsieve lay-out](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)

* Gemaakt ter ondersteuning van [eenvoudige lokalisatie](localization.md)

Componenten zijn beschikbaar op het tabblad **Componenten** van het zijpaneel van de pagina-editor wanneer [een pagina](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) bewerkt.

Componenten worden gegroepeerd volgens categorieën die componentgroepen worden genoemd, zodat u de componenten eenvoudig kunt ordenen en filteren. De naam van de componentengroep wordt getoond met de component in [componentenbrowser](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) en het is ook mogelijk om per groep te filtreren om de juiste component gemakkelijk te vinden.

>[!NOTE]
>
>De componenten van de Kern zijn door gebrek een verborgen groep en zijn niet zichtbaar binnen componentenbrowser.
>
>Voeg de vereiste componenten toe aan een zichtbare groep of pas deze aan zodat ze beschikbaar zijn voor auteurs.

## Vooraf configureren van kerncomponenten {#pre-configuring-core-components}

Het vormen de Componenten van de Stichting was de baan van een ontwikkelaar. Nochtans met de Componenten van de Kern, kan een malplaatjeauteur een aantal mogelijkheden via de malplaatjeredacteur nu vormen.

Als het uploaden van afbeeldingen vanuit het bestandssysteem bijvoorbeeld niet is toegestaan door een afbeeldingscomponent, of als een tekstcomponent alleen bepaalde alineaopmaak moet toestaan, kunnen deze functies met een eenvoudige klik in- of uitgeschakeld worden.

Zie [Paginasjablonen maken](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) voor meer informatie.

### Dialoogvensters {#edit-and-design-dialogs} bewerken en ontwerpen

Omdat de Componenten van de Kern door malplaatjeauteurs kunnen worden pre-gevormd om te bepalen welke opties als deel van een malplaatje worden toegestaan, en dan verder door de paginaauteur worden gevormd om daadwerkelijke paginainhoud te bepalen, kan elke component opties in twee verschillende dialogen hebben.

|  | Beschrijving | Wat het controleert | Voorbeelden |
|--- |--- |--- |--- |
| **Dialoogvenster Bewerken** | Opties die een **pagina auteur** tijdens normale paginabewerking voor de geplaatste componenten kan wijzigen | De inhoud die door de component wordt weergegeven en hoe deze uiteindelijk op de pagina wordt weergegeven. | Opmaak van inhoudstekst, een afbeelding op een pagina roteren |
| **Ontwerpdialoogvenster** | Opties die een **malplaatjeauteur** kan wijzigen wanneer het vormen van een paginamalplaatje. | Welke opties de auteur van de pagina bij het uitgeven van de component beschikbaar heeft | Welke opties voor tekstopmaak beschikbaar zijn, welke opties voor plaatsindeling van afbeeldingen beschikbaar zijn |

### Componentstijlen {#component-styling}

De stijlen van de meeste Core Components kunnen worden bepaald gebruikend het de stijlsysteem van de AEM.

* Een sjabloonauteur kan bepalen welke stijlen beschikbaar zijn voor een bepaalde component in het dialoogvenster Ontwerpen van die component.
* De auteur van de inhoud kan vervolgens kiezen welke stijlen u wilt toepassen bij het toevoegen van de component en het maken van inhoud.

Zie de documentatie [Stijlsysteem](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html) voor meer informatie.

## Bronnen voor ontwikkelaars {#developer-resources}

Zie de [Developing Core Components](/help/developing/overview.md) documentatie voor ontwikkelaars voor technische informatie betreffende kerncomponenten.
