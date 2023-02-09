---
title: Adaptieve Forms Core-component - Afbeelding
description: De Adaptive Forms Image Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
source-git-commit: 1e6460d318f4f9a5dfdcbb81723da01b51b72f3f
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 0%

---


# Afbeelding {#image-adaptive-forms-core-component}

Een afbeeldingscomponent in een adaptief formulier is een manier om afbeeldingen op te nemen in een formulier. Deze afbeeldingen kunnen worden gebruikt om het algehele ontwerp van het formulier te verbeteren, aanvullende informatie te verstrekken of als visuele hulp om gebruikers te helpen het doel van het formulier te begrijpen. Met de afbeeldingscomponent kunt u een logo, foto of afbeelding aan het formulier toevoegen.

Voor toegankelijkheid is het belangrijk om **Alternatieve tekst** in de afbeelding om een kort beschrijvend tekstalternatief voor de afbeelding te bieden, waarin de afbeelding wordt beschreven voor gebruikers die deze niet kunnen zien.


**Voorbeeld**

![](/help/adaptive-forms/assets/image.png)


## Gebruik {#reasons-to-use-image-in-a-form}

Er zijn verschillende redenen waarom het nuttig is om een component Image op te nemen in een adaptief formulier, zoals:

* **Branding**: Een afbeelding kan worden gebruikt om het logo of de naam weer te geven van de organisatie die het formulier heeft gemaakt, zodat merkherkenning en geloofwaardigheid worden gewaarborgd.

* **Visuele hulpmiddelen**: Een afbeelding kan gebruikers extra informatie bieden door te fungeren als visueel hulpmiddel om gebruikers te helpen het doel van het formulier te begrijpen.

* **Decoratie**: Een afbeelding kan worden gebruikt om het algehele ontwerp van het formulier te verbeteren en het visueel aantrekkelijker te maken.

* **Gebruikerservaring**: Een afbeelding kan worden gebruikt om het formulier gebruiksvriendelijker te maken door gebruikers een duidelijke en intuïtieve manier te bieden om formuliervelden te openen en in te vullen.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Image Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/versions.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Core Components-versies](/help/versions.md) document.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Ga voor de nieuwste informatie over de Adaptive Forms Image Core Component naar de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). Raadpleeg de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).


## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u uw beeldervaring eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig afbeeldingsopties definiëren voor een naadloze gebruikerservaring.

![Eigenschappen, tabblad](/help/adaptive-forms/assets/image_properties.png)

* **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

* **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

* **Document met bindingsverwijzing record** - Met deze optie kunt u een veld Adaptief formulier koppelen aan het veld Document of Record. Wanneer een gebruiker een waarde invoert in een gekoppeld veld van een adaptief formulier, wordt die waarde ook weergegeven in het gekoppelde veld van het corresponderende document met records. Zo kunt u bijvoorbeeld een bindingsverwijzing naar Document of Record gebruiken om de naam en het adres van een klant weer te geven in een Document of Record, op basis van de id die de klant in het formulier heeft ingevoerd. Op deze manier kunt u met AEM Forms Document of Record genereren en beschikt u over een naadloze gebruikerservaring voor het verzamelen en beheren van gegevens.

* **Beschrijving** - Een beschrijving is een korte tekstuitleg die aanvullende informatie of verduidelijking verschaft over het doel van een specifieke afbeelding.

* **Hier een element neerzetten of naar een bestand bladeren om te uploaden** - Met deze optie kunt u elementen zoals afbeeldingen, neerzetten door met de muis te slepen. U kunt een bestand ook uploaden vanaf een lokaal bestandssysteem met de opdracht **Bladeren** knop. Nadat u een afbeelding hebt toegevoegd, staan er drie knoppen onder aan de afbeelding:
   * **Bewerken** - Tik of klik **Bewerken** om de vertoningen van het element in de Redacteur van Activa te beheren.
   * **Wissen** - Tik of klik **Wissen** om de selectie van de geselecteerde afbeelding op te heffen.
   * **Selecteren** - Tik of klik **Selecteren**  om een andere afbeelding in de map Middelen te selecteren.

* **Alternatieve tekst** - Deze optie wordt gebruikt om de tekst in te voeren die een kort en beschrijvend tekstalternatief biedt voor de afbeelding, waarin de afbeelding wordt beschreven voor visueel gehandicapte gebruikers.

* **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

* **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Image te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Image Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

**Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Image Core Component.

**Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight&quot; opgeven: vet&quot;. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.