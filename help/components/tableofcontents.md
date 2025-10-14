---
title: Component Inhoudsopgave
description: De component Inhoudsopgave maakt een inhoudsopgave op basis van de titels in de pagina-inhoud, zodat uw lezers snel door de pagina kunnen navigeren.
role: Architect, Developer, Admin, User
exl-id: 006adde2-ebff-4e74-8e79-325cccd43e8f
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 0%

---


# Component Inhoudsopgave {#table-of-contents-component}

De component Inhoudsopgave maakt een inhoudsopgave op basis van de titels in de pagina-inhoud, zodat uw lezers snel door de pagina kunnen navigeren.

{{traditional-aem}}

## Gebruik {#usage}

Met de component Inhoudsopgave kunnen sitebezoekers snel door de inhoud van uw pagina navigeren via een efficiënt gegenereerde inhoudsopgave op basis van de titels van de pagina-inhoud.

* De ToC wordt geproduceerd serverzijde.
* Deze wordt volledig in cache geplaatst door de verzender voor snelle levering.
* Het werkt met alle componenten op de pagina, niet alleen de Componenten van de Kern.

Het [&#x200B; geeft dialoog &#x200B;](#edit-dialog) uit staat de inhoudauteur toe om de waaier van titels te bepalen die in ToC moeten worden gebruikt. Gebruikend de [&#x200B; ontwerpdialoog &#x200B;](#design-dialog), kan de malplaatjeauteur de standaardwaarde voor de titels plaatsen wanneer een inhoudsauteur een Component van de Inhoudslijst aan een pagina toevoegt evenals titels beperken inbegrepen in ToC die op klassennamen wordt gebaseerd.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Inhoudsopgave is v1, die in mei 2022 is geïntroduceerd met versie 2.20.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [&#x200B; Kern &#x200B;](/help/versions.md).

>[!NOTE]
>
>In AEM as a Cloud Service moet uw beheerder een filter voor de component inschakelen om de inhoud van de component te kunnen renderen.
>
>[&#x200B; gelieve te zien de documentatie GitHub van de component &#x200B;](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1) voor meer informatie.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Inhoudsopgave [&#x200B; kan op GitHub &#x200B;](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [&#x200B; de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden &#x200B;](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de bereiken definiëren van titelniveaus die de component Inhoudsopgave als een ToC moet weergeven.

![&#x200B; Lijst van Inhoud geeft de Component dialoog uit &#x200B;](/help/assets/tableofcontents-edit.png)

**Type van Lijst** - Deze optie bepaalt als de lijst een genummerde lijst of een genummerde lijst zou moeten zijn.
* **het Niveau van het Begin van de Titel** - Deze optie bepaalt het hoogste niveau van titels dat de Component van de Inhoudsopgave zou moeten teruggeven.
* **Niveau van het Einde van de Titel** - Deze optie bepaalt het laagste niveau van titels dat de Component van de Inhoudsopgave zou moeten teruggeven.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [&#x200B; Laag van Gegevens te controleren &#x200B;](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

Met behulp van het ontwerpdialoogvenster kan de sjabloonauteur de standaardwaarde voor het titelbereik van de component Inhoudsopgave instellen en titels in de inhoudsopgave beperken op basis van klassenamen.

### Tabblad Eigenschappen {#properties-tab}

![&#x200B; Snelle het ontwerpdialoog van de Component van het Onderzoek van het Snelle &#x200B;](/help/assets/tableofcontents-design.png)

* **Beperk het Type van Lijst** - Deze optie bepaalt het type van lijst dat de component zal produceren. Als u deze optie selecteert, kan de auteur van de inhoud alleen een ander lijsttype kiezen.
* **Beperk het Niveau van het Begin** - Deze optie bepaalt het hoogste titelniveau dat de inhoudauteur voor het bepalen van ToC kan selecteren.
* **Beperk het Niveau van het Einde** - deze optie bepaalt het laagste titelniveau dat de inhoudauteur voor het bepalen van ToC kan selecteren.
* **omvat de Namen van de Klasse** - als deze optie wordt geplaatst, slechts zullen de titels met de gespecificeerde klassennamen of bevat binnen elementen van de gespecificeerde klassennamen door de Component van de Inhoudsopgave worden overwogen.
   * Tik of klik **voeg** pictogram toe om één of meerdere klassennamen toe te voegen.
   * Tik of klik het **pictogram van de Schrapping** naast een klassennaam om het te schrappen.
* **negeert de Namen van de Klasse** - als deze optie wordt geplaatst, zullen de titels met de gespecificeerde klassennamen of bevat binnen elementen van de gespecificeerde klassennamen door de Component van de Inhoudslijst worden genegeerd.
   * Tik of klik **voeg** pictogram toe om één of meerdere klassennamen toe te voegen.
   * Tik of klik het **pictogram van de Schrapping** naast een klassennaam om het te schrappen.

### Tabblad Stijlen {#styles-tab}

De component van de Lijst van Inhoud steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De component van de Lijst van Inhoud steunt de [&#x200B; Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
