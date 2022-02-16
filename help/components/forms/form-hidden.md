---
title: Verborgen component van formulier
description: Met de component Core Component Form Hidden kunt u een verborgen veld weergeven.
role: Architect, Developer, Admin, User
exl-id: 0364cd3b-3c09-46db-9392-a67e3f9ea7a5
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 1%

---

# Verborgen component van formulier{#form-hidden-component}

Met de component Core Component Form Hidden kunt u een verborgen veld weergeven.

## Gebruik {#usage}

Met de component Core Component Form Hidden kunt u verborgen velden maken die informatie over de huidige pagina teruggeven aan AEM en die samen met de [formuliercontainercomponent](form-container.md).

De veldeigenschappen kunnen worden gedefinieerd door de inhoudeditor in het dialoogvenster [dialoogvenster configureren](form-hidden.md).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Form Hidden is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel | Compatibel |
| [v1](/help/components/v1/form-hidden-v1.md) | Compatibel | Compatibel | - |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de component Formulier verborgen wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_form_hidden).

### Technische details {#technical-details}

De meest recente technische documentatie over de component Form Hidden [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_form_hidden_v2).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud de parameters van het verborgen veld definiëren.

![Dialoogvenster Formulier verborgen bewerken](/help/assets/form-hidden-edit.png)

* **Naam** - De naam van het veld dat met de formuliergegevens wordt verzonden
* **Waarde** - De waarde van het veld, dat met de formuliergegevens wordt verzonden
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

Omdat de component Formulier verborgen normaal geen zichtbare kenmerken heeft, wordt de tijdelijke aanduiding van de component in de editor weergegeven als **Naam** en **Waarde** veldwaarden als deze zijn toegewezen, zodat de auteur de juiste component Form Hidden kan vinden.

![Voorbeeld van een component Formulier Verborgen](/help/assets/form-hidden-example.png)

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component Form Hidden ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
