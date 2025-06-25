---
title: Formulier verborgen component (v1)
description: Met de component Core Component Form Hidden kunt u een verborgen veld weergeven.
index: n
role: Architect, Developer, Admin, User
exl-id: 8e30dac0-5b4b-4fc7-af99-5791c98c90bf
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# Formulier verborgen component (v1) {#form-hidden-component-v}

Met de component Core Component Form Hidden kunt u een verborgen veld weergeven.

## Gebruik {#usage}

De Verborgen Component van de Component van de Kern staat voor de verwezenlijking van verborgen gebieden toe om informatie over de huidige pagina terug naar AEM over te gaan en is bedoeld om samen met de [ component van de vormcontainer ](form-container-v1.md) worden gebruikt.

De gebiedseigenschappen kunnen door de inhoudsredacteur in [ worden bepaald vormen dialoog ](#configure-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Form Hidden Component beschreven, die oorspronkelijk werd geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van versie 1 van de component Formulier verborgen weergegeven.

| AEM-versie | Verborgen component van formulier v1 |
|--- |--- |
| 6,3 | Compatibel |
| 6,4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Formulier verborgen beschreven.
>
>Voor details van de huidige versie van de Vorm Verborgen Component, zie het [ Verborgen Component van de Vorm ](/help/components/forms/form-hidden.md) document.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende wordt steekproef genomen van [ We.Retail ](https://helpx.adobe.com/nl/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Gelieve te zien de [ verenigbaarheidsinformatie voor de Componenten van de Kern v1 ](/help/versions.md#release-history-and-compatibility) voor meer informatie.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud de parameters van het verborgen veld definiëren.

![](/help/assets/chlimage_1-26.png)

* **Naam** - de naam van het gebied, dat met de vormgegevens wordt voorgelegd
* **Waarde** - de waarde van het gebied, dat met de vormgegevens wordt voorgelegd
* **Identifier** - het herkenningsteken zou op de pagina uniek moeten zijn en kan worden gebruikt om manuscripten aan dit vormgebied te binden

## Ontwerpdialoogvenster {#design-dialog}

Er is geen dialoogvenster voor het ontwerp van de component Formulier verborgen.

## Technische details {#technical-details}

De recentste technische documentatie over de Vorm Verborgen Component [ kan op GitHub ](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden) worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).
