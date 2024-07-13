---
title: Lijstcomponent (v1)
description: De component van de Lijst van de Component van de Kern staat voor de gemakkelijke verwezenlijking van dynamische en statische lijsten toe.
index: n
role: Architect, Developer, Admin, User
exl-id: 510d059c-e60a-40aa-9032-66a901109f6e
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# Lijstcomponent (v1) {#list-component-v}

De component van de Lijst van de Component van de Kern staat voor de gemakkelijke verwezenlijking van dynamische en statische lijsten toe.

## Gebruik {#usage}

De component List kan worden gebruikt om bijvoorbeeld een dynamische lijst met onderliggende pagina&#39;s of een statische lijst met willekeurig gedefinieerde items te maken.

Het type van beschikbare lijsten en het formatteren opties kunnen door de malplaatjeauteur in de [ ontwerpdialoog ](#design-dialog) worden bepaald. De inhoudsredacteur kan uit beschikbare lijsttypes selecteren en hoe te om de lijstelementen in [ uit te maken uitgeeft dialoog ](#edit-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de component List beschreven. Deze versie is oorspronkelijk geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van v1 van de component List weergegeven.

| AEM | List Component v1 |
|--- |--- |
| 6,3 | Compatibel |
| 6,4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component List beschreven.
>
>Voor details van de huidige versie van de Component van de Lijst, zie het ](/help/components/list.md) document van de Component van de Lijst 0} {.[

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende wordt steekproef genomen van [ We.Retail ](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Gelieve te zien de [ verenigbaarheidsinformatie voor de Componenten van de Kern v1 ](/help/versions.md) voor meer informatie.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de lijst en de lijstelementen configureren.

### Lijstinstellingen {#list-settings}

De lijst kan op verschillende manieren worden samengesteld.

* [Onderliggende pagina&#39;s](#child-pages)
* [Vaste lijst](#fixed-list)
* [Zoeken](#search-list)
* [Tags](#tags)

Ongeacht hoe de lijst wordt gebouwd, zijn er [ Opties van de Soort ](#sort-options) die altijd kunnen worden gevormd.

![](/help/assets/chlimage_1-38.png)

Afhankelijk van de manier waarop de auteur van de inhoud ervoor kiest de lijst te maken, worden de aanvullende configuratieopties gewijzigd.

#### Onderliggende pagina&#39;s {#child-pages}

De lijst kan van de kindpagina&#39;s van de huidige pagina of een andere pagina worden samengesteld.

![](/help/assets/chlimage_1-39.png)

* **Bovenliggende pagina**
   * De pagina waarvan de onderliggende pagina&#39;s de lijst moeten maken
   * Leeg laten om de huidige pagina te gebruiken
* **kind-diepte** - hoeveel niveaus neer in de hiërarchie zouden moeten worden gebruikt

#### Vaste lijst {#fixed-list}

De lijst kan worden samengesteld met behulp van een vaste lijst met items.

![](/help/assets/chlimage_1-40.png)

Tik of klik **voeg** knoop toe om een nieuw punt aan de lijst binnen te brengen.

* Ga tekst voor het punt in de lijst in of gebruik de **Dialoog van de Selectie** om een punt van AEM te kiezen.
* Gebruik de sleepgreep om de items in de lijst opnieuw te rangschikken.
* Gebruik het prullenbakpictogram om items in de lijst te verwijderen.

#### Zoeken {#search-list}

De lijst kan worden samengesteld met de resultaten van een zoekopdracht naar AEM inhoud.

![](/help/assets/chlimage_1-41.png)

* **vraag van het Onderzoek** - het koord waarvoor een full-text onderzoek zal in werking worden gesteld om de lijstelementen te produceren
* **Onderzoek in** - waar het onderzoek in werking zou moeten worden gesteld
   * Gebruik de **Dialoog van de Selectie** om de plaats in AEM te kiezen
   * Huidige pagina gebruiken als deze leeg blijft

#### Tags {#tags}

De lijst kan worden samengesteld met pagina&#39;s die overeenkomen met bepaalde codes onder een bepaalde locatie.

![](/help/assets/chlimage_1-42.png)

* **Bovenliggende pagina** - waar de markering aanpassing zou moeten beginnen
   * Gebruik de **Dialoog van de Selectie** om de plaats in AEM te kiezen
   * Huidige pagina gebruiken als deze leeg blijft
* **Markeringen** - welke markeringen zouden moeten worden aangepast
   * Gebruik **doorbladert** dialoog om de markeringen te selecteren
* **Gelijke** - bepaal welk soort gelijke een pagina zou moeten kwalificeren om in de lijst worden opgenomen
   * **om het even welke markering**
   * **alle markeringen**

#### Sorteeropties {#sort-options}

Ongeacht hoe u de lijst maakt, zijn er bepaalde sorteeropties die altijd kunnen worden gedefinieerd.

![](/help/assets/chlimage_1-43.png)

* **Orde door** - hoe de elementen zouden moeten worden bevolen
   * **Titel**
   * **Laatste gewijzigde datum**
* **de Orde van de Sortering** - de orde waarin de punten zouden moeten worden bevolen
   * **oplopend**
   * **dalend**
* **Max Punten** - Maximum aantal punten die in lijst worden getoond.
   * Laat leeg om alle items te retourneren.

### Iteminstellingen {#item-settings}

Gebruikend het **lusje van de Montages van het Punt 0} {, kan het formatteren van de lijstelementen worden gevormd.**

![](/help/assets/chlimage_1-44.png)

* **Punten van de Verbinding**
Items koppelen aan de bijbehorende pagina
* **toon Beschrijving**
Beschrijvingen van het koppelingsitem weergeven
* **toon Datum**
Wijzigingsdatum van het koppelingsitem weergeven

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur definiëren welke typen lijsten zijn toegestaan aan de auteurs van de inhoud en de beschikbare iteminstellingen.

### Lijstinstellingen {#list-settings-1}

Op het **lusje van de Montages van de Lijst**, kan het datumformaat worden bepaald evenals welk type van lijsten in de component aan de inhoudsauteurs beschikbaar zouden moeten zijn.

![](/help/assets/chlimage_1-45.png)

* **Formaat van de Datum** - Formaat voor de vertoning van de laatste wijzigingsdatum te gebruiken
* **maak Kinderen** onbruikbaar - maak het type van kindlijst in de component onbruikbaar
* **maak Statisch** onbruikbaar - maak het statische lijsttype in de component onbruikbaar
* **maak Onderzoek** onbruikbaar - maak het type van onderzoekslijst in de component onbruikbaar
* **maak Codes** onbruikbaar - maak het type van markeringslijst in de component onbruikbaar

### Iteminstellingen {#item-settings-1}

Op het **lusje van de Montages van het Punt**, kunnen de het formatteren opties voor de individuele lijstelementen die in de component voor de inhoudsauteurs beschikbaar zouden moeten zijn worden bepaald.

![](/help/assets/chlimage_1-46.png)

* **Punten van de Verbinding** - laat de optie van Punten van de Verbinding in [ toe geef dialoog ](#edit-dialog) uit
* **toon Beschrijvingen** - laat de optie van Beschrijvingen in [ toe uitgeeft dialoog ](#edit-dialog)
* **toon Datum** - laat de optie van de Datum van de Show in [ toe geef dialoog ](#edit-dialog) uit

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Lijst [ kan op GitHub ](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list) worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).
