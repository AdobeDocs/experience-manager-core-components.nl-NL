---
title: Component Voortgangsbalk
description: De component van de vooruitgangsbar vertegenwoordigt visueel vooruitgang in de richting van een doel
translation-type: tm+mt
source-git-commit: cba1d898d7789af7f4045ef9aa052b4da6a6b33a
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 2%

---


# Component Voortgangsbalk {#progress-bar-component}

De component van de Bar van de Voortgang van de Component van de Kern vertegenwoordigt visueel vooruitgang in de richting van een doel.

## Gebruik {#usage}

Met de component ProgressBar kan de auteur van de inhoud eenvoudig een voortgangsbalk maken door een voltooiingspercentage te definiëren, zodat de voortgang in de richting van een doel op intuïtieve wijze zichtbaar is.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component ProgressBar is v1, die in mei 2020 is geïntroduceerd met versie 2.9.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel | Compatibel | Compatibel |

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_progressbar)voor meer informatie over de component Progress Bar en voorbeelden van de bijbehorende configuratieopties en over HTML- en JSON-uitvoer.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Bar van de Voortgang [kan op GitHub](https://adobe.com/go/aem_cmp_tech_progress_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster configureren {#configure-dialog}

![Dialoogvenster voor bewerken van component Progress](/help/assets/progress-bar-edit.png)

* **Voltooiing** - De vooruitgang uitgedrukt in een percentage
* **ID** - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de stijlen definiëren die zijn toegepast op de component Progress Bar.

### Tabblad Stijlen {#styles-tab}

De component ProgressBar ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).