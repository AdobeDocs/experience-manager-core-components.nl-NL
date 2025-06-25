---
title: Component Snel zoeken (v1)
description: De component Snel zoeken biedt zoekmogelijkheden voor een website en biedt zoekresultaten zodat bezoekers de site kunnen doorzoeken en de resultaten kunnen filteren.
role: Architect, Developer, Admin, User
exl-id: 60a043b7-d82c-4bc1-b91a-b77f748f7bc2
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---


# Component Snel zoeken (v1) {#quick-search-component}

De component Snel zoeken biedt zoekmogelijkheden voor een website en biedt zoekresultaten zodat bezoekers gemakkelijk overeenkomende inhoud kunnen vinden en de resultaten kunnen bekijken.

## Gebruik {#usage}

Met de component Snel zoeken kunnen sitebezoekers naar inhoud zoeken, de resultaten op hun plaats bekijken en eenvoudig naar de overeenkomende pagina&#39;s navigeren. Nieuwe resultaten worden dynamisch opgehaald terwijl de gebruiker door de zoekresultaten schuift.

Het [ geeft dialoog uit ](#edit-dialog) staat de inhoudauteur toe om te bepalen waar in de inhoudsboom het onderzoek zou moeten beginnen. Gebruikend de [ ontwerpdialoog ](#design-dialog), kan de malplaatjeauteur de standaardwaarde voor plaatsen waar in de inhoudsboom het onderzoek evenals een maximumresultaatvastgestelde grootte en minimumlengte van de onderzoekstermijn zou moeten beginnen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Snelle component van het Onderzoek is v1, die met versie 2.0.0 van de Componenten van de Kern in Januari 2018 werd geïntroduceerd, en in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel systeem met <br>[ versie 2.17.4 ](/help/versions.md) en vroeger | Compatibel | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de Quick Search-component beschreven.
>&#x200B;>Voor details van de huidige versie van de Snelle Component van het Onderzoek, zie het [ Snelle document van de Component van het Onderzoek ](/help/components/quick-search.md).

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

### Technische details {#technical-details}

>[!NOTE]
>
>De component Search of een op AEM gebaseerde toepassing beschermen tegen DOS-aanvallen moet op een hoger niveau worden geïmplementeerd, bijvoorbeeld door `mod_security` op de dispatcher te gebruiken.

De recentste technische documentatie over de Snelle Component van het Onderzoek [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_search_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud definiëren waar in de inhoudsstructuur de zoekopdracht moet beginnen.

![ Snelle component van het Onderzoek geeft dialoog uit ](/help/assets/quick-search-edit.png)

**Wortel van het Onderzoek** - de wortelpagina van waar te om het onderzoek te beginnen. De hoofdmap van de zoekopdracht kan een standaardpagina of een hoofdstramien voor de blauwdruk zijn.
* **identiteitskaart** - Deze optie staat controle van het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens toe.](/help/developing/data-layer/overview.md)
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

>[!NOTE]
>
>Als de **Wortel van het Onderzoek** niet wordt gevormd of niet kan worden opgelost, blijft het Snelle Onderzoek aan het zoeken onder de huidige pagina in gebreke.

## Ontwerpdialoogvenster {#design-dialog}

Met behulp van het ontwerpdialoogvenster kan de sjabloonauteur de standaardwaarde instellen voor de plaats in de inhoudsstructuur waar de zoekopdracht moet beginnen, alsmede een maximale grootte voor de resultaatset en een minimale lengte voor de zoekterm. In het dialoogvenster Ontwerp kan de sjabloonauteur definiëren welke opties voor tekstopmaak beschikbaar zijn voor de auteurs van de inhoud.

### Tabblad Eigenschappen {#properties-tab}

![ Snelle het ontwerpdialoog van de Component van het Onderzoek van het Snelle ](/help/assets/quick-search-design.png)

* **Wortel van het Onderzoek**
De standaardwaarde van zoekroot wanneer een inhoudsontwerper de component Snel zoeken op een inhoudspagina plaatst
* **Grootte van Resultaten**
Het maximumaantal resultaten dat wordt opgehaald door een zoekaanvraag
* **Term Minimale Lengte van het Onderzoek**
Minimale lengte van de zoekterm om de zoekopdracht te starten

>[!NOTE]
>
>**Grootte van Resultaten** en **de Minimale Lengte van het Onderzoek van de Term** kan slechts op ontwerpwijze en daarom slechts op het malplaatjeniveau worden geplaatst, betekenend inhoudsauteurs kunnen deze waarden niet wijzigen.

>[!CAUTION]
>
>**Grootte van Resultaten** en **de Minimale Lengte van het Onderzoek van de Term** kan prestatiesgevolgen hebben als zij te hoog of te laag, respectievelijk worden geplaatst.

### Tabblad Stijlen {#styles-tab}

De Snelle Component van het Onderzoek steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).
