---
title: Adaptive Forms Core Component - Koptekst
description: De Adaptive Forms Header Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: aa18def9-0bec-4475-8dde-213860621ef5
source-git-commit: 59cd9d65bf4c1be6ab2eaf15bbb747b532863fdd
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 1%

---

# Koptekst {#header-adaptive-forms-core-component}

Een koptekstcomponent in een adaptief formulier is een sectie boven aan het formulier die doorgaans de titel, het logo of de naam van het formulier bevat. De koptekst kan ook andere informatie bevatten, zoals een korte beschrijving van het doel van het formulier, de naam van de organisatie die het formulier heeft gemaakt of contactgegevens voor hulp bij het formulier. De koptekst wordt gebruikt om gebruikers een overzicht van het formulier te geven en context te bieden voor de informatie die ze op het punt staan in te vullen. Deze wordt gebruikt om gebruikers te helpen het doel van het formulier te begrijpen en het formulier correct in te vullen.

**Voorbeeld**

![](/help/adaptive-forms/assets/header.png)

## Gebruik {#reasons-to-use-header}

* **Branding**: Een koptekst kan worden gebruikt om het logo of de naam weer te geven van de organisatie die het formulier heeft gemaakt, zodat merkherkenning en geloofwaardigheid worden gegarandeerd.

* **Context**: Een koptekst kan een korte beschrijving van het doel van het formulier bevatten, zodat gebruikers weten in welke context het formulier wordt gebruikt.

* **Navigatie**: Een koptekst kan koppelingen of knoppen bevatten waarmee gebruikers naar andere delen van de website of toepassing kunnen navigeren.

* **Informatie**: Een koptekst kan contactgegevens of koppelingen bevatten om bronnen te helpen, waardoor gebruikers gemakkelijker hulp kunnen krijgen als ze dat nodig hebben.

* **Gebruikerservaring**: Een koptekst kan worden gebruikt om het formulier gebruiksvriendelijker te maken door gebruikers een duidelijke en intuïtieve manier te bieden om formuliervelden te openen en in te vullen.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.12](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technische details {#technical-details}

Ga voor de nieuwste informatie over de Adaptive Forms Header Core Component naar de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageheader/v1/pageheader). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de headerervaring voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig koptekstopties definiëren voor een naadloze gebruikerservaring.

### Tabblad Afbeelding {#image-tab}

Dit gedeelte van de koptekst bevat de koptekst en de afbeelding.

![Afbeelding, tabblad](/help/adaptive-forms/assets/header_image.png)

* **Afbeeldingselement** - Met deze optie kunt u elementen zoals afbeeldingen, neerzetten door met de muis te slepen. U kunt een bestand ook uploaden vanaf een lokaal bestandssysteem met de opdracht **Bladeren** knop. Nadat u een afbeelding hebt toegevoegd, staan er drie knoppen onder aan de afbeelding. Nadat u een afbeelding hebt toegevoegd, staan er drie knoppen onder aan de afbeelding:
   * **Bewerken** - Tik of klik **Bewerken** om de vertoningen van het element in de Redacteur van Activa te beheren.
   * **Wissen** - Tik of klik **Wissen** om de selectie van de geselecteerde afbeelding op te heffen.
   * **Selecteren** - Tik of klik **Selecteren**  om een andere afbeelding in de map Middelen te selecteren.

* **Titel** - Deze optie wordt gebruikt om de kop aan de koptekst toe te voegen. De vooraf gedefinieerde tekst staat in het dialoogvenster en kan door de gebruiker worden gewijzigd.
* **Koppeling naar** - U kunt de kop koppelen aan de map met de **Bladeren** pictogram.
* **Beschrijving** - Een beschrijving is een korte tekstuitleg die aanvullende informatie of verduidelijking verschaft over het doel van een specifieke afbeelding.
* **Grootte (px)** - U kunt hiermee de lengte en breedte van de afbeelding aanpassen door de pixels te vergroten of te verkleinen.

![toegankelijkheidstab](/help/adaptive-forms/assets/header_accessibility.png)

* **Alternatieve tekst** - Deze optie wordt gebruikt om de tekst in te voeren die een kort en beschrijvend tekstalternatief biedt voor de afbeelding, waarin de afbeelding wordt beschreven voor visueel gehandicapte gebruikers.

* **Afbeelding is decoratief** - Controleer of het beeld door ondersteunende hulpmiddelen moet worden genegeerd en of er daarom geen alternatieve tekst nodig is. Dit geldt alleen voor decoratieve afbeeldingen.

### Tabblad Tekst {#text-tab}

In deze sectie kunt u de tekst invoeren die in de koptekst moet worden opgenomen.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->


>[!MORELIKETHIS]
>
>* [Accordeon](/help/adaptive-forms/components/accordion.md)
>* [Knop](/help/adaptive-forms/components/button.md)
>* [Selectievakjesgroep](/help/adaptive-forms/components/checkbox-group.md)
>* [Datumkiezer](/help/adaptive-forms/components/date-picker.md)
>* [Vervolgkeuzelijst](/help/adaptive-forms/components/drop-down.md)
>* [E-mailinvoer](/help/adaptive-forms/components/email-input.md)
>* [Formuliercontainer](/help/adaptive-forms/components/form-container.md)
>* [Bestandsbijlage](/help/adaptive-forms/components/file-attachment.md)
>* [Voettekst](/help/adaptive-forms/components/footer.md)
>* [Horizontale tabs](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Afbeelding](/help/adaptive-forms/components/image.md)
>* [Nummerinvoer](/help/adaptive-forms/components/number-input.md)
>* [Deelvenstercontainer](/help/adaptive-forms/components/panel-container.md)
>* [Keuzerondje](/help/adaptive-forms/components/radio-button.md)
>* [Knop Opnieuw instellen](/help/adaptive-forms/components/reset-button.md)
>* [Verzendknop](/help/adaptive-forms/components/submit-button.md)
>* [Telefooninvoer](/help/adaptive-forms/components/telephone-input.md)
>* [Tekstinvoer](/help/adaptive-forms/components/text-input.md)
>* [Tekst](/help/adaptive-forms/components/text.md)
>* [Titel](/help/adaptive-forms/components/title.md)
>* [Wizard](/help/adaptive-forms/components/wizard.md)

## Zie ook {#see-also}

{{see-also}}