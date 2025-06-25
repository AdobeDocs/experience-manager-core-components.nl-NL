---
title: Component List
description: De component van de Lijst van de Component van de Kern staat voor de gemakkelijke verwezenlijking van dynamische en statische lijsten toe.
role: Architect, Developer, Admin, User
exl-id: 662ab508-0253-4d28-b95c-8c4cde8173bd
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '1204'
ht-degree: 0%

---


# Component List{#list-component}

De component van de Lijst van de Component van de Kern staat voor de gemakkelijke verwezenlijking van dynamische en statische lijsten toe.

{{traditional-aem}}

## Gebruik {#usage}

De component List kan worden gebruikt om bijvoorbeeld een dynamische lijst met onderliggende pagina&#39;s of een statische lijst met willekeurig gedefinieerde items te maken. Het type van beschikbare lijsten en het formatteren opties kunnen door de malplaatjeauteur in de [ ontwerpdialoog ](#design-dialog) worden bepaald. De inhoudsredacteur kan uit beschikbare lijsttypes selecteren en hoe te om de lijstelementen in [ uit te maken uitgeeft dialoog ](#edit-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component List is v4, die in februari 2023 is geïntroduceerd met release 2.22.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v4 | - | Compatibel | Compatibel |
| [ v3 ](/help/components/v3/list.md) | - | Compatibel | Compatibel | Compatibel |
| [ v2 ](/help/components/v2/list.md) | Compatibel | Compatibel | - | Compatibel |
| [ v1 ](/help/components/v1/list-v1.md) | Compatibel | Compatibel | - | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Omleiding in lijsten {#redirects}

Wanneer een pagina een omleidingsdoel heeft (ongeacht of deze naar een externe URL of naar een andere AEM-pagina verwijst), dan een lijst die koppelingen naar dat punt rechtstreeks naar de URL van het omleidingsdoel bevat.

### Voorbeeld {#redirect-example}

* Maak een pagina A die wordt omgeleid naar pagina B.
* Een pagina C maken die wordt omgeleid naar `https://aemcomponents.dev`
* Voeg op een pagina D een lijstcomponent in die pagina A en C bevat
* De respectievelijke koppelingen die worden gegenereerd, verwijzen vervolgens rechtstreeks naar pagina B en `https://aemcomponents.dev`

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Lijst te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_list).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Lijst [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_list_v3) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de lijst en de lijstitems configureren.

### Tabblad Lijstinstellingen {#list-settings-tab}

De lijst kan op verschillende manieren worden samengesteld.

* [Onderliggende pagina&#39;s](#child-pages)
* [Vaste lijst](#fixed-list)
* [Zoeken](#search-options)
* [Tags](#tags)

Ongeacht hoe de lijst wordt gebouwd, zijn er [ de Opties van de Soort en van identiteitskaart ](#sort-options) die altijd kunnen worden gevormd.

![ de Edit dialoog van de Component van de Lijst ](/help/assets/list-edit.png)

Afhankelijk van de manier waarop de auteur van de inhoud ervoor kiest de lijst te maken, worden de aanvullende configuratieopties gewijzigd.

#### Onderliggende pagina&#39;s {#child-pages}

De lijst kan van de kindpagina&#39;s van de huidige pagina of een andere pagina worden samengesteld.

![ de paginaopties van het Kind ](/help/assets/list-edit-child-pages.png)

* **Bovenliggende pagina**
   * De pagina waarvan de onderliggende pagina&#39;s de lijst moeten maken
   * Leeg laten om de huidige pagina te gebruiken

* **kind-diepte**
Hoeveel niveaus onderaan in de hiërarchie zouden moeten worden gebruikt

#### Vaste lijst {#fixed-list}

De lijst kan worden samengesteld met behulp van een vaste lijst met items.

![ Vaste lijstopties ](/help/assets/list-edit-fixed.png)

Tik of klik **voeg** knoop toe om een nieuw punt aan de lijst binnen te brengen.

* In het **gebied van de Verbinding** gaat of
   * Een volledig gekwalificeerde URL
   * Een relatieve URL naar bestaande AEM-inhoud
      * U kunt de **Dialoog van de Selectie** gebruiken om een punt van AEM te kiezen.
* Op het **gebied van de Tekst**, ga de tekst in die voor de verbinding in de lijst zal tonen.
* Schakel het selectievakje in als de koppeling moet worden geopend op een nieuw browsertabblad

Als er meer dan één item voor de lijst is gemaakt, kunt u de lijst rangschikken.

* Gebruik de sleepgreep om de items in de lijst opnieuw te rangschikken.
* Gebruik het prullenbakpictogram om items in de lijst te verwijderen.

#### Zoeken {#search-options}

De lijst kan worden samengesteld met behulp van de resultaten van een zoekopdracht naar AEM-inhoud.

![ de lijstopties van het Onderzoek ](/help/assets/list-edit-search.png)

* **vraag van het Onderzoek**
De tekenreeks waarvoor een zoekopdracht in volledige tekst wordt uitgevoerd om de lijstelementen te genereren
* **Onderzoek in**
Waar de zoekopdracht moet worden uitgevoerd
   * Gebruik de **Dialoog van de Selectie** om de plaats in AEM te kiezen
   * Huidige pagina gebruiken als deze leeg blijft

#### Tags {#tags}

De lijst kan worden samengesteld met pagina&#39;s die overeenkomen met bepaalde codes onder een bepaalde locatie.

![ de lijstopties van Markeringen ](/help/assets/list-edit-tags.png)

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

![ de opties van de Sortering ](/help/assets/list-edit-sort-options.png)

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
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Iteminstellingen {#item-settings-tab}

Met het tabblad Iteminstellingen kunt u de opmaak van de lijstelementen configureren.

![ montages van het Punt ](/help/assets/list-edit-item-settings.png)

* **Punten van de Verbinding** - de punten van de Verbinding met de overeenkomstige pagina
* **toon Beschrijving** - toon beschrijvingen van het verbindingspunt
* **toon Datum** - toon wijzigingsdatum van het verbindingspunt
* **Vertoning als teaser** - wanneer gecontroleerd, wordt het punt getoond als teaser

### Tabblad Stijlen {#styles-tab-edit}

De Component van de Lijst steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [ ontwerpdialoog ](#design-dialog) worden gevormd opdat het drop-down menu beschikbaar is.

![ Stijlen lusje van uitgeeft dialoog van de Component van de Lijst ](/help/assets/list-edit-styles.png)

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur definiëren welke typen lijsten zijn toegestaan aan de auteurs van de inhoud en de beschikbare iteminstellingen.

### Lijstinstellingen {#list-settings}

Op het **lusje van de Montages van de Lijst**, kan het datumformaat worden bepaald evenals welk type van lijsten in de component aan de inhoudsauteurs beschikbaar zouden moeten zijn.

{het plaatsen van de het ontwerpdialoog van de Component van 0} Lijst ![&#128279;](/help/assets/list-design-list-settings.png)

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

![ de montages van het het ontwerpdialoogpunt van de Component van de Lijst ](/help/assets/list-design-item-settings.png)

* **de punten van de Verbinding**
Laat de optie van Punten van de Verbinding in [ toe uitgeven dialoog ](#edit-dialog)
* **toon beschrijvingen**
Laat de optie van Beschrijvingen van de Show in [ toe uitgeven dialoog ](#edit-dialog)
* **toon datum**
Laat de optie van de Datum van de Show in [ toe uitgeven dialoog ](#edit-dialog)

### Tabblad Stijlen {#styles-tab}

De Component van het Beeld steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De Component van de Lijst steunt de [ Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
