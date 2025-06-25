---
title: Taser-component (v1)
description: De teaser-component kan een afbeelding, een titel, RTF-tekst en eventueel een koppeling naar andere inhoud weergeven.
role: Architect, Developer, Admin, User
exl-id: 48e56938-660a-43e7-9e62-8069283ae73f
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 0%

---


# Taser-component (v1) {#teaser-component}

De component van de Teaser Component van de Kern kan een beeld, een titel, rijke-tekst, en naar keuze verbinding aan verdere inhoud tonen.

## Gebruik {#usage}

Met de component Taser kan de auteur van de inhoud eenvoudig een gummetje maken om inhoud te verfraaien met een afbeelding, titel of tekst met opmaak en een koppeling maken naar andere inhoud of andere handelingen.

De malplaatjeauteur kan de [ ontwerpdialoog ](#design-dialog) gebruiken om te bepalen als de opties om vraag-aan-acties tot stand te brengen en verbindingen toe te voegen beschikbaar zijn evenals het onbruikbaar maken van diverse vertoningsopties. De inhoudauteur kan [ gebruiken vormt dialoog ](#configure-dialog) om een beeld te plaatsen, CTAs te bepalen, titels en beschrijvingen te plaatsen, en verbindingen aan het individuele meetapparaat te vormen. Het [ geeft dialoog uit ](image-v1.md#edit-dialog) van de [ Component van het Beeld ](image-v1.md) kan worden betreden om het teaser beeld te wijzigen.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Teaser Component beschreven. Deze versie is in juli 2018 geïntroduceerd met versie 2.1.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 1 van de Taser-component beschreven.
>
>Voor details van de huidige versie van de Component van het Taser, zie het ](/help/components/teaser.md) document van de Component van 0} Taser.[

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van het Teken te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_teaser).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van het Taser [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_teaser_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

De auteur van de inhoud kan het dialoogvenster Configure gebruiken om de eigenschappen van de afzonderlijke teaser te definiëren. Er is ook een [ uitgeeft dialoog ](#edit-dialog) om het teasbeeld te wijzigen als men wordt geselecteerd.

### Afbeelding {#image}

![ de bewerkingsdialoog van de Component van de Taser het beeldlusje van de dialoog ](/help/assets/teaser-edit-image.png)

* **activa van het Beeld**
   * Daling een activa van [ activa browser ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of ontvang **doorbladert** optie om van een lokaal dossiersysteem te uploaden.
   * Tik of klik **Duidelijk** om het momenteel geselecteerde beeld te deselecteren.
   * Tik of klik **uitgeven** [ om de vertoningen van de activa ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in de activaredacteur te beheren.

>[!NOTE]
>
>[ de Dynamische eigenschappen van Media ](image-v1.md#dynamic-media) zijn momenteel niet beschikbaar in de Component van het Taser.

### Tekst {#text}

![ de Edit van de Component van de Taser de tekst van de de dialoogdoos tabel ](/help/assets/teaser-edit-text.png)

* **Pretitle** - de voortitel zal vóór de titel van het meetapparaat worden getoond.
* **Titel** - bepaalt een titel om als titel voor het meetapparaat te tonen.
   * **krijgt titel van verbonden pagina** - wanneer gecontroleerd, zal de titel met de verbonden titel van de pagina worden bevolkt.
* **Beschrijving** - bepaalt een beschrijving aan vertoning als onderverdeling van het gummetje.
   * **krijgt beschrijving van verbonden pagina** - wanneer gecontroleerd, zal de beschrijving met de verbonden beschrijving van de pagina worden bevolkt.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Koppelingen en handelingen {#links-actions}

![ de bewerkingsdialoog van de Component van de Taser component lusje ](/help/assets/teaser-edit-link.png)

* **Verbinding** - Verbinding die op het meetapparaat wordt toegepast. Gebruik de padbrowser om het doel van de koppeling te selecteren.
* **laat vraag-aan-Acties** toe - wanneer gecontroleerd, laat definitie van vraag-aan-Acties toe. De eerste Call-to-action-koppeling in de lijst wordt gebruikt als de koppeling voor andere teaser-elementen.

## Dialoogvenster Bewerken {#edit-dialog}

De Component van het Taser delegeert beeld dat aan de [ Component van het Beeld ](image-v1.md) teruggeeft. Daarom geeft [ dialoog uit ](image-v1.md#edit-dialog) van de Component van het Beeld is beschikbaar aan de inhoudauteur om het teaser beeld te manipuleren.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de teasopties definiëren die de auteur van de inhoud heeft bij het gebruik van deze component.

### Taser Tab {#teaser-tab}

{het ontwerpdialoog van de Component van 0} Taser ](/help/assets/teaser-design.png)![

* **vraag-aan-Acties**
   * **maak vraag-aan-Acties** onbruikbaar - verberg **vraag-aan-Acties** optie voor inhoudsauteurs
* **Elementen**
   * **Verberg pretitle** - verbergt de **optie van de Pretitle** voor inhoudsauteurs
   * **Verberg titel** - verbergt de **optie van de Titel** voor inhoudsauteurs
      * Wanneer geselecteerd wordt het **Type van Titel** verborgen
   * **Verberg beschrijving** - verberg de **optie van de Beschrijving** voor inhoudsauteurs
* **Type van Titel** - bepaalt de markering van H die door de titel van het meetapparaat moet worden gebruikt.
* **Verbindingen**
   * **verbind niet het beeld** - wanneer geselecteerd, wordt het teasbeeld niet verbonden
   * **verbind niet de titel** - wanneer geselecteerd, wordt de teaser titel niet verbonden
* **Afgevaardigde van het Beeld** - Informatieve vertoning die op welke component wijst het Teaser beeld behandeling delegeert.

### Tabblad Stijlen {#styles-tab}

De Component van het Taser steunt het Systeem van de Stijl van AEM [ ](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De Component van het Taser steunt de [ Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
