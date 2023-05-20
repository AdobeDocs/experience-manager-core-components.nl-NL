---
title: Component Formulierknop
description: Met de component Core Component Form Hidden kunt u een verborgen veld in een formulier opnemen.
role: Architect, Developer, Admin, User
exl-id: 1e5cff43-57db-4bfc-b2d2-23307eaf5eb3
source-git-commit: 16930ccaa281f9d9c4ddbb890d4222e128557580
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 1%

---

# Component Formulierknop {#form-button-component}

Met de component Core Component Form Button kan een knop worden opgenomen waarmee een handeling op een pagina wordt geactiveerd.

## Gebruik {#usage}

Met de component Core Component Form Button kunt u een knopveld maken dat vaak de verzending van het formulier activeert en dat samen met het [component Form Container](form-container.md).

De knopeigenschappen kunnen door de inhoudeditor in het dialoogvenster [dialoogvenster configureren](#configure-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Form Button is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel | Compatibel |
| [v1](/help/components/v1/form-button-v1.md) | Compatibel | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de component Form Button wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_form_button).

### Technische details {#technical-details}

De meest recente technische documentatie over de component FormButton [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_form_button_v2).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud de parameters van de knop definiëren.

### Tabblad Eigenschappen {#properties-tab}

![Het dialoogvenster Bewerken van component Form Button](/help/assets/form-button-edit.png)

* **Type**

   * **Knop**
   * **Verzenden**

* **Titel** - De tekst die op de knop wordt weergegeven

   * Als er niets is opgegeven, wordt het knoptype standaard ingesteld

* **Naam** - De naam van de knop, die samen met de formuliergegevens wordt verzonden
* **Waarde** - De waarde van de knop, die samen met de formuliergegevens wordt verzonden

* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component Form Button ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
