---
title: Component Title
description: De component van de Titel van de Component van de Kern is een component van de sectiekop die op zijn plaats het uitgeven kenmerkt.
role: Architect, Developer, Admin, User
exl-id: 393af72c-549f-4609-afb0-2712f827b549
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 1%

---

# Component Title{#title-component}

De component van de Titel van de Component van de Kern is een component van de sectiekop die op zijn plaats het uitgeven kenmerkt.

## Gebruik {#usage}

De component Titel is bedoeld voor gebruik als de titel of koptekst van een sectie met inhoud. De beschikbare kopniveaus kunnen door de sjabloonauteur worden gedefinieerd in het [ontwerpdialoogvenster](#design-dialog). De inhoudeditor kan kiezen uit beschikbare koptekstniveaus in het dialoogvenster [bewerken](#edit-dialog). Voor meer gemak is het ook mogelijk de koptekst eenvoudig op locatie te bewerken.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Title is v2, die in januari 2018 is geïntroduceerd met release 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | Compatibel | Compatibel | Compatibel |
| [v1](v1/title-v1.md) | Compatibel | Compatibel | - |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_title) om de component Title te ervaren en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Titel [kan op GitHub](https://adobe.com/go/aem_cmp_tech_title_v2) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de titeltekst definiëren en het kopniveau selecteren.

* **Titel**  - Als de paginatitel leeg is, wordt deze gebruikt
* **Type/Grootte**  - Hiermee definieert u het kopniveau van de titel
* **Link**  - Hiermee definieert u de inhoud waaraan de titel wordt gekoppeld. Dit kan een pad zijn naar een inhoudspagina, een externe URL of een pagina-anker.
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
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

* **Toegestane typen/grootten voor auteurs**  - Keuzentypen inschakelen of uitschakelen die beschikbaar zijn voor auteurs van inhoud wanneer zij de component Titel gebruiken.
* **Standaardtype / Grootte** - Definieer het koptype dat automatisch wordt toegewezen wanneer een auteur van de inhoud de component Titel aan een pagina toevoegt.
* **Koppeling** uitschakelen - Schakel ondersteuning voor koppelingen in de titelcomponent uit om te voorkomen dat auteurs van inhoud koppelingen maken van titels.

>[!NOTE]
>
>De capaciteit om een verbinding voor de titel te bepalen werd geïntroduceerd met versie 2.2.0 van de Componenten van de Kern.

### Tabblad Stijlen {#styles-tab}

De component Title ondersteunt het AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component van de Titel steunt [de Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
