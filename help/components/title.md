---
title: Component Title
description: De component van de Titel van de Component van de Kern is een component van de sectiekop die op zijn plaats het uitgeven kenmerkt.
role: Architect, Developer, Admin, User
exl-id: 393af72c-549f-4609-afb0-2712f827b549
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---

# Component Title{#title-component}

De component van de Titel van de Component van de Kern is een component van de sectiekop die op zijn plaats het uitgeven kenmerkt.

## Gebruik {#usage}

De component Titel is bedoeld voor gebruik als de titel of koptekst van een sectie met inhoud. De beschikbare rubriekniveaus kunnen door de malplaatjeauteur in de [ ontwerpdialoog ](#design-dialog) worden bepaald. De inhoudsredacteur kan uit beschikbare rubrieken in [ selecteren uitgeeft dialoog ](#edit-dialog). Voor meer gemak is het ook mogelijk de koptekst eenvoudig op locatie te bewerken.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Title is v3, die in februari 2022 is geïntroduceerd met release 2.18.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v3 | - | Compatibel | Compatibel | Compatibel |
| [ v2 ](v2/title.md) | Compatibel | Compatibel | - | Compatibel |
| [ v1 ](v1/title-v1.md) | Compatibel | Compatibel | - | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Titel te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_title).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Titel [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_title_v3) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de titeltekst definiëren en het kopniveau selecteren.

* **Titel** - als leeg de paginatitel zal worden gebruikt
* **Type/Grootte** - bepaalt het kopniveau van de titel
* **Verbinding** - bepaalt de inhoud waaraan de titel zal verbinden. Dit kan een pad zijn naar een inhoudspagina, een externe URL of een pagina-anker.
* **Open verbinding in nieuw lusje** - wanneer gecontroleerd, zal de verbinding in een nieuwe browser tabel openen.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

![ de Component van de Titel geeft dialoog uit ](/help/assets/title-edit.png)

U kunt de editor op zijn plaats ook gebruiken om de tekst van de titelcomponent te bewerken.

![ Op plaats het uitgeven van de Component van de Titel ](/help/assets/title-edit-inline.png)

### Tabblad Stijlen {#styles-tab-edit}

De Component van de Titel steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [ ontwerpdialoog ](#design-dialog) worden gevormd opdat het drop-down menu beschikbaar is.

![ het lusje van Stijlen van uitgeeft dialoog van de Component van de Titel ](/help/assets/title-edit-styles.png)

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur het standaardkopniveau definiëren dat titelcomponenten hebben wanneer ze door de auteurs van de inhoud worden gemaakt.

### Tabblad Grootte {#sizes-tab}

![ het ontwerpdialoog van de Component van de Titel ](/help/assets/title-design.png)

* **Toegestane Types/Grootte voor Auteurs** - laat of maak rubriektypes toe onbruikbaar die voor inhoudsauteurs beschikbaar zullen zijn wanneer zij de Component van de Titel gebruiken.
* **StandaardType/Grootte** - bepaal het rubriektype dat automatisch zal worden toegewezen wanneer een inhoudsauteur de Component van de Titel aan een pagina toevoegt.
* **maak Verbinding** onbruikbaar - maak steun voor verbindingen in de titelcomponent onbruikbaar om inhoudsauteurs van titels te verbieden te verbinden.

### Tabblad Stijlen {#styles-tab}

De Component van de Titel steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De Component van de Titel steunt de [ Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
