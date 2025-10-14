---
title: Verborgen component van formulier
description: Met de component Core Component Form Hidden kunt u een verborgen veld weergeven.
role: Architect, Developer, Admin, User
exl-id: 0364cd3b-3c09-46db-9392-a67e3f9ea7a5
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 1%

---

# Verborgen component van formulier{#form-hidden-component}

Met de component Core Component Form Hidden kunt u een verborgen veld weergeven.

## Gebruik {#usage}

De Verborgen Component van de Component van de Kern staat voor de verwezenlijking van verborgen gebieden toe om informatie over de huidige pagina terug naar AEM over te gaan en is bedoeld om samen met de [&#x200B; component van de vormcontainer &#x200B;](form-container.md) worden gebruikt.

De gebiedseigenschappen kunnen door de inhoudsredacteur in [&#x200B; worden bepaald vormen dialoog &#x200B;](form-hidden.md).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Form Hidden is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | Compatibel systeem met <br>[&#x200B; versie 2.17.4 &#x200B;](/help/versions.md) en vroeger | Compatibel | Compatibel | Compatibel |
| [&#x200B; v1 &#x200B;](/help/components/v1/form-hidden-v1.md) | Compatibel | Compatibel | - | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [&#x200B; Kern &#x200B;](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Vorm Verborgen Component te ervaren evenals voorbeelden van zijn configuratieopties evenals de output van HTML en JSON te zien, bezoek de [&#x200B; Bibliotheek van de Component &#x200B;](https://adobe.com/go/aem_cmp_library_form_hidden).

### Technische details {#technical-details}

De recentste technische documentatie over de Vorm Verborgen Component [&#x200B; kan op GitHub &#x200B;](https://adobe.com/go/aem_cmp_tech_form_hidden_v2) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [&#x200B; de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden &#x200B;](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud de parameters van het verborgen veld definiëren.

![&#x200B; Verborgen vorm geeft dialoog uit &#x200B;](/help/assets/form-hidden-edit.png)

* **Naam** - de naam van het gebied, dat met de vormgegevens wordt voorgelegd
* **Waarde** - de waarde van het gebied, dat met de vormgegevens wordt voorgelegd
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [&#x200B; Laag van Gegevens te controleren &#x200B;](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

Omdat de Vorm Verborgen component normaal geen zichtbare attributen heeft, toont placeholder van de component in de redacteur de **Naam** en **waarde** gebiedswaarden als zij worden toegewezen om de auteur te helpen de aangewezen Vorm Verborgen component identificeren.

![&#x200B; Voorbeeld van Vorm Verborgen Component &#x200B;](/help/assets/form-hidden-example.png)

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De Vorm Verborgen Component steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).
