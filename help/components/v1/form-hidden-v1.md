---
title: Formulier verborgen component (v1)
description: Met de component Core Component Form Hidden kunt u een verborgen veld weergeven.
index: n
role: Architect, Developer, Admin, User
exl-id: 8e30dac0-5b4b-4fc7-af99-5791c98c90bf
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Formulier verborgen component (v1) {#form-hidden-component-v}

Met de component Core Component Form Hidden kunt u een verborgen veld weergeven.

## Gebruik {#usage}

Met de component Core Component Form Hidden kunt u verborgen velden maken die informatie over de huidige pagina teruggeven aan AEM en die samen met de [formuliercontainercomponent](form-container-v1.md).

De veldeigenschappen kunnen worden gedefinieerd door de inhoudeditor in het dialoogvenster [dialoogvenster configureren](#configure-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Form Hidden Component beschreven, die oorspronkelijk werd geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van versie 1 van de component Formulier verborgen weergegeven.

| AEM | Verborgen component van formulier v1 |
|--- |--- |
| 6.3 | Compatibel |
| 6.4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Formulier verborgen beschreven.
>
>Voor meer informatie over de huidige versie van de component Form Hidden raadpleegt u de [Verborgen component van formulier](/help/components/forms/form-hidden.md) document.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende monster wordt genomen uit [Wij.Detailhandel](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
  <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
   <div class="visible aem-GridColumn aem-GridColumn--default--12">
    <input type="hidden" id="ghostToast" name="Invisible Toast" value="ghostToast">
   </div>
 </form>
</div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "hidden": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/hidden",
                  "name": "Invisible Toast",
                  "id": "ghostToast",
                  "value": "ghostToast"
                }
              },
              ":itemsOrder": [
                "hidden"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Zie de [compatibiliteitsinformatie voor Core Components v1](/help/versions.md#release-history-and-compatibility) voor meer informatie .

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud de parameters van het verborgen veld definiëren.

![](/help/assets/chlimage_1-26.png)

* **Naam** - De naam van het veld dat met de formuliergegevens wordt verzonden
* **Waarde** - De waarde van het veld, dat met de formuliergegevens wordt verzonden
* **Id** - De id moet uniek zijn op de pagina en kan worden gebruikt om scripts te binden aan dit formulierveld

## Ontwerpdialoogvenster {#design-dialog}

Er is geen dialoogvenster voor het ontwerp van de component Formulier verborgen.

## Technische details {#technical-details}

De meest recente technische documentatie over de component Form Hidden [kan op GitHub worden gevonden](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).
