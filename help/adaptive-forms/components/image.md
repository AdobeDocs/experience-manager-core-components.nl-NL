---
title: Adaptieve Forms Core-component - Afbeelding
description: De Adaptive Forms Image Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: 9ee42d5d-16e3-4973-8364-5bc512ebe72e
source-git-commit: c3401da271efd930d1a2711bcab25c29f763f38e
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 0%

---

# Afbeeldingscomponent{#image-adaptive-forms-core-component}

Een afbeeldingscomponent in een adaptief formulier is een manier om afbeeldingen op te nemen in een formulier. Deze afbeeldingen kunnen worden gebruikt om het algehele ontwerp van het formulier te verbeteren, aanvullende informatie te verstrekken of als visuele hulp om gebruikers te helpen het doel van het formulier te begrijpen. Met de afbeeldingscomponent kunt u een logo, foto of afbeelding aan het formulier toevoegen.

Voor toegankelijkheid is het belangrijk om **Alternatieve tekst** in de afbeelding om een kort beschrijvend tekstalternatief voor de afbeelding te bieden, waarin de afbeelding wordt beschreven voor gebruikers die deze niet kunnen zien.

**Voorbeeld**

![voorbeeld](/help/adaptive-forms/assets/image.png)


## Gebruik {#reasons-to-use-image-in-a-form}

Er zijn verschillende redenen waarom het nuttig is om een component Image op te nemen in een adaptief formulier, zoals:

- **Branding**: Een afbeelding kan worden gebruikt om het logo of de naam weer te geven van de organisatie die het formulier heeft gemaakt, zodat merkherkenning en geloofwaardigheid worden gewaarborgd.

- **Visuele hulpmiddelen**: Een afbeelding kan gebruikers extra informatie bieden door te fungeren als een visuele hulp die gebruikers helpt het doel van het formulier te begrijpen.

- **Decoratie**: Met een afbeelding kunt u het algehele ontwerp van het formulier verbeteren en het visueel aantrekkelijker maken.

- **Gebruikerservaring**: Een afbeelding kan worden gebruikt om het formulier gebruiksvriendelijker te maken door gebruikers een duidelijke en intuïtieve manier te bieden om formuliervelden te openen en in te vullen.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.12](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Ga voor de nieuwste informatie over de Adaptive Forms Image Core Component naar de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).


## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u uw beeldervaring eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig afbeeldingsopties definiëren voor een naadloze gebruikerservaring.

![Eigenschappen, tabblad](/help/adaptive-forms/assets/image_properties.png)

- **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

- **Markeren als niet-gebonden formulierelement**: Selecteer de optie om een formulierveld te configureren dat niet is gekoppeld aan een schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.

<!--   **Document of Record bind reference** - This option allows you to associate an Adaptive Form field with Document of Record field. When user enters any value in a linked field of an Adaptive Form that value also appears in the linked field of the corresponding Document of Record. For example, a Document of Record bind reference can be used to display a customer's name and address in a Document of Record, based on the customer's ID entered into the form. In this way, AEM Forms enable you to generate Document of Record and offers a seamless user experience for collecting and managing data.-->

- **Beschrijving** - Een beschrijving is een korte tekstuitleg die aanvullende informatie of verduidelijking verschaft over het doel van een specifieke afbeelding.

- **Hier een element neerzetten of naar een bestand bladeren om te uploaden** - Met deze optie kunt u elementen zoals afbeeldingen, neerzetten door met de muis te slepen. U kunt een bestand ook uploaden vanaf een lokaal bestandssysteem met de opdracht **Bladeren** knop. Nadat u een afbeelding hebt toegevoegd, staan er drie knoppen onder aan de afbeelding:
   - **Bewerken** - Tik of klik **Bewerken** om de vertoningen van het element in de Redacteur van Activa te beheren.
   - **Wissen** - Tik of klik **Wissen** om de selectie van de geselecteerde afbeelding op te heffen.
   - **Selecteren** - Tik of klik **Selecteren**  om een andere afbeelding in de map Middelen te selecteren.

- **Alternatieve tekst** - Deze optie wordt gebruikt om de tekst in te voeren die een kort en beschrijvend tekstalternatief biedt voor de afbeelding, waarin de afbeelding wordt beschreven voor visueel gehandicapte gebruikers.

- **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

<!--   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
-->

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Image te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Image Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Ontwerpdialoogvenster](/help/adaptive-forms/assets/checkbox-style.png)

- **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Image Core Component.

- **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![Dialoogvenster Aangepaste eigenschappen](/help/adaptive-forms/assets/checkbox-customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Groepsnaam**: U kunt een naam opgeven om de groep met aangepaste eigenschappen te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **Belangrijke paren**: U kunt meerdere aangepaste eigenschapnamen en aangepaste eigenschapswaarden toevoegen door op de knop **Toevoegen** knop voor elke aangepaste groep eigenschappen.

   - **Verwijderen**: Tik of klik om de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te verwijderen.

   - **Opnieuw rangschikken**: Tik of klik en sleep om de volgorde van de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te wijzigen.

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}