---
title: component Button (v1)
description: Met de component Knop Core-component kunt u een knop maken en weergeven.
role: Architect, Developer, Admin, User
exl-id: 63af16e4-dd4d-426d-88ef-769ecd1b3175
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---


# component Button (v1) {#button-component}

De component van de Knoop van de Component van de Kern staat voor de configuratie en de vertoning van een knooppunt op een pagina toe.

## Gebruik {#usage}

Met de component Core Component Button kan een knop op een pagina worden opgenomen.

* De eigenschappen van de knoop kunnen in [ worden geselecteerd vormen dialoog ](#configure-dialog).
* De stijlen voor de Component van de Knoop kunnen in de [ ontwerpdialoog ](#design-dialog) worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

Het document beschrijft v1 van de component Button, die in juni 2019 werd geïntroduceerd met versie 2.5.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Button beschreven.
>
>Voor details van de huidige versie van de Component van de Knoop, zie het [ document van de Component van de Knoop ](/help/components/button.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Knoop te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_button).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Knoop [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_button_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud de knop definiëren en bepalen hoe deze zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

### Tabblad Eigenschappen {#properties-tab}

![ het lusje van Eigenschappen van uitgeeft dialoog van de Component van de Knoop ](/help/assets/button-edit-properties.png)

* **Tekst** - de tekst om op de knoop te tonen
* **Verbinding** - Verbinding met een inhoudspagina binnen AEM, een extern middel, of een anker
   * Gebruik de **Dialoog van de Selectie** om een weg binnen AEM te kiezen.
* **Pictogram** - Herkenningsteken voor het tonen van een pictogram in de knoop
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Toegankelijkheid {#accessibility-tab}

![ Toegankelijkheid lusje van uitgeeft dialoog van de Component van de Knoop ](/help/assets/button-edit-accessibility.png)

Op het **lusje van de Toegankelijkheid**, kunnen de waarden voor [ de toegankelijkheidslabels van ARIA ](https://www.w3.org/WAI/standards-guidelines/aria/) voor de component worden geplaatst.

* **Etiket** - Waarde van een ARIA etiketattribuut voor de component

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component van de Knoop steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De component van de Knoop steunt de [ Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
