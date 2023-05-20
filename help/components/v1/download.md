---
title: Component downloaden (v1)
description: Met de component Core Component Download kunt u een downloadoptie op een pagina maken.
role: Architect, Developer, Admin, User
exl-id: ebd63522-218d-4784-bea0-1627c64f5230
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Component downloaden (v1) {#download-component}

Met de component Core Component Download kunt u een downloadoptie op een pagina maken.

## Gebruik {#usage}

Met de component Core Component Download kunnen een downloadoptie en het bijbehorende element op een pagina worden opgenomen.

* De eigenschappen van de downloadoptie kunnen worden geselecteerd in het dialoogvenster [dialoogvenster configureren](#configure-dialog).
* De standaardwaarden voor de downloadcomponent kunnen worden gedefinieerd in het dialoogvenster [ontwerpdialoogvenster](#design-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Download Component beschreven, die in juni 2019 is geïntroduceerd met versie 2.5.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 1 van de downloadcomponent beschreven.
>
>Voor meer informatie over de huidige versie van de Download-component raadpleegt u de [Component downloaden](/help/components/download.md) document.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de downloadcomponent wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_download).

## Technische details {#technical-details}

De meest recente technische documentatie over de Download Component [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_download_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het downloaditem definiëren en bepalen hoe het zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

![Het tabblad Middelen van het dialoogvenster Bewerken van component downloaden](/help/assets/download-edit-asset.png)

### Tabblad Element {#asset-tab}

De selectie van een downloadmiddel lijkt sterk op de functionaliteit van de [Afbeeldingscomponent](image-v1.md) en ook als hefboom AEM DAM.

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
