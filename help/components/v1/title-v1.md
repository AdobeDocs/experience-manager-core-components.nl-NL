---
title: Titelcomponent (v1)
description: De component van de Titel van de Component van de Kern is een component van de sectiekop die op zijn plaats het uitgeven kenmerkt.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Titelcomponent (v1) {#title-component-v}

De component van de Titel van de Component van de Kern is een component van de sectiekop die op zijn plaats het uitgeven kenmerkt.

## Gebruik {#usage}

De component Titel is bedoeld voor gebruik als de titel of koptekst van een sectie met inhoud.

De beschikbare kopniveaus kunnen door de sjabloonauteur in het [ontwerpdialoogvenster](#design-dialog)worden gedefinieerd. De inhoudeditor kan kiezen uit beschikbare koptekstniveaus in het dialoogvenster [](#edit-dialog)Bewerken. Voor meer gemak is het ook mogelijk de koptekst eenvoudig op locatie te bewerken.

## Versie en compatibiliteit {#version-and-compatibility}

Dit document beschrijft v1 van de Component van de Titel, oorspronkelijk geïntroduceerd met versie 1.0.0 van de Componenten van de Kern met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van v1 van de component Title weergegeven.

| AEM-versie | Titelcomponent v1 |
|--- |--- |
| 6.3 | Compatibel |
| 6.4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Title beschreven.
>
>Zie het document [Titel Component](/help/components/title.md) voor meer informatie over de huidige versie van Title Component.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Hier volgt een voorbeeld van [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Schermafbeelding {#screenshot}

![](/help/assets/chlimage_1-36.png)

### HTML {#html}

```
<div class="cmp cmp-title aem-GridColumn aem-GridColumn--default--12">
     <h2>Welcome! This is our finest equipment!</h2>
</div>
```

### JSON {#json}

```
"title": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/title",
              "jcr:title": "Welcome! This is our finest equipment!",
              "type": "h2"
            }
```

>[!NOTE]
>
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Zie de [compatibiliteitsinformatie voor Core Components v1](/help/versions.md) voor meer informatie.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de titeltekst definiëren en het kopniveau selecteren.

>[!NOTE]
>
>Als de titel een lege waarde heeft, wordt de paginatitel weergegeven.

![](/help/assets/chlimage_1-91.png)

U kunt de editor op zijn plaats ook gebruiken om de tekst van de titelcomponent te bewerken.

![](/help/assets/chlimage_1-37.png)

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur het standaardkopniveau definiëren dat titelcomponenten hebben wanneer ze door de auteurs van de inhoud worden gemaakt.

![](/help/assets/chlimage_1-92.png)

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Titel [kan op GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title)worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.
