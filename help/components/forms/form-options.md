---
title: Component Formulieropties
description: Met de component Core Component Form Options kunt u vooraf gedefinieerde opties in verschillende indelingen selecteren.
role: Architect, Developer, Admin, User
exl-id: 8a74bd37-9b12-4fa6-bff2-53e337b16251
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# Component Formulieropties {#form-options-component}

Met de component Formulieropties voor kerncomponenten kunt u vooraf gedefinieerde opties in verschillende indelingen selecteren.

## Gebruik {#usage}

De component van de Opties van de Vorm van de Component van de Kern staat voor de voorlegging van verschillende types van opties toe die op vele verschillende manieren worden voorgesteld en is bedoeld om samen met de [&#x200B; component van de Container van de Vorm &#x200B;](form-container.md) worden gebruikt.

De presentatie van de opties, de etiketten, en de individuele opties kunnen door de inhoudsredacteur in [&#x200B; worden bepaald vormt dialoog &#x200B;](#configure-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Formulieropties is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatibel systeem met <br>[&#x200B; versie 2.17.4 &#x200B;](/help/versions.md) en vroeger | Compatibel | Compatibel | Compatibel |
| [&#x200B; v1 &#x200B;](/help/components/v1/form-options-v1.md) | Compatibel | Compatibel | - | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [&#x200B; Kern &#x200B;](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Opties van de Vorm te ervaren evenals voorbeelden van zijn configuratieopties evenals uitvoer te zien HTML en JSON, bezoek de [&#x200B; Bibliotheek van de Component &#x200B;](https://adobe.com/go/aem_cmp_library_form_options).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Opties van de Vorm [&#x200B; kan op GitHub &#x200B;](https://adobe.com/go/aem_cmp_tech_form_options_v2) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [&#x200B; de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden &#x200B;](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het type opties definiëren dat moet worden weergegeven, de labels en de beschikbare opties.

![&#x200B; de bewerkingsdialoog van de Component van de Opties van de Vorm &#x200B;](/help/assets/form-options-edit.png)

* **Types** - hoe de opties zullen worden voorgesteld
   * **Checkboxes**
   * **Keuzerondjes**
   * **drop-down**
   * **multi-uitgezochte drop-down**
* **Titel** - de titel die als etiket voor de opties zal worden getoond
* **Naam** - de naam van het gebied dat met de vormgegevens wordt voorgelegd
* **Source** - waar de opties worden bepaald
   * **Lokaal** - die binnen de component wordt bepaald
      * Tik of klik **voeg** knoop toe om een waarde toe te voegen, **Schrapping** om een waarde te verwijderen
         * **Waarde** - de waarde bewaard wanneer die optie wordt geselecteerd wanneer de vorm wordt voorgelegd
         * **Tekst** - het etiket voor de optie die op de vorm wordt getoond
         * **Actief** - de optie wordt duidelijk zoals geselecteerd wanneer de vorm laadt
         * **Gehandicapten** - de optie is niet selecteerbaar maar nog getoond
   * **Lijst** - een statische die lijst elders in AEM wordt bepaald wordt gebruikt voor de opties
      * **Lijst** - de weg van de statische lijst in AEM
         * Gebruik de Browse knoop om van het lijstmiddel de plaats te bepalen
   * **Gegevensbron** - een gegevensbron wordt gebruikt voor de opties
      * **Gegevensbron** - Het type van Middel van de gegevensbron
* **het bericht van de Hulp** - een wenk voor de gebruiker van wat op het gebied kan zijn ingegaan
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [&#x200B; Laag van Gegevens te controleren &#x200B;](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component van de Opties van de Vorm steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).
