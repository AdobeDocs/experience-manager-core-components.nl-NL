---
title: Lijstcomponent (v2)
description: De component van de Lijst van de Component van de Kern staat voor de gemakkelijke verwezenlijking van dynamische en statische lijsten toe.
role: Architect, Developer, Admin, User
exl-id: fa34be64-b345-45cd-baf3-571973414852
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 0%

---


# Lijstcomponent (v2) {#list-component}

De component van de Lijst van de Component van de Kern staat voor de gemakkelijke verwezenlijking van dynamische en statische lijsten toe.

## Gebruik {#usage}

De component List kan worden gebruikt om bijvoorbeeld een dynamische lijst met onderliggende pagina&#39;s of een statische lijst met willekeurig gedefinieerde items te maken. Het type van beschikbare lijsten en het formatteren opties kunnen door de malplaatjeauteur in de [&#x200B; ontwerpdialoog &#x200B;](#design-dialog) worden bepaald. De inhoudsredacteur kan uit beschikbare lijsttypes selecteren en hoe te om de lijstelementen in [&#x200B; uit te maken uitgeeft dialoog &#x200B;](#edit-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de component List beschreven. Deze versie is in januari 2018 geïntroduceerd met versie 2.0.0 van de kerncomponenten.

>[!CAUTION]
>
>In dit document wordt versie 2 van de component List beschreven.
>
>Voor details van de huidige versie van de Component van de Lijst, zie het [&#128279;](/help/components/list.md) document van de Component van de Lijst 0&rbrace; &lbrace;.

## Omleiding in lijsten {#redirects}

Wanneer een pagina een omleidingsdoel heeft (ongeacht of deze naar een externe URL of naar een andere AEM-pagina verwijst), dan een lijst die koppelingen naar dat punt rechtstreeks naar de URL van het omleidingsdoel bevat.

### Voorbeeld {#redirect-example}

* Maak een pagina A die wordt omgeleid naar pagina B.
* Een pagina C maken die wordt omgeleid naar `https://aemcomponents.dev`
* Voeg op een pagina D een lijstcomponent in die pagina A en C bevat
* De respectievelijke koppelingen die worden gegenereerd, verwijzen vervolgens rechtstreeks naar pagina B en `https://aemcomponents.dev`

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Lijst te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [&#x200B; Bibliotheek van de Component &#x200B;](https://adobe.com/go/aem_cmp_library_list).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Lijst [&#x200B; kan op GitHub &#x200B;](https://adobe.com/go/aem_cmp_tech_list_v2) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [&#x200B; de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden &#x200B;](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de lijst en de lijstitems configureren.

### Tabblad Lijstinstellingen {#list-settings-tab}

De lijst kan op verschillende manieren worden samengesteld.

* [Onderliggende pagina&#39;s](#child-pages)
* [Vaste lijst](#fixed-list)
* [Zoeken](#search-options)
* [Tags](#tags)

Ongeacht hoe de lijst wordt gebouwd, zijn er [&#x200B; de Opties van de Soort en van identiteitskaart &#x200B;](#sort-options) die altijd kunnen worden gevormd.

![&#x200B; de Edit dialoog van de Component van de Lijst &#x200B;](/help/assets/v2/list-edit.png)

Afhankelijk van de manier waarop de auteur van de inhoud ervoor kiest de lijst te maken, worden de aanvullende configuratieopties gewijzigd.

#### Onderliggende pagina&#39;s {#child-pages}

De lijst kan van de kindpagina&#39;s van de huidige pagina of een andere pagina worden samengesteld.

![&#x200B; de paginaopties van het Kind &#x200B;](/help/assets/v2/list-edit-child-pages.png)

* **Bovenliggende pagina**
   * De pagina waarvan de onderliggende pagina&#39;s de lijst moeten maken
   * Leeg laten om de huidige pagina te gebruiken

* **kind-diepte**
Hoeveel niveaus onderaan in de hiërarchie zouden moeten worden gebruikt

#### Vaste lijst {#fixed-list}

De lijst kan worden samengesteld met behulp van een vaste lijst met items.

![&#x200B; Vaste lijstopties &#x200B;](/help/assets/v2/list-edit-fixed-list.png)

Tik of klik **voeg** knoop toe om een nieuw punt aan de lijst binnen te brengen.

* Ga tekst voor het punt in de lijst in of gebruik de **Dialoog van de Selectie** om een punt van AEM te kiezen.
* Gebruik de sleepgreep om de items in de lijst opnieuw te rangschikken.
* Gebruik het prullenbakpictogram om items in de lijst te verwijderen.

#### Zoeken {#search-options}

De lijst kan worden samengesteld met behulp van de resultaten van een zoekopdracht naar AEM-inhoud.

![&#x200B; de lijstopties van het Onderzoek &#x200B;](/help/assets/v2/list-edit-search.png)

* **vraag van het Onderzoek**
De tekenreeks waarvoor een zoekopdracht in volledige tekst wordt uitgevoerd om de lijstelementen te genereren
* **Onderzoek in**
Waar de zoekopdracht moet worden uitgevoerd
   * Gebruik de **Dialoog van de Selectie** om de plaats in AEM te kiezen
   * Huidige pagina gebruiken als deze leeg blijft

#### Tags {#tags}

De lijst kan worden samengesteld met pagina&#39;s die overeenkomen met bepaalde codes onder een bepaalde locatie.

![&#x200B; de lijstopties van Markeringen &#x200B;](/help/assets/v2/list-edit-tags.png)

* **Bovenliggende pagina**
Waar de tagovereenkomst moet beginnen
   * Gebruik de **Dialoog van de Selectie** om de plaats in AEM te kiezen
   * Huidige pagina gebruiken als deze leeg blijft
* **Markeringen**
Welke labels moeten worden aangepast
   * Gebruik **doorbladert** dialoog om de markeringen te selecteren
* **Gelijke**
Bepaal welke soort overeenkomst een pagina zou moeten kwalificeren om in de lijst te worden opgenomen
   * **om het even welke markering**
   * **alle markeringen**

#### Sorteeropties {#sort-options}

Ongeacht hoe u de lijst maakt, zijn er bepaalde sorteeropties die altijd kunnen worden gedefinieerd.

![&#x200B; de opties van de Sortering &#x200B;](/help/assets/v2/list-edit-sort-options.png)

* **Orde door**
Hoe de elementen moeten worden geordend
   * **Titel**
   * **Laatste gewijzigde datum**
* **de Orde van de Sortering**
De volgorde waarin de items moeten worden geordend
   * **oplopend**
   * **dalend**
* **Max Punten**
Maximumaantal items dat in de lijst wordt weergegeven.
   * Laat leeg om alle items te retourneren.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [&#x200B; Laag van Gegevens te controleren &#x200B;](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Iteminstellingen {#item-settings-tab}

Met het tabblad Iteminstellingen kunt u de opmaak van de lijstelementen configureren.

![&#x200B; montages van het Punt &#x200B;](/help/assets/v2/list-edit-item-settings.png)

* **Punten van de Verbinding**
Items koppelen aan de bijbehorende pagina
* **toon Beschrijving**
Beschrijvingen van het koppelingsitem weergeven
* **toon Datum**
Wijzigingsdatum van het koppelingsitem weergeven

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur definiëren welke typen lijsten zijn toegestaan aan de auteurs van de inhoud en de beschikbare iteminstellingen.

### Lijstinstellingen {#list-settings}

Op het **lusje van de Montages van de Lijst**, kan het datumformaat worden bepaald evenals welk type van lijsten in de component aan de inhoudsauteurs beschikbaar zouden moeten zijn.

{het plaatsen van de het ontwerpdialoog van de Component van 0} Lijst ![&#128279;](/help/assets/v2/list-design-list-settings.png)

* **Formaat van de Datum**
Formaat voor de weergave van de laatste wijzigingsdatum
* **maak kinderen** onbruikbaar
Het lijsttype voor onderliggende items in de component uitschakelen
* **maak statisch** onbruikbaar
Het type statische lijst in de component uitschakelen
* **maak onderzoek** onbruikbaar
Het type zoeklijst in de component uitschakelen
* **maak markeringen** onbruikbaar
Lijsttype van labels in de component uitschakelen

### Iteminstellingen {#item-settings}

Op het **lusje van de Montages van het Punt**, kunnen de het formatteren opties voor de individuele lijstelementen die in de component voor de inhoudsauteurs beschikbaar zouden moeten zijn worden bepaald.

![&#x200B; de montages van het het ontwerpdialoogpunt van de Component van de Lijst &#x200B;](/help/assets/v2/list-design-item-settings.png)

* **de punten van de Verbinding**
Laat de optie van Punten van de Verbinding in [&#x200B; toe uitgeven dialoog &#x200B;](#edit-dialog)
* **toon beschrijvingen**
Laat de optie van Beschrijvingen van de Show in [&#x200B; toe uitgeven dialoog &#x200B;](#edit-dialog)
* **toon datum**
Laat de optie van de Datum van de Show in [&#x200B; toe uitgeven dialoog &#x200B;](#edit-dialog)

### Tabblad Stijlen {#styles-tab}

De Component van het Beeld steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De Component van de Lijst steunt de [&#x200B; Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
