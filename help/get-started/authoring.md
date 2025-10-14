---
title: Ontwerpen met kerncomponenten
description: In AEM, zijn de componenten de structurele elementen die de inhoud van de pagina's vormen die worden ontworpen - de Componenten van de Kern bieden flexibele en eigenschap-rijke auteursfunctionaliteit aan.
role: Architect, Developer, Admin, User
exl-id: 56e58303-a178-45ab-b59d-e374c9cf90cf
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# Auteur met kerncomponenten

In Adobe Experience Manager zijn componenten de structuurelementen die de inhoud vormen van de pagina&#39;s die worden gemaakt.

De componenten van de Kern bieden flexibele en eigenschap-rijke auteursfunctionaliteit aan. De [&#x200B; WKND verwijzingsplaats &#x200B;](https://wknd.site) en zijn illustraties hoe de kerncomponenten kunnen worden gebruikt om een rijke websiteervaring uit te voeren.

Om de Componenten van de Kern te ervaren en voorbeelden van hun configuratieopties evenals HTML en output te zien JSON, bezoek de [&#x200B; Bibliotheek van de Component &#x200B;](https://adobe.com/go/aem_cmp_library).

Voor een meer diepgaande, op ontwikkelaar-georiënteerde inleiding aan het uitvoeren van de Componenten van de Kern op een AEM project door [&#x200B; AEM Archetype van het Project &#x200B;](/help/developing/archetype/overview.md) controle [&#x200B; uit te gebruiken WKND leerprogramma.](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=nl-NL)

>[!NOTE]
>
>De Componenten van de kern zijn niet onmiddellijk beschikbaar aan auteurs, moet het [&#x200B; ontwikkelingsteam hen aan uw milieu &#x200B;](/help/get-started/using.md) eerst integreren. Zodra geïntegreerd, kunnen zij beschikbaar worden gemaakt en pre-gevormd via de [&#x200B; malplaatjedacteur &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=nl-NL).

>[!CAUTION]
>
>De Componenten van de kern [&#x200B; vereisen AEM 6.4 of hoger &#x200B;](/help/versions.md) en vereisen het gebruik van [&#x200B; editable malplaatjes &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=nl-NL). Zij werken niet met Klassieke UI noch met statische malplaatjes.

## Ontwerpen met kerncomponenten {#authoring-with-core-components}

Als auteur zult u verscheidene voordelen van de Componenten van de Kern opmerken, die omvatten:

* Eenvoudig te gebruiken en goed-geïntegreerd met de [&#x200B; paginaredacteur &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=nl-NL)

* Eigenschap-rijke mogelijkheden om vele gebruiksgevallen aan te passen zoals die door de [&#x200B; WKND verwijzingsplaats &#x200B;](https://wknd.site) evenals in de [&#x200B; Bibliotheek van de Component &#x200B;](https://adobe.com/go/aem_cmp_library) worden geïllustreerd

* [&#x200B; pre-configureerbaar &#x200B;](#pre-configuring-core-components) om te bepalen welke eigenschappen aan paginaauteurs via de [&#x200B; malplaatjeredacteur &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=nl-NL) beschikbaar zijn

* Gebouwd rond [&#x200B; toegankelijkheidsrichtlijnen &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=nl-NL)

* Gebouwd om [&#x200B; ontvankelijke lay-out &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html?lang=nl-NL) te steunen

* Gebouwd om [&#x200B; gemakkelijke localisatie te steunen &#x200B;](localization.md)

De componenten zijn beschikbaar op het **lusje van Componenten** van het zijpaneel van de paginaredacteur wanneer [&#x200B; het uitgeven van een pagina &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=nl-NL).

Componenten worden gegroepeerd volgens categorieën die componentgroepen worden genoemd, zodat u de componenten eenvoudig kunt ordenen en filteren. De naam van de componentengroep wordt getoond met de component in [&#x200B; componentenbrowser &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=nl-NL) en het is ook mogelijk om door groep te filtreren om de juiste component gemakkelijk te vinden.

>[!NOTE]
>
>De componenten van de Kern zijn door gebrek een verborgen groep en zijn niet zichtbaar binnen componentenbrowser.
>
>Voeg de vereiste componenten toe aan een zichtbare groep of pas deze aan zodat ze beschikbaar zijn voor auteurs.

## Kerncomponenten vooraf configureren {#pre-configuring-core-components}

Het vormen de Componenten van de Stichting was de baan van een ontwikkelaar. Nochtans met de Componenten van de Kern, kan een malplaatjeauteur een aantal mogelijkheden via de malplaatjeredacteur nu vormen.

Als het uploaden van afbeeldingen vanuit het bestandssysteem bijvoorbeeld niet is toegestaan door een afbeeldingscomponent, of als een tekstcomponent alleen bepaalde alineaopmaak moet toestaan, kunnen deze functies met een eenvoudige klik in- of uitgeschakeld worden.

Zie [&#x200B; Creërend de Malplaatjes van de Pagina &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=nl-NL) voor meer informatie.

### Dialoogvensters Bewerken en Ontwerpen {#edit-and-design-dialogs}

Omdat de Componenten van de Kern door malplaatjeauteurs kunnen worden pre-gevormd om te bepalen welke opties als deel van een malplaatje worden toegestaan, en dan verder door de paginaauteur worden gevormd om daadwerkelijke paginainhoud te bepalen, kan elke component opties in twee verschillende dialogen hebben.

|  | Beschrijving | Wat het controleert | Voorbeelden |
|--- |--- |--- |--- |
| **geef Dialoog** uit | Opties dat de auteur van de a **pagina** tijdens normale pagina die voor de geplaatste componenten uitgeeft kan wijzigen | De inhoud die door de component wordt weergegeven en hoe deze uiteindelijk op de pagina wordt weergegeven. | Opmaak van inhoudstekst, een afbeelding op een pagina roteren |
| **Dialoog van het Ontwerp** | Opties die de auteur van het a **malplaatje** kan wijzigen wanneer het vormen van een paginamalplaatje. | Welke opties de auteur van de pagina bij het uitgeven van de component beschikbaar heeft | Welke opties voor tekstopmaak beschikbaar zijn, welke opties voor plaatsindeling van afbeeldingen beschikbaar zijn |

### Componentstijlen {#component-styling}

De stijlen van de meeste Core Components kunnen worden bepaald gebruikend het de stijlsysteem van de AEM.

* Een sjabloonauteur kan bepalen welke stijlen beschikbaar zijn voor een bepaalde component in het dialoogvenster Ontwerpen van die component.
* De auteur van de inhoud kan vervolgens kiezen welke stijlen u wilt toepassen bij het toevoegen van de component en het maken van inhoud.

Voor verdere details zie de [&#128279;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/style-system.html?lang=nl-NL) documentatie van het Systeem van de Stijl 0&rbrace;.

## Bronnen voor ontwikkelaars {#developer-resources}

Zie [&#x200B; het Ontwikkelen van de ontwikkelaarsdocumentatie van de Componenten van de Kern &#x200B;](/help/developing/overview.md) voor technische informatie betreffende kerncomponenten.
