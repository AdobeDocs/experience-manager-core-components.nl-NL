---
title: Component Inhoudsopgave
description: De component Inhoudsopgave maakt een inhoudsopgave op basis van de titels in de pagina-inhoud, zodat uw lezers snel door de pagina kunnen navigeren.
role: Architect, Developer, Admin, User
exl-id: 006adde2-ebff-4e74-8e79-325cccd43e8f
source-git-commit: 8beae61676340e8aafaee469018d865ea7ed934e
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Component Inhoudsopgave {#table-of-contents-component}

De component Inhoudsopgave maakt een inhoudsopgave op basis van de titels in de pagina-inhoud, zodat uw lezers snel door de pagina kunnen navigeren.

## Gebruik {#usage}

Met de component Inhoudsopgave kunnen sitebezoekers snel door de inhoud van uw pagina navigeren via een efficiënt gegenereerde inhoudsopgave op basis van de titels van de pagina-inhoud.

* De ToC wordt geproduceerd serverzijde.
* Deze wordt volledig in cache geplaatst door de verzender voor snelle levering.
* Het werkt met alle componenten op de pagina, niet alleen de Componenten van de Kern.

De [dialoogvenster bewerken](#edit-dialog) Hiermee kan de auteur van de inhoud het bereik definiëren van titels die in de inhoudsopgave moeten worden gebruikt. Met de [ontwerpdialoogvenster](#design-dialog), kan de sjabloonauteur de standaardwaarde voor de titels instellen wanneer een inhoudsontwerper een inhoudsopgave-component aan een pagina toevoegt en titels in de inhoudsopgave beperken op basis van klassenamen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Inhoudsopgave is v1, die in mei 2022 is geïntroduceerd met versie 2.20.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

>[!NOTE]
>
>Op AEM as a Cloud Service, moet uw beheerder een filter voor de component toelaten opdat het de inhoud van de component teruggeeft.
>
>[Gelieve te zien de documentatie GitHub van de component](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1) voor meer informatie .

### Technische details {#technical-details}

De meest recente technische documentatie over de component Inhoudsopgave [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de bereiken definiëren van titelniveaus die de component Inhoudsopgave als een ToC moet weergeven.

![Dialoogvenster Inhoudsopgave component bewerken](/help/assets/tableofcontents-edit.png)

**Lijsttype** - Met deze optie bepaalt u of de lijst een lijst met opsommingstekens of een genummerde lijst moet zijn.
* **Beginniveau titel** - Met deze optie definieert u het hoogste niveau van titels dat de component Inhoudsopgave moet renderen.
* **Niveau titelstop** - Met deze optie definieert u het laagste niveau van titels dat de component Inhoudsopgave moet renderen.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

Met behulp van het ontwerpdialoogvenster kan de sjabloonauteur de standaardwaarde voor het titelbereik van de component Inhoudsopgave instellen en titels in de inhoudsopgave beperken op basis van klassenamen.

### Tabblad Eigenschappen {#properties-tab}

![Het ontwerpdialoogvenster van de component Snel zoeken](/help/assets/tableofcontents-design.png)

* **Lijsttype beperken** - Met deze optie definieert u het type lijst dat de component genereert. Als u deze optie selecteert, kan de auteur van de inhoud alleen een ander lijsttype kiezen.
* **Het beginniveau beperken** - Deze optie definieert het hoogste titelniveau dat de auteur van de inhoud kan selecteren voor het definiëren van de inhoudsopgave.
* **Het stopniveau beperken** - Deze optie definieert het laagste titelniveau dat de auteur van de inhoud kan selecteren voor het definiëren van de inhoudsopgave.
* **Klassenamen opnemen** - Als deze optie is ingesteld, worden alleen titels met de opgegeven klassennamen of opgenomen in elementen van de opgegeven klassennamen door de component Inhoudsopgave in overweging genomen.
   * Tik of klik op de knop **Toevoegen** om een of meer klassennamen toe te voegen.
   * Tik of klik op de knop **Verwijderen** naast een klassenaam om deze te verwijderen.
* **Klassenamen negeren** - Als deze optie is ingesteld, worden titels met de opgegeven klassennamen of opgenomen in elementen van de opgegeven klassennamen genegeerd door de component Inhoudsopgave.
   * Tik of klik op de knop **Toevoegen** om een of meer klassennamen toe te voegen.
   * Tik of klik op de knop **Verwijderen** naast een klassenaam om deze te verwijderen.

### Tabblad Stijlen {#styles-tab}

De component Inhoudsopgave ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component Inhoudsopgave ondersteunt de component [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
