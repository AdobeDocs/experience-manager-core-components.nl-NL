---
title: Component Formulieropties
description: Met de component Core Component Form Options kunt u vooraf gedefinieerde opties in verschillende indelingen selecteren.
role: Architect, ontwikkelaar, beheerder, praktijkgerichte
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 1%

---


# Component Formulieropties {#form-options-component}

Met de component Formulieropties kerncomponent kunt u vooraf gedefinieerde opties in verschillende indelingen selecteren.

## Gebruik {#usage}

De component van de Opties van de Vorm van de Component van de Kern staat voor de voorlegging van verschillende types van opties toe die op vele verschillende manieren worden voorgesteld en is bedoeld om samen met de [component van de Container van de Vorm worden gebruikt](form-container.md).

De presentatie van de opties, de etiketten, en de individuele opties kunnen door de inhoudsredacteur in [vormen dialoog](#configure-dialog) worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Formulieropties is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatibel | Compatibel | Compatibel |
| [v1](/help/components/v1/form-options-v1.md) | Compatibel | Compatibel | - |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_form_options) voor meer informatie over de component Formulieropties en voorbeelden van de bijbehorende configuratieopties en over HTML- en JSON-uitvoer.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Opties van de Vorm [kan op GitHub](https://adobe.com/go/aem_cmp_tech_form_options_v2) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster {#configure-dialog} configureren

In het dialoogvenster Configureren kan de auteur van de inhoud het type opties definiëren dat moet worden weergegeven, de labels en de beschikbare opties.

![Dialoogvenster Formulieropties Component bewerken](/help/assets/form-options-edit.png)

* **Typen**  - Hoe worden de opties weergegeven
   * **Selectievakjes**
   * **Keuzerondjes**
   * **Vervolgkeuzelijst**
   * **Vervolgkeuzelijst Multi-select**
* **Titel**  - De titel die als label voor de opties wordt weergegeven
* **Naam**  - De naam van het veld dat met de formuliergegevens is verzonden
* **Bron**  - Waar worden de opties gedefinieerd
   * **Lokaal**  - Gedefinieerd binnen de component
      * Tik of klik op de knop **Toevoegen** om een waarde toe te voegen, **Verwijderen** om een waarde te verwijderen
         * **Waarde**  - De waarde die wordt opgeslagen wanneer die optie is geselecteerd bij het verzenden van het formulier
         * **Tekst**  - Het label voor de optie die op het formulier wordt weergegeven
         * **Actief**  - De optie is gemarkeerd als geselecteerd wanneer het formulier wordt geladen
         * **Uitgeschakeld**  - De optie kan niet worden geselecteerd, maar wordt wel weergegeven
   * **List**  - Een statische lijst die elders in AEM is gedefinieerd, wordt gebruikt voor de opties
      * **List**  - Het pad van de statische lijst in AEM
         * Gebruik de Browse knoop om van het lijstmiddel de plaats te bepalen
   * **Gegevensbron**  - Een gegevensbron wordt gebruikt voor de opties
      * **Gegevensbron**  - Type bron van gegevensbron
* **Help-bericht**  - Een tip voor de gebruiker wat in het veld kan worden ingevoerd
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component Formulieropties ondersteunt het AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
