---
title: Component Formulieropties (v1)
description: Met de component Core Component Form Options kunt u vooraf gedefinieerde opties in verschillende indelingen selecteren.
index: n
role: Architect, Developer, Admin, User
exl-id: a5e8656b-eddd-48ec-876b-39bbaa70edf6
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# Component Formulieropties (v1) {#form-options-component-v}

Met de component Core Component Form Options kunt u vooraf gedefinieerde opties in verschillende indelingen selecteren.

## Gebruik {#usage}

Met de component Core Component Form Options kunnen verschillende typen opties worden ingediend die op verschillende manieren worden gepresenteerd. Deze component is bedoeld om samen met de component [formuliercontainercomponent](form-container-v1.md).

De presentatie van de opties, labels en afzonderlijke opties kan worden gedefinieerd door de inhoudseditor in het dialoogvenster [dialoogvenster configureren](#configure-dialog).

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
>Voor meer informatie over de huidige versie van de component Formulieropties raadpleegt u de [Component Formulieropties](/help/components/forms/form-options.md) document.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende monster wordt genomen uit [Wij.Detailhandel](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Zie de [compatibiliteitsinformatie voor Core Components v1](/help/versions.md) voor meer informatie .

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het type opties definiëren dat moet worden weergegeven, de labels en de beschikbare opties.

![](/help/assets/chlimage_1-90.png)

* **Typen**
Hoe de opties worden weergegeven

   * **Selectievakjes**
   * **Keuzerondjes**
   * **Vervolgkeuzelijst**
   * **Vervolgkeuzelijst Multi-select**

* **Titel** - De titel die wordt weergegeven als het label voor de opties
* **Naam** - De naam van het veld dat met de formuliergegevens wordt verzonden
* **Bron** - Waar de opties zijn gedefinieerd

   * **Lokaal** - Gedefinieerd binnen de component
      * Tik of klik op de knop **Toevoegen** knop om een waarde toe te voegen, **Verwijderen** om een waarde te verwijderen
      * **Waarde** - De waarde die wordt opgeslagen wanneer deze optie wordt geselecteerd wanneer het formulier wordt verzonden
      * **Tekst** - Het label voor de optie die op het formulier wordt weergegeven
      * **Actief** - De optie wordt gemarkeerd als geselecteerd wanneer het formulier wordt geladen
      * **Uitgeschakeld** - De optie kan niet worden geselecteerd, maar wordt wel weergegeven
      * **Lijst** - Een statische lijst die elders in AEM is gedefinieerd, wordt gebruikt voor de optie
         * **Lijst** - Het pad van de statische lijst in AEM
            * Gebruik de Browse knoop om van het lijstmiddel de plaats te bepalen
      * **Gegevensbron** - Een gegevensbron wordt gebruikt voor de opties
         * **Gegevensbron** - soort bron van de gegevensbron
* **Help-bericht** - Een tip voor de gebruiker wat in het veld kan worden ingevoerd

## Ontwerpdialoogvenster {#design-dialog}

Er is geen dialoogvenster voor het ontwerp van de component Formulieropties.

## Technische details {#technical-details}

De meest recente technische documentatie over de component Formulieropties [kan op GitHub worden gevonden](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v1/options).

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).
