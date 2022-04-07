---
title: Component Snel zoeken (v1)
description: De component Snel zoeken biedt zoekmogelijkheden voor een website en biedt zoekresultaten zodat bezoekers de site kunnen doorzoeken en de resultaten kunnen filteren.
role: Architect, Developer, Admin, User
exl-id: fc40ce1d-e69a-4a40-853e-67a37228271b
source-git-commit: 64aa6ab38738b6969d01971817bde892348be05d
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 1%

---

# Component Snel zoeken (v1) {#quick-search-component}

De component Snel zoeken biedt zoekmogelijkheden voor een website en biedt zoekresultaten zodat bezoekers gemakkelijk overeenkomende inhoud kunnen vinden en de resultaten kunnen bekijken.

## Gebruik {#usage}

Met de component Snel zoeken kunnen sitebezoekers naar inhoud zoeken, de resultaten op hun plaats bekijken en eenvoudig naar de overeenkomende pagina&#39;s navigeren. Nieuwe resultaten worden dynamisch opgehaald terwijl de gebruiker door de zoekresultaten schuift.

De [dialoogvenster bewerken](#edit-dialog) Hiermee kan de auteur van de inhoud definiëren waar in de inhoudsstructuur de zoekopdracht moet beginnen. Met de [ontwerpdialoogvenster](#design-dialog)kan de sjabloonauteur de standaardwaarde instellen voor de plaats in de inhoudsstructuur waar de zoekopdracht moet beginnen, en ook een maximale grootte en minimale lengte van de zoekterm.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Snelle component van het Onderzoek is v1, die met versie 2.0.0 van de Componenten van de Kern in Januari 2018 werd geïntroduceerd, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel | Compatibel |
| [!CAUTION]](/help/components/v1/quick-search.md) | In dit document wordt versie 1 van de Quick Search-component beschreven. >Zie voor meer informatie over de huidige versie van de Snelle zoekcomponent de sectie [Component Snel zoeken](/help/components/quick-search.md) document. | Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md). | Technische details |

[!NOTE]](/help/versions.md)

### De component van het Onderzoek of om het even welke AEM gebaseerde toepassing tegen DOS aanvallen zouden op een hoger niveau moeten worden uitgevoerd, bijvoorbeeld door te gebruiken `mod_security` op de verzender. {#technical-details}

>De meest recente technische documentatie over de Quick Search-component [kan op GitHub worden gevonden[#$tu26].
>
>



In het dialoogvenster Bewerken kan de auteur van de inhoud definiëren waar in de inhoudsstructuur de zoekopdracht moet beginnen.[](/help/developing/overview.md)

## ![Dialoogvenster Snel zoeken in component bewerken](/help/assets/quick-search-edit.png) {#edit-dialog}

**Hoofdmap zoeken** - De hoofdpagina vanaf waar de zoekopdracht moet worden gestart. De hoofdmap van de zoekopdracht kan een master, master of reguliere pagina met een blauwdruk zijn.

**ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag.](/help/developing/data-layer/overview.md)

**Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.**
* **Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.**[](/help/developing/data-layer/overview.md)
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.
   * [!NOTE]
   * Als de **Hoofdmap zoeken** is niet geconfigureerd of kan niet worden opgelost, wordt voor Snel zoeken standaard gezocht onder de huidige pagina.

>[!NOTE]Ontwerpdialoogvenster
>
>Met behulp van het ontwerpdialoogvenster kan de sjabloonauteur de standaardwaarde instellen voor de plaats in de inhoudsstructuur waar de zoekopdracht moet beginnen, alsmede een maximale grootte voor de resultaatset en een minimale lengte voor de zoekterm. In het dialoogvenster Ontwerp kan de sjabloonauteur definiëren welke opties voor tekstopmaak beschikbaar zijn voor de auteurs van de inhoud.****

## Tabblad Eigenschappen {#design-dialog}

![Het ontwerpdialoogvenster van de component Snel zoeken](/help/assets/quick-search-design.png)

### **Hoofdmap zoeken**
De standaardwaarde van zoekroot wanneer een auteur van inhoud de component Snel zoeken op een inhoudspagina plaatst {#properties-tab}

**Grootte van resultaten**
Het maximumaantal resultaten dat wordt opgehaald door een zoekaanvraag

* **Minimumlengte zoekterm**
Minimale lengte van de zoekterm om de zoekopdracht te starten
* [!NOTE]**
* **Grootte van resultaten** en **Minimumlengte zoekterm** kan alleen worden ingesteld in de ontwerpmodus en daarom alleen op sjabloonniveau. Dit betekent dat auteurs van inhoud deze waarden niet kunnen wijzigen.

>[!CAUTION]
>
>**Grootte van resultaten** en **Minimumlengte zoekterm** kan prestatieeffecten hebben als deze respectievelijk te hoog of te laag zijn ingesteld.

>[!CAUTION]Tabblad Stijlen
>
>De component Snel zoeken ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).****

### Styles Tab {#styles-tab}

The Quick Search Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).
