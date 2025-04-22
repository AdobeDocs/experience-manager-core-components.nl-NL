---
title: Component Formulierknop
description: Met de component Core Component Form Hidden kunt u een verborgen veld in een formulier opnemen.
role: Architect, Developer, Admin, User
exl-id: 1e5cff43-57db-4bfc-b2d2-23307eaf5eb3
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 1%

---

# Component Formulierknop {#form-button-component}

Met de component Core Component Form Button kan een knop worden opgenomen waarmee een handeling op een pagina wordt geactiveerd.

## Gebruik {#usage}

De component van de Knoop van de Vorm van de Component van de Kern staat voor de verwezenlijking van knoopgebied toe, vaak om de voorlegging van de vorm teweeg te brengen en is bedoeld om samen met de [ component van de Container van de Vorm ](form-container.md) worden gebruikt.

De knoopeigenschappen kunnen door de inhoudsredacteur in [ worden bepaald vormen dialoog ](#configure-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Form Button is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | Compatibel systeem met <br>[ versie 2.17.4 ](/help/versions.md) en vroeger | Compatibel | Campatibel | Compatibel |
| [ v1 ](/help/components/v1/form-button-v1.md) | Compatibel | Compatibel | - | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Knoop van de Vorm te ervaren evenals voorbeelden van zijn configuratieopties evenals uitvoer te zien HTML en JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_form_button).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Knoop van de Vorm [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_form_button_v2) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud de parameters van de knop definiëren.

### Tabblad Eigenschappen {#properties-tab}

![ De component van de Knoop van de Vorm geeft dialoog uit ](/help/assets/form-button-edit.png)

* **Type**

   * **Knoop**
   * **voorleggen**

* **Titel** - de tekst die op de knoop wordt getoond

   * Als er niets is opgegeven, wordt het knoptype standaard ingesteld

* **Naam** - de naam van de knoop, die met de vormgegevens wordt voorgelegd
* **Waarde** - de waarde van de knoop, die met de vormgegevens wordt voorgelegd

* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component van de Knoop van de Vorm steunt het Systeem van de Stijl van AEM [ ](/help/get-started/authoring.md#component-styling).
