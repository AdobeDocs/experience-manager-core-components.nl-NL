---
title: Formuliertekstcomponent (v1)
description: Met de component Tekst van formulier voor kerncomponenttekst kan formuliertekst worden verzonden.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Formuliertekstcomponent (v1) {#form-text-component-v}

Met de component Tekst van formulier voor kerncomponenttekst kan formuliertekst worden verzonden.

## Gebruik {#usage}

Met de component Formuliertekst kunt u verschillende typen tekst verzenden. Deze component is bedoeld voor gebruik samen met de [component](form-container-v1.md)van de formuliercontainer.

Het type van tekstbevestiging, etiketten, en hulpberichten kunnen door de inhoudsredacteur in [vormen dialoog](#configure-dialog)worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Form Text Component beschreven, die oorspronkelijk werd geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van versie 1 van de component Formuliertekst weergegeven.

| AEM-versie | Formuliertekstcomponent v1 |
|--- |--- |
| 6.3 | Compatibel |
| 6.4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Formuliertekst beschreven.
>
>Zie het document [Form Text Component](/help/components/forms/form-text.md) voor meer informatie over de huidige versie van Form Text Component.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Hier volgt een voorbeeld van [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Zie de [compatibiliteitsinformatie voor Core Components v1](/help/versions.md) voor meer informatie.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het type tekst definiëren dat moet worden ingevoerd, evenals standaardwaarden en -labels.

### Hoofd {#main}

![](/help/assets/chlimage_1-23.png)

* **Restrictie** - Het type tekst dat moet worden ingevoerd en waartegen moet worden gevalideerd

   * **Tekst**
   * **Tekstgebied**
   * **E-mail**
   * **Tel**
   * **Date**
   * **Getal**
   * **Wachtwoord**

* **Tekstregels** - Aantal regels dat in het tekstgebied moet worden weergegeven (wordt alleen weergegeven wanneer **Restrictie** is ingesteld op **Tekstgebied**)

* **Label** - Het label dat voor het veld wordt weergegeven
* **Het label verbergen zodat het niet kan worden weergegeven** - Dit is nodig als het label alleen nodig is voor toegankelijkheidsdoeleinden en geen aanvullende visuele informatie over het veld bevat
* **Elementnaam** - De naam van het veld dat met de formuliergegevens wordt verzonden
* **Waarde** - Standaardwaarde die vooraf in het veld is ingevuld

### Info {#about}

![](/help/assets/chlimage_1-24.png)

* **Help-bericht** - Een tip voor de gebruiker wat in het veld kan worden ingevoerd
* **Help-bericht weergeven als tijdelijke aanduiding** - Het Help-bericht weergeven in de formulierinvoer als deze leeg en niet geconcentreerd is

### Restricties {#constraints}

![](/help/assets/chlimage_1-25.png)

* **Restrictiebericht**

   * Bericht weergegeven als knopinfo bij het verzenden van het formulier als de waarde het gekozen type niet valideert
   * Niet weergegeven voor restrictietypen **Tekst** en **Tekstgebied**

* **Vereist** - Als deze optie is geselecteerd, moet de gebruiker een waarde invullen voordat het formulier wordt verzonden
* **Alleen** -lezen maken - Als deze optie is geselecteerd, kan de gebruiker de waarde van het veld niet wijzigen

## Ontwerpdialoogvenster {#design-dialog}

Er is geen ontwerpdialoogvenster voor de component Formuliertekst.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Tekst van de Vorm [kan op GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text)worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.
