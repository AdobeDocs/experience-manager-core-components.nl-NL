---
title: Taser-component (v1)
description: De teaser-component kan een afbeelding, een titel, RTF-tekst en eventueel een koppeling naar andere inhoud weergeven.
role: Architect, Developer, Admin, User
exl-id: 48e56938-660a-43e7-9e62-8069283ae73f
source-git-commit: 84e09fa64b3a7ae40ff3ff1a04ea1c7504db29d2
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# Taser-component (v1) {#teaser-component}

De component van de Teaser Component van de Kern kan een beeld, een titel, rijke-tekst, en naar keuze verbinding aan verdere inhoud tonen.

## Gebruik {#usage}

Met de component Taser kan de auteur van de inhoud eenvoudig een gummetje maken om inhoud te verfraaien met een afbeelding, titel of tekst met opmaak en een koppeling naar andere inhoud of andere handelingen tot stand te brengen.

De sjabloonauteur kan de opdracht [ontwerpdialoogvenster](#design-dialog) om te bepalen als de opties om vraag-aan-acties tot stand te brengen en verbindingen toe te voegen beschikbaar zijn evenals het onbruikbaar maken van diverse vertoningsopties. De auteur van de inhoud kan de [dialoogvenster configureren](#configure-dialog) om een afbeelding in te stellen, CTA&#39;s te definiëren, titels en beschrijvingen in te stellen en koppelingen naar het afzonderlijke Taser te configureren. De [dialoogvenster bewerken](image-v1.md#edit-dialog) van de [Afbeeldingscomponent](image-v1.md) kan worden geopend om de teasafbeelding te wijzigen.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Teaser Component beschreven. Deze versie is in juli 2018 geïntroduceerd met versie 2.1.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 1 van de Taser Component beschreven.
>
>Zie voor meer informatie over de huidige versie van de Taser-component de klasse [Teaser-component](/help/components/teaser.md) document.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de Taser-component wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_teaser).

### Technische details {#technical-details}

De meest recente technische documentatie over de Teaser Component [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_teaser_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

De auteur van de inhoud kan het dialoogvenster Configure gebruiken om de eigenschappen van de afzonderlijke teaser te definiëren. Er is ook een [dialoogvenster bewerken](#edit-dialog) om de laserafbeelding te wijzigen als deze is geselecteerd.

### Afbeelding {#image}

![Het tabblad Afbeelding van het dialoogvenster Bewerken van de Teasercomponent](/help/assets/teaser-edit-image.png)

* **Afbeeldingselement**
   * Middelen uit het deelvenster [middelenbrowser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of tik op **doorbladeren** uploaden vanuit een lokaal bestandssysteem.
   * Tik of klik op **Wissen** om de selectie van de geselecteerde afbeelding op te heffen.
   * Tik of klik op **Bewerken** tot [de uitvoeringen van het actief beheren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in de middeleneditor.

>[!NOTE]
>
>[Dynamic Media-functies](image-v1.md#dynamic-media) zijn momenteel niet beschikbaar in de Taser-component.

### Tekst {#text}

![Het teksttabblad van het dialoogvenster Bewerken van de component Teaser](/help/assets/teaser-edit-text.png)

* **Pretitle** - De voortitel wordt vóór de titel van de taser weergegeven.
* **Titel** - Definieert een titel die moet worden weergegeven als de kop voor het gummetje.
   * **Titel ophalen van gekoppelde pagina** - Als deze optie is ingeschakeld, wordt de titel van de gekoppelde pagina ingevuld.
* **Beschrijving** - Definieert een beschrijving die moet worden weergegeven als subcode van het gummetje.
   * **Beschrijving ophalen van gekoppelde pagina** - Als deze optie is ingeschakeld, wordt de beschrijving gevuld met de beschrijving van de gekoppelde pagina.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Koppelingen en handelingen {#links-actions}

![Het tabblad voor het dialoogvenster voor het bewerken van de component Teaser](/help/assets/teaser-edit-link.png)

* **Koppeling** - Koppeling toegepast op het gummetje. Gebruik de padbrowser om het doel van de koppeling te selecteren.
* **Vraag-aan-Acties toelaten** - Wanneer gecontroleerd, laat definitie van vraag-aan-Acties toe. De eerste vraag-aan-actie verbinding in de lijst wordt gebruikt als verbinding voor andere teaser elementen.

## Dialoogvenster Bewerken {#edit-dialog}

De component Teaser delegeert het renderen van afbeeldingen aan de [Afbeeldingscomponent](image-v1.md). Daarom [dialoogvenster bewerken](image-v1.md#edit-dialog) van de Afbeeldingscomponent is beschikbaar voor de auteur van de inhoud om de laserafbeelding te bewerken.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de teasopties definiëren die de auteur van de inhoud heeft bij het gebruik van deze component.

### Taser Tab {#teaser-tab}

![Ontwerpdialoogvenster van de Teaser Component](/help/assets/teaser-design.png)

* **Oproep tot actie**
   * **Schakel Vraag-aan-Acties onbruikbaar** - Verberg de **Oproep tot actie** optie voor auteurs van inhoud
* **Elementen**
   * **Voortitel verbergen** - Verbergt de **Pretitle** optie voor auteurs van inhoud
   * **Titel verbergen** - Verbergt de **Titel** optie voor auteurs van inhoud
      * Als u **Type titel** is verborgen
   * **Beschrijving verbergen** - Verberg de **Beschrijving** optie voor auteurs van inhoud
* **Type titel** - Definieert de tag H die moet worden gebruikt door de titel van het gummetje.
* **Koppelingen**
   * **Koppel de afbeelding niet** - Als deze optie is geselecteerd, wordt de laserafbeelding niet gekoppeld
   * **Koppel de titel niet** - Als deze optie is geselecteerd, is de lasertitel niet gekoppeld
* **Afbeelding delegeren** - Informatieweergave die aangeeft aan welke component de Taser de beeldverwerking delegeert.

### Tabblad Stijlen {#styles-tab}

De component Taser ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component Teaser ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
