---
title: Taalnavigatie-component
description: De component Taalnavigatie biedt een taal-/landnavigatie voor een site, zodat bezoekers naar dezelfde pagina in een andere landinstelling kunnen navigeren.
role: Architect, Developer, Admin, User
exl-id: 10b218b4-c439-4a0f-a46f-0b15d78b0360
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---


# Taalnavigatie-component{#language-navigation-component}

De taalnavigatiecomponent biedt een taal-/landnavigatie voor een site, zodat bezoekers naar dezelfde pagina in een andere landinstelling kunnen navigeren.

{{traditional-aem}}

## Gebruik {#usage}

Websites worden vaak in meerdere talen aangeboden voor verschillende gebieden. Met de taalnavigatiecomponent kan een bezoeker dezelfde pagina in verschillende talen/landinstellingen bekijken. Dus als je een lezer bent op de Zwitserse Duitse versie van de website, kun je gemakkelijk overschakelen naar de Engelse versie van de Verenigde Staten van dezelfde pagina. Met de component Taalnavigatie krijgt u inzicht in de taalstructuur van de site en wordt de bijbehorende pagina automatisch gevonden.

* Voor een voorbeeld van hoe de localisatieeigenschap van de Component van de Navigatie van de Taal werkt, zie [&#x200B; de sectie hieronder &#x200B;](#example).
* Voor een voorbeeld van hoe de localisatieeigenschappen van de andere Componenten van de Kern samenwerken, zie de [&#x200B; Eigenschappen van de Locatie van de pagina van de Componenten van de Kern &#x200B;](/help/get-started/localization.md).

Het [&#x200B; geeft dialoog &#x200B;](#edit-dialog) uit staat de definitie van de globale wortel van de plaatsnavigatie evenals toe hoe diep in de structuur de navigatie zou moeten gaan. Gebruikend de [&#x200B; ontwerpdialoog &#x200B;](#design-dialog), kan de malplaatjeauteur de standaardwaarden voor de zelfde opties plaatsen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de taalnavigatiecomponent is v2, die in februari 2022 is geïntroduceerd met versie 2.18.0 van de kerncomponenten en in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | - | Compatibel | Compatibel | Compatibel |
| [&#x200B; v1 &#x200B;](v1/language-navigation.md) | Compatibel | Compatibel | - | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [&#x200B; Kern &#x200B;](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Navigatie van de Taal te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [&#x200B; Bibliotheek van de Component &#x200B;](https://adobe.com/go/aem_cmp_library_langnav).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Navigatie van de Taal [&#x200B; kan op GitHub &#x200B;](https://adobe.com/go/aem_cmp_tech_langnav_v2) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [&#x200B; de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden &#x200B;](/help/developing/overview.md).

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kunt u de globale hoofdmap voor sitenavigatie definiëren en aangeven hoe diep de structuur van de navigatie in moet gaan.

Doorgaans hoeven deze configuraties alleen op paginasjabloonniveau te worden uitgevoerd. Nochtans, kunnen zij op het paginaniveau via [&#x200B; worden veranderd uitgeeft dialoog &#x200B;](#edit-dialog).

### Tabblad Eigenschappen {#properties-tab}

{het ontwerpdialoog van de Component van de Navigatie van 0} Taal ![&#128279;](/help/assets/language-navigation-design.png)

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

Met de **waarde van de Root van de Navigatie 0&rbrace;, weet de Component van de Taal dat na `/content/wknd` dat de navigatie begint en het taalnavigatieopties kan produceren door de volgende twee niveaus in de inhoudsboom als de taalnavigatiestructuur van de plaats (zoals die door de** waarde van de Diepte van de Structuur van de Taal **wordt bepaald) te erkennen.**

Ongeacht welke pagina een gebruiker bekijkt, kan de component van de Navigatie van de Taal de overeenkomstige pagina in een andere taal vinden, door de plaats van de huidige pagina te kennen en achterwaarts aan de wortel te werken, en dan door:sturen aan de overeenkomstige pagina.

### Tabblad Stijlen {#styles-tab}

De component van de Navigatie van de Taal steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Dialoogvenster Bewerken {#edit-dialog}

### Tabblad Eigenschappen {#properties-tab-edit}

Doorgaans hoeft de component Taalnavigatie alleen aan de paginasjablonen van een site te worden toegevoegd en geconfigureerd. Nochtans als de component van de Navigatie van de Taal aan een individuele inhoudspagina moet worden toegevoegd, geeft dialoog een inhoudsauteur toe om de zelfde waarden te vormen zoals die in de [&#x200B; ontwerpdialoog &#x200B;](#design-dialog) worden beschreven

Bovendien kunt u een **identiteitskaart** plaatsen. Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [&#x200B; Laag van Gegevens &#x200B;](/help/developing/data-layer/overview.md) te controleren.

* Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
* Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
* Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

{de Component van de Navigatie van 0} Taal geeft dialoog uit ![&#128279;](/help/assets/language-navigation-edit.png)

### Tabblad Toegankelijkheid {#accessibility-tab}

* **Etiket** - Deze optie zou moeten worden bepaald als er meer dan één taalnavigatie op de pagina is om de aria etiketattributen van de component te plaatsen.

![&#x200B; Toegankelijkheid tabel van de Navigatie van de Taal &#x200B;](/help/assets/language-navigation-edit-accessibility.png)

### Tabblad Stijlen {#styles-tab-edit}

De Component van de Navigatie van de Taal steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [&#x200B; ontwerpdialoog &#x200B;](#design-dialog) worden gevormd opdat het drop-down menu beschikbaar is.

![&#x200B; Stijlen lusje van uitgeeft dialoog van de Component van de Navigatie van de Taal &#x200B;](/help/assets/language-navigation-edit-styles.png)

## Adobe Client Data Layer {#data-layer}

De Component van de Navigatie van de Taal steunt de [&#x200B; Gegevens van de Cliënt van Adobe Laag.](/help/developing/data-layer/overview.md)
