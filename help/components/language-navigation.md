---
title: Taalnavigatie-component
description: De component Taalnavigatie biedt een taal-/landnavigatie voor een site, zodat bezoekers naar dezelfde pagina in een andere landinstelling kunnen navigeren.
role: Architect, Developer, Admin, User
exl-id: 10b218b4-c439-4a0f-a46f-0b15d78b0360
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 1%

---

# Taalnavigatie-component{#language-navigation-component}

De taalnavigatiecomponent biedt een taal-/landnavigatie voor een site, zodat bezoekers naar dezelfde pagina in een andere landinstelling kunnen navigeren.

## Gebruik {#usage}

Websites worden vaak in meerdere talen aangeboden voor verschillende regio&#39;s. Met de taalnavigatiecomponent kan een bezoeker dezelfde pagina in verschillende talen/landinstellingen bekijken. Dus als je een lezer bent op de Zwitserse Duitse versie van de website, kun je gemakkelijk overschakelen naar de Engelse versie van de Verenigde Staten van dezelfde pagina. Met de component Taalnavigatie krijgt u inzicht in de taalstructuur van de site en wordt de bijbehorende pagina automatisch gevonden.

* Zie [de sectie hieronder](#example) voor een voorbeeld van hoe de lokalisatiefunctie van de taalnavigatie-component werkt.
* Voor een voorbeeld van hoe de localisatiefuncties van de andere Componenten van de Kern samenwerken, zie [Localisatiefuncties van de pagina van de Componenten van de Kern](/help/get-started/localization.md).

Met het dialoogvenster [Bewerken](#edit-dialog) kunt u de globale hoofdmap voor sitenavigatie definiëren en aangeven hoe diep de structuur van de navigatie moet zijn. Met behulp van het [ontwerpdialoogvenster](#design-dialog) kan de sjabloonauteur de standaardwaarden voor dezelfde opties instellen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de taalnavigatiecomponent is v1, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de kerncomponenten en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_langnav) om de taalnavigatiecomponent te bekijken en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Navigatie van de Taal [kan op GitHub](https://adobe.com/go/aem_cmp_tech_langnav_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Bewerken kunt u de globale hoofdmap voor sitenavigatie definiëren en aangeven hoe diep de structuur van de navigatie in moet gaan.

Doorgaans hoeven deze configuraties alleen op paginasjabloonniveau te worden uitgevoerd. Ze kunnen echter wel op paginaniveau worden gewijzigd via het dialoogvenster [bewerken](#edit-dialog).

### Tabblad Eigenschappen {#properties-tab}

![Ontwerpdialoogvenster taalnavigatie-component](/help/assets/language-navigation-design.png)

* **Navigatieroot**
   * Hier moet de taalnavigatie van de site worden gestart.
   * De taalstructuur van de site begint op het volgende niveau onder deze hoofdmap.
* **Diepte taalstructuur**
   * Dit is hoeveel niveaus van de inhoudsstructuur onder **Navigatieroot** de taalstructuur van de site vertegenwoordigen. Voorbeelden:
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

Voor de plaats WKND, zou u waarschijnlijk de component van de Navigatie van de Taal op een paginamalplaatje als deel van de kopbal willen plaatsen. Als een onderdeel van de sjabloon is gemaakt, kunt u de **Navigation Root** van de component instellen op `/content/wknd`, aangezien dat het begin is van de gelokaliseerde inhoud voor die site. U zou ook **Taalstructuurdiepte** willen plaatsen om `2` te zijn aangezien uw structuur van twee niveaus (land toen taal) is.

Met de waarde **Navigation Root** weet de taalcomponent dat nadat `/content/wknd` dat de navigatie begint en het taalnavigatieopties kan produceren door de volgende twee niveaus in de inhoudsstructuur te erkennen als de taalnavigatiestructuur van de site (zoals bepaald door de waarde **Taalstructuurdiepte**).

Ongeacht welke pagina een gebruiker bekijkt, kan de component van de Navigatie van de Taal de overeenkomstige pagina in een andere taal vinden, door de plaats van de huidige pagina te kennen en achterwaarts aan de wortel te werken, en dan door:sturen aan de overeenkomstige pagina.

### Tabblad Stijlen {#styles-tab}

De component van de Navigatie van de Taal steunt het AEM [Systeem van de Stijl](/help/get-started/authoring.md#component-styling).

## Dialoogvenster Bewerken {#edit-dialog}

Doorgaans hoeft de component Taalnavigatie alleen aan de paginasjablonen van een site te worden toegevoegd en geconfigureerd. Als de component Taalnavigatie echter moet worden toegevoegd aan een afzonderlijke inhoudspagina, kan het dialoogvenster voor bewerken een auteur van de inhoud dezelfde waarden configureren als in het ontwerpdialoogvenster [a1/> worden beschreven.](#design-dialog)

Daarnaast kunt u een **ID** instellen. Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).

* Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
* Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
* Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

![Dialoogvenster Taalnavigatie-component bewerken](/help/assets/language-navigation-edit.png)

## Gegevenslaag Adobe-client {#data-layer}

De component van de Navigatie van de Taal steunt [de Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
