---
title: Taalnavigatie-component
description: De component Taalnavigatie biedt een taal-/landnavigatie voor een site, zodat bezoekers naar dezelfde pagina in een andere landinstelling kunnen navigeren.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 1%

---


# Taalnavigatie-component{#language-navigation-component}

De taalnavigatiecomponent biedt een taal-/landnavigatie voor een site, zodat bezoekers naar dezelfde pagina in een andere landinstelling kunnen navigeren.

## Gebruik {#usage}

Websites worden vaak in meerdere talen aangeboden voor verschillende regio&#39;s. Met de taalnavigatiecomponent kan een bezoeker dezelfde pagina in verschillende talen/landinstellingen bekijken. Dus als je een lezer bent op de Zwitserse Duitse versie van de website, kun je gemakkelijk overschakelen naar de Engelse versie van de Verenigde Staten van dezelfde pagina. Met de component Taalnavigatie krijgt u inzicht in de taalstructuur van de site en wordt de bijbehorende pagina automatisch gevonden.

* Zie [de onderstaande](#example)sectie voor een voorbeeld van de werking van de lokalisatiefunctie van de taalnavigatiecomponent.
* Zie de [lokalisatiefuncties van de pagina](/help/get-started/localization.md)Core Components voor een voorbeeld van hoe de lokalisatiefuncties van de andere Core Components samenwerken.

In het dialoogvenster [](#edit-dialog) Bewerken kunt u de globale hoofdmap voor sitenavigatie definiëren en aangeven hoe diep de structuur van de navigatie in moet gaan. In het dialoogvenster [](#design-dialog)Ontwerp kan de sjabloonauteur de standaardwaarden voor dezelfde opties instellen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de taalnavigatiecomponent is v1, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de kerncomponenten en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel | Compatibel | Compatibel |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_langnav)voor meer informatie over de taalnavigatiecomponent en voorbeelden van de bijbehorende configuratieopties en over HTML- en JSON-uitvoer.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Navigatie van de Taal [kan op GitHub](https://adobe.com/go/aem_cmp_tech_langnav_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Bewerken kunt u de globale hoofdmap voor sitenavigatie definiëren en aangeven hoe diep de structuur van de navigatie in moet gaan.

Doorgaans hoeven deze configuraties alleen op paginasjabloonniveau te worden uitgevoerd. Deze kunnen echter wel op paginaniveau worden gewijzigd via het dialoogvenster [](#edit-dialog)Bewerken.

### Tabblad Eigenschappen {#properties-tab}

![Ontwerpdialoogvenster taalnavigatie-component](/help/assets/language-navigation-design.png)

* **Navigatieroot**
   * Hier moet de taalnavigatie van de site worden gestart.
   * De taalstructuur van de site begint op het volgende niveau onder deze hoofdmap.
* **Diepte taalstructuur**
   * Dit is het aantal niveaus van de inhoudsstructuur onder de **navigatieroot** dat de taalstructuur van de site vertegenwoordigt. Voorbeelden:
      * `1` doorgaans betekent dit dat u alleen de taal kunt kiezen.
      * `2` doorgaans betekent dit dat u een keuze hebt tussen taal en land.
      * `3` betekent doorgaans dat u een keuze hebt uit taal, land en regio.

#### Voorbeeld {#example}

Laten we zeggen dat de inhoud er zo uitziet:

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

Voor de plaats WKND, zou u waarschijnlijk de component van de Navigatie van de Taal op een paginamalplaatje als deel van de kopbal willen plaatsen. Als een onderdeel van de sjabloon is gemaakt, kunt u de **navigatieroot** van de component instellen op `/content/wknd` aangezien dat het begin is van de gelokaliseerde inhoud voor die site. U wilt ook de **taalstructuurdiepte** instellen `2` omdat uw structuur op twee niveaus ligt (land en taal).

Met de waarde van de **Basis** van de Navigatie, weet de Component van de Taal dat na `/content/wknd` dat de navigatie begint en het taalnavigatieopties kan produceren door de volgende twee niveaus in de inhoudsboom als de taalnavigatiestructuur van de plaats (zoals die door de waarde van de Diepte **van de Structuur van de** Taal wordt bepaald) te erkennen.

Ongeacht welke pagina een gebruiker bekijkt, kan de component van de Navigatie van de Taal de overeenkomstige pagina in een andere taal vinden, door de plaats van de huidige pagina te kennen en achterwaarts aan de wortel te werken, en dan door:sturen aan de overeenkomstige pagina.

### Tabblad Stijlen {#styles-tab}

De taalnavigatiecomponent ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).

## Dialoogvenster Bewerken {#edit-dialog}

Doorgaans hoeft de component Taalnavigatie alleen aan de paginasjablonen van een site te worden toegevoegd en geconfigureerd. Als de component Taalnavigatie echter moet worden toegevoegd aan een afzonderlijke inhoudspagina, kan het dialoogvenster Bewerken een auteur van de inhoud dezelfde waarden configureren als in het [ontwerpdialoogvenster](#design-dialog)worden beschreven.

Bovendien kunt u een **id** instellen. Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [gegevenslaag](/help/developing/data-layer/overview.md).

* Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
* Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
* Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

![Dialoogvenster Taalnavigatie-component bewerken](/help/assets/language-navigation-edit.png)
