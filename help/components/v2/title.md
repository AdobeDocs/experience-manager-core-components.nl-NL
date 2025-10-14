---
title: Titelcomponent (v2)
description: De component van de Titel van de Component van de Kern is een component van de sectiekop die op zijn plaats het uitgeven kenmerkt.
role: Architect, Developer, Admin, User
exl-id: f853ec46-19fd-4569-a9d3-5c376d2a2101
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---


# Titelcomponent (v2) {#title-component}

De component van de Titel van de Component van de Kern is een component van de sectiekop die op zijn plaats het uitgeven kenmerkt.

## Gebruik {#usage}

De component Titel is bedoeld voor gebruik als de titel of koptekst van een sectie met inhoud. De beschikbare rubriekniveaus kunnen door de malplaatjeauteur in de [&#x200B; ontwerpdialoog &#x200B;](#design-dialog) worden bepaald. De inhoudsredacteur kan uit beschikbare rubrieken in [&#x200B; selecteren uitgeeft dialoog &#x200B;](#edit-dialog). Voor meer gemak is het ook mogelijk de koptekst eenvoudig op locatie te bewerken.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 2 van de component Title beschreven, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 2 van de component Title beschreven.
>
>Voor details van de huidige versie van de Component van de Titel, zie het [&#128279;](/help/components/title.md) document van de Component van de Titel 0&rbrace; &lbrace;.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Titel te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [&#x200B; Bibliotheek van de Component &#x200B;](https://adobe.com/go/aem_cmp_library_title).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Titel [&#x200B; kan op GitHub &#x200B;](https://adobe.com/go/aem_cmp_tech_title_v2) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [&#x200B; de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden &#x200B;](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de titeltekst definiëren en het kopniveau selecteren.

* **Titel** - als leeg de paginatitel zal worden gebruikt
* **Type/Grootte** - bepaalt het kopniveau van de titel
* **Verbinding** - bepaalt de inhoud waaraan de titel zal verbinden. Dit kan een pad zijn naar een inhoudspagina, een externe URL of een pagina-anker.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [&#x200B; Laag van Gegevens te controleren &#x200B;](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

![&#x200B; de Component van de Titel geeft dialoog uit &#x200B;](/help/assets/title-edit.png)

>[!NOTE]
>
>De capaciteit om een verbinding voor de titel te bepalen werd geïntroduceerd met versie 2.2.0 van de Componenten van de Kern.

U kunt de editor op zijn plaats ook gebruiken om de tekst van de titelcomponent te bewerken.

![&#x200B; Op plaats het uitgeven van de Component van de Titel &#x200B;](/help/assets/title-edit-inline.png)

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur het standaardkopniveau definiëren dat titelcomponenten hebben wanneer ze door de auteurs van de inhoud worden gemaakt.

### Tabblad Grootte {#sizes-tab}

![&#x200B; het ontwerpdialoog van de Component van de Titel &#x200B;](/help/assets/title-design.png)

* **Toegestane Types/Grootte voor Auteurs** - laat of maak rubriektypes toe onbruikbaar die voor inhoudsauteurs beschikbaar zullen zijn wanneer zij de Component van de Titel gebruiken.
* **StandaardType/Grootte** - bepaal het rubriektype dat automatisch zal worden toegewezen wanneer een inhoudsauteur de Component van de Titel aan een pagina toevoegt.
* **maak Verbinding** onbruikbaar - maak steun voor verbindingen in de titelcomponent onbruikbaar om inhoudsauteurs van titels te verbieden te verbinden.

>[!NOTE]
>
>De capaciteit om een verbinding voor de titel te bepalen werd geïntroduceerd met versie 2.2.0 van de Componenten van de Kern.

### Tabblad Stijlen {#styles-tab}

De Component van de Titel steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De Component van de Titel steunt de [&#x200B; Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
