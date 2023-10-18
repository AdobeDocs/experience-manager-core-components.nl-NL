---
title: Adaptieve Forms Core-component - Formuliercontainer
description: Voeg een adaptief formulier toe aan een webpagina.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 0bebc248ee2b708f7677950d90356abd5bc70a98
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Formuliercontainer {#form-container-adaptive-forms-core-component}

Forms stelt bezoekers van websites in staat om te communiceren met de website door waardevolle informatie te verstrekken, die de betrokkenheid en gebruikerstevredenheid kan verhogen. Met een adaptieve formuliercontainer in Adobe Experience Manager-sites (AEM) kunnen eigenaars van websites gemakkelijk formulieren toevoegen aan hun pagina&#39;s. Hierdoor wordt de communicatie tussen websitebezoekers en de eigenaar of organisatie van de website vergemakkelijkt doordat bezoekers op een gestroomlijnde manier feedback kunnen geven, vragen kunnen stellen en andere handelingen kunnen uitvoeren

## Gebruik {#reasons-to-use-forms-container}

Er zijn verschillende redenen waarom een formulier aan een website kan worden toegevoegd:

* **Gegevensverzameling**: Forms kan worden gebruikt om gegevens van websitebezoekers te verzamelen voor verschillende doeleinden, zoals marktonderzoek, analyse van gebruikersgedrag en meer.

* **Loodgeneratie**: Een formulier kan worden gebruikt om informatie van potentiële klanten, zoals naam en e-mailadres, te verzamelen om leads voor verkoop- en marketingactiviteiten te genereren.

* **E-handel**: Forms kan worden gebruikt voor online winkelen, zodat klanten bestellingen kunnen plaatsen en betalingen kunnen verrichten via de website.

* **Contact**: Met een contactformulier kunnen bezoekers van de website gemakkelijk contact opnemen met de eigenaar of organisatie van de website.

* **Enquêtes en peilingen**: Forms kan worden gebruikt om via enquêtes en opiniepeilingen feedback en meningen van websitebezoekers te verzamelen.

* **Gebeurtenisregistratie**: Forms kan worden gebruikt voor gebeurtenisregistratie, zodat websitebezoekers zich kunnen aanmelden voor gebeurtenissen of webinars.

* **Abonnementen**: Forms kan worden gebruikt voor websiteabonnementen, zodat bezoekers zich kunnen aanmelden voor een nieuwsbrief of andere regelmatige communicatie.

* **Gebruikersverificatie**: Forms kan worden gebruikt voor gebruikersverificatie, zodat websitebezoekers accounts kunnen maken en zich kunnen aanmelden voor toegang tot exclusieve inhoud of functies.

* **Conversiesnelheid verhogen**: Een goed ontworpen formulier kan de conversiesnelheid verhogen door het gebruikers gemakkelijk te maken een gewenste actie uit te voeren, zoals het aanschaffen van een product of het aanmelden voor een service.


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

* **Vooraf ingevulde services** - Met deze optie kan de gebruiker een vooraf ingevulde service selecteren voor het ophalen van gegevens wanneer het adaptieve formulier wordt weergegeven. Meer informatie over [hoe te om een vooraf ingevulde dienst tot stand te brengen en te vormen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=en#aem-forms-custom-prefill-service).

* **Categorie Clientbibliotheek** - De gebruiker kan een aangepaste JavaScript-bibliotheek configureren per adaptief formulier. Het wordt aanbevolen alleen de herbruikbare functies in de bibliotheek te behouden, die afhankelijk zijn van bibliotheken van derden jquery en underscore.js.

### Tabblad Verzending {#submission-tab}

![Tabblad Verzending](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

Gebruikers kunnen verschillende handelingen configureren voor het verzenden van een adaptief formulier.

* **URL/pad omleiden** - Met deze optie kan de gebruiker een pagina configureren voor elk formulier, waarnaar de gebruikers van het formulier worden omgeleid na het verzenden van een adaptief formulier. Klik hier voor meer informatie over [omleidingspagina&#39;s configureren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html).

![Berichtvenster tonen, tabblad](/help/adaptive-forms/assets/formconatiner_showmessage.png)

* **Bericht tonen** - Met deze optie kunnen gebruikers een bericht toevoegen dat wordt weergegeven wanneer het Adaptief formulier is verzonden. De vooraf gedefinieerde tekst wordt opgenomen in het dialoogvenster en kan door de gebruiker worden gewijzigd. Het dialoogvenster Bericht tonen ondersteunt gereedschappen voor tekstopmaak waarmee gebruikers de toegevoegde tekst kunnen opmaken.

* **Handeling verzenden** - Een handeling Verzenden wordt geactiveerd wanneer een gebruiker op de knop Verzenden klikt op een adaptief formulier. Gebruikers kunnen in de vervolgkeuzelijst de optie Handelingen verzenden selecteren die in het vak worden ondersteund. Leer hoe u [Een handeling verzenden configureren op het tabblad Verzending](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#supporting-custom-functions-in-validation-expressions-br).

## Verwante artikelen {#related-article}

* [Een adaptief formulier maken in AEM Sites Page of Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

* [Een zelfstandig adaptief formulier maken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)


>[!MORELIKETHIS]
>
>* [Accordeon](/help/adaptive-forms/components/accordion.md)
>* [Knop](/help/adaptive-forms/components/button.md)
>* [Selectievakjesgroep](/help/adaptive-forms/components/checkbox-group.md)
>* [Datumkiezer](/help/adaptive-forms/components/date-picker.md)
>* [Vervolgkeuzelijst](/help/adaptive-forms/components/drop-down.md)
>* [E-mailinvoer](/help/adaptive-forms/components/email-input.md)
>* [Bestandsbijlage](/help/adaptive-forms/components/file-attachment.md)
>* [Voettekst](/help/adaptive-forms/components/footer.md)
>* [Koptekst](/help/adaptive-forms/components/header.md)
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