---
title: Component Formulieropties (v1)
description: Met de component Core Component Form Options kunt u vooraf gedefinieerde opties in verschillende indelingen selecteren.
index: n
role: Architect, Developer, Admin, User
exl-id: a5e8656b-eddd-48ec-876b-39bbaa70edf6
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Component Formulieropties (v1) {#form-options-component-v}

Met de component Core Component Form Options kunt u vooraf gedefinieerde opties in verschillende indelingen selecteren.

## Gebruik {#usage}

De component van de Opties van de Vorm van de Component van de Kern staat voor de voorlegging van verschillende types van opties toe die op vele verschillende manieren worden voorgesteld en is bedoeld om samen met de [ component van de vormcontainer ](form-container-v1.md) worden gebruikt.

De presentatie van de opties, de etiketten, en de individuele opties kunnen door de inhoudsredacteur in [ worden bepaald vormt dialoog ](#configure-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de component Formulieropties beschreven, die oorspronkelijk is geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van versie 1 van de component Formulieropties weergegeven.

| Componentversie | AEM 6,3 | AEM 6,4 |
|--- |--- |--- |
| v2 | Compatibel | Compatibel |
| v1 | Compatibel | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Formulieropties beschreven.
>
>Voor details van de huidige versie van de Component van de Opties van de Vorm, zie het ](/help/components/forms/form-options.md) document van de Component van de Opties van de Vorm 0} {.[

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende wordt steekproef genomen van [ We.Retail ](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Gelieve te zien de [ verenigbaarheidsinformatie voor de Componenten van de Kern v1 ](/help/versions.md) voor meer informatie.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het type opties definiëren dat moet worden weergegeven, de labels en de beschikbare opties.

![](/help/assets/chlimage_1-90.png)

* **Types**
Hoe de opties worden weergegeven

   * **Checkboxes**
   * **Keuzerondjes**
   * **drop-down**
   * **multi-uitgezochte drop-down**

* **Titel** - de titel die als etiket voor de opties zal worden getoond
* **Naam** - de naam van het gebied dat met de vormgegevens wordt voorgelegd
* **Source** - waar de opties worden bepaald

   * **Lokaal** - die binnen de component wordt bepaald
      * Tik of klik **voeg** knoop toe om een waarde toe te voegen, **Schrapping** om een waarde te verwijderen
      * **Waarde** - de waarde bewaard wanneer die optie wordt geselecteerd wanneer de vorm wordt voorgelegd
      * **Tekst** - het etiket voor de optie die op de vorm wordt getoond
      * **Actief** - de optie wordt duidelijk zoals geselecteerd wanneer de vorm laadt
      * **Gehandicapten** - de optie is niet selecteerbaar maar nog getoond
      * **Lijst** - een statische die lijst elders in AEM wordt bepaald wordt gebruikt voor de optie
         * **Lijst** - de weg van de statische lijst in AEM
            * Gebruik de Browse knoop om van het lijstmiddel de plaats te bepalen
      * **Gegevensbron** - een gegevensbron wordt gebruikt voor de opties
         * **Gegevensbron** - middeltype van de gegevensbron
* **het bericht van de Hulp** - een wenk voor de gebruiker van wat op het gebied kan zijn ingegaan

## Ontwerpdialoogvenster {#design-dialog}

Er is geen dialoogvenster voor het ontwerp van de component Formulieropties.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Opties van de Vorm [ kan op GitHub ](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v1/options) worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).
