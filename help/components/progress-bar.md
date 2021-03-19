---
title: Component Voortgangsbalk
description: De component van de vooruitgangsbar vertegenwoordigt visueel vooruitgang in de richting van een doel
role: Architect, ontwikkelaar, beheerder, praktijkgerichte
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 2%

---


# Voortgangsbalkcomponent {#progress-bar-component}

De component van de Bar van de Voortgang van de Component van de Kern vertegenwoordigt visueel vooruitgang in de richting van een doel.

## Gebruik {#usage}

Met de component ProgressBar kan de auteur van de inhoud eenvoudig een voortgangsbalk maken door een voltooiingspercentage te definiëren, zodat de voortgang in de richting van een doel op intuïtieve wijze zichtbaar is.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component ProgressBar is v1, die in mei 2020 is geïntroduceerd met versie 2.9.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel | Compatibel | Compatibel |

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_progressbar) om de component Progress Bar te ervaren en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Bar van de Voortgang [kan op GitHub](https://adobe.com/go/aem_cmp_tech_progress_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster {#configure-dialog} configureren

![Dialoogvenster voor bewerken van component Progress](/help/assets/progress-bar-edit.png)

* **Voltooiing**  - De vooruitgang uitgedrukt in een percentage
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de stijlen definiëren die zijn toegepast op de component Progress Bar.

### Tabblad Stijlen {#styles-tab}

De component ProgressBar ondersteunt het AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Adobe-gegevenslaag client {#data-layer}

De component van de Bar van de Voortgang steunt [de Laag van de Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
