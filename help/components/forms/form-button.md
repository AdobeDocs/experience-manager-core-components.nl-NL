---
title: Component Formulierknop
description: Met de component Core Component Form Hidden kunt u een verborgen veld in een formulier opnemen.
role: Architect, Developer, Admin, User
exl-id: 1e5cff43-57db-4bfc-b2d2-23307eaf5eb3
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 2%

---

# Component Formulierknop {#form-button-component}

Met de component Core Component Form Button kan een knop worden opgenomen waarmee een handeling op een pagina wordt geactiveerd.

## Gebruik {#usage}

De component van de Knoop van de Vorm van de Component van de Kern staat voor de verwezenlijking van knoopgebied toe, vaak om de voorlegging van de vorm teweeg te brengen en is bedoeld om samen met de [component van de Container van de Vorm ](form-container.md) worden gebruikt.

De knoopeigenschappen kunnen door de inhoudsredacteur in [vormen dialoog](#configure-dialog) worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Form Button is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatibel | Compatibel | Compatibel |
| [v1](/help/components/v1/form-button-v1.md) | Compatibel | Compatibel | - |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_form_button) voor meer informatie over de component Formulierknopcomponent en voorbeelden van de bijbehorende configuratieopties, alsook over HTML- en JSON-uitvoer.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Knoop van de Vorm [kan op GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud de parameters van de knop definiëren.

### Tabblad Eigenschappen {#properties-tab}

![Het dialoogvenster Bewerken van component Form Button](/help/assets/form-button-edit.png)

* **Type**

   * **Knop**
   * **Verzenden**

* **Titel**  - De tekst die op de knop wordt weergegeven

   * Als er niets is opgegeven, wordt het knoptype standaard ingesteld

* **Naam**  - De naam van de knop die samen met de formuliergegevens wordt verzonden
* **Waarde**  - De waarde van de knop die samen met de formuliergegevens wordt verzonden

* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component van de Knoop van de Vorm steunt het AEM [Systeem van de Stijl](/help/get-started/authoring.md#component-styling).
