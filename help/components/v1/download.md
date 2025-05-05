---
title: Component downloaden (v1)
description: Met de component Core Component Download kunt u een downloadoptie op een pagina maken.
role: Architect, Developer, Admin, User
exl-id: ebd63522-218d-4784-bea0-1627c64f5230
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---

# Component downloaden (v1) {#download-component}

Met de component Core Component Download kunt u een downloadoptie op een pagina maken.

## Gebruik {#usage}

Met de component Core Component Download kunnen een downloadoptie en het bijbehorende element op een pagina worden opgenomen.

* De eigenschappen van de downloadoptie kunnen in [ worden geselecteerd vormen dialoog ](#configure-dialog).
* De gebreken voor de downloadcomponent kunnen in de [ ontwerpdialoog ](#design-dialog) worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Download Component beschreven, die in juni 2019 is geïntroduceerd met versie 2.5.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 1 van de downloadcomponent beschreven.
>
>Voor details van de huidige versie van de Component van de Download, zie het [ document van de Component van de Download ](/help/components/download.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Download te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_download).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Download [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_download_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het downloaditem definiëren en bepalen hoe het zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

![ het lusje van Activa van de Download Component geeft dialoog uit ](/help/assets/download-edit-asset.png)

### Tabblad Element {#asset-tab}

De selectie van een downloadactiva is zeer gelijkaardig aan de functionaliteit van de [ Component van het Beeld ](image-v1.md) en eveneens hefboomwerkingen AEM DAM.

* **Activa van de Download**
   * Daling een activa van [ activa browser ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=nl-NL) of ontvang **doorbladert** optie om van een lokaal dossiersysteem te uploaden.
   * Tik of klik **Duidelijk** om het momenteel geselecteerde beeld te deselecteren.
   * Tik of klik **uitgeven** [ om de vertoningen van de activa ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=nl-NL) in de activaredacteur te beheren.

### Tabblad Eigenschappen {#properties-tab}

![ het lusje van Eigenschappen van de Download Component geeft dialoog uit ](/help/assets/download-edit-properties.png)

* **Titel** - Toont als titel voor het downloadpunt
   * **krijgt titel van activa DAM** - wanneer geselecteerd, wordt de titel automatisch bevolkt met de titel van het element DAM.
* **Beschrijving** - Toont als beschrijvende ondertitel van het downloadpunt
   * **krijgt beschrijving van activa DAM** - wanneer geselecteerd, wordt de beschrijving automatisch bevolkt met de beschrijving van het element DAM.
* **Tekst van de Actie** - Toont als actietekst voor het downloadpunt
   * Dit veld is vereist wanneer u een element uploadt van het bestandssysteem.
   * **Inline van de Vertoning** - wanneer geselecteerd zal de verstrekte **Tekst van de Actie** inline tonen.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de component Download gebruikt.

### Tabblad Eigenschappen {#properties-tab-design}

![ dialoog van het Ontwerp van de Component van de Download ](/help/assets/download-design.png)

* **sta upload van dossiersysteem** toe - staat de inhoudsauteur toe om activa van zijn/haar lokaal filesystem als downloadmiddel te uploaden.
   * De standaardwaarde is niet geselecteerd.
* **Type van Titel** - het element van HTML dat voor de titel van de Component van de Download wordt gebruikt.
   * Als er geen waarde is geselecteerd, is de standaardwaarde H3.
* **Grootte van het Dossier van de Vertoning** - wanneer geselecteerd zal de dossiergrootte van de activa in de downloadcomponent worden getoond.
   * De standaardwaarde is geselecteerd.
* **het Formaat van het Dossier van de Vertoning** - wanneer geselecteerd zal het dossierformaat van de activa in de downloadcomponent worden getoond.
   * De standaardwaarde is geselecteerd.
* **Filename van de Vertoning** - wanneer geselecteerd filename van het element in de downloadcomponent zal worden getoond.
   * De standaardwaarde is geselecteerd.

### Tabblad Stijlen {#styles-tab}

De Component van het Beeld steunt het AEM [ Systeem van de Stijl ](/help/get-started/authoring.md#component-styling).
