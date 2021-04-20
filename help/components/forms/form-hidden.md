---
title: Verborgen component van formulier
description: Met de component Core Component Form Hidden kunt u een verborgen veld weergeven.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 1%

---


# Verborgen component van formulier{#form-hidden-component}

Met de component Core Component Form Hidden kunt u een verborgen veld weergeven.

## Gebruik {#usage}

Met de component Core Component Form Hidden kunt u verborgen velden maken die informatie over de huidige pagina teruggeven aan AEM. Deze component is bedoeld voor gebruik samen met de [component Form container](form-container.md).

De veldeigenschappen kunnen door de inhoudsredacteur in [vormen dialoog](form-hidden.md) worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Form Hidden is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatibel | Compatibel | Compatibel |
| [v1](/help/components/v1/form-hidden-v1.md) | Compatibel | Compatibel | - |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_form_hidden) voor meer informatie over de component Formulier Verborgen en voorbeelden van de bijbehorende configuratieopties en de HTML- en JSON-uitvoer.

### Technische details {#technical-details}

De recentste technische documentatie over de Vorm Verborgen Component [kan op GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster {#configure-dialog} configureren

In het dialoogvenster voor configureren kan de auteur van de inhoud de parameters van het verborgen veld definiëren.

![Dialoogvenster Formulier verborgen bewerken](/help/assets/form-hidden-edit.png)

* **Naam**  - De naam van het veld dat met de formuliergegevens wordt verzonden
* **Waarde**  - De waarde van het veld dat met de formuliergegevens wordt verzonden
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

Aangezien de component Formulier verborgen normaal geen zichtbare kenmerken heeft, worden in de tijdelijke aanduiding van de component in de editor de veldwaarden **Naam** en **Waarde** weergegeven als deze zijn toegewezen, zodat de auteur de juiste component Formulier verborgen kan identificeren.

![Voorbeeld van een component Formulier Verborgen](/help/assets/form-hidden-example.png)

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component Formulier verborgen ondersteunt het AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
