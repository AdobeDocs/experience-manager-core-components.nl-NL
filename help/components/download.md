---
title: Component downloaden
description: Met de component Core Component Download kunt u een downloadoptie op een pagina maken.
role: Architect, Developer, Admin, User
exl-id: 48e7ade0-b849-4d1f-b836-51196e5ac507
source-git-commit: 327c239b02e0aecee878784c918bfa98d960530e
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 1%

---

# Component downloaden{#download-component}

Met de component Core Component Download kunt u een downloadoptie op een pagina maken.

## Gebruik {#usage}

Met de component Core Component Download kunnen een downloadoptie en het bijbehorende element op een pagina worden opgenomen.

* De eigenschappen van de downloadoptie kunnen worden geselecteerd in het dialoogvenster [dialoogvenster configureren](#configure-dialog).
* De standaardwaarden voor de downloadcomponent kunnen worden gedefinieerd in het dialoogvenster [ontwerpdialoogvenster](#design-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Download Component is v2, die in februari 2022 werd geïntroduceerd met versie 2.18.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v2 | - | Compatibel | Compatibel |
| [v1](v1/download.md) | Compatibel | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de downloadcomponent wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_download).

## Technische details {#technical-details}

De meest recente technische documentatie over de Download Component [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_download_v2).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het downloaditem definiëren en bepalen hoe het zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

![Het tabblad Middelen van het dialoogvenster Bewerken van component downloaden](/help/assets/download-edit-asset.png)

### Tabblad Element {#asset-tab}

De selectie van een downloadmiddel lijkt sterk op de functionaliteit van de [Afbeeldingscomponent](image.md) en ook als hefboom AEM DAM.

* **Element downloaden**
   * Middelen uit het deelvenster [middelenbrowser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of tik op **doorbladeren** uploaden vanuit een lokaal bestandssysteem.
   * Tik of klik op **Wissen** om de selectie van de geselecteerde afbeelding op te heffen.
   * Tik of klik op **Bewerken** tot [de uitvoeringen van het actief beheren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in de middeleneditor.

### Tabblad Eigenschappen {#properties-tab}

![Eigenschappen, tabblad van het dialoogvenster Bewerken van downloadcomponent](/help/assets/download-edit-properties.png)

* **Titel** - Wordt weergegeven als een kop voor het downloaditem
   * **Titel ophalen van DAM-middelen** - Als deze optie is geselecteerd, wordt de titel van het DAM-element automatisch ingevuld.
* **Beschrijving** - Wordt weergegeven als een beschrijvende subkop van het downloaditem
   * **Beschrijving ophalen van DAM-element** - Als deze optie is geselecteerd, wordt de beschrijving automatisch ingevuld met de beschrijving van het DAM-element.
* **Tekst van handeling** - Wordt weergegeven als actietekst voor het downloaditem
   * Dit veld is vereist wanneer u een element uploadt van het bestandssysteem.
   * **Inline weergeven** - Als u de optie selecteert **Tekst van handeling** wordt inline weergegeven.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Stijlen {#styles-tab-edit}

![Het tabblad Stijlen van het dialoogvenster voor bewerken van component downloaden](/help/assets/download-edit-styles.png)

De component Download ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in worden gevormd [ontwerpdialoogvenster](#design-dialog) zodat het vervolgkeuzemenu beschikbaar is.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de component Download gebruikt.

### Tabblad Eigenschappen {#properties-tab-design}

![Het dialoogvenster Ontwerpen van de component Download](/help/assets/download-design.png)

* **Uploaden vanuit bestandssysteem toestaan** - Hiermee kan de auteur van de inhoud een element uit zijn/haar lokale bestandssysteem uploaden als het downloadmiddel.
   * De standaardwaarde is niet geselecteerd.
* **Type titel** - Het HTML-element dat wordt gebruikt voor de titel van de downloadcomponent.
   * Als er geen waarde is geselecteerd, is de standaardwaarde H3.
* **Bestandsgrootte weergeven** - Als deze optie is geselecteerd, wordt de bestandsgrootte van het element weergegeven in de downloadcomponent.
   * De standaardwaarde is geselecteerd.
* **Bestandsindeling weergeven** - Als deze optie is geselecteerd, wordt de bestandsindeling van het element weergegeven in de downloadcomponent.
   * De standaardwaarde is geselecteerd.
* **Bestandsnaam weergeven** - Als deze optie is geselecteerd, wordt de bestandsnaam van het element weergegeven in de downloadcomponent.
   * De standaardwaarde is geselecteerd.

### Tabblad Stijlen {#styles-tab}

De component Image ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
