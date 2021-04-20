---
title: Scheidingscomponent
description: De component separator maakt een einde tussen componenten op een pagina
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 2%

---


# Scheidingscomponent {#separator-component}

De component van de Scheiding van de Component van de Kern toont een horizontale lijn voor het scheiden van inhoud.

## Gebruik {#usage}

Met de scheidingscomponent kan de auteur van de inhoud eenvoudig een horizontale lijn maken als een onderbreking tussen de inhoud om de informatie op een pagina beter te ordenen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Scheidingscomponent is v1, die in februari 2019 met versie 2.3.0 van de Core Components is geïntroduceerd en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel | Compatibel | Compatibel |

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_separator) om de Scheidingscomponent te ervaren en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Scheiding [kan op GitHub](https://adobe.com/go/aem_cmp_tech_separator_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster {#configure-dialog} configureren

![Dialoogvenster voor bewerken van scheidingscomponent](/help/assets/separator-edit.png)

* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de stijlen definiëren die op de scheidingscomponent zijn toegepast.

### Tabblad Stijlen {#styles-tab}

De scheidingscomponent ondersteunt het AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
