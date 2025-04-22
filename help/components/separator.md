---
title: Scheidingscomponent
description: De component separator maakt een einde tussen componenten op een pagina
role: Architect, Developer, Admin, User
exl-id: 79f19368-67fa-4864-93f7-2aa801d13fdb
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 1%

---

# Scheidingscomponent {#separator-component}

De component van de Scheiding van de Component van de Kern toont een horizontale lijn voor het scheiden van inhoud.

## Gebruik {#usage}

Met de scheidingscomponent kan de auteur van de inhoud eenvoudig een horizontale lijn maken als een onderbreking tussen de inhoud om de informatie op een pagina beter te ordenen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Scheidingscomponent is v1, die in februari 2019 met versie 2.3.0 van de Core Components is geïntroduceerd en in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.17.4 ](/help/versions.md) en vroeger | Compatibel | Compatibel | Compatibel |

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Scheiding te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_separator).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Scheiding [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_separator_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

![ de bewerkingsdialoog van de Component van de Scheiding ](/help/assets/separator-edit.png)

* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de stijlen definiëren die op de scheidingscomponent zijn toegepast.

### Tabblad Stijlen {#styles-tab}

De component van de Scheiding steunt het Systeem van de Stijl van AEM [ ](/help/get-started/authoring.md#component-styling).
