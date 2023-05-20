---
title: Titelcomponent (v2)
description: De component van de Titel van de Component van de Kern is een component van de sectiekop die op zijn plaats het uitgeven kenmerkt.
role: Architect, Developer, Admin, User
exl-id: f853ec46-19fd-4569-a9d3-5c376d2a2101
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---

# Titelcomponent (v2) {#title-component}

De component van de Titel van de Component van de Kern is een component van de sectiekop die op zijn plaats het uitgeven kenmerkt.

## Gebruik {#usage}

De component Titel is bedoeld voor gebruik als de titel of koptekst van een sectie met inhoud. De beschikbare kopniveaus kunnen door de sjabloonauteur in het dialoogvenster [ontwerpdialoogvenster](#design-dialog). De inhoudeditor kan een keuze maken uit beschikbare koptekstniveaus in het dialoogvenster [dialoogvenster bewerken](#edit-dialog). Voor meer gemak is het ook mogelijk de koptekst eenvoudig op locatie te bewerken.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 2 van de component Title beschreven, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 2 van de component Title beschreven.
>
>Voor meer informatie over de huidige versie van de component Title raadpleegt u de [Component Title](/help/components/title.md) document.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de component Title wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_title).

### Technische details {#technical-details}

De meest recente technische documentatie over de component Title [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_title_v2).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de titeltekst definiëren en het kopniveau selecteren.

* **Titel** - Als de paginatitel leeg is, wordt deze gebruikt
* **Tekst/grootte** - Definieert het kopniveau van de titel
* **Koppeling** - Hiermee definieert u de inhoud waaraan de titel wordt gekoppeld. Dit kan een pad zijn naar een inhoudspagina, een externe URL of een pagina-anker.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

![Dialoogvenster voor bewerken van titelcomponent](/help/assets/title-edit.png)

>[!NOTE]
>
>De capaciteit om een verbinding voor de titel te bepalen werd geïntroduceerd met versie 2.2.0 van de Componenten van de Kern.

U kunt de editor op zijn plaats ook gebruiken om de tekst van de titelcomponent te bewerken.

![Lokaal bewerken van component Title](/help/assets/title-edit-inline.png)

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur het standaardkopniveau definiëren dat titelcomponenten hebben wanneer ze door de auteurs van de inhoud worden gemaakt.

### Tabblad Grootte {#sizes-tab}

![Ontwerpdialoogvenster van component Title](/help/assets/title-design.png)

* **Toegestane typen/grootten voor auteurs** - Schakel koptypen in of uit die beschikbaar zijn voor auteurs van inhoud wanneer zij de component Titel gebruiken.
* **Standaardtype/grootte**- Definieer het koptype dat automatisch wordt toegewezen wanneer een auteur van de inhoud de component Titel aan een pagina toevoegt.
* **Koppeling uitschakelen**- Schakel ondersteuning voor koppelingen in de component title uit om te voorkomen dat auteurs van inhoud koppelingen naar titels maken.

>[!NOTE]
>
>De capaciteit om een verbinding voor de titel te bepalen werd geïntroduceerd met versie 2.2.0 van de Componenten van de Kern.

### Tabblad Stijlen {#styles-tab}

De component Title ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component Title ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
