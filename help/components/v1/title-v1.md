---
title: Titelcomponent (v1)
description: De component van de Titel van de Component van de Kern is een component van de sectiekop die op zijn plaats het uitgeven kenmerkt.
index: n
role: Architect, Developer, Admin, User
exl-id: 79549ac0-82f2-4ea0-9cce-d534d0b47b5c
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---


# Titelcomponent (v1) {#title-component-v}

De component van de Titel van de Component van de Kern is een component van de sectiekop die op zijn plaats het uitgeven kenmerkt.

## Gebruik {#usage}

De component Titel is bedoeld voor gebruik als de titel of koptekst van een sectie met inhoud.

De beschikbare rubriekniveaus kunnen door de malplaatjeauteur in de [ ontwerpdialoog ](#design-dialog) worden bepaald. De inhoudsredacteur kan uit beschikbare rubrieken in [ selecteren uitgeeft dialoog ](#edit-dialog). Voor meer gemak is het ook mogelijk de koptekst eenvoudig op locatie te bewerken.

## Versie en compatibiliteit {#version-and-compatibility}

Dit document beschrijft v1 van de Component van de Titel, oorspronkelijk geïntroduceerd met versie 1.0.0 van de Componenten van de Kern met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van v1 van de component Title weergegeven.

| AEM-versie | Titelcomponent v1 |
|--- |--- |
| 6,3 | Compatibel |
| 6,4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Title beschreven.
>
>Voor details van de huidige versie van de Component van de Titel, zie het [&#128279;](/help/components/title.md) document van de Component van de Titel 0&rbrace; &lbrace;.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende wordt steekproef genomen van [ We.Retail ](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Gelieve te zien de [ verenigbaarheidsinformatie voor de Componenten van de Kern v1 ](/help/versions.md) voor meer informatie.

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

De recentste technische documentatie over de Component van de Titel [ kan op GitHub ](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title) worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).
