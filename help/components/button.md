---
title: Component Button
description: Met de component Knop Core-component kunt u een knop maken en weergeven.
role: Architect, Developer, Admin, User
exl-id: e17efd1d-90d4-497a-9e7d-45934d81bc28
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---


# Component Button{#button-component}

De component van de Knoop van de Component van de Kern staat voor de configuratie en de vertoning van een knooppunt op een pagina toe.

{{traditional-aem}}

## Gebruik {#usage}

Met de component Core Component Button kan een knop op een pagina worden opgenomen.

* De eigenschappen van de knoop kunnen in [ worden geselecteerd vormen dialoog ](#configure-dialog).
* De stijlen voor de Component van de Knoop kunnen in de [ ontwerpdialoog ](#design-dialog) worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Button is v2, die in februari 2022 is geïntroduceerd met release 2.18.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v2 | - | Compatibel | Compatibel | Compatibel |
| [ v1 ](v1/button.md) | Compatibel | Compatibel | - | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Knoop te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_button).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Knoop [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_button_v2) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud de knop definiëren en bepalen hoe deze zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

### Tabblad Eigenschappen {#properties-tab}

![ het lusje van Eigenschappen van uitgeeft dialoog van de Component van de Knoop ](/help/assets/button-edit-properties.png)

* **Tekst** - de tekst om op de knoop te tonen
* **Verbinding** - Verbinding met een inhoudspagina binnen AEM, een extern middel, of een anker
   * Gebruik de **Dialoog van de Selectie** om een weg binnen AEM te kiezen.
* **Open verbinding in nieuw lusje** - als gecontroleerd, zal de verbinding in een nieuwe browser tabel openen.
* **Pictogram** - Herkenningsteken voor het tonen van een pictogram in de knoop
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Toegankelijkheid {#accessibility-tab}

![ Toegankelijkheid lusje van uitgeeft dialoog van de Component van de Knoop ](/help/assets/button-edit-accessibility.png)

Op het **lusje van de Toegankelijkheid**, kunnen de waarden voor [ de toegankelijkheidslabels van ARIA ](https://www.w3.org/WAI/standards-guidelines/aria/) voor de component worden geplaatst.

* **Etiket** - Waarde van een ARIA etiketattribuut voor de component

### Tabblad Stijlen {#styles-tab-edit}

![ het lusje van Stijlen van uitgeeft dialoog van de Component van de Knoop ](/help/assets/button-edit-styles.png)

De component van de Knoop steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [ ontwerpdialoog ](#design-dialog) worden gevormd opdat het drop-down menu beschikbaar is.

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component van de Knoop steunt het Systeem van de Stijl van AEM [ ](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De component van de Knoop steunt de [ Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
