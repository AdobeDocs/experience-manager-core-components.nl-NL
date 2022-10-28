---
title: Component E-mailknop
description: Met de component E-mailknop kunt u een knopitem in uw inhoud configureren en weergeven.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 1%

---


# Component E-mailknop {#email-button-component}

Met de component E-mailknop kunt u een knopitem in uw inhoud configureren en weergeven.

## Gebruik {#usage}

Met de component E-mailknop kunt u een knop in uw inhoud opnemen, waarop door de inhoudslezer kan worden geklikt en die aan extra bronnen is gekoppeld.

* De eigenschappen van de knop kunnen worden geselecteerd in het dialoogvenster [configureren, dialoogvenster.](#configure-dialog)
* Stijlen voor de component E-mailknop kunnen worden gedefinieerd in het gedeelte [ontwerpdialoogvenster.](#design-dialog)

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Email Button is v1, die in oktober 2022 is geïntroduceerd met release x van de Email Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies e-mailen.](/help/email/versions.md)

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga voor meer informatie over de component E-mailknop en de configuratieopties en de HTML- en JSON-uitvoer naar de [Componentbibliotheek.](https://adobe.com/go/aem_cmp_library_email_button)

## Technische details {#technical-details}

De meest recente technische documentatie over de component Email Button [kan op GitHub worden gevonden.](https://adobe.com/go/aem_cmp_tech_email_button_v1)

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [De ontwikkelaarsdocumentatie van de Componenten van de kern.](/help/developing/overview.md)

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud de knop definiëren en bepalen hoe deze zich gedraagt en wordt weergegeven voor een lezer van uw inhoud.

### Tabblad Eigenschappen {#properties-tab}

![Het tabblad Eigenschappen van het dialoogvenster Bewerken van component Button](/help/email/assets/email-button-edit-properties.png)

* **Tekst** - De tekst die op de knop moet worden weergegeven
   * Klik op het pictogram Campagne om het dialoogvenster [Adobe Campaign-variabele selecteren](/help/email/campaign-variables.md) om dynamische inhoud uit Adobe Campaign in te voegen.
* **Koppeling** - Koppeling maken naar een inhoudspagina binnen AEM, een externe bron of een anker
   * Gebruik de **Dialoogvenster Selectie** om een pad te kiezen binnen AEM.
   * Klik op het pictogram Campagne om het dialoogvenster [Adobe Campaign-variabele selecteren](/help/email/campaign-variables.md) om dynamische inhoud uit Adobe Campaign in te voegen.
* **Pictogram** - Id voor weergave van een pictogram in de knop
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML bepalen.
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende inhoud te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor CSS.
* **Koppeling openen op nieuw tabblad** - Als deze optie is ingeschakeld, wordt de koppeling geopend in een nieuw browsertabblad.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheid, tabblad van het dialoogvenster Bewerken van component Button](/help/email/assets/email-button-edit-accessibility.png)

Op de **Toegankelijkheid** tab, waarden kunnen worden ingesteld voor [Toegankelijkheid ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) labels voor de component.

* **Label** - Waarde van een ARIA-labelkenmerk voor de component

### Tabblad Stijlen {#styles-tab-edit}

De component Email Button ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in worden gevormd [ontwerpdialoogvenster](#design-dialog) zodat het tabblad beschikbaar is.

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component Email Button ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
