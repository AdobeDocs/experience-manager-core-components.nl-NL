---
title: Component Formulierknop
description: Met de component Core Component Form Hidden kunt u een verborgen veld in een formulier opnemen.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 2%

---


# Component Formulierknop {#form-button-component}

Met de component Core Component Form Button kan een knop worden opgenomen waarmee een handeling op een pagina wordt geactiveerd.

## Gebruik {#usage}

Met de component Core Component Form Button kunt u knopvelden maken, vaak om de verzending van het formulier te activeren en deze component is bedoeld voor gebruik samen met de component [](form-container.md)Form Container.

De knoopeigenschappen kunnen door de inhoudsredacteur in [vormen dialoog](#configure-dialog)worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Form Button is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | - | Compatibel | Compatibel | Compatibel |
| [v1](/help/components/v1/form-button-v1.md) | Compatibel | Compatibel | Compatibel | - |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_form_button)voor meer informatie over de component Formulierknoppen en voorbeelden van de configuratieopties ervan en over HTML- en JSON-uitvoer.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Knoop van de Vorm [kan op GitHub](https://adobe.com/go/aem_cmp_tech_form_button_v2)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud de parameters van de knop definiëren.

### Tabblad Eigenschappen {#properties-tab}

![Het dialoogvenster Bewerken van component Form Button](/help/assets/form-button-edit.png)

* **Type**

   * **Knop**
   * **Verzenden**

* **Titel** - De tekst die op de knop wordt weergegeven

   * Als er niets is opgegeven, wordt het knoptype standaard ingesteld

* **Naam** - De naam van de knop die samen met de formuliergegevens wordt verzonden
* **Waarde** - De waarde van de knop die samen met de formuliergegevens wordt verzonden

* **ID** - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component Form Button ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).
