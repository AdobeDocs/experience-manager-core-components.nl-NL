---
title: Component List
description: De component van de Lijst van de Component van de Kern staat voor de gemakkelijke verwezenlijking van dynamische en statische lijsten toe.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 1%

---


# Component List{#list-component}

De component van de Lijst van de Component van de Kern staat voor de gemakkelijke verwezenlijking van dynamische en statische lijsten toe.

## Gebruik {#usage}

De component List kan worden gebruikt om bijvoorbeeld een dynamische lijst met onderliggende pagina&#39;s of een statische lijst met willekeurig gedefinieerde items te maken. Het type beschikbare lijsten en opmaakopties kan door de sjabloonauteur in het [ontwerpdialoogvenster](#design-dialog)worden gedefinieerd. De inhoudseditor kan kiezen uit beschikbare lijsttypen en de opmaak van de lijstelementen in het dialoogvenster [](#edit-dialog)Bewerken.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component List is v2, die in januari 2018 is geïntroduceerd met release 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatibel | Compatibel | Compatibel |
| [v1](v1/list-v1.md) | Compatibel | Compatibel | - |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_list)om de component List te bekijken en voorbeelden te zien van de configuratieopties en de HTML- en JSON-uitvoer.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Lijst [kan op GitHub](https://adobe.com/go/aem_cmp_tech_list_v2)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de lijst en de lijstitems configureren.

### Tabblad Lijstinstellingen {#list-settings-tab}

De lijst kan op verschillende manieren worden samengesteld.

* [Onderliggende pagina&#39;s](#child-pages)
* [Vaste lijst](#fixed-list)
* [Zoeken](#search-options)
* [Tags](#tags)

Ongeacht hoe de lijst wordt gebouwd, zijn er de Opties [van de](#sort-options) Soort en van identiteitskaart die altijd kunnen worden gevormd.

![Bewerkingsdialoogvenster van component List](/help/assets/list-edit.png)

Afhankelijk van de manier waarop de auteur van de inhoud ervoor kiest de lijst te maken, worden de aanvullende configuratieopties gewijzigd.

#### Onderliggende pagina&#39;s {#child-pages}

De lijst kan van de kindpagina&#39;s van de huidige pagina of een andere pagina worden samengesteld.

![Opties voor onderliggende pagina&#39;s](/help/assets/list-edit-child-pages.png)

* **Bovenliggende pagina**
   * De pagina waarvan de onderliggende pagina&#39;s de lijst moeten maken
   * Leeg laten om de huidige pagina te gebruiken

* **Child-Depth** Hoeveel niveaus neer in de hiërarchie zouden moeten worden gebruikt

#### Vaste lijst {#fixed-list}

De lijst kan worden samengesteld met behulp van een vaste lijst met items.

![Opties voor vaste lijsten](/help/assets/list-edit-fixed.png)

Tik of klik op de knop **Toevoegen** om een nieuw item aan de lijst toe te voegen.

* Voer tekst in voor het item in de lijst of gebruik het dialoogvenster **** Selectie om een item uit AEM te kiezen.
* Gebruik de sleepgreep om de items in de lijst opnieuw te rangschikken.
* Gebruik het prullenbakpictogram om items in de lijst te verwijderen.

#### Zoeken {#search-options}

De lijst kan worden samengesteld met behulp van de resultaten van een zoekopdracht naar AEM inhoud.

![Opties voor zoeklijsten](/help/assets/list-edit-search.png)

* **Zoekquery** De tekenreeks waarvoor een full-text zoekopdracht wordt uitgevoerd om de lijstelementen te genereren
* **Zoeken in** waar de zoekopdracht moet worden uitgevoerd
   * Kies in het dialoogvenster **** Selectie de locatie in AEM
   * Huidige pagina gebruiken als deze leeg blijft

#### Tags {#tags}

De lijst kan worden samengesteld met pagina&#39;s die overeenkomen met bepaalde codes onder een bepaalde locatie.

![Opties in de lijst Tags](/help/assets/list-edit-tags.png)

* **Bovenliggende pagina** waarop de tagovereenkomst moet beginnen
   * Kies in het dialoogvenster **** Selectie de locatie in AEM
   * Huidige pagina gebruiken als deze leeg blijft
* **Tags** waaraan labels moeten voldoen
   * De labels selecteren in het dialoogvenster **Bladeren**
* **Identiek aan** Definiëren welk type overeenkomst een pagina moet kwalificeren om in de lijst te worden opgenomen
   * **elke tag**
   * **alle tags**

#### Sorteeropties {#sort-options}

Ongeacht hoe u de lijst maakt, zijn er bepaalde sorteeropties die altijd kunnen worden gedefinieerd.

![Sorteeropties](/help/assets/list-edit-sort-options.png)

* **Volgorde door** Hoe de elementen zouden moeten worden bevolen
   * **Titel**
   * **Laatst gewijzigd**
* **Sorteervolgorde** De volgorde waarin de items moeten worden geordend
   * **Oplopend**
   * **Aflopend**
* **Max. items** Maximum aantal items dat in de lijst wordt weergegeven.
   * Laat leeg om alle items te retourneren.
* **ID** - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Iteminstellingen {#item-settings-tab}

Met het tabblad Iteminstellingen kunt u de opmaak van de lijstelementen configureren.

![Iteminstellingen](/help/assets/list-edit-items.png)

* **Items** koppelenItems koppelen aan de corresponderende pagina
* **Beschrijving** tonen Beschrijving van koppelingsitem weergeven
* **Wijzigingsdatum** van koppelingsitem weergeven

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur definiëren welke typen lijsten zijn toegestaan aan de auteurs van de inhoud en welke beschikbare iteminstellingen zijn toegestaan.

### Lijstinstellingen {#list-settings}

Op het tabblad **Lijstinstellingen** kunt u de datumnotatie en het type lijsten definiëren dat in de component beschikbaar moet zijn voor de auteurs van de inhoud.

![De ontwerpdialoogvensterinstelling van de component List](/help/assets/list-design-list-settings.png)

* **Datumnotatie** die moet worden gebruikt voor de weergave van de laatste wijzigingsdatum
* **Onderliggende** items uitschakelen Het type lijst met onderliggende items in de component uitschakelen
* **Statisch** uitschakelen Het type statische lijst in de component uitschakelen
* **Zoekopdracht** uitschakelen Het type zoeklijst in de component uitschakelen
* **Tags** uitschakelen Lijsttype Tags in component uitschakelen

### Iteminstellingen {#item-settings}

Op het tabblad **Iteminstellingen** kunnen de opmaakopties voor de afzonderlijke lijstelementen worden gedefinieerd die in de component beschikbaar moeten zijn voor de makers van de inhoud.

![Instellingen van het ontwerpdialoogvenster van component weergeven](/help/assets/list-design-item-settings.png)

* **De optie Koppelingsitems** inschakelen in het dialoogvenster [Bewerken](#edit-dialog)
* **Beschrijvingen** tonen optie Omschrijvingen tonen inschakelen in het dialoogvenster [Bewerken](#edit-dialog)
* **De optie Datum** tonen inschakelen in het dialoogvenster [Bewerken](#edit-dialog)

### Tabblad Stijlen {#styles-tab}

De component van het Beeld steunt het systeem [van de](/help/get-started/authoring.md#component-styling)Stijl van het AEM.
