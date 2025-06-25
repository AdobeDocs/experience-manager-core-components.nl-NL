---
title: Taalnavigatiecomponent (v1)
description: De component Taalnavigatie biedt een taal-/landnavigatie voor een site, zodat bezoekers naar dezelfde pagina in een andere landinstelling kunnen navigeren.
role: Architect, Developer, Admin, User
exl-id: 41194ba0-6833-40e5-88d9-036e9c231edd
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 0%

---


# Taalnavigatiecomponent (v1) {#language-navigation-component}

De taalnavigatiecomponent biedt een taal-/landnavigatie voor een site, zodat bezoekers naar dezelfde pagina in een andere landinstelling kunnen navigeren.

## Gebruik {#usage}

Websites worden vaak in meerdere talen aangeboden voor verschillende gebieden. Met de taalnavigatiecomponent kan een bezoeker dezelfde pagina in verschillende talen/landinstellingen bekijken. Dus als je een lezer bent op de Zwitserse Duitse versie van de website, kun je gemakkelijk overschakelen naar de Engelse versie van de Verenigde Staten van dezelfde pagina. Met de component Taalnavigatie krijgt u inzicht in de taalstructuur van de site en wordt de bijbehorende pagina automatisch gevonden.

* Voor een voorbeeld van hoe de localisatieeigenschap van de Component van de Navigatie van de Taal werkt, zie [ de sectie hieronder ](#example).
* Voor een voorbeeld van hoe de localisatieeigenschappen van de andere Componenten van de Kern samenwerken, zie de [ Eigenschappen van de Locatie van de pagina van de Componenten van de Kern ](/help/get-started/localization.md).

Het [ geeft dialoog ](#edit-dialog) uit staat de definitie van de globale wortel van de plaatsnavigatie evenals toe hoe diep in de structuur de navigatie zou moeten gaan. Gebruikend de [ ontwerpdialoog ](#design-dialog), kan de malplaatjeauteur de standaardwaarden voor de zelfde opties plaatsen.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de taalnavigatiecomponent beschreven, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de kerncomponenten.

>[!CAUTION]
>
>In dit document wordt versie 1 van de taalnavigatiecomponent beschreven.
>
>Voor details van de huidige versie van de Component van de Navigatie van de Taal, zie het ](/help/components/language-navigation.md) document van de Component van de Navigatie van 0} Taal.[

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Navigatie van de Taal te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_langnav).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Navigatie van de Taal [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_langnav_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Bewerken kunt u de globale hoofdmap voor sitenavigatie definiëren en aangeven hoe diep de structuur van de navigatie in moet gaan.

Doorgaans hoeven deze configuraties alleen op paginasjabloonniveau te worden uitgevoerd. Nochtans, kunnen zij op het paginaniveau via [ worden veranderd uitgeeft dialoog ](#edit-dialog).

### Tabblad Eigenschappen {#properties-tab}

{het ontwerpdialoog van de Component van de Navigatie van 0} Taal ](/help/assets/language-navigation-design.png)![

* **Basis van de Navigatie**
   * Hier moet de taalnavigatie van de site worden gestart.
   * De taalstructuur van de site begint op het volgende niveau onder deze hoofdmap.
* **Diepte van de Structuur van de Taal**
   * Dit is hoeveel niveaus van de inhoudsboom onder de **Wortel van de Navigatie** de taalstructuur van de plaats vertegenwoordigen. Voorbeelden:
      * `1` betekent doorgaans dat u alleen de taal kunt kiezen.
      * `2` betekent doorgaans dat u een taal- en landkeuze hebt.
      * `3` betekent doorgaans dat u een keuze hebt uit taal, land en regio.

#### Voorbeeld {#example}

Laten we zeggen dat uw inhoud er ongeveer als volgt uitziet:

```
/content
+-- wknd
   +-- language-masters
   +-- us
      +-- en
      \-- es
   \-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Voor de plaats WKND, zou u waarschijnlijk de component van de Navigatie van de Taal op een paginamalplaatje als deel van de kopbal willen plaatsen. Zodra een deel van het malplaatje, kunt u de **Wortel van de Navigatie** van de component aan `/content/wknd` plaatsen aangezien dat is waar uw gelokaliseerde inhoud voor die plaats begint. U zou ook de **Diepte van de Structuur van de Taal** willen plaatsen om `2` te zijn aangezien uw structuur van twee niveaus (land toen taal) is.

Met de **waarde van de Root van de Navigatie 0}, weet de Component van de Taal dat na `/content/wknd` dat de navigatie begint en het taalnavigatieopties kan produceren door de volgende twee niveaus in de inhoudsboom als de taalnavigatiestructuur van de plaats (zoals die door de** waarde van de Diepte van de Structuur van de Taal **wordt bepaald) te erkennen.**

Ongeacht welke pagina een gebruiker bekijkt, kan de component van de Navigatie van de Taal de overeenkomstige pagina in een andere taal vinden, door de plaats van de huidige pagina te kennen en achterwaarts aan de wortel te werken, en dan door:sturen aan de overeenkomstige pagina.

### Tabblad Stijlen {#styles-tab}

De component van de Navigatie van de Taal steunt het Systeem van de Stijl van AEM [ ](/help/get-started/authoring.md#component-styling).

## Dialoogvenster Bewerken {#edit-dialog}

Doorgaans hoeft de component Taalnavigatie alleen aan de paginasjablonen van een site te worden toegevoegd en geconfigureerd. Nochtans als de component van de Navigatie van de Taal aan een individuele inhoudspagina moet worden toegevoegd, geeft dialoog een inhoudauteur toe om de zelfde waarden te vormen zoals die in de [ ontwerpdialoog ](#design-dialog) worden beschreven.

Bovendien kunt u een **identiteitskaart** plaatsen. Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens ](/help/developing/data-layer/overview.md) te controleren.

* Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
* Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
* Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

{de Component van de Navigatie van 0} Taal geeft dialoog uit ](/help/assets/language-navigation-edit.png)![

## Adobe Client Data Layer {#data-layer}

De Component van de Navigatie van de Taal steunt de [ Gegevens van de Cliënt van Adobe Laag.](/help/developing/data-layer/overview.md)
