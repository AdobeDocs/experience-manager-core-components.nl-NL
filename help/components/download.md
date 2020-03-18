---
title: Component downloaden
description: Met de component Core Component Download kunt u een downloadoptie op een pagina maken.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Component downloaden{#download-component}

Met de component Core Component Download kunt u een downloadoptie op een pagina maken.

## Gebruik {#usage}

Met de component Core Component Download kunnen een downloadoptie en het bijbehorende element op een pagina worden opgenomen.

* De eigenschappen van de downloadoptie kunnen worden geselecteerd in het dialoogvenster [](#configure-dialog)configureren.
* De standaardwaarden voor de downloadcomponent kunnen worden gedefinieerd in het dialoogvenster [](#design-dialog)Ontwerp.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Download Component is v1, die in juni 2019 met versie 2.5.0 van de Core Components is geïntroduceerd en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v1 | Compatibel | Compatibel | Compatibel | Compatibel |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_download)voor meer informatie over de downloadcomponent en voorbeelden van de configuratieopties en over HTML- en JSON-uitvoer.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Download [kan op GitHub](https://adobe.com/go/aem_cmp_tech_download_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het downloaditem definiëren en bepalen hoe het zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

![](/help/assets/screen-shot-2019-06-17-09.49.14.png)

### Tabblad Element {#asset-tab}

De selectie van een downloadmiddel is zeer gelijkaardig aan de functionaliteit van de Component [van het](image.md) Beeld en gebruikt eveneens DAM van AEM.

* **Element downloaden**
   * Zet een element neer vanuit de [middelenbrowser](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of tik op de **bladeroptie** om te uploaden vanaf een lokaal bestandssysteem.
   * Tik of klik op **Wissen** om de selectie van de geselecteerde afbeelding ongedaan te maken.
   * Tik of klik op **Bewerken** om de uitvoeringen van het element [in de middeleneditor te](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) beheren.

### Tabblad Eigenschappen {#properties-tab}

![](/help/assets/screen-shot-2019-06-17-09.49.51.png)

* **Titel** - Wordt weergegeven als een kop voor het downloaditem
   * **Titel ophalen van DAM-element** - Als deze optie is geselecteerd, wordt de titel automatisch gevuld met de titel van het DAM-element.
* **Beschrijving** - Wordt weergegeven als een beschrijvende subkop van het downloaditem
   * **Beschrijving ophalen van DAM-element** - Als deze optie is geselecteerd, wordt de beschrijving automatisch gevuld met de beschrijving van het DAM-element.
* **Tekst** van handeling - wordt weergegeven als actietekst voor het downloaditem
   * Dit veld is vereist wanneer u een element uploadt van het bestandssysteem.
   * **Inline** weergeven - Als u deze optie selecteert, wordt de opgegeven **handelingstekst** inline weergegeven.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de component Download gebruikt.

### Tabblad Eigenschappen {#properties-tab-design}

![](/help/assets/screen-shot-2019-06-17-10.04.31.png)

* **Standaardhandelingstekst** - Definieert de standaardtekst voor **handelingen** die wordt opgegeven wanneer een auteur de component Download aan een pagina toevoegt.
* **Uploaden vanuit bestandssysteem** toestaan - Hiermee kan de auteur van de inhoud een element uit zijn/haar lokale bestandssysteem uploaden als het downloadmiddel.
   * De standaardwaarde is niet geselecteerd.
* **Titeltype** : het HTML-element dat wordt gebruikt voor de titel van de component Download.
   * Als er geen waarde is geselecteerd, is de standaardwaarde H3.
* **Bestandsgrootte** weergeven - Als u deze optie selecteert, wordt de bestandsgrootte van het element weergegeven in de downloadcomponent.
   * De standaardwaarde is geselecteerd.
* **Bestandsindeling** weergeven - Als u deze optie selecteert, wordt de bestandsindeling van het element weergegeven in de downloadcomponent.
   * De standaardwaarde is geselecteerd.
* **Bestandsnaam** weergeven - Als deze optie is geselecteerd, wordt de bestandsnaam van het element weergegeven in de downloadcomponent.
   * De standaardwaarde is geselecteerd.

### Tabblad Stijlen {#styles-tab}

De component Image ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).
