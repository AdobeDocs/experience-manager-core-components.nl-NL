---
title: Adaptieve Forms Core-component - Afbeelding
description: De Adaptive Forms Image Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: 9ee42d5d-16e3-4973-8364-5bc512ebe72e
source-git-commit: ad3e3bca5cb46f14e864e4704c90ac3b62779794
workflow-type: tm+mt
source-wordcount: '1051'
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

* **Visuele hulpmiddelen**: Een afbeelding kan gebruikers extra informatie bieden door te fungeren als een visuele hulp die gebruikers helpt het doel van het formulier te begrijpen.

* **Decoratie**: Met een afbeelding kunt u het algehele ontwerp van het formulier verbeteren en het visueel aantrekkelijker maken.

* **Gebruikerservaring**: Een afbeelding kan worden gebruikt om het formulier gebruiksvriendelijker te maken door gebruikers een duidelijke en intuïtieve manier te bieden om formuliervelden te openen en in te vullen.

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

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Image Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Ontwerpdialoogvenster](/help/adaptive-forms/assets/image_designdialog.png)

**Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Image Core Component.

**Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

## Verwante artikelen {#related-article}

* [Een adaptief formulier maken in AEM Sites Page of Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

* [Een zelfstandig adaptief formulier maken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)


## Zie ook {#see-also}

* [Accordeon](/help/adaptive-forms/components/accordion.md)
* [Knop](/help/adaptive-forms/components/button.md)
* [Selectievakjesgroep](/help/adaptive-forms/components/checkbox-group.md)
* [Datumkiezer](/help/adaptive-forms/components/date-picker.md)
* [Vervolgkeuzelijst](/help/adaptive-forms/components/drop-down.md)
* [E-mailinvoer](/help/adaptive-forms/components/email-input.md)
* [Formuliercontainer](/help/adaptive-forms/components/form-container.md)
* [Bestandsbijlage](/help/adaptive-forms/components/file-attachment.md)
* [Voettekst](/help/adaptive-forms/components/footer.md)
* [Koptekst](/help/adaptive-forms/components/header.md)
* [Horizontale tabs](/help/adaptive-forms/components/horizontal-tabs.md)
* [Nummerinvoer](/help/adaptive-forms/components/number-input.md)
* [Deelvenstercontainer](/help/adaptive-forms/components/panel-container.md)
* [Keuzerondje](/help/adaptive-forms/components/radio-button.md)
* [Knop Opnieuw instellen](/help/adaptive-forms/components/reset-button.md)
* [Verzendknop](/help/adaptive-forms/components/submit-button.md)
* [Telefooninvoer](/help/adaptive-forms/components/telephone-input.md)
* [Tekstinvoer](/help/adaptive-forms/components/text-input.md)
* [Tekst](/help/adaptive-forms/components/text.md)
* [Titel](/help/adaptive-forms/components/title.md)
* [Wizard](/help/adaptive-forms/components/wizard.md)