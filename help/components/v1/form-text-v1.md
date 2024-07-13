---
title: Formuliertekstcomponent (v1)
description: Met de component Tekst van formulier voor kerncomponenttekst kan formuliertekst worden verzonden.
index: n
role: Architect, Developer, Admin, User
exl-id: d6fbc596-cb42-4478-8a3c-aa5aead3be0a
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---

# Formuliertekstcomponent (v1) {#form-text-component-v}

Met de component Tekst van formulier voor kerncomponenttekst kan formuliertekst worden verzonden.

## Gebruik {#usage}

De Component van de Tekst van de Vorm staat voor de voorlegging van verschillende types van tekst toe en is bedoeld om samen met de [ component van de vormcontainer ](form-container-v1.md) worden gebruikt.

Het type van tekstbevestiging, etiketten, en hulpberichten kunnen door de inhoudsredacteur in [ worden bepaald vormen dialoog ](#configure-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Form Text Component beschreven, die oorspronkelijk werd geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van versie 1 van de component Formuliertekst weergegeven.

| AEM | Formuliertekstcomponent v1 |
|--- |--- |
| 6,3 | Compatibel |
| 6,4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Formuliertekst beschreven.
>
>Voor details van de huidige versie van de Component van de Tekst van de Vorm, zie het ](/help/components/forms/form-text.md) document van de Component van de Tekst van de Vorm 0} {.[

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende wordt steekproef genomen van [ We.Retail ](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Schermafbeelding {#screenshot}

![](/help/assets/chlimage_1-22.png)

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
     <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
     <div class="cmp cmp-form-field aem-GridColumn aem-GridColumn--default--12">
   <div class="form-group">
       <label for="form-text-978484744">How many pieces of toast would you like?</label>
          <input type="number" id="form-text-978484744" name="pieces">
   </div>
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
                "text": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/text",
                  "name": "piecesOfToast",
                  "jcr:title": "How many pieces of toast would you like?",
                  "type": "number",
                  "rows": "2"
                }
              },
              ":itemsOrder": [
                "text"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Gelieve te zien de [ verenigbaarheidsinformatie voor de Componenten van de Kern v1 ](/help/versions.md) voor meer informatie.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het type tekst definiëren dat moet worden ingevoerd, evenals standaardwaarden en -labels.

### Hoofd {#main}

![](/help/assets/chlimage_1-23.png)

* **Beperking** - het type van tekst dat moet worden ingevoerd en tegen zal worden bevestigd

   * **Tekst**
   * **Gebied van de Tekst**
   * **E-mail**
   * **Tel**
   * **Datum**
   * **Aantal**
   * **Wachtwoord**

* **lijnen van de Tekst** - Aantal lijnen die op het tekstgebied (slechts getoond worden wanneer **Beperking** aan **Gebied van de Tekst** wordt geplaatst)

* **Etiket** - het etiket dat voor het gebied zal worden getoond
* **Verberg het etiket wordt getoond** - Nodig als het etiket slechts voor toegankelijkheidsdoeleinden wordt vereist en geen extra visuele informatie over het gebied impart
* **Naam van het Element** - de naam van het gebied dat met de vormgegevens wordt voorgelegd
* **Waarde** - Gebrek waarde die op het gebied pre-bevolkt is

### Info {#about}

![](/help/assets/chlimage_1-24.png)

* **Bericht van de Hulp** - een wenk aan de gebruiker van wat op het gebied kan zijn ingegaan
* **het hulpbericht van de Vertoning als placeholder** - om het hulpbericht binnen de vorminput te tonen wanneer het leeg en niet geconcentreerd is

### Restricties {#constraints}

![](/help/assets/chlimage_1-25.png)

* **Bericht van de Beperking**

   * Bericht weergegeven als knopinfo bij het verzenden van het formulier als de waarde het gekozen type niet valideert
   * Niet getoond voor **Tekst** en **de beperkingstypes van het Gebied van de Tekst**

* **Vereist** - als geselecteerd de gebruiker een waarde moet invullen alvorens de vorm voor te leggen
* **maak slechts lezen** - als geselecteerd kan de gebruiker niet de waarde van het gebied wijzigen

## Ontwerpdialoogvenster {#design-dialog}

Er is geen ontwerpdialoogvenster voor de component Formuliertekst.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Tekst van de Vorm [ kan op GitHub ](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text) worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).
