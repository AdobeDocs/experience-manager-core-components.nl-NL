---
title: Component downloaden
description: Met de component Core Component Download kunt u een downloadoptie op een pagina maken.
role: Architect, Developer, Admin, User
exl-id: 48e7ade0-b849-4d1f-b836-51196e5ac507
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 1%

---

# Component downloaden{#download-component}

Met de component Core Component Download kunt u een downloadoptie op een pagina maken.

## Gebruik {#usage}

Met de component Core Component Download kunnen een downloadoptie en het bijbehorende element op een pagina worden opgenomen.

* De eigenschappen van de downloadoptie kunnen worden geselecteerd in [vorm dialoog](#configure-dialog).
* De standaardwaarden voor de downloadcomponent kunnen worden gedefinieerd in het [ontwerpdialoogvenster](#design-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Download Component is v1, die in juni 2019 met versie 2.5.0 van de Core Components is geïntroduceerd en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_download) om de Download-component te ervaren en voorbeelden van de configuratieopties en de HTML- en JSON-uitvoer te bekijken.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Download [kan op GitHub](https://adobe.com/go/aem_cmp_tech_download_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het downloaditem definiëren en bepalen hoe het zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

![Het tabblad Middelen van het dialoogvenster Bewerken van component downloaden](/help/assets/download-edit-asset.png)

### Tabblad Element {#asset-tab}

De selectie van een downloadmiddel is zeer gelijkaardig aan de functionaliteit van [de Component van het Beeld](image.md) en ook hefboomwerkingen AEM DAM.

* **Element downloaden**
   * Zet een element neer vanuit de [assetbrowser](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of tik op de optie **browse** om te uploaden vanaf een lokaal bestandssysteem.
   * Tik of klik op **Wissen** om de selectie van de geselecteerde afbeelding ongedaan te maken.
   * Tik of klik op **Bewerken** om de uitvoeringen van het element te beheren](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in de elementeneditor.[

### Tabblad Eigenschappen {#properties-tab}

![Eigenschappen, tabblad van het dialoogvenster Bewerken van downloadcomponent](/help/assets/download-edit-properties.png)

* **Titel**  - Toont als titel voor het downloadpunt
   * **Haal de titel op van DAM-element** . Als deze optie is geselecteerd, wordt de titel automatisch ingevuld met de titel van het DAM-element.
* **Beschrijving**  - Wordt weergegeven als een beschrijvende subkop van het downloaditem
   * **Beschrijving ophalen van DAM-element**  - Als deze optie is geselecteerd, wordt de beschrijving automatisch gevuld met de beschrijving van het DAM-element.
* **Tekst**  van handeling - wordt weergegeven als actietekst voor het downloaditem
   * Dit veld is vereist wanneer u een element uploadt van het bestandssysteem.
   * **Inline**  weergeven - Als u deze optie selecteert, wordt de opgegeven  **Action** Text inline weergegeven.
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de component Download gebruikt.

### Tabblad Eigenschappen {#properties-tab-design}

![Het dialoogvenster Ontwerpen van de component Download](/help/assets/download-design.png)

* **Uploaden vanuit bestandssysteem**  toestaan - Hiermee kan de auteur van de inhoud een element uit zijn/haar lokale bestandssysteem uploaden als het downloadmiddel.
   * De standaardwaarde is niet geselecteerd.
* **Titeltype** : het HTML-element dat wordt gebruikt voor de titel van de component Download.
   * Als er geen waarde is geselecteerd, is de standaardwaarde H3.
* **Bestandsgrootte**  weergeven - Als u deze optie selecteert, wordt de bestandsgrootte van het element weergegeven in de downloadcomponent.
   * De standaardwaarde is geselecteerd.
* **Bestandsindeling**  weergeven - Als u deze optie selecteert, wordt de bestandsindeling van het element weergegeven in de downloadcomponent.
   * De standaardwaarde is geselecteerd.
* **Bestandsnaam**  weergeven - Als deze optie is geselecteerd, wordt de bestandsnaam van het element weergegeven in de downloadcomponent.
   * De standaardwaarde is geselecteerd.

### Tabblad Stijlen {#styles-tab}

De component van het Beeld steunt het AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
