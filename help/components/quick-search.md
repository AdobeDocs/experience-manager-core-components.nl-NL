---
title: Component Snel zoeken
description: De component Snel zoeken biedt zoekmogelijkheden voor een website en biedt zoekresultaten zodat bezoekers de site kunnen doorzoeken en de resultaten kunnen filteren.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 1%

---


# Component Snel zoeken {#quick-search-component}

De component Snel zoeken biedt zoekmogelijkheden voor een website en biedt zoekresultaten zodat bezoekers gemakkelijk overeenkomende inhoud kunnen vinden en de resultaten kunnen bekijken.

## Gebruik {#usage}

Met de component Snel zoeken kunnen sitebezoekers naar inhoud zoeken, de resultaten op hun plaats bekijken en eenvoudig naar de overeenkomende pagina&#39;s navigeren. Nieuwe resultaten worden dynamisch opgehaald terwijl de gebruiker door de zoekresultaten schuift.

In het dialoogvenster [](#edit-dialog) Bewerken kan de auteur van de inhoud bepalen waar in de inhoudsstructuur de zoekopdracht moet beginnen. Met behulp van het dialoogvenster [](#design-dialog)Ontwerp kan de sjabloonauteur de standaardwaarde instellen voor de plaats in de inhoudsstructuur waar de zoekopdracht moet beginnen, en ook een maximale grootte en minimale lengte voor de zoekterm.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Snelle component van het Onderzoek is v1, die met versie 2.0.0 van de Componenten van de Kern in Januari 2018 werd geïntroduceerd, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel | Compatibel | Compatibel |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

### Technische details {#technical-details}

>[!NOTE]
>
>Het beschermen van de Component van het Onderzoek of om het even welke op AEM gebaseerde toepassing tegen DOS aanvallen zou op een hoger niveau moeten worden uitgevoerd, bijvoorbeeld door `mod_security` op de verzender te gebruiken.

De recentste technische documentatie over de Snelle Component van het Onderzoek [kan op GitHub](https://adobe.com/go/aem_cmp_tech_search_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud definiëren waar in de inhoudsstructuur de zoekopdracht moet beginnen.

![Dialoogvenster Snel zoeken in component bewerken](/help/assets/quick-search-edit.png)

**Hoofdmap** zoeken - De hoofdpagina vanaf waar de zoekopdracht moet worden gestart. De hoofdmap van de zoekopdracht kan een standaardpagina of een hoofdstramien voor de blauwdruk zijn.
* **ID** - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

Met behulp van het ontwerpdialoogvenster kan de sjabloonauteur de standaardwaarde instellen voor de plaats in de inhoudsstructuur waar de zoekopdracht moet beginnen, alsmede een maximale grootte voor de resultaatset en een minimale lengte voor de zoekterm. In het dialoogvenster Ontwerp kan de sjabloonauteur definiëren welke opties voor tekstopmaak beschikbaar zijn voor de auteurs van de inhoud.

### Tabblad Eigenschappen {#properties-tab}

![Het ontwerpdialoogvenster van de component Snel zoeken](/help/assets/quick-search-design.png)

* **Hoofdmap** zoeken De standaardwaarde van de zoekhoofdmap wanneer een auteur van inhoud de component Snel zoeken op een inhoudspagina plaatst
* **Grootte** van resultaten Het maximum aantal resultaten dat door een onderzoeksverzoek wordt gehaald
* **Zoektermijn Minimale lengte** minimumlengte van zoekterm om de zoekopdracht te starten

>[!NOTE]
>
>**Grootte** van resultaten en Minimumlengte **van** zoektermen kunnen alleen worden ingesteld in de ontwerpmodus en daarom alleen op sjabloonniveau. Dit betekent dat auteurs van inhoud deze waarden niet kunnen wijzigen.

>[!CAUTION]
>
>**Grootte** van resultaten en Minimumlengte **van** zoekterm kunnen prestatieeffecten hebben als deze te hoog of te laag zijn ingesteld.

### Tabblad Stijlen {#styles-tab}

De component Snel zoeken ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).
