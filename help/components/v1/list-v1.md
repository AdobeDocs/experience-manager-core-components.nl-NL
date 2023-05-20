---
title: Lijstcomponent (v1)
description: De component van de Lijst van de Component van de Kern staat voor de gemakkelijke verwezenlijking van dynamische en statische lijsten toe.
index: n
role: Architect, Developer, Admin, User
exl-id: 510d059c-e60a-40aa-9032-66a901109f6e
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 0%

---

# Lijstcomponent (v1) {#list-component-v}

De component van de Lijst van de Component van de Kern staat voor de gemakkelijke verwezenlijking van dynamische en statische lijsten toe.

## Gebruik {#usage}

De component List kan worden gebruikt om bijvoorbeeld een dynamische lijst met onderliggende pagina&#39;s of een statische lijst met willekeurig gedefinieerde items te maken.

Het type beschikbare lijsten en opmaakopties kan door de sjabloonauteur in het dialoogvenster [ontwerpdialoogvenster](#design-dialog). De inhoudeditor kan kiezen uit beschikbare lijsttypen en hoe u de lijstelementen opmaakt in het dialoogvenster [dialoogvenster bewerken](#edit-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de component List beschreven. Deze versie is oorspronkelijk geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van v1 van de component List weergegeven.

| AEM | List Component v1 |
|--- |--- |
| 6.3 | Compatibel |
| 6.4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component List beschreven.
>
>Voor meer informatie over de huidige versie van de component List raadpleegt u de [Component List](/help/components/list.md) document.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende monster wordt genomen uit [Wij.Detailhandel](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Zie de [compatibiliteitsinformatie voor Core Components v1](/help/versions.md) voor meer informatie .

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de lijst en de lijstelementen configureren.

### Lijstinstellingen {#list-settings}

De lijst kan op verschillende manieren worden samengesteld.

* [Onderliggende pagina&#39;s](#child-pages)
* [Vaste lijst](#fixed-list)
* [Zoeken](#search-list)
* [Tags](#tags)

Ongeacht hoe de lijst wordt samengesteld, zijn er [Sorteeropties](#sort-options) dat altijd kan worden gevormd.

![](/help/assets/chlimage_1-38.png)

Afhankelijk van de manier waarop de auteur van de inhoud ervoor kiest de lijst te maken, worden de aanvullende configuratieopties gewijzigd.

#### Onderliggende pagina&#39;s {#child-pages}

De lijst kan van de kindpagina&#39;s van de huidige pagina of een andere pagina worden samengesteld.

![](/help/assets/chlimage_1-39.png)

* **Bovenliggende pagina**
   * De pagina waarvan de onderliggende pagina&#39;s de lijst moeten maken
   * Leeg laten om de huidige pagina te gebruiken
* **Onderliggende diepte** - Hoeveel niveaus lager in de hiërarchie zouden moeten worden gebruikt

#### Vaste lijst {#fixed-list}

De lijst kan worden samengesteld met behulp van een vaste lijst met items.

![](/help/assets/chlimage_1-40.png)

Tik of klik op de knop **Toevoegen** om een nieuw item aan de lijst toe te voegen.

* Voer tekst in voor het item in de lijst of gebruik de optie **Dialoogvenster Selectie** om een item te kiezen uit AEM.
* Gebruik de sleepgreep om de items in de lijst opnieuw te rangschikken.
* Gebruik het prullenbakpictogram om items in de lijst te verwijderen.

#### Zoeken {#search-list}

De lijst kan worden samengesteld met behulp van de resultaten van een zoekopdracht naar AEM inhoud.

![](/help/assets/chlimage_1-41.png)

* **Zoekquery** - De tekenreeks waarvoor een zoekopdracht in volledige tekst wordt uitgevoerd om de lijstelementen te genereren
* **Zoeken in** - Waar de zoekopdracht moet worden uitgevoerd
   * Gebruik de **Dialoogvenster Selectie** om de locatie in AEM te kiezen
   * Huidige pagina gebruiken als deze leeg blijft

#### Tags {#tags}

De lijst kan worden samengesteld met pagina&#39;s die overeenkomen met bepaalde codes onder een bepaalde locatie.

![](/help/assets/chlimage_1-42.png)

* **Bovenliggende pagina** - Waar de tagovereenkomst moet beginnen
   * Gebruik de **Dialoogvenster Selectie** om de locatie in AEM te kiezen
   * Huidige pagina gebruiken als deze leeg blijft
* **Tags** - Welke labels moeten worden aangepast
   * Gebruik de **Bladeren** dialoogvenster om de tags te selecteren
* **Overeenkomst** - Bepaal welke soort overeenkomst een pagina zou moeten kwalificeren om in de lijst te worden opgenomen
   * **elke tag**
   * **alle tags**

#### Sorteeropties {#sort-options}

Ongeacht hoe u de lijst maakt, zijn er bepaalde sorteeropties die altijd kunnen worden gedefinieerd.

![](/help/assets/chlimage_1-43.png)

* **Volgorde van** - Hoe de elementen moeten worden gerangschikt
   * **Titel**
   * **Laatst gewijzigd**
* **Sorteervolgorde** - De volgorde waarin de items moeten worden besteld
   * **Oplopend**
   * **Aflopend**
* **Max. items** - Maximum aantal items dat in de lijst wordt weergegeven.
   * Laat leeg om alle items te retourneren.

### Iteminstellingen {#item-settings}

Met de **Iteminstellingen** kunt u de opmaak van de lijstelementen configureren.

![](/help/assets/chlimage_1-44.png)

* **Items koppelen**
Items koppelen aan de corresponderende pagina
* **Beschrijving tonen**
Beschrijvingen van het koppelingsitem weergeven
* **Datum tonen**
Wijzigingsdatum van het koppelingsitem weergeven

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur definiëren welke typen lijsten zijn toegestaan aan de auteurs van de inhoud en de beschikbare iteminstellingen.

### Lijstinstellingen {#list-settings-1}

Op de **Lijstinstellingen** , kan de datumnotatie worden gedefinieerd en kunt u aangeven welk type lijst in de component beschikbaar moet zijn voor de auteurs van de inhoud.

![](/help/assets/chlimage_1-45.png)

* **Datumnotatie** - Formaat voor de weergave van de laatste wijzigingsdatum
* **Onderliggende niveaus uitschakelen** - Schakel het type lijst met onderliggende items in de component uit
* **Statisch uitschakelen** - Het type statische lijst in de component uitschakelen
* **Zoeken uitschakelen** - Schakel het type zoeklijst in de component uit
* **Labels uitschakelen** - Labellijsttype uitschakelen in de component

### Iteminstellingen {#item-settings-1}

Op de **Iteminstellingen** kunt u de opmaakopties definiëren voor de afzonderlijke lijstelementen die in de component beschikbaar moeten zijn voor de makers van de inhoud.

![](/help/assets/chlimage_1-46.png)

* **Items koppelen** - Schakel de optie Koppelingsitems in het dialoogvenster [dialoogvenster bewerken](#edit-dialog)
* **Beschrijvingen tonen** - Schakel de optie Omschrijvingen tonen in het dialoogvenster [dialoogvenster bewerken](#edit-dialog)
* **Datum tonen** - Schakel de optie Datum tonen in het dialoogvenster [dialoogvenster bewerken](#edit-dialog)

## Technische details {#technical-details}

De meest recente technische documentatie over de component List [kan op GitHub worden gevonden](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list).

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).
