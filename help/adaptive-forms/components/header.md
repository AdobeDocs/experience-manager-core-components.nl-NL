---
title: Adaptive Forms Core Component - Koptekst
description: De Adaptive Forms Header Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: aa18def9-0bec-4475-8dde-213860621ef5
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---


# Koptekst {#header-adaptive-forms-core-component}

Een koptekstcomponent in een adaptief formulier is een sectie boven aan het formulier die doorgaans de titel, het logo of de naam van het formulier bevat. De koptekst kan ook andere informatie bevatten, zoals een korte beschrijving van het doel van het formulier, de naam van de organisatie die het formulier heeft gemaakt of contactgegevens voor hulp bij het formulier. De koptekst wordt gebruikt om gebruikers een overzicht van het formulier te geven en context te bieden voor de informatie die ze op het punt staan in te vullen. Deze wordt gebruikt om gebruikers te helpen het doel van het formulier te begrijpen en het formulier correct in te vullen.

{{traditional-aem}}

**Voorbeeld**

![ voorbeeld ](/help/adaptive-forms/assets/header.png)

## Gebruik {#reasons-to-use-header}

- **Branding**: Een kopbal kan worden gebruikt om het embleem of de naam van de organisatie te tonen die de vorm creeerde, die merkerkenning en geloofwaardigheid helpen vestigen.

- **Context**: Een kopbal kan een korte beschrijving van het doel van de vorm verstrekken, die gebruikers helpen de context begrijpen waarin de vorm wordt gebruikt.

- **Navigatie**: Een kopbal kan verbindingen of knopen omvatten die gebruikers toestaan om aan andere delen van de website of de toepassing te navigeren.

- **Informatie**: Een kopbal kan contactinformatie of verbindingen omvatten om middelen te helpen, die het voor gebruikers gemakkelijker maken om hulp te krijgen als zij het nodig hebben.

- **Ervaring van de Gebruiker**: Een kopbal kan worden gebruikt om de vorm gebruikersvriendelijker te maken door een duidelijke en intuïtieve manier voor gebruikers te verstrekken om tot vormgebieden toegang te hebben en in te vullen.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms header Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 for AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM-compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/adaptive-forms/version.md) en later | Compatibel met <br>[ versie 1.1.12 ](/help/adaptive-forms/version.md) en later maar minder dan 2.0.0. |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het [&#128279;](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0&rbrace;.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Krijg de recentste informatie over de Adaptieve Component van de Kern van de Kopbal van Forms in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageheader/v1/pageheader). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de headerervaring voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig koptekstopties definiëren voor een naadloze gebruikerservaring.

### Tabblad Afbeelding {#image-tab}

Dit gedeelte van de koptekst bevat de koptekst en de afbeelding.

![ Imagetab ](/help/adaptive-forms/assets/header_image.png)

- **Activa van het Beeld** - deze optie staat toe om activa zoals beeld met muisbelemmering en daling te laten vallen. U kunt een dossier van een lokaal dossiersysteem ook uploaden gebruikend **doorbladert** knoop. Nadat u een afbeelding hebt toegevoegd, staan er drie knoppen onder aan de afbeelding. Nadat u een afbeelding hebt toegevoegd, staan er drie knoppen onder aan de afbeelding:
   - **geef** uit - Tik of klik **geef** uit om de vertoningen van de activa in de Redacteur van Assets te beheren.
   - **Duidelijk** - Tik of klik **Duidelijk** om het momenteel geselecteerde beeld te deselecteren.
   - **Keuze** - Tik of klik **Keuze** optie om een ander beeld van de omslag van Assets te selecteren.

- **Titel** - deze optie wordt gebruikt om de rubriek aan de kopbal toe te voegen. De vooraf gedefinieerde tekst staat in het dialoogvenster en kan door de gebruiker worden gewijzigd.
- **Verbinding aan** - u kunt de rubriek met de omslag verbinden gebruikend **doorbladert** pictogram.
- **Beschrijving** - een beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek beeld verstrekt.
- **Grootte (px)** - het helpt in het aanpassen van de lengte en de breedte van het beeld door de pixel te verhogen of te verminderen.

![ toegankelijkheidslusje ](/help/adaptive-forms/assets/header_accessibility.png)

- **Alternatieve Tekst** - Deze optie wordt gebruikt om de tekst in te gaan die een kort en beschrijvend tekstalternatief voor het beeld verstrekt, dat het beeld aan visueel gehandicapte gebruikers beschrijft.

- **Beeld is decoratief** - controleer als het beeld door ondersteunende technologie zou moeten worden genegeerd en daarom geen alternatieve tekst vereist. Dit geldt alleen voor decoratieve afbeeldingen.

### Tabblad Tekst {#text-tab}

In deze sectie kunt u de tekst invoeren die in de koptekst moet worden opgenomen.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=nl-NL)

-->

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
