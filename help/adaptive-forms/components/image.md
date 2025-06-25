---
title: Adaptieve Forms Core-component - Afbeelding
description: De Adaptive Forms Image Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: 9ee42d5d-16e3-4973-8364-5bc512ebe72e
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 0%

---


# Afbeeldingscomponent{#image-adaptive-forms-core-component}

Een afbeeldingscomponent in een adaptief formulier is een manier om afbeeldingen op te nemen in een formulier. Deze afbeeldingen kunnen worden gebruikt om het algehele ontwerp van het formulier te verbeteren, aanvullende informatie te verstrekken of als visuele hulp om gebruikers te helpen het doel van het formulier te begrijpen. Met de afbeeldingscomponent kunt u een logo, foto of afbeelding aan het formulier toevoegen.

Voor toegankelijkheid, is het belangrijk om **Afwisselende tekst** aan het beeld te specificeren om een kort, beschrijvend tekstalternatief voor het beeld te verstrekken, dat het beeld aan gebruikers beschrijft die het niet kunnen zien.

{{traditional-aem}}

**Voorbeeld**

![ voorbeeld ](/help/adaptive-forms/assets/image.png)


## Gebruik {#reasons-to-use-image-in-a-form}

Er zijn verschillende redenen waarom het nuttig is om een component Image op te nemen in een adaptief formulier, zoals:

- **Branding**: Een beeld kan worden gebruikt om het embleem of de naam van de organisatie te tonen die de vorm creeerde, die merkerkenning en geloofwaardigheid helpen vestigen.

- **Visuele Hulpmiddelen**: Een beeld kan helpen om een extra niveau van informatie aan gebruikers te verstrekken, door als visuele hulp te dienen om gebruikers te helpen het doel van de vorm begrijpen.

- **Decoratie**: Een beeld kan worden gebruikt om het algemene ontwerp van de vorm te verbeteren en het visueel aantrekkelijker te maken.

- **Ervaring van de Gebruiker**: Een beeld kan worden gebruikt om de vorm gebruikersvriendelijker te maken door een duidelijke en intuïtieve manier voor gebruikers te verstrekken om tot vormgebieden toegang te hebben en in te vullen.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Image Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 voor Cloud Service en Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM-compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/adaptive-forms/version.md) en later | Compatibel met <br>[ versie 1.1.12 ](/help/adaptive-forms/version.md) en later maar minder dan 2.0.0. |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het ](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0}.[


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Krijg de recentste informatie over de AanpassingsComponent van de Kern van het Beeld van Forms in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).


## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u uw beeldervaring eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig afbeeldingsopties definiëren voor een naadloze gebruikerservaring.

![ Eigenschappen tabel ](/help/adaptive-forms/assets/image_properties.png)

- **Naam** - u kunt een vormcomponent gemakkelijk met zijn unieke naam zowel in de vorm als in de regelredacteur identificeren, maar de naam moet geen ruimten of speciale karakters bevatten.

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bovenop de component. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

- **Teken als Niet-gebonden Element van de Vorm**: Selecteer de optie om een vormgebied te vormen niet verbonden aan om het even welk schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.

<!--   **Document of Record bind reference** - This option allows you to associate an Adaptive Form field with Document of Record field. When user enters any value in a linked field of an Adaptive Form that value also appears in the linked field of the corresponding Document of Record. For example, a Document of Record bind reference can be used to display a customer's name and address in a Document of Record, based on the customer's ID entered into the form. In this way, AEM Forms enable you to generate Document of Record and offers a seamless user experience for collecting and managing data.-->

- **Beschrijving** - een beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek beeld verstrekt.

- **Daling hier een activa of doorblader voor een dossier om te uploaden** - Deze optie staat toe om activa zoals beeld met muisbelemmering en daling te laten vallen. U kunt een dossier van een lokaal dossiersysteem ook uploaden gebruikend **doorbladert** knoop. Nadat u een afbeelding hebt toegevoegd, staan er drie knoppen onder aan de afbeelding:
   - **geef** uit - Tik of klik **geef** uit om de vertoningen van de activa in de Redacteur van Assets te beheren.
   - **Duidelijk** - Tik of klik **Duidelijk** om het momenteel geselecteerde beeld te deselecteren.
   - **Keuze** - Tik of klik **Keuze** optie om een ander beeld van de omslag van Assets te selecteren.

- **Afwisselende tekst** - Deze optie wordt gebruikt om de tekst in te gaan die een kort en beschrijvend tekstalternatief voor het beeld verstrekt, dat het beeld aan visueel gehandicapte gebruikers beschrijft.

- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

<!--   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
-->

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Image te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De adaptieve Component van de Kern van het Beeld van Forms steunt het systeem van de Stijl van AEM [ ](/help/get-started/authoring.md#component-styling).

![ Dialoog van het Ontwerp ](/help/adaptive-forms/assets/checkbox-style.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de Aangepaste Component van de Kern van het Beeld van Forms verstrekken.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![ de Dialoog van Eigenschappen van de Douane ](/help/adaptive-forms/assets/checkbox-customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de orde van de naam van het douanebezit en de waarde van het douanebezit te herschikken.

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}