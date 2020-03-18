---
title: Lijstcomponent (v1)
description: De component van de Lijst van de Component van de Kern staat voor de gemakkelijke verwezenlijking van dynamische en statische lijsten toe.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Lijstcomponent (v1) {#list-component-v}

De component van de Lijst van de Component van de Kern staat voor de gemakkelijke verwezenlijking van dynamische en statische lijsten toe.

## Gebruik {#usage}

De component List kan worden gebruikt om bijvoorbeeld een dynamische lijst met onderliggende pagina&#39;s of een statische lijst met willekeurig gedefinieerde items te maken.

Het type beschikbare lijsten en opmaakopties kan door de sjabloonauteur in het [ontwerpdialoogvenster](#design-dialog)worden gedefinieerd. De inhoudseditor kan kiezen uit beschikbare lijsttypen en de opmaak van de lijstelementen in het dialoogvenster [](#edit-dialog)Bewerken.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de component List beschreven. Deze versie is oorspronkelijk geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van v1 van de component List weergegeven.

| AEM-versie | List Component v1 |
|--- |--- |
| 6.3 | Compatibel |
| 6.4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component List beschreven.
>
>Zie het document [List Component](/help/components/list.md) voor meer informatie over de huidige versie van de component List.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Hier volgt een voorbeeld van [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Schermafbeelding {#screenshot}

![](/help/assets/chlimage_1-47.png)

### HTML {#html}

```
<div class="cmp cmp-list aem-GridColumn aem-GridColumn--default--12">

<ul>
    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/arctic-surfing-in-lofoten.html">
            <span class="cmp-list--item-title">Arctic Surfing In Lofoten</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/summit-success-in-the-himalayas.html">
            <span class="cmp-list--item-title">Summit Success in the Himalayas</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/climbing-on-kalymnos-island--greece.html">
            <span class="cmp-list--item-title">Climbing on Kalymnos Island, Greece</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/running-at-the-great-wall-marathon.html">
            <span class="cmp-list--item-title">Running at the Great Wall Marathon</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/skiing-deep-powder-in-siberia.html">
            <span class="cmp-list--item-title">Skiing deep powder in Siberia</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/climbing-in-the-massif-du-mont-blanc.html">
            <span class="cmp-list--item-title">Climbing in the Massif du Mont Blanc</span>
            
        </a>
        
    </article>
</li>
</ul>

</div>
```

### JSON {#json}

```
"articles_list": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/articleslist",
              "tagsMatch": "any",
              "displayAs": "teaser",
              "feedEnabled": "true",
              "listFrom": "children",
              "limit": "0",
              "orderBy": "cq:lastModified",
              "pageMax": "0"
            }
```

>[!NOTE]
>
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Zie de [compatibiliteitsinformatie voor Core Components v1](/help/versions.md) voor meer informatie.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de lijst en de lijstelementen configureren.

### Lijstinstellingen {#list-settings}

De lijst kan op verschillende manieren worden samengesteld.

* [Onderliggende pagina&#39;s](#child-pages)
* [Vaste lijst](#fixed-list)
* [Zoeken](#search-list)
* [Tags](#tags)

Ongeacht hoe de lijst wordt gebouwd, zijn er Opties [van de](#sort-options) Soort die altijd kunnen worden gevormd.

![](/help/assets/chlimage_1-38.png)

Afhankelijk van de manier waarop de auteur van de inhoud ervoor kiest de lijst te maken, worden de aanvullende configuratieopties gewijzigd.

#### Onderliggende pagina&#39;s {#child-pages}

De lijst kan van de kindpagina&#39;s van de huidige pagina of een andere pagina worden samengesteld.

![](/help/assets/chlimage_1-39.png)

* **Bovenliggende pagina**
   * De pagina waarvan de onderliggende pagina&#39;s de lijst moeten maken
   * Leeg laten om de huidige pagina te gebruiken
* **Child-Depth** - Hoeveel niveaus neer in de hiërarchie zouden moeten worden gebruikt

#### Vaste lijst {#fixed-list}

De lijst kan worden samengesteld met behulp van een vaste lijst met items.

![](/help/assets/chlimage_1-40.png)

Tik of klik op de knop **Toevoegen** om een nieuw item aan de lijst toe te voegen.

* Voer tekst in voor het item in de lijst of kies een item in AEM in het dialoogvenster **** Selectie.
* Gebruik de sleepgreep om de items in de lijst opnieuw te rangschikken.
* Gebruik het prullenbakpictogram om items in de lijst te verwijderen.

#### Zoeken {#search-list}

De lijst kan worden samengesteld met behulp van de resultaten van een zoekopdracht naar AEM-inhoud.

![](/help/assets/chlimage_1-41.png)

* **Zoekquery** - De tekenreeks waarvoor een full-text zoekopdracht wordt uitgevoerd om de lijstelementen te genereren
* **Zoeken in** - waar de zoekopdracht moet worden uitgevoerd
   * Kies in het dialoogvenster **** Selectie de locatie in AEM
   * Huidige pagina gebruiken als deze leeg blijft

#### Tags {#tags}

De lijst kan worden samengesteld met pagina&#39;s die overeenkomen met bepaalde codes onder een bepaalde locatie.

![](/help/assets/chlimage_1-42.png)

* **Bovenliggende pagina** - Waar de overeenkomende tag moet beginnen
   * Kies in het dialoogvenster **** Selectie de locatie in AEM
   * Huidige pagina gebruiken als deze leeg blijft
* **Tags** - Welke labels moeten overeenkomen
   * De labels selecteren in het dialoogvenster **Bladeren**
* **Overeenkomst** - Bepaal welke soort gelijke een pagina zou moeten kwalificeren om in de lijst worden opgenomen
   * **elke tag**
   * **alle tags**

#### Sorteeropties {#sort-options}

Ongeacht hoe u de lijst maakt, zijn er bepaalde sorteeropties die altijd kunnen worden gedefinieerd.

![](/help/assets/chlimage_1-43.png)

* **Volgorde bij** - Hoe de elementen moeten worden geordend
   * **Titel**
   * **Laatst gewijzigd**
* **Sorteervolgorde** - De volgorde waarin de items moeten worden geordend
   * **Oplopend**
   * **Aflopend**
* **Max. items** - Maximum aantal items dat in de lijst wordt weergegeven.
   * Laat leeg om alle items te retourneren.

### Iteminstellingen {#item-settings}

Met het tabblad **Iteminstellingen** kunt u de opmaak van de lijstelementen configureren.

![](/help/assets/chlimage_1-44.png)

* **Items** koppelenItems koppelen aan de corresponderende pagina
* **Beschrijving** tonen Beschrijving van koppelingsitem weergeven
* **Wijzigingsdatum** van koppelingsitem weergeven

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur definiëren welke typen lijsten zijn toegestaan aan de auteurs van de inhoud en welke beschikbare iteminstellingen zijn toegestaan.

### Lijstinstellingen {#list-settings-1}

Op het tabblad **Lijstinstellingen** kunt u de datumnotatie en het type lijsten definiëren dat in de component beschikbaar moet zijn voor de auteurs van de inhoud.

![](/help/assets/chlimage_1-45.png)

* **Datumnotatie** - Indeling die moet worden gebruikt voor de weergave van de laatste wijzigingsdatum
* **Onderliggende** items uitschakelen - het type lijst met onderliggende items in de component uitschakelen
* **Statisch** uitschakelen - het type statische lijst in de component uitschakelen
* **Zoeken** uitschakelen - Het type zoeklijst in de component uitschakelen
* **Labels** uitschakelen - Lijsttype voor labels in de component uitschakelen

### Iteminstellingen {#item-settings-1}

Op het tabblad **Iteminstellingen** kunnen de opmaakopties voor de afzonderlijke lijstelementen worden gedefinieerd die in de component beschikbaar moeten zijn voor de makers van de inhoud.

![](/help/assets/chlimage_1-46.png)

* **Koppelingsitems** - optie Koppelingsitems inschakelen in het dialoogvenster [Bewerken](#edit-dialog)
* **Omschrijvingen** tonen - de optie Omschrijvingen tonen inschakelen in het dialoogvenster [Bewerken](#edit-dialog)
* **Datum** tonen - de optie Datum tonen inschakelen in het dialoogvenster [Bewerken](#edit-dialog)

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Lijst [kan op GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list)worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.