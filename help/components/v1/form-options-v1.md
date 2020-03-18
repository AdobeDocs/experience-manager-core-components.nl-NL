---
title: Component Formulieropties (v1)
description: Met de component Core Component Form Options kunt u vooraf gedefinieerde opties in verschillende indelingen selecteren.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Component Formulieropties (v1) {#form-options-component-v}

Met de component Core Component Form Options kunt u vooraf gedefinieerde opties in verschillende indelingen selecteren.

## Gebruik {#usage}

Met de component Core Component Form Options kunnen verschillende typen opties worden ingediend die op verschillende manieren worden gepresenteerd. Deze component is bedoeld voor gebruik in combinatie met de [component](form-container-v1.md)van de formuliercontainer.

De presentatie van de opties, de etiketten, en de individuele opties kunnen door de inhoudsredacteur in [vormen dialoog](#configure-dialog)worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de component Formulieropties beschreven, die oorspronkelijk is geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van versie 1 van de component Formulieropties weergegeven.

| Componentversie | AEM 6.3 | AEM 6.4 |
|--- |--- |--- |
| v2 | Compatibel | Compatibel |
| v1 | Compatibel | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Formulieropties beschreven.
>
>Meer informatie over de huidige versie van de component Formulieropties vindt u in het document van de component [Formulieropties](/help/components/forms/form-options.md) .

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Hier volgt een voorbeeld van [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Schermafbeelding {#screenshot}

![](/help/assets/chlimage_1-89.png)

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
<form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
    
    <div class="cmp cmp-options aem-GridColumn aem-GridColumn--default--12">

    <fieldset class="form-group checkbox">
        <legend>What is your favorite type of toast?</legend>
        
        <div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="dry">
              Plain dry toast
            </label>
        </div>
<div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="french">
              French toast
            </label>
        </div>
<div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="texas">
              Texas toast
            </label>
        </div>

    </fieldset>
    
</div>
    
</form></div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "options": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/options",
                  "name": "toastTypes",
                  "jcr:title": "What is your favorite type of toast?",
                  "source": "local",
                  "type": "checkbox"
                }
              },
              ":itemsOrder": [
                "options"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Zie de [compatibiliteitsinformatie voor Core Components v1](/help/versions.md) voor meer informatie.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het type opties definiëren dat moet worden weergegeven, de labels en de beschikbare opties.

![](/help/assets/chlimage_1-90.png)

* **Typen** Hoe de opties worden weergegeven

   * **Selectievakjes**
   * **Keuzerondjes**
   * **Vervolgkeuzelijst**
   * **Vervolgkeuzelijst Multi-select**

* **Titel** - De titel die als label voor de opties wordt weergegeven
* **Naam** - De naam van het veld dat met de formuliergegevens is verzonden
* **Bron** - Waar zijn de opties gedefinieerd

   * **Lokaal** - Gedefinieerd binnen de component
      * Tik of klik op de knop **Toevoegen** om een waarde toe te voegen, **verwijder** om een waarde te verwijderen
      * **Waarde** - De waarde die wordt opgeslagen wanneer die optie wordt geselecteerd wanneer het formulier wordt verzonden
      * **Tekst** - Het label voor de optie die op het formulier wordt weergegeven
      * **Actief** - De optie wordt gemarkeerd als geselecteerd wanneer het formulier wordt geladen
      * **Uitgeschakeld** - De optie kan niet worden geselecteerd, maar wordt wel weergegeven
      * **List** - Een statische lijst die elders in AEM is gedefinieerd, wordt gebruikt voor de optie
         * **List** - Het pad van de statische lijst in AEM
            * Gebruik de Browse knoop om van het lijstmiddel de plaats te bepalen
      * **Gegevensbron** - Een gegevensbron wordt gebruikt voor de opties
         * **Gegevensbron** - brontype van de gegevensbron
* **Help-bericht** - Een tip voor de gebruiker wat in het veld kan worden ingevoerd

## Ontwerpdialoogvenster {#design-dialog}

Er is geen dialoogvenster voor het ontwerp van de component Formulieropties.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Opties van de Vorm [kan op GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v1/options)worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.
