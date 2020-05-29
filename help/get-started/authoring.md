---
title: Ontwerpen met kerncomponenten
description: In AEM, zijn de componenten de structurele elementen die de inhoud van de pagina's vormen die - de Componenten van de Kern bieden flexibele en eigenschap-rijke auteursfunctionaliteit aan.
translation-type: tm+mt
source-git-commit: 4281f6421482682f603f6a7f5e18df61f9a6d98c
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---


# Auteur met kerncomponenten

In Adobe Experience Manager zijn componenten de structuurelementen die de inhoud vormen van de pagina&#39;s die worden gemaakt.

De componenten van de Kern bieden flexibele en eigenschap-rijke auteursfunctionaliteit aan. De [WKND-referentiesite](https://wknd.site) en de bijbehorende illustratie laten zien hoe de kerncomponenten kunnen worden gebruikt om een rijke ervaring op websites te implementeren.

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library)voor meer informatie over de Core Components en voorbeelden van hun configuratieopties en de HTML- en JSON-uitvoer.

Voor een meer diepgaande, op ontwikkelaars-georiënteerde inleiding aan het uitvoeren van de Componenten van de Kern op een AEM- project door de Archetype [van het Project van](/help/developing/archetype/overview.md) AEM controle uit [het WKND leerprogramma te gebruiken.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

>[!NOTE]
>
>De Componenten van de kern zijn niet onmiddellijk beschikbaar aan auteurs, moet het [ontwikkelingsteam hen aan uw milieu](/help/get-started/using.md)eerst integreren. Zodra geïntegreerd, kunnen zij beschikbaar worden gemaakt en via de [malplaatjeredacteur](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)worden gevormd.

>[!CAUTION]
>
>Core Components [vereist AEM 6.3 of hoger](/help/versions.md) en [bewerkbare sjablonen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html). Zij werken niet met Klassieke UI noch met statische malplaatjes.

## Ontwerpen met kerncomponenten {#authoring-with-core-components}

Als auteur zult u verscheidene voordelen van de Componenten van de Kern opmerken, die omvatten:

* Eenvoudig te gebruiken en goed geïntegreerd met de [paginaeditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html)

* Veelzijdige mogelijkheden voor veel gebruik, zoals wordt geïllustreerd door de [WKND-referentiesite](https://wknd.site) en in de [componentbibliotheek](https://adobe.com/go/aem_cmp_library)

* [Pre-configureerbaar](#pre-configuring-core-components) om te bepalen welke eigenschappen aan paginaaauteurs via de [malplaatjeredacteur beschikbaar zijn](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

* Gebaseerd op [toegankelijkheidsrichtlijnen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

* Gebouwd voor ondersteuning van [responsieve lay-out](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)

* Gebouwd voor ondersteuning van [eenvoudige lokalisatie](localization.md)

Componenten zijn beschikbaar op het tabblad **Componenten** van het zijpaneel van de pagina-editor wanneer u een pagina [](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html)bewerkt.

Componenten worden gegroepeerd volgens categorieën die componentgroepen worden genoemd, zodat u de componenten eenvoudig kunt ordenen en filteren. De naam van de componentengroep wordt getoond met de component in [componentenbrowser](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) en het is ook mogelijk om per groep te filtreren om de juiste component gemakkelijk te vinden.

>[!NOTE]
>
>De componenten van de Kern zijn door gebrek een verborgen groep en zijn niet zichtbaar binnen componentenbrowser.
>
>Voeg de vereiste componenten toe aan een zichtbare groep of pas deze aan zodat ze beschikbaar zijn voor auteurs.

## Basiscomponenten vooraf configureren {#pre-configuring-core-components}

Het vormen de Componenten van de Stichting was de baan van een ontwikkelaar. Nochtans met de Componenten van de Kern, kan een malplaatjeauteur een aantal mogelijkheden via de malplaatjeredacteur nu vormen.

Als het uploaden van afbeeldingen vanuit het bestandssysteem bijvoorbeeld niet is toegestaan door een afbeeldingscomponent, of als een tekstcomponent alleen bepaalde alineaopmaak moet toestaan, kunnen deze functies met een eenvoudige klik in- of uitgeschakeld worden.

Zie [Paginasjablonen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) maken voor meer informatie.

### Dialoogvensters Bewerken en Ontwerpen {#edit-and-design-dialogs}

Omdat de Componenten van de Kern door malplaatjeauteurs kunnen worden pre-gevormd om te bepalen welke opties als deel van een malplaatje worden toegestaan, en dan verder door de paginaauteur worden gevormd om daadwerkelijke paginainhoud te bepalen, kan elke component opties in twee verschillende dialogen hebben.

|  | Beschrijving | Wat het controleert | Voorbeelden |
|--- |--- |--- |--- |
| **Dialoogvenster Bewerken** | Opties die de auteur **van een** pagina tijdens normale paginabewerking kan wijzigen voor de geplaatste componenten | De inhoud die door de component wordt weergegeven en hoe deze uiteindelijk op de pagina wordt weergegeven. | Opmaak van inhoudstekst, een afbeelding op een pagina roteren |
| **Ontwerpdialoogvenster** | Opties die een **sjabloonauteur** kan wijzigen bij het configureren van een paginasjabloon. | Welke opties de auteur van de pagina bij het uitgeven van de component beschikbaar heeft | Welke opties voor tekstopmaak beschikbaar zijn, welke opties voor plaatsindeling van afbeeldingen beschikbaar zijn |

### Componentstijlen {#component-styling}

De stijlen van de meeste Core Components kunnen worden gedefinieerd met behulp van het AEM-stijlsysteem.

* Een sjabloonauteur kan bepalen welke stijlen beschikbaar zijn voor een bepaalde component in het dialoogvenster Ontwerpen van die component.
* De auteur van de inhoud kan vervolgens kiezen welke stijlen u wilt toepassen bij het toevoegen van de component en het maken van inhoud.

Zie de documentatie van het [Stijlsysteem](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html) voor meer informatie.

>[!NOTE]
>
>In AEM 6.3, wordt de dienstpak 2 (6.3.2.0) of nieuwer vereist om de eigenschap van het stijlsysteem toe te laten.

## Bronnen voor ontwikkelaars {#developer-resources}

Raadpleeg de documentatie voor ontwikkelaars van [Core Components](/help/developing/overview.md) voor technische informatie over kerncomponenten.
