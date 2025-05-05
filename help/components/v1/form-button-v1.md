---
title: Component Formulierknop (v1)
description: Met de component Core Component Form Hidden kunt u een verborgen veld in een formulier opnemen.
index: n
role: Architect, Developer, Admin, User
exl-id: 2c06a942-7ac5-4847-9d11-7bbcd0ea51bd
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Component Formulierknop (v1) {#form-button-component-v}

Met de component Core Component Form Button kunt u een knopveld in een formulier opnemen om een handeling te activeren.

## Gebruik {#usage}

De component van de Knoop van de Vorm van de Component van de Kern staat voor de verwezenlijking van knoopgebied toe, vaak om de voorlegging van de vorm teweeg te brengen en is bedoeld om samen met de [ component van de vormcontainer ](form-container-v1.md) worden gebruikt.

De knoopeigenschappen kunnen door de inhoudsredacteur in [ worden bepaald vormen dialoog ](#configure-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Form Button-component beschreven, die oorspronkelijk werd geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van versie 1 van de component Formulierknop weergegeven.

| AEM | Formulierknopcomponent v1 |
|--- |--- |
| 6,3 | Compatibel |
| 6,4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Form Button beschreven.
>
>Voor details van de huidige versie van de Component van de Knoop van de Vorm, zie het [&#128279;](/help/components/forms/form-button.md) document van de Component van de Knoop van de Vorm 0&rbrace; &lbrace;.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende wordt steekproef genomen van [ We.Retail ](https://helpx.adobe.com/nl/experience-manager/6-4/sites/developing/using/we-retail.html).

### Schermafbeelding {#screenshot}

![](/help/assets/chlimage_1-48.png)

### HTML {#html}

```
<div class="cmp cmp-button aem-GridColumn aem-GridColumn--default--12">
    <div class="cmp cmp-button">
        <button type="BUTTON" class="btn btn-action btn-primary" name="loveToast" value="ILoveToast">
            Click here if you love toast!
        </button>
    </div>
</div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "button": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/button",
                  "name": "loveToast",
                  "jcr:title": "Click here if you love toast!",
                  "type": "submit",
                  "value": "ILoveToast"
                }
              },
              ":itemsOrder": [
                "button"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Gelieve te zien de [ verenigbaarheidsinformatie voor de Componenten van de Kern v1 ](/help/versions.md) voor meer informatie.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud de parameters van de knop definiëren.

![](/help/assets/chlimage_1-49.png)

* **Type**
   * **Knoop**
   * **voorleggen**

* **Titel** - de tekst die op de knoop wordt getoond
   * Als er niets is opgegeven, wordt het knoptype standaard ingesteld

* **Naam** - de naam van de knoop, die met de vormgegevens wordt voorgelegd
* **Waarde** - de waarde van de knoop, die met de vormgegevens wordt voorgelegd

## Ontwerpdialoogvenster {#design-dialog}

Er is geen dialoogvenster voor het ontwerp van de component Form Button.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Knoop van de Vorm [ kan op GitHub ](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button) worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).
