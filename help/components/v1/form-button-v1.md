---
title: Component Formulierknop (v1)
description: Met de component Core Component Form Hidden kunt u een verborgen veld in een formulier opnemen.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Component Formulierknop (v1) {#form-button-component-v}

Met de component Core Component Form Button kunt u een knopveld in een formulier opnemen om een handeling te activeren.

## Gebruik {#usage}

Met de component Knop voor kerncomponentformulieren kunt u knopveld maken, vaak om het verzenden van het formulier te starten en wordt deze component samen met de [formuliercontainercomponent](form-container-v1.md)gebruikt.

De knoopeigenschappen kunnen door de inhoudsredacteur in [vormen dialoog](#configure-dialog)worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Form Button-component beschreven, die oorspronkelijk werd geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van versie 1 van de component Formulierknop weergegeven.

| AEM-versie | Formulierknopcomponent v1 |
|--- |--- |
| 6.3 | Compatibel |
| 6.4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Form Button beschreven.
>
>Zie het document [Component](/help/components/forms/form-button.md) Form Button voor meer informatie over de huidige versie van de component Form Button.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Hier volgt een voorbeeld van [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Zie de [compatibiliteitsinformatie voor Core Components v1](/help/versions.md) voor meer informatie.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud de parameters van de knop definiëren.

![](/help/assets/chlimage_1-49.png)

* **Type**
   * **Knop**
   * **Verzenden**

* **Titel** - De tekst die op de knop wordt weergegeven
   * Als er niets is opgegeven, wordt het knoptype standaard ingesteld

* **Naam** - De naam van de knop die samen met de formuliergegevens wordt verzonden
* **Waarde** - De waarde van de knop die samen met de formuliergegevens wordt verzonden

## Ontwerpdialoogvenster {#design-dialog}

Er is geen dialoogvenster voor het ontwerp van de component Form Button.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Knoop van de Vorm [kan op GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button)worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.
