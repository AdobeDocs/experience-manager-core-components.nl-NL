---
title: Component Voortgangsbalk
description: De component van de vooruitgangsbar vertegenwoordigt visueel vooruitgang in de richting van een doel
role: Architect, Developer, Admin, User
exl-id: 47afc5a6-ac57-4b6c-92c4-015ca956a20b
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 2%

---

# Component Voortgangsbalk {#progress-bar-component}

De component van de Bar van de Voortgang van de Component van de Kern vertegenwoordigt visueel vooruitgang in de richting van een doel.

## Gebruik {#usage}

Met de component ProgressBar kan de auteur van de inhoud eenvoudig een voortgangsbalk maken door een voltooiingspercentage te definiëren, zodat de voortgang in de richting van een doel op intuïtieve wijze zichtbaar is.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component ProgressBar is v1, die in mei 2020 is geïntroduceerd met versie 2.9.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel | Compatibel |

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de component ProgressBar wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_progressbar).

### Technische details {#technical-details}

De meest recente technische documentatie over de component ProgressBar [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_progress_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

![Dialoogvenster voor bewerken van component Progress](/help/assets/progress-bar-edit.png)

* **Voltooiing** - De vooruitgang uitgedrukt als een percentage
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de stijlen definiëren die zijn toegepast op de component Progress Bar.

### Tabblad Stijlen {#styles-tab}

De component ProgressBar ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component ProgressBar ondersteunt de component [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
