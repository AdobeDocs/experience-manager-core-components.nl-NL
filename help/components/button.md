---
title: Component Button
description: Met de component Knop Core-component kunt u een knop maken en weergeven.
role: Architect, Developer, Admin, User
exl-id: e17efd1d-90d4-497a-9e7d-45934d81bc28
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 1%

---

# Component Button{#button-component}

De component van de Knoop van de Component van de Kern staat voor de configuratie en de vertoning van een knooppunt op een pagina toe.

## Gebruik {#usage}

Met de component Core Component Button kan een knop op een pagina worden opgenomen.

* De eigenschappen van de knoop kunnen in [vormen dialoog](#configure-dialog) worden geselecteerd.
* De stijlen voor de Component van de Knoop kunnen in [ontwerpdialoog](#design-dialog) worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Button is v1, die in juni 2019 is geïntroduceerd met versie 2.5.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_button) om de component Button te ervaren en voorbeelden van de configuratieopties en de HTML- en JSON-uitvoer te bekijken.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Knoop [kan op GitHub](https://adobe.com/go/aem_cmp_tech_button_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud de knop definiëren en bepalen hoe deze zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

### Tabblad Eigenschappen {#properties-tab}

![Het tabblad Eigenschappen van het dialoogvenster Bewerken van component Button](/help/assets/button-edit-properties.png)

* **Tekst**  - De tekst die op de knop moet worden weergegeven
* **Koppeling**  - Koppeling maken naar een inhoudspagina binnen AEM, een externe bron of een anker
   * Gebruik **Dialoogvenster Selectie** om een pad binnen AEM te kiezen.
* **Pictogram**  - Id voor weergave van een pictogram in de knop
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheid, tabblad van het dialoogvenster Bewerken van component Button](/help/assets/button-edit-accessibility.png)

Op het tabblad **Toegankelijkheid** kunnen waarden worden ingesteld voor [ARIA-toegankelijkheidslabels](https://www.w3.org/WAI/standards-guidelines/aria/) voor de component.

* **Label**  - waarde van een ARIA-labelkenmerk voor de component

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component Button ondersteunt het AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component Button ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
