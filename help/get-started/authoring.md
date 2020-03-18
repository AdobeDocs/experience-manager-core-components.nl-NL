---
title: Ontwerpen met kerncomponenten
description: In AEM, zijn de componenten de structurele elementen die de inhoud van de pagina's vormen die - de Componenten van de Kern bieden flexibele en eigenschap-rijke auteursfunctionaliteit aan.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

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

## Lijst met beschikbare kerncomponenten {#list-of-core-components-available}

Hieronder volgt een lijst met de beschikbare kerncomponenten die zijn gekoppeld aan pagina&#39;s en die hun mogelijkheden in het dialoogvenster Bewerken en Ontwerpen gedetailleerd beschrijven.

In de huidige versie van Core Components zijn de volgende componenten beschikbaar.

* [Accordeon](/help/components/accordion.md)
* [Broodkruimel](/help/components/breadcrumb.md)
* [Knop](/help/components/button.md)
* [Container](/help/components/container.md)
* [Carousel](/help/components/carousel.md)
* [Inhoudsfragment](/help/components/content-fragment-component.md)
* [Lijst met inhoudsfragmenten](/help/components/content-fragment-list.md)
* [Downloaden](/help/components/download.md)
* [Insluiten](/help/components/embed.md)
* [Ervaar fragment](/help/components/experience-fragment.md)
* [Formulierknop](/help/components/forms/form-button.md)
* [Formuliercontainer](/help/components/forms/form-container.md)
* [Formulier verborgen](/help/components/forms/form-hidden.md)
* [Formulieropties](/help/components/forms/form-options.md)
* [Formuliertekst](/help/components/forms/form-text.md)
* [Afbeelding](/help/components/image.md)
* [Taalnavigatie](/help/components/language-navigation.md)
* [Lijst](/help/components/list.md)
* [Navigatie](/help/components/navigation.md)
* [Pagina](/help/components/page.md)
* [Snel zoeken](/help/components/quick-search.md)
* [Scheidingsteken](/help/components/separator.md)
* [Delen van sociale media](/help/components/sharing.md)
* [Tabs](/help/components/tabs.md)
* [Tekst](/help/components/text.md)
* [Titel](/help/components/title.md)

>[!CAUTION]
>
>Sommige versies van afzonderlijke Core Components zijn mogelijk alleen compatibel met bepaalde versies van AEM.
>
>Zie de afzonderlijke Help-pagina (die is gekoppeld aan de vorige lijst) voor de specifieke component voor compatibiliteitsinformatie of raadpleeg het document [Core Components Versions](/help/versions.md) voor meer informatie.

>[!NOTE]
>
>Afhankelijk van uw instantie kunt u aangepaste componenten hebben die uitdrukkelijk voor uw vereisten worden ontwikkeld. Deze kunnen zelfs de zelfde naam hebben zoals sommige componenten hier besproken.
>De kerncomponenten van het formulier zijn niet gerelateerd aan AEM Forms.

## Bronnen voor ontwikkelaars {#developer-resources}

Raadpleeg de documentatie voor ontwikkelaars van [Core Components](/help/developing/overview.md) voor technische informatie over kerncomponenten.
