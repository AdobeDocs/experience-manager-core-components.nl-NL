---
title: Component Snel zoeken
description: De component Snel zoeken biedt zoekmogelijkheden voor een website en biedt zoekresultaten zodat bezoekers de site kunnen doorzoeken en de resultaten kunnen filteren.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Component Snel zoeken {#quick-search-component}

De component Snel zoeken biedt zoekmogelijkheden voor een website en biedt zoekresultaten zodat bezoekers gemakkelijk overeenkomende inhoud kunnen vinden en de resultaten kunnen bekijken.

## Gebruik {#usage}

Met de component Snel zoeken kunnen sitebezoekers naar inhoud zoeken, de resultaten op hun plaats bekijken en eenvoudig naar de overeenkomende pagina&#39;s navigeren. Nieuwe resultaten worden dynamisch opgehaald terwijl de gebruiker door de zoekresultaten schuift.

In het dialoogvenster [](#edit-dialog) Bewerken kan de auteur van de inhoud bepalen waar in de inhoudsstructuur de zoekopdracht moet beginnen. Met behulp van het dialoogvenster [](#design-dialog)Ontwerp kan de sjabloonauteur de standaardwaarde instellen voor de plaats in de inhoudsstructuur waar de zoekopdracht moet beginnen, en ook een maximale grootte en minimale lengte voor de zoekterm.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Snelle component van het Onderzoek is v1, die met versie 2.0.0 van de Componenten van de Kern in Januari 2018 werd geïntroduceerd, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v1 | Compatibel | Compatibel | Compatibel | Compatibel |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Hier volgt een voorbeeld van [We.Retail](https://docs.adobe.com/content/help/en/experience-manager-65/developing/bestpractices/we-retail/we-retail.html).

### Schermafbeelding {#screenshot}

![](/help/assets/screen_shot_2018-01-19at094248.png)

### HTML {#html}

```
<section class="cmp-search" role="search" data-cmp-is="search" data-cmp-min-length="3" data-cmp-results-size="10">
    <form class="cmp-search__form" data-cmp-hook-search="form" method="get" action="/content/we-retail/us/en/equipment.searchresults.json/_jcr_content/root/responsivegrid/search" autocomplete="off">
        <div class="cmp-search__field">
            <i class="cmp-search__icon" data-cmp-hook-search="icon"></i>
            <span class="cmp-search__loading-indicator" data-cmp-hook-search="loadingIndicator"></span>
            <input class="cmp-search__input" data-cmp-hook-search="input" type="text" name="fulltext" placeholder="Search" role="combobox" aria-autocomplete="list" aria-haspopup="true" aria-invalid="false">
            <button class="cmp-search__clear" data-cmp-hook-search="clear">
                <i class="cmp-search__clear-icon"></i>
            </button>
        </div>
    </form>
    <div class="cmp-search__results" data-cmp-hook-search="results" role="listbox" aria-multiselectable="false"></div>
    
<script data-cmp-hook-search="itemTemplate" type="x-template">
    <a class="cmp-search__item" data-cmp-hook-search="item">
        <span class="cmp-search__item-title" data-cmp-hook-search="itemTitle"></span>
    </a>
</script>
</section>
```

### JSON {#json}

```
"search":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "relativePath":"/jcr:content/root/responsivegrid/search",
                     "resultsSize":10,
                     "searchTermMinimumLength":3,
                     ":type":"core/wcm/components/search/v1/search"
                  }
```

### Technische details {#technical-details}

>[!NOTE]
>
>Het beschermen van de Component van het Onderzoek of om het even welke op AEM gebaseerde toepassing tegen DOS aanvallen zou op een hoger niveau moeten worden uitgevoerd, bijvoorbeeld door `mod_security` op de verzender te gebruiken.

De recentste technische documentatie over de Snelle Component van het Onderzoek [kan op GitHub](https://adobe.com/go/aem_cmp_tech_search_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud definiëren waar in de inhoudsstructuur de zoekopdracht moet beginnen.

![](/help/assets/screen_shot_2018-04-03at120132.png)

**Hoofdmap** zoeken - De hoofdpagina vanaf waar de zoekopdracht moet worden gestart. De hoofdmap van de zoekopdracht kan een standaardpagina of een hoofdstramien voor de blauwdruk zijn.

## Ontwerpdialoogvenster {#design-dialog}

Met behulp van het ontwerpdialoogvenster kan de sjabloonauteur de standaardwaarde instellen voor de plaats in de inhoudsstructuur waar de zoekopdracht moet beginnen, alsmede een maximale grootte voor de resultaatset en een minimale lengte voor de zoekterm. In het dialoogvenster Ontwerp kan de sjabloonauteur definiëren welke opties voor tekstopmaak beschikbaar zijn voor de auteurs van de inhoud.

### Tabblad Eigenschappen {#properties-tab}

![](/help/assets/screen_shot_2018-04-03at120028.png)

* **Hoofdmap** zoeken De standaardwaarde van de zoekhoofdmap wanneer een auteur van inhoud de component Snel zoeken op een inhoudspagina plaatst
* **Grootte** van resultaten Het maximum aantal resultaten dat door een onderzoeksverzoek wordt gehaald
* **Zoektermijn Minimale lengte** minimumlengte van zoekterm om de zoekopdracht te starten

>[!NOTE]
>
>**Grootte** van resultaten en Minimumlengte **van** zoektermen kunnen alleen worden ingesteld in de ontwerpmodus en daarom alleen op sjabloonniveau. Dit betekent dat auteurs van inhoud deze waarden niet kunnen wijzigen.

>[!CAUTION]
>
>**Grootte** van resultaten en Minimumlengte **van** zoekterm kunnen prestatieeffecten hebben als deze te hoog of te laag zijn ingesteld.

### Tabblad Stijlen {#styles-tab}

De component Snel zoeken ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).
