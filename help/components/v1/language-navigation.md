---
title: Taalnavigatiecomponent (v1)
description: De component Taalnavigatie biedt een taal-/landnavigatie voor een site, zodat bezoekers naar dezelfde pagina in een andere landinstelling kunnen navigeren.
role: Architect, Developer, Admin, User
exl-id: 41194ba0-6833-40e5-88d9-036e9c231edd
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---

# Taalnavigatiecomponent (v1) {#language-navigation-component}

De taalnavigatiecomponent biedt een taal-/landnavigatie voor een site, zodat bezoekers naar dezelfde pagina in een andere landinstelling kunnen navigeren.

## Gebruik {#usage}

Websites worden vaak in meerdere talen aangeboden voor verschillende regio&#39;s. Met de taalnavigatiecomponent kan een bezoeker dezelfde pagina in verschillende talen/landinstellingen bekijken. Dus als je een lezer bent op de Zwitserse Duitse versie van de website, kun je gemakkelijk overschakelen naar de Engelse versie van de Verenigde Staten van dezelfde pagina. Met de component Taalnavigatie krijgt u inzicht in de taalstructuur van de site en wordt de bijbehorende pagina automatisch gevonden.

* Voor een voorbeeld van hoe de lokalisatiefunctie van de Component van de Navigatie van de Taal werkt, zie [het onderstaande gedeelte](#example).
* Voor een voorbeeld van hoe de lokalisatiefuncties van de andere Core Components samenwerken, zie [Localisatiefuncties van de pagina Core Components](/help/get-started/localization.md).

De [dialoogvenster bewerken](#edit-dialog) Hiermee kunt u de globale hoofdmap voor sitenavigatie definiëren en aangeven hoe diep de structuur van de navigatie moet zijn. Met de [ontwerpdialoogvenster](#design-dialog)kan de sjabloonauteur de standaardwaarden voor dezelfde opties instellen.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de taalnavigatiecomponent beschreven, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de kerncomponenten.

>[!CAUTION]
>
>In dit document wordt versie 1 van de taalnavigatiecomponent beschreven.
>
>Zie voor meer informatie over de huidige versie van de taalnavigatiecomponent de sectie [Taalnavigatie-component](/help/components/language-navigation.md) document.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de taalnavigatiecomponent wilt ervaren en voorbeelden wilt zien van de configuratieopties en de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_langnav).

## Technische details {#technical-details}

De meest recente technische documentatie over de taalnavigatiecomponent [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_langnav_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Bewerken kunt u de globale hoofdmap voor sitenavigatie definiëren en aangeven hoe diep de structuur van de navigatie in moet gaan.

Doorgaans hoeven deze configuraties alleen op paginasjabloonniveau te worden uitgevoerd. Deze kunnen echter op paginaniveau worden gewijzigd via de [dialoogvenster bewerken](#edit-dialog).

### Tabblad Eigenschappen {#properties-tab}

![Ontwerpdialoogvenster taalnavigatie-component](/help/assets/language-navigation-design.png)

* **Navigatieroot**
   * Hier moet de taalnavigatie van de site worden gestart.
   * De taalstructuur van de site begint op het volgende niveau onder deze hoofdmap.
* **Diepte taalstructuur**
   * Dit is het aantal niveaus van de inhoudsstructuur onder de **Navigatieroot** de taalstructuur van de site weergeven. Voorbeelden:
      * `1` doorgaans betekent dit dat u alleen de taal kunt kiezen.
      * `2` doorgaans betekent dit dat u een keuze hebt tussen taal en land.
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

Voor de plaats WKND, zou u waarschijnlijk de component van de Navigatie van de Taal op een paginamalplaatje als deel van de kopbal willen plaatsen. Als een deel van de sjabloon is gemaakt, kunt u de **Navigatieroot** van de component `/content/wknd` aangezien dat de plaats is waar uw gelokaliseerde inhoud voor die plaats begint. U wilt ook de opdracht **Diepte taalstructuur** te worden `2` omdat uw structuur op twee niveaus ligt ( land en taal ) .

Met de **Navigatieroot** waarde, de Component van de Taal weet dat na `/content/wknd` dat de navigatie begint en taalnavigatieopties kan genereren door de volgende twee niveaus in de inhoudsstructuur te herkennen als de taalnavigatiestructuur van de site (zoals gedefinieerd door de **Diepte taalstructuur** waarde).

Ongeacht welke pagina een gebruiker bekijkt, kan de component van de Navigatie van de Taal de overeenkomstige pagina in een andere taal vinden, door de plaats van de huidige pagina te kennen en achterwaarts aan de wortel te werken, en dan door:sturen aan de overeenkomstige pagina.

### Tabblad Stijlen {#styles-tab}

De taalnavigatiecomponent ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Dialoogvenster Bewerken {#edit-dialog}

Doorgaans hoeft de component Taalnavigatie alleen aan de paginasjablonen van een site te worden toegevoegd en geconfigureerd. Als de component Taalnavigatie echter moet worden toegevoegd aan een afzonderlijke inhoudspagina, kan het dialoogvenster voor bewerken een auteur van de inhoud dezelfde waarden configureren als in het dialoogvenster [ontwerpdialoogvenster](#design-dialog).

Bovendien kunt u een **ID**. Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).

* Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
* Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
* Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

![Dialoogvenster Taalnavigatie-component bewerken](/help/assets/language-navigation-edit.png)

## Gegevenslaag Adobe-client {#data-layer}

De taalnavigatiecomponent ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
