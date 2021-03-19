---
title: Component Snel zoeken
description: De component Snel zoeken biedt zoekmogelijkheden voor een website en biedt zoekresultaten zodat bezoekers de site kunnen doorzoeken en de resultaten kunnen filteren.
role: Architect, ontwikkelaar, beheerder, praktijkgerichte
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 1%

---


# Quick Search-component {#quick-search-component}

De component Snel zoeken biedt zoekmogelijkheden voor een website en biedt zoekresultaten zodat bezoekers gemakkelijk overeenkomende inhoud kunnen vinden en de resultaten kunnen bekijken.

## Gebruik {#usage}

Met de component Snel zoeken kunnen sitebezoekers naar inhoud zoeken, de resultaten op hun plaats bekijken en eenvoudig naar de overeenkomende pagina&#39;s navigeren. Nieuwe resultaten worden dynamisch opgehaald terwijl de gebruiker door de zoekresultaten schuift.

In het dialoogvenster [Bewerken](#edit-dialog) kan de auteur van de inhoud definiëren waar in de inhoudsstructuur de zoekopdracht moet beginnen. Met behulp van het [ontwerpdialoogvenster](#design-dialog) kan de sjabloonauteur de standaardwaarde instellen voor de plaats in de inhoudsstructuur waar de zoekopdracht moet beginnen, evenals een maximale resultaatingestelde grootte en minimale lengte van de zoekterm.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Snelle component van het Onderzoek is v1, die met versie 2.0.0 van de Componenten van de Kern in Januari 2018 werd geïntroduceerd, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

### Technische details {#technical-details}

>[!NOTE]
>
>Het beschermen van de Component van het Onderzoek of om het even welke AEM gebaseerde toepassing tegen DOS aanvallen zou op een hoger niveau moeten worden uitgevoerd, bijvoorbeeld door `mod_security` op de verzender te gebruiken.

De recentste technische documentatie over de Snelle Component van het Onderzoek [kan op GitHub](https://adobe.com/go/aem_cmp_tech_search_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster {#edit-dialog} bewerken

In het dialoogvenster Bewerken kan de auteur van de inhoud definiëren waar in de inhoudsstructuur de zoekopdracht moet beginnen.

![Dialoogvenster Snel zoeken in component bewerken](/help/assets/quick-search-edit.png)

**Hoofdmap**  zoeken - De hoofdpagina vanaf waar de zoekopdracht moet worden gestart. De hoofdmap van de zoekopdracht kan een master, master of reguliere pagina met een blauwdruk zijn.
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

Met behulp van het ontwerpdialoogvenster kan de sjabloonauteur de standaardwaarde instellen voor de plaats in de inhoudsstructuur waar de zoekopdracht moet beginnen, alsmede een maximale grootte voor de resultaatset en een minimale lengte voor de zoekterm. In het dialoogvenster Ontwerp kan de sjabloonauteur definiëren welke opties voor tekstopmaak beschikbaar zijn voor de auteurs van de inhoud.

### Tabblad Eigenschappen {#properties-tab}

![Het ontwerpdialoogvenster van de component Snel zoeken](/help/assets/quick-search-design.png)

* **Hoofdmap**
zoekenDe standaardwaarde van de zoekhoofdmap wanneer een auteur van inhoud de component Snel zoeken op een inhoudspagina plaatst
* **Grootte**
resultatenHet maximum aantal resultaten dat door een zoekverzoek wordt opgehaald
* **Zoekterm Minimale**
lengteMinimale lengte van de zoekterm om de zoekopdracht te starten

>[!NOTE]
>
>**De** Grootte van resultaten en de Minimumlengte van de  **** Term van het Onderzoek kunnen slechts op ontwerpwijze en daarom slechts op het malplaatjeniveau worden geplaatst, betekenend inhoudsauteurs kunnen deze waarden niet wijzigen.

>[!CAUTION]
>
>**De** Grootte van de resultaten en de Minimumlengte van de  **Term van het Onderzoek** kunnen prestaties beïnvloeden als zij, respectievelijk te hoog of te laag worden geplaatst.

### Tabblad Stijlen {#styles-tab}

De Snelle Component van het Onderzoek steunt het AEM [Systeem van de Stijl](/help/get-started/authoring.md#component-styling).
