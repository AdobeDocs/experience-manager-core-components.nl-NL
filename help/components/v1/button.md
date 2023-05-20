---
title: component Button (v1)
description: Met de component Knop Core-component kunt u een knop maken en weergeven.
role: Architect, Developer, Admin, User
exl-id: 63af16e4-dd4d-426d-88ef-769ecd1b3175
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# component Button (v1) {#button-component}

De component van de Knoop van de Component van de Kern staat voor de configuratie en de vertoning van een knooppunt op een pagina toe.

## Gebruik {#usage}

Met de component Core Component Button kan een knop op een pagina worden opgenomen.

* De eigenschappen van de knop kunnen worden geselecteerd in het dialoogvenster [dialoogvenster configureren](#configure-dialog).
* Stijlen voor de component Button kunnen worden gedefinieerd in het gedeelte [ontwerpdialoogvenster](#design-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

Het document beschrijft v1 van de component Button, die in juni 2019 werd geïntroduceerd met versie 2.5.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Button beschreven.
>
>Voor meer informatie over de huidige versie van de component Button raadpleegt u de [Component Button](/help/components/button.md) document.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de component Button wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_button).

## Technische details {#technical-details}

De meest recente technische documentatie over de component Button [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_button_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud de knop definiëren en bepalen hoe deze zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

### Tabblad Eigenschappen {#properties-tab}

![Het tabblad Eigenschappen van het dialoogvenster Bewerken van component Button](/help/assets/button-edit-properties.png)

* **Tekst** - De tekst die op de knop moet worden weergegeven
* **Koppeling** - Koppeling maken naar een inhoudspagina binnen AEM, een externe bron of een anker
   * Gebruik de **Dialoogvenster Selectie** om een pad te kiezen binnen AEM.
* **Pictogram** - Id voor weergave van een pictogram in de knop
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheid, tabblad van het dialoogvenster Bewerken van component Button](/help/assets/button-edit-accessibility.png)

Op de **Toegankelijkheid** tab, waarden kunnen worden ingesteld voor [Toegankelijkheid ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) labels voor de component.

* **Label** - Waarde van een ARIA-labelkenmerk voor de component

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component Button ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component Button ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
