---
title: Teaser-component
description: De teaser-component kan een afbeelding, een titel, RTF-tekst en eventueel een koppeling naar andere inhoud weergeven.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 1%

---


# Teaser-component {#teaser-component}

De component van de Teaser Component van de Kern kan een beeld, een titel, rijke-tekst, en naar keuze verbinding aan verdere inhoud tonen.

## Gebruik {#usage}

Met de component Taser kan de auteur van de inhoud eenvoudig een gummetje maken om inhoud te verfraaien met een afbeelding, titel of tekst met opmaak en een koppeling naar andere inhoud of andere handelingen tot stand te brengen.

De sjabloonauteur kan het [ontwerpdialoogvenster](#design-dialog) gebruiken om te bepalen of de opties voor het maken van oproepen naar acties en het toevoegen van koppelingen beschikbaar zijn en om verschillende weergaveopties uit te schakelen. De auteur van de inhoud kan het dialoogvenster [](#configure-dialog) configureren gebruiken om een afbeelding in te stellen, CTA&#39;s te definiëren, titels en beschrijvingen in te stellen en koppelingen naar de afzonderlijke teaser te configureren. Het dialoogvenster [](image.md#edit-dialog) Bewerken van de [Afbeeldingscomponent](image.md) kan worden geopend om de laserafbeelding te wijzigen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Teaser Component is v1, die in juli 2018 is geïntroduceerd met versie 2.1.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel | Compatibel | Compatibel |

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_teaser)om de Taser-component te ervaren en voorbeelden van de configuratieopties en de HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Taser [kan op GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster configureren {#configure-dialog}

De auteur van de inhoud kan het dialoogvenster Configure gebruiken om de eigenschappen van de afzonderlijke teaser te definiëren. Er is ook een dialoogvenster [](#edit-dialog) Bewerken waarin u de laserafbeelding kunt wijzigen als deze is geselecteerd.

### Image {#image}

![Het tabblad Afbeelding van het dialoogvenster Bewerken van de Teasercomponent](/help/assets/teaser-edit-image.png)

* **Afbeeldingselement**
   * Zet een element neer vanuit de [middelenbrowser](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of tik op de **bladeroptie** om te uploaden vanaf een lokaal bestandssysteem.
   * Tik of klik op **Wissen** om de selectie van de geselecteerde afbeelding ongedaan te maken.
   * Tik of klik op **Bewerken** om de uitvoeringen van het element [in de middeleneditor te](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) beheren.

### Tekst {#text}

![Het teksttabblad van het dialoogvenster Bewerken van de component Teaser](/help/assets/teaser-edit-text.png)

* **Voortitel** - De voortitel wordt vóór de titel van het gummetje weergegeven.
* **Titel** - Definieert een titel die moet worden weergegeven als de kop voor het gummetje.
   * **Titel ophalen van gekoppelde pagina** - Als deze optie is ingeschakeld, wordt de titel van de gekoppelde pagina gevuld.
* **Beschrijving** - Hiermee definieert u een beschrijving die u wilt weergeven als subcode van het gummetje.
   * **Beschrijving ophalen van gekoppelde pagina** - Als deze optie is ingeschakeld, wordt de beschrijving gevuld met de beschrijving van de gekoppelde pagina.
* **ID** - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Koppelingen en handelingen {#links-actions}

![Het tabblad voor het dialoogvenster voor het bewerken van de component Teaser](/help/assets/teaser-edit-link.png)

* **Koppeling** - Koppeling toegepast op het taser. Gebruik de padbrowser om het doel van de koppeling te selecteren.
* **Laat vraag-aan-Acties** toe - wanneer gecontroleerd, laat definitie van vraag-aan-Acties toe. De eerste vraag-aan-actie verbinding in de lijst wordt gebruikt als verbinding voor andere teaser elementen.

## Dialoogvenster Bewerken {#edit-dialog}

De component Teaser delegeert het renderen van afbeeldingen naar de [afbeeldingscomponent](image.md). Daarom is het dialoogvenster []Bewerken (image.md#edit-dialog van de Image Component) beschikbaar voor de auteur van de inhoud om de teasafbeelding te bewerken.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de teasopties definiëren die de auteur van de inhoud heeft bij het gebruik van deze component.

### Taser Tab {#teaser-tab}

![Ontwerpdialoogvenster van de Teaser Component](/help/assets/teaser-design.png)

* **Oproep tot actie**
   * **Schakel Vraag-aan-Acties** uit - verberg de **vraag-aan-Acties** optie voor inhoudsauteurs
* **Elementen**
   * **Voortitel** verbergen - Verbergt de optie **Voortitel** voor auteurs van inhoud
   * **Titel** verbergen - Verbergt de optie **Titel** voor auteurs van inhoud
      * Wanneer u deze optie selecteert, wordt het **titeltype** verborgen
   * **Beschrijving** verbergen - De optie **Beschrijving** verbergen voor auteurs van inhoud
* **Titeltype** - Hiermee definieert u de tag H die door de titel van het gummetje moet worden gebruikt.
* **Koppelingen**
   * **Koppel de afbeelding** niet. Als deze optie is geselecteerd, wordt de laserafbeelding niet gekoppeld
   * **De titel** niet koppelen - Als deze optie is geselecteerd, is de teastitel niet gekoppeld
* **Afbeelding gedelegeerd** - Informatieweergave die aangeeft aan welke component de taser de beeldverwerking delegeert.

### Tabblad Stijlen {#styles-tab}

De component Teaser ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).
