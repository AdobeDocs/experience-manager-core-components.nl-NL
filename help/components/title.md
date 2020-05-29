---
title: Component Title
description: De component van de Titel van de Component van de Kern is een component van de sectiekop die op zijn plaats het uitgeven kenmerkt.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 1%

---


# Component Title{#title-component}

De component van de Titel van de Component van de Kern is een component van de sectiekop die op zijn plaats het uitgeven kenmerkt.

## Gebruik {#usage}

De component Titel is bedoeld voor gebruik als de titel of koptekst van een sectie met inhoud. De beschikbare kopniveaus kunnen door de sjabloonauteur in het [ontwerpdialoogvenster](#design-dialog)worden gedefinieerd. De inhoudeditor kan kiezen uit beschikbare koptekstniveaus in het dialoogvenster [](#edit-dialog)Bewerken. Voor meer gemak is het ook mogelijk de koptekst eenvoudig op locatie te bewerken.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Title is v2, die in januari 2018 is geïntroduceerd met release 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|---|
| v2 | - | Compatibel | Compatibel | Compatibel |
| [v1](v1/title-v1.md) | Compatibel | Compatibel | Compatibel | - |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_title)om de component Title te ervaren en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Titel [kan op GitHub](https://adobe.com/go/aem_cmp_tech_title_v2)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de titeltekst definiëren en het kopniveau selecteren.

* **Titel** - Als de paginatitel leeg is, wordt deze gebruikt
* **Type/Grootte** - Hiermee definieert u het kopniveau van de titel
* **Koppeling** - Hiermee definieert u de inhoud waaraan de titel wordt gekoppeld. Dit kan een pad zijn naar een inhoudspagina, een externe URL of een pagina-anker.
* **ID** - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [gegevenslaag](/help/developing/data-layer/overview.md).
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
* **Standaardtype / Grootte**- Definieer het koptype dat automatisch wordt toegewezen wanneer een auteur van de inhoud de component Titel aan een pagina toevoegt.
* **Koppeling** uitschakelen - Schakel ondersteuning voor koppelingen in de titelcomponent uit om te voorkomen dat auteurs van inhoud koppelingen maken van titels.

>[!NOTE]
>
>De capaciteit om een verbinding voor de titel te bepalen werd geïntroduceerd met versie 2.2.0 van de Componenten van de Kern.

### Tabblad Stijlen {#styles-tab}

De component Title ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).
