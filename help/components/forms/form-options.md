---
title: Component Formulieropties
description: Met de component Core Component Form Options kunt u vooraf gedefinieerde opties in verschillende indelingen selecteren.
role: Architect, Developer, Admin, User
exl-id: 8a74bd37-9b12-4fa6-bff2-53e337b16251
source-git-commit: 16930ccaa281f9d9c4ddbb890d4222e128557580
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 1%

---

# Component Formulieropties {#form-options-component}

Met de component Formulieropties kerncomponent kunt u vooraf gedefinieerde opties in verschillende indelingen selecteren.

## Gebruik {#usage}

Met de component Formulieropties voor kerncomponenten kunt u verschillende typen opties indienen die op verschillende manieren worden gepresenteerd. Deze opties zijn bedoeld om samen met de component [component Form Container](form-container.md).

De presentatie van de opties, labels en afzonderlijke opties kan worden gedefinieerd door de inhoudseditor in het dialoogvenster [dialoogvenster configureren](#configure-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Formulieropties is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel | Compatibel |
| [v1](/help/components/v1/form-options-v1.md) | Compatibel | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de component Formulieropties wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_form_options).

### Technische details {#technical-details}

De meest recente technische documentatie over de component Formulieropties [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_form_options_v2).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het type opties definiëren dat moet worden weergegeven, de labels en de beschikbare opties.

![Dialoogvenster Formulieropties Component bewerken](/help/assets/form-options-edit.png)

* **Typen** - Hoe de opties worden gepresenteerd
   * **Selectievakjes**
   * **Keuzerondjes**
   * **Vervolgkeuzelijst**
   * **Vervolgkeuzelijst Multi-select**
* **Titel** - De titel die wordt weergegeven als het label voor de opties
* **Naam** - De naam van het veld dat met de formuliergegevens wordt verzonden
* **Bron** - Waar de opties zijn gedefinieerd
   * **Lokaal** - Gedefinieerd binnen de component
      * Tik of klik op de knop **Toevoegen** knop om een waarde toe te voegen, **Verwijderen** om een waarde te verwijderen
         * **Waarde** - De waarde die wordt opgeslagen wanneer deze optie wordt geselecteerd wanneer het formulier wordt verzonden
         * **Tekst** - Het label voor de optie die op het formulier wordt weergegeven
         * **Actief** - De optie wordt gemarkeerd als geselecteerd wanneer het formulier wordt geladen
         * **Uitgeschakeld** - De optie kan niet worden geselecteerd, maar wordt wel weergegeven
   * **Lijst** - Een statische lijst die elders in AEM is gedefinieerd, wordt gebruikt voor de opties
      * **Lijst** - Het pad van de statische lijst in AEM
         * Gebruik de Browse knoop om van het lijstmiddel de plaats te bepalen
   * **Gegevensbron** - Een gegevensbron wordt gebruikt voor de opties
      * **Gegevensbron** - Type gegevensbron
* **Help-bericht** - Een tip voor de gebruiker wat in het veld kan worden ingevoerd
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component Formulieropties ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
