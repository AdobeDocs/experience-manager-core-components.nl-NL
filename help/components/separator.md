---
title: Scheidingscomponent
description: De component separator maakt een einde tussen componenten op een pagina
role: Architect, Developer, Admin, User
exl-id: 79f19368-67fa-4864-93f7-2aa801d13fdb
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '308'
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
| v1 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel | Compatibel |

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de scheidingscomponent wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_separator).

### Technische details {#technical-details}

De meest recente technische documentatie over de separatorcomponent [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_separator_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

![Dialoogvenster voor bewerken van scheidingscomponent](/help/assets/separator-edit.png)

* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de stijlen definiëren die op de scheidingscomponent zijn toegepast.

### Tabblad Stijlen {#styles-tab}

De scheidingscomponent ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
