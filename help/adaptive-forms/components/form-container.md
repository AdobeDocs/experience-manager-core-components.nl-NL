---
title: Adaptieve Forms Core-component - Formuliercontainer
description: Voeg een adaptief formulier toe aan een webpagina.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 8bba79956a04020647d5d04f9fe6fa674affedf1
workflow-type: tm+mt
source-wordcount: '1340'
ht-degree: 0%

---

# Formuliercontainer {#form-container-adaptive-forms-core-component}

Forms stelt bezoekers van websites in staat om te communiceren met de website door waardevolle informatie te verstrekken, die de betrokkenheid en gebruikerstevredenheid kan verhogen. Met een adaptieve formuliercontainer in Adobe Experience Manager-sites (AEM) kunnen eigenaars van websites gemakkelijk formulieren toevoegen aan hun pagina&#39;s. Hierdoor wordt de communicatie tussen websitebezoekers en de eigenaar of organisatie van de website vergemakkelijkt doordat bezoekers op een gestroomlijnde manier feedback kunnen geven, vragen kunnen stellen en andere handelingen kunnen uitvoeren

## Gebruik {#reasons-to-use-forms-container}

Er zijn verschillende redenen waarom een formulier aan een website kan worden toegevoegd:
- **Gegevensverzameling**: Forms kan worden gebruikt om gegevens van websitebezoekers te verzamelen voor verschillende doeleinden, zoals marktonderzoek, analyse van gebruikersgedrag en meer.

- **Loodgeneratie**: Een formulier kan worden gebruikt om informatie van potentiële klanten, zoals naam en e-mailadres, te verzamelen om leads voor verkoop- en marketingactiviteiten te genereren.

- **E-handel**: Forms kan worden gebruikt voor online winkelen, zodat klanten bestellingen kunnen plaatsen en betalingen kunnen verrichten via de website.

- **Contact**: Met een contactformulier kunnen bezoekers van de website gemakkelijk contact opnemen met de eigenaar of organisatie van de website.

- **Enquêtes en peilingen**: Forms kan worden gebruikt om via enquêtes en opiniepeilingen feedback en meningen van websitebezoekers te verzamelen.

- **Gebeurtenisregistratie**: Forms kan worden gebruikt voor gebeurtenisregistratie, zodat websitebezoekers zich kunnen aanmelden voor gebeurtenissen of webinars.

- **Abonnementen**: Forms kan worden gebruikt voor websiteabonnementen, zodat bezoekers zich kunnen aanmelden voor een nieuwsbrief of andere regelmatige communicatie.

- **Gebruikersverificatie**: Forms kan worden gebruikt voor gebruikersverificatie, zodat websitebezoekers accounts kunnen maken en zich kunnen aanmelden voor toegang tot exclusieve inhoud of functies.

- **Conversiesnelheid verhogen**: Een goed ontworpen formulier kan de conversiesnelheid verhogen door het gebruikers gemakkelijk te maken een gewenste actie uit te voeren, zoals het aanschaffen van een product of het aanmelden voor een service.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.12](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Lees de nieuwste informatie over de Adaptive Forms Container Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de ervaring van uw formuliercontainer eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig opties voor formuliercontainers definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![Het tabblad Basis](/help/adaptive-forms/assets/formcontainer_basictab.png)

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

- **Vooraf ingevulde services** - Met deze optie kan de gebruiker een vooraf ingevulde service selecteren voor het ophalen van gegevens wanneer het adaptieve formulier wordt weergegeven. Meer informatie over [hoe te om een vooraf ingevulde dienst tot stand te brengen en te vormen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=en#aem-forms-custom-prefill-service).

- **Categorie Clientbibliotheek** - De gebruiker kan een aangepaste JavaScript-bibliotheek configureren per adaptief formulier. Het wordt aanbevolen alleen de herbruikbare functies in de bibliotheek te behouden, die afhankelijk zijn van bibliotheken van derden jquery en underscore.js.
Als er soms **complexe validatieregels** Het exacte validatiescript bevindt zich in aangepaste functies en gebruikers roepen deze aangepaste functies aan vanuit de expressie voor veldvalidatie. Als u deze aangepaste functiebibliotheek bekend en beschikbaar wilt maken tijdens het uitvoeren van validaties aan de serverzijde, kan de gebruiker de naam van AEM clientbibliotheek configureren onder de **[!UICONTROL Basic]** tabblad Adaptieve formuliercontainereigenschappen, zoals hieronder weergegeven.

De gebruiker kan de aangepaste JavaScript-bibliotheek per adaptief formulier configureren. Houd in de bibliotheek alleen de herbruikbare functies die afhankelijk zijn van bibliotheken van derden jquery en underscore.js.

### Tabblad Gegevensmodel {#data-model-tab}

![Tabblad Verzending](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

Met het formuliergegevensmodel kunt u een formulier verbinden met een gegevensbron om gegevens te verzenden en te ontvangen op basis van gebruikersacties. U kunt een formulier ook verbinden met een JSON-schema om de verzonden gegevens in een vooraf gedefinieerde indeling te ontvangen. Afhankelijk van de vereiste verbinding, sluit uw formulier aan op een JSON-schema of formuliergegevensmodel:
- Een JSON-schema maken en uploaden naar uw omgeving
- Een formuliergegevensmodel maken

### Tabblad Verzending {#submission-tab}

Gebruikers kunnen verschillende handelingen configureren voor het verzenden van een adaptief formulier.

- **URL/pad omleiden** - Met deze optie kan de gebruiker een pagina configureren voor elk formulier, waarnaar de gebruikers van het formulier worden omgeleid na het verzenden van een adaptief formulier. Klik hier voor meer informatie over [omleidingspagina&#39;s configureren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html).

![Tabblad Verzending](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **Bericht tonen** - Met deze optie kunnen gebruikers een bericht toevoegen dat wordt weergegeven wanneer het Adaptief formulier is verzonden. De vooraf gedefinieerde tekst wordt opgenomen in het dialoogvenster en kan door de gebruiker worden gewijzigd. Het dialoogvenster Bericht tonen ondersteunt gereedschappen voor tekstopmaak waarmee gebruikers de toegevoegde tekst kunnen opmaken.

![Berichtvenster tonen, tabblad](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **Handeling verzenden** - Een handeling Verzenden wordt geactiveerd wanneer een gebruiker op de knop Verzenden klikt op een adaptief formulier. Gebruikers kunnen in de vervolgkeuzelijst de optie Handelingen verzenden selecteren die in het vak worden ondersteund. Leer hoe u [Een handeling verzenden configureren op het tabblad Verzending](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#supporting-custom-functions-in-validation-expressions-br).

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Form Container te definiëren en te beheren.

### Tabblad Toegestane componenten {#allowed-components-tab}

![Dialoogvenster Toegestaan component, tabblad](/help/adaptive-forms/assets/formcontainer-allowedcomponents.png)

De **Toegestane componenten** kunt u in de sjablooneditor de componenten instellen die als items kunnen worden toegevoegd aan de deelvensters in de component in de Adaptieve Forms-editor.

### Tabblad Standaardcomponenten {#default-components-tab}

![Standaardtabblad van dialoogvenster Ontwerp](/help/adaptive-forms/assets/formcontainer-defaultcomponents.png)

De **Standaardcomponenten** kunt u in de sjablooneditor opgeven welke componenten standaard zichtbaar zijn als items in de formuliercontainercomponent in de Adaptive Forms-editor.

### Tab Instellingen voor responsief {#responsive-tab}

![Instellingen tabblad van dialoogvenster Ontwerpen](/help/adaptive-forms/assets/formcontainer-responsivestyle.png)

De **Instellingen voor responsie** kunt u in de sjablooneditor het aantal kolommen in het raster opgeven dat zich in de formuliercontainercomponent van de Adaptieve Forms-editor bevindt.

### Tabblad Stijlen {#styles-tab}

De Adaptive Forms File Attachment Core-component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Ontwerpdialoogvenster](/help/adaptive-forms/assets/formcontainer-styletab.png)

- **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Form Container Core Component.

- **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Tabblad Aangepaste eigenschappen

![Dialoogvenster Aangepaste eigenschappen](/help/adaptive-forms/assets/formcontainer-custompropertiestab.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Groepsnaam**: U kunt een naam opgeven om de groep met aangepaste eigenschappen te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **Belangrijke paren**: U kunt meerdere aangepaste eigenschapnamen en aangepaste eigenschapswaarden toevoegen door op de knop **Toevoegen** knop voor elke aangepaste groep eigenschappen.

   - **Verwijderen**: Tik of klik om de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te verwijderen.

   - **Opnieuw rangschikken**: Tik of klik en sleep om de volgorde van de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te wijzigen.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}