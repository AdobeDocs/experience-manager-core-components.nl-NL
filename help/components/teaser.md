---
title: Teaser-component
description: De teaser-component kan een afbeelding, een titel, RTF-tekst en eventueel een koppeling naar andere inhoud weergeven.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Teaser-component {#teaser-component}

De component van de Teaser Component van de Kern kan een beeld, een titel, rijke-tekst, en naar keuze verbinding aan verdere inhoud tonen.

## Gebruik {#usage}

Met de component Taser kan de auteur van de inhoud eenvoudig een gummetje maken om inhoud te verfraaien met een afbeelding, titel of tekst met opmaak en een koppeling naar andere inhoud of andere handelingen tot stand te brengen.

De sjabloonauteur kan het [ontwerpdialoogvenster](#design-dialog) gebruiken om te bepalen of de opties voor het maken van oproepen naar acties en het toevoegen van koppelingen beschikbaar zijn en om verschillende weergaveopties uit te schakelen. De auteur van de inhoud kan het dialoogvenster [](#configure-dialog) configureren gebruiken om een afbeelding in te stellen, CTA&#39;s te definiëren, titels en beschrijvingen in te stellen en koppelingen naar de afzonderlijke teaser te configureren. Het dialoogvenster [](image.md#edit-dialog) Bewerken van de [Afbeeldingscomponent](image.md) kan worden geopend om de laserafbeelding te wijzigen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Teaser Component is v1, die in juli 2018 is geïntroduceerd met versie 2.1.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|---|
| v1 | Compatibel | Compatibel | Compatibel | Compatibel |

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_teaser)om de Taser-component te ervaren en voorbeelden van de configuratieopties en de HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Taser [kan op GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster configureren {#configure-dialog}

De auteur van de inhoud kan het dialoogvenster Configure gebruiken om de eigenschappen van de afzonderlijke teaser te definiëren. Er is ook een dialoogvenster [](#edit-dialog) Bewerken waarin u de laserafbeelding kunt wijzigen als deze is geselecteerd.

### Image {#image}

![](/help/assets/screen_shot_2018-07-03at104125.png)

* **Afbeeldingselement**
   * Zet een element neer vanuit de [middelenbrowser](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of tik op de **bladeroptie** om te uploaden vanaf een lokaal bestandssysteem.
   * Tik of klik op **Wissen** om de selectie van de geselecteerde afbeelding ongedaan te maken.
   * Tik of klik op **Bewerken** om de uitvoeringen van het element [in de middeleneditor te](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) beheren.

### Tekst {#text}

![](/help/assets/screen_shot_2018-07-03at104138.png)

* **Titel** definieert een titel die moet worden weergegeven als de kop voor het gereedschap Taser.
* **De titel ophalen van de gekoppelde pagina** Als deze optie is ingeschakeld, wordt de titel van de gekoppelde pagina ingevuld.
* **Omschrijving** definieert een beschrijving die wordt weergegeven als subcode van het gummetje.
* **Beschrijving van gekoppelde pagina** ophalen Als deze optie is ingeschakeld, wordt de beschrijving gevuld met de beschrijving van de gekoppelde pagina.

### Koppelingen en handelingen {#links-actions}

![](/help/assets/screen_shot_2018-07-03at104146.png)

* **Koppelingskoppeling** toegepast op het taser. Gebruik de padbrowser om het doel van de koppeling te selecteren.
* **Laat vraag-aan-Acties** toe wanneer gecontroleerd, laat definitie van vraag-aan-Acties toe. De eerste vraag-aan-actie verbinding in de lijst wordt gebruikt als verbinding voor andere teaser elementen.

## Dialoogvenster Bewerken {#edit-dialog}

De component Teaser delegeert het renderen van afbeeldingen naar de [afbeeldingscomponent](image.md). Daarom is het dialoogvenster []Bewerken (image.md#edit-dialog van de Image Component) beschikbaar voor de auteur van de inhoud om de teasafbeelding te bewerken.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de teasopties definiëren die de auteur van de inhoud heeft bij het gebruik van deze component.

### Taser Tab {#teaser-tab}

![](/help/assets/screen_shot_2018-07-03at105958.png)

* **Oproep tot actie**
   * **Schakel Vraag-aan-Acties** onbruikbaar makenVerberg de **vraag-aan-Acties** optie voor inhoudsauteurs
* **Elementen**
   * **Titel verbergen**
      * Hiermee verbergt u de optie **Titel** voor auteurs van inhoud
      * Wanneer u deze optie selecteert, wordt het **titeltype** verborgen
   * **Beschrijving** verbergen De optie **Beschrijving** verbergen voor auteurs van inhoud
* **Titeltype** definieert de tag H die moet worden gebruikt door de titel van het gummetje.
* **Koppelingen**
   * **Koppel de afbeelding** niet aan als deze is geselecteerd, wordt de laserafbeelding niet gekoppeld
   * **Koppel de titel** niet als deze is geselecteerd. De teastitel is dan niet gekoppeld

### Tabblad Stijlen {#styles-tab}

De component Teaser ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).
