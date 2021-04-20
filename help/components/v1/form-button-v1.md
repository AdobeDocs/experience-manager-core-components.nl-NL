---
title: Component Formulierknop (v1)
description: Met de component Core Component Form Hidden kunt u een verborgen veld in een formulier opnemen.
index: n
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 2%

---


# Formulierknopcomponent (v1) {#form-button-component-v}

Met de component Core Component Form Button kunt u een knopveld in een formulier opnemen om een handeling te activeren.

## Gebruik {#usage}

De component van de Knoop van de Vorm van de Component van de Kern staat voor de verwezenlijking van knoopgebied toe, vaak om de voorlegging van de vorm teweeg te brengen en is bedoeld om samen met de [component van de vormcontainer](form-container-v1.md) worden gebruikt.

De knoopeigenschappen kunnen door de inhoudsredacteur in [vormen dialoog](#configure-dialog) worden bepaald.

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
>Zie het document [Form Button Component](/help/components/forms/form-button.md) voor meer informatie over de huidige versie van de Form Button Component.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende voorbeeld wordt genomen uit [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

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
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Zie [compatibiliteitsinformatie voor Core Components v1](/help/versions.md) voor meer informatie.

## Dialoogvenster {#configure-dialog} configureren

In het dialoogvenster voor configureren kan de auteur van de inhoud de parameters van de knop definiëren.

![](/help/assets/chlimage_1-49.png)

* **Type**
   * **Knop**
   * **Verzenden**

* **Titel**  - De tekst die op de knop wordt weergegeven
   * Als er niets is opgegeven, wordt het knoptype standaard ingesteld

* **Naam**  - De naam van de knop die samen met de formuliergegevens wordt verzonden
* **Waarde**  - De waarde van de knop die samen met de formuliergegevens wordt verzonden

## Ontwerpdialoogvenster {#design-dialog}

Er is geen dialoogvenster voor het ontwerp van de component Form Button.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Knoop van de Vorm [kan op GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button) worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).
