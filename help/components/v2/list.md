---
title: Lijstcomponent (v2)
description: De component van de Lijst van de Component van de Kern staat voor de gemakkelijke verwezenlijking van dynamische en statische lijsten toe.
role: Architect, Developer, Admin, User
exl-id: fa34be64-b345-45cd-baf3-571973414852
source-git-commit: 241c86240377858a73f4a022368d428da9c11100
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 0%

---

# Lijstcomponent (v2) {#list-component}

De component van de Lijst van de Component van de Kern staat voor de gemakkelijke verwezenlijking van dynamische en statische lijsten toe.

## Gebruik {#usage}

De component List kan worden gebruikt om bijvoorbeeld een dynamische lijst met onderliggende pagina&#39;s of een statische lijst met willekeurig gedefinieerde items te maken. Het type beschikbare lijsten en opmaakopties kan door de sjabloonauteur in het dialoogvenster [ontwerpdialoogvenster](#design-dialog). De inhoudeditor kan kiezen uit beschikbare lijsttypen en hoe u de lijstelementen opmaakt in het dialoogvenster [dialoogvenster bewerken](#edit-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de component List beschreven. Deze versie is in januari 2018 geïntroduceerd met versie 2.0.0 van de kerncomponenten.

>[!CAUTION]
>
>In dit document wordt versie 2 van de component List beschreven.
>
>Voor meer informatie over de huidige versie van de component List raadpleegt u de [Component List](/help/components/list.md) document.

## Omleiding in lijsten {#redirects}

Wanneer een pagina een omleidingsdoel heeft (ongeacht of deze naar een externe URL of naar een andere AEM pagina verwijst), dan een lijst die koppelingen naar dat punt rechtstreeks naar de URL van het omleidingsdoel bevat.

### Voorbeeld {#redirect-example}

* Maak een pagina A die wordt omgeleid naar pagina B.
* Een pagina C maken waarnaar wordt omgeleid `https://aemcomponents.dev`
* Voeg op een pagina D een lijstcomponent in die de pagina&#39;s A en C bevat
* De respectievelijke koppelingen die vervolgens worden gegenereerd, verwijzen rechtstreeks naar pagina B en `https://aemcomponents.dev`

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de component List wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_list).

### Technische details {#technical-details}

De meest recente technische documentatie over de component List [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_list_v2).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de lijst en de lijstitems configureren.

### Tabblad Lijstinstellingen {#list-settings-tab}

De lijst kan op verschillende manieren worden samengesteld.

* [Onderliggende pagina&#39;s](#child-pages)
* [Vaste lijst](#fixed-list)
* [Zoeken](#search-options)
* [Tags](#tags)

Ongeacht hoe de lijst wordt samengesteld, zijn er [Opties voor sorteren en id](#sort-options) dat altijd kan worden gevormd.

![Bewerkingsdialoogvenster van component List](/help/assets/v2/list-edit.png)

Afhankelijk van de manier waarop de auteur van de inhoud ervoor kiest de lijst te maken, worden de aanvullende configuratieopties gewijzigd.

#### Onderliggende pagina&#39;s {#child-pages}

De lijst kan van de kindpagina&#39;s van de huidige pagina of een andere pagina worden samengesteld.

![Opties voor onderliggende pagina&#39;s](/help/assets/v2/list-edit-child-pages.png)

* **Bovenliggende pagina**
   * De pagina waarvan de onderliggende pagina&#39;s de lijst moeten maken
   * Leeg laten om de huidige pagina te gebruiken

* **Onderliggende diepte**
Hoeveel niveaus onderaan in de hiërarchie zouden moeten worden gebruikt

#### Vaste lijst {#fixed-list}

De lijst kan worden samengesteld met behulp van een vaste lijst met items.

![Opties voor vaste lijsten](/help/assets/v2/list-edit-fixed-list.png)

Tik of klik op de knop **Toevoegen** om een nieuw item aan de lijst toe te voegen.

* Voer tekst in voor het item in de lijst of gebruik de optie **Dialoogvenster Selectie** om een item te kiezen uit AEM.
* Gebruik de sleepgreep om de items in de lijst opnieuw te rangschikken.
* Gebruik het prullenbakpictogram om items in de lijst te verwijderen.

#### Zoeken {#search-options}

De lijst kan worden samengesteld met behulp van de resultaten van een zoekopdracht naar AEM inhoud.

![Opties voor zoeklijsten](/help/assets/v2/list-edit-search.png)

* **Zoekquery**
De tekenreeks waarvoor een zoekopdracht in volledige tekst wordt uitgevoerd om de lijstelementen te genereren
* **Zoeken in**
Waar de zoekopdracht moet worden uitgevoerd
   * Gebruik de **Dialoogvenster Selectie** om de locatie in AEM te kiezen
   * Huidige pagina gebruiken als deze leeg blijft

#### Tags {#tags}

De lijst kan worden samengesteld met pagina&#39;s die overeenkomen met bepaalde codes onder een bepaalde locatie.

![Opties in de lijst Tags](/help/assets/v2/list-edit-tags.png)

* **Bovenliggende pagina**
Waar de tagovereenkomst moet beginnen
   * Gebruik de **Dialoogvenster Selectie** om de locatie in AEM te kiezen
   * Huidige pagina gebruiken als deze leeg blijft
* **Tags**
Welke labels moeten worden aangepast
   * Gebruik de **Bladeren** dialoogvenster om de tags te selecteren
* **Overeenkomst**
Bepaal welke soort overeenkomst een pagina zou moeten kwalificeren om in de lijst te worden opgenomen
   * **elke tag**
   * **alle tags**

#### Sorteeropties {#sort-options}

Ongeacht hoe u de lijst maakt, zijn er bepaalde sorteeropties die altijd kunnen worden gedefinieerd.

![Sorteeropties](/help/assets/v2/list-edit-sort-options.png)

* **Volgorde van**
Hoe de elementen moeten worden gerangschikt
   * **Titel**
   * **Laatst gewijzigd**
* **Sorteervolgorde**
De volgorde waarin de items moeten worden geordend
   * **Oplopend**
   * **Aflopend**
* **Max. items**
Maximumaantal items dat in de lijst wordt weergegeven.
   * Laat leeg om alle items te retourneren.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Iteminstellingen {#item-settings-tab}

Met het tabblad Iteminstellingen kunt u de opmaak van de lijstelementen configureren.

![Iteminstellingen](/help/assets/v2/list-edit-item-settings.png)

* **Items koppelen**
Items koppelen aan de corresponderende pagina
* **Beschrijving tonen**
Beschrijvingen van het koppelingsitem weergeven
* **Datum tonen**
Wijzigingsdatum van het koppelingsitem weergeven

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur definiëren welke typen lijsten zijn toegestaan aan de auteurs van de inhoud en de beschikbare iteminstellingen.

### Lijstinstellingen {#list-settings}

Op de **Lijstinstellingen** , kan de datumnotatie worden gedefinieerd en kunt u aangeven welk type lijst in de component beschikbaar moet zijn voor de auteurs van de inhoud.

![De ontwerpdialoogvensterinstelling van de component List](/help/assets/v2/list-design-list-settings.png)

* **Datumnotatie**
Formaat voor de weergave van de laatste wijzigingsdatum
* **Kinderen uitschakelen**
Het lijsttype voor onderliggende items in de component uitschakelen
* **Statisch uitschakelen**
Het type statische lijst in de component uitschakelen
* **Zoekopdracht uitschakelen**
Het type zoeklijst in de component uitschakelen
* **Tags uitschakelen**
Lijsttype van labels in de component uitschakelen

### Iteminstellingen {#item-settings}

Op de **Iteminstellingen** kunt u de opmaakopties definiëren voor de afzonderlijke lijstelementen die in de component beschikbaar moeten zijn voor de makers van de inhoud.

![Instellingen van het ontwerpdialoogvenster van component weergeven](/help/assets/v2/list-design-item-settings.png)

* **Items koppelen**
De optie Koppelingsitems inschakelen in het dialoogvenster [dialoogvenster bewerken](#edit-dialog)
* **Beschrijvingen weergeven**
Schakel de optie Beschrijvingen tonen in het dialoogvenster [dialoogvenster bewerken](#edit-dialog)
* **Datum tonen**
De optie Datum tonen inschakelen in het dialoogvenster [dialoogvenster bewerken](#edit-dialog)

### Tabblad Stijlen {#styles-tab}

De component Image ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component List ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
