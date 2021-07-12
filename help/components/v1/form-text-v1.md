---
title: Formuliertekstcomponent (v1)
description: Met de component Tekst van formulier voor kerncomponenttekst kan formuliertekst worden verzonden.
index: n
role: Architect, Developer, Admin, User
exl-id: d6fbc596-cb42-4478-8a3c-aa5aead3be0a
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 1%

---

# Formuliertekstcomponent (v1) {#form-text-component-v}

Met de component Tekst van formulier voor kerncomponenttekst kan formuliertekst worden verzonden.

## Gebruik {#usage}

De component van de Tekst van de Vorm staat voor de voorlegging van verschillende types van tekst toe en is bedoeld om samen met de [component van de vormcontainer ](form-container-v1.md) worden gebruikt.

Het type van tekstbevestiging, etiketten, en hulpberichten kunnen door de inhoudsredacteur in [vorm dialoog](#configure-dialog) worden bepaald.

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
>Zie het document [Form Text Component](/help/components/forms/form-text.md) voor meer informatie over de huidige versie van Form Text Component.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende voorbeeld wordt genomen uit [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Zie [compatibiliteitsinformatie voor Core Components v1](/help/versions.md) voor meer informatie.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het type tekst definiëren dat moet worden ingevoerd, evenals standaardwaarden en -labels.

### Hoofd {#main}

![](/help/assets/chlimage_1-23.png)

* **Restrictie**  - Het type tekst dat moet worden ingevoerd en waartegen moet worden gevalideerd

   * **Tekst**
   * **Tekstgebied**
   * **E-mail**
   * **Tel**
   * **Date**
   * **Getal**
   * **Wachtwoord**

* **Tekstregels**  - Aantal regels dat in het tekstgebied moet worden weergegeven (alleen wordt weergegeven wanneer  **** Restricties zijn ingesteld op  **Tekstgebied**)

* **Label**  - Het label dat voor het veld wordt weergegeven
* **Het label verbergen zodat het niet kan worden weergegeven** . Dit is nodig als het label alleen nodig is voor toegankelijkheidsdoeleinden en geen aanvullende visuele informatie over het veld bevat
* **Elementnaam**  - De naam van het veld dat met de formuliergegevens wordt verzonden
* **Waarde**  - Standaardwaarde die vooraf in het veld is ingevuld

### Info {#about}

![](/help/assets/chlimage_1-24.png)

* **Help-bericht**  - Een tip voor de gebruiker wat in het veld kan worden ingevoerd
* **Help-bericht weergeven als tijdelijke aanduiding**  - Het Help-bericht weergeven in de formulierinvoer als het leeg en niet gefocust is

### Restricties {#constraints}

![](/help/assets/chlimage_1-25.png)

* **Restrictiebericht**

   * Bericht weergegeven als knopinfo bij het verzenden van het formulier als de waarde het gekozen type niet valideert
   * Niet weergegeven voor restrictietypen **Tekst** en **Tekstgebied**

* **Vereist**  - Als deze optie is geselecteerd, moet de gebruiker een waarde invullen voordat het formulier wordt verzonden
* **Alleen** -lezen maken - Als deze optie is geselecteerd, kan de gebruiker de waarde van het veld niet wijzigen

## Ontwerpdialoogvenster {#design-dialog}

Er is geen ontwerpdialoogvenster voor de component Formuliertekst.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Tekst van de Vorm [kan op GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text) worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).
