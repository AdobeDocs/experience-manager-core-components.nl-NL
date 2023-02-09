---
title: Ontwerpen met kerncomponenten
description: In AEM, zijn de componenten de structurele elementen die de inhoud van de pagina's vormen die worden ontworpen - de Componenten van de Kern bieden flexibele en eigenschap-rijke auteursfunctionaliteit aan.
role: Architect, Developer, Admin, User
exl-id: 56e58303-a178-45ab-b59d-e374c9cf90cf
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# Auteur met kerncomponenten

In Adobe Experience Manager zijn componenten de structuurelementen die de inhoud vormen van de pagina&#39;s die worden gemaakt.

De componenten van de Kern bieden flexibele en eigenschap-rijke auteursfunctionaliteit aan. De [WKND-referentiesite](https://wknd.site) en het illustreert hoe de kerncomponenten kunnen worden gebruikt om een rijke websiteervaring uit te voeren.

Als u de Core Components (Basiscomponenten) wilt ervaren en voorbeelden wilt zien van hun configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library).

Voor een meer diepgaande, ontwikkelaar-georiënteerde inleiding aan het uitvoeren van de Componenten van de Kern op een AEM project door te gebruiken [Projectarchetype AEM](/help/developing/archetype/overview.md) uitchecken [de WKND-zelfstudie.](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

>[!NOTE]
>
>De belangrijkste componenten zijn niet onmiddellijk beschikbaar aan auteurs, [ontwikkelingsteam moet deze eerst integreren in uw omgeving](/help/get-started/using.md). Zodra geïntegreerd, kunnen zij beschikbaar worden gemaakt en vooraf gevormd via [sjablooneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!CAUTION]
>
>Kernonderdelen [AEM 6.4 of hoger vereist](/help/versions.md) en het gebruik van [bewerkbare sjablonen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html). Zij werken niet met Klassieke UI noch met statische malplaatjes.

## Ontwerpen met kerncomponenten {#authoring-with-core-components}

Als auteur zult u verscheidene voordelen van de Componenten van de Kern opmerken, die omvatten:

* Eenvoudig in gebruik en goed geïntegreerd met de [paginaeditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html)

* De eigenschap-rijke mogelijkheden om vele gebruiksgevallen aan te passen zoals die door [WKND-referentiesite](https://wknd.site) en in de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library)

* [Pre-configureerbaar](#pre-configuring-core-components) om te bepalen welke functies beschikbaar zijn voor auteurs van pagina&#39;s via de [sjablooneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

* Ingebouwd rond [toegankelijkheidsrichtlijnen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

* Gebouwd voor ondersteuning [responsieve indeling](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)

* Gebouwd voor ondersteuning [eenvoudige lokalisatie](localization.md)

Componenten zijn beschikbaar op de **Componenten** tabblad van het zijpaneel van de pagina-editor wanneer [pagina&#39;s bewerken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html).

Componenten worden gegroepeerd volgens categorieën die componentgroepen worden genoemd, zodat u de componenten eenvoudig kunt ordenen en filteren. De naam van de componentgroep wordt met de component in het dialoogvenster [componentbrowser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) en het is ook mogelijk om per groep te filteren om de juiste component gemakkelijk te vinden.

>[!NOTE]
>
>De componenten van de Kern zijn door gebrek een verborgen groep en zijn niet zichtbaar binnen componentenbrowser.
>
>Voeg de vereiste componenten toe aan een zichtbare groep of pas deze aan zodat ze beschikbaar zijn voor auteurs.

## Basiscomponenten vooraf configureren {#pre-configuring-core-components}

Het vormen de Componenten van de Stichting was de baan van een ontwikkelaar. Nochtans met de Componenten van de Kern, kan een malplaatjeauteur een aantal mogelijkheden via de malplaatjeredacteur nu vormen.

Als het uploaden van afbeeldingen vanuit het bestandssysteem bijvoorbeeld niet is toegestaan door een afbeeldingscomponent, of als een tekstcomponent alleen bepaalde alineaopmaak moet toestaan, kunnen deze functies met een eenvoudige klik in- of uitgeschakeld worden.

Zie [Paginasjablonen maken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) voor meer informatie .

### Dialoogvensters Bewerken en Ontwerpen {#edit-and-design-dialogs}

Omdat de Componenten van de Kern door malplaatjeauteurs kunnen worden pre-gevormd om te bepalen welke opties als deel van een malplaatje worden toegestaan, en dan verder door de paginaauteur worden gevormd om daadwerkelijke paginainhoud te bepalen, kan elke component opties in twee verschillende dialogen hebben.

|  | Beschrijving | Wat het controleert | Voorbeelden |
|--- |--- |--- |--- |
| **Dialoogvenster Bewerken** | Opties die een **paginaauteur** kan worden gewijzigd tijdens normale paginabewerking voor de geplaatste componenten | De inhoud die door de component wordt weergegeven en hoe deze uiteindelijk op de pagina wordt weergegeven. | Opmaak van inhoudstekst, een afbeelding op een pagina roteren |
| **Ontwerpdialoogvenster** | Opties die een **sjabloonauteur** kan worden gewijzigd bij het configureren van een paginasjabloon. | Welke opties de auteur van de pagina bij het uitgeven van de component beschikbaar heeft | Welke opties voor tekstopmaak beschikbaar zijn, welke opties voor plaatsindeling van afbeeldingen beschikbaar zijn |

### Componentstijlen {#component-styling}

De stijlen van de meeste Core Components kunnen worden bepaald gebruikend het de stijlsysteem van de AEM.

* Een sjabloonauteur kan bepalen welke stijlen beschikbaar zijn voor een bepaalde component in het dialoogvenster Ontwerpen van die component.
* De auteur van de inhoud kan vervolgens kiezen welke stijlen u wilt toepassen bij het toevoegen van de component en het maken van inhoud.

Zie voor meer informatie de [Stijlsysteem](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/style-system.html) documentatie.

## Bronnen voor ontwikkelaars {#developer-resources}

Zie de [Basiscomponenten ontwikkelen](/help/developing/overview.md) ontwikkelaarsdocumentatie voor technische informatie betreffende kerncomponenten.
