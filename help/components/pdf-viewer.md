---
title: PDF Viewer-component
description: Met de component PDF Viewer kunt u een PDF-document weergeven.
role: Architect, ontwikkelaar, beheerder, praktijkgerichte
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 1%

---


# PDF-viewercomponent {#pdf-viewer-component}

Met de component Core Component PDF Viewer kunt u een PDF-document op een pagina opnemen.

## Gebruik {#usage}

De component Core Component PDF Viewer sluit een viewer in om PDF-bestanden weer te geven die als elementen op de pagina zijn opgeslagen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de PDF Viewer Component is v1, die in juni 2020 is geïntroduceerd met release 2.10.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_pdfviewer) om de PDF Viewer Component te bekijken en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Kijker PDF [kan op GitHub](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

>[!NOTE]
>
>De PDF Viewer Component gebruikt [Document Services API&#39;s](https://www.adobe.io/apis/documentcloud/dcsdk.html) en vereist dat uw beheerder een [contextbewuste configuratie](/help/developing/context-aware-configs.md) configureert om deze services te kunnen gebruiken. Controleer de technische documentatie van de component voor [details op deze configuratie.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)

## Dialoogvenster {#configure-dialog} configureren

In het dialoogvenster Configureren kan de auteur van de inhoud de viewer definiëren en bepalen hoe deze zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

### Tabblad Configuratie {#configuration-tab}

Op het tabblad Configuratie kan de auteur definiëren welke PDF moet worden weergegeven. Het pad kan worden gedefinieerd als een element in AEM of als een absoluut pad naar een andere bron.

![Tabblad Configuratie van het dialoogvenster Bewerken van de component PDF Viewer](/help/assets/pdf-viewer-edit-configuration.png)

### Tab {#customize-tab} aanpassen

Op het tabblad Aanpassen kan de auteur de opties definiëren die beschikbaar zijn in de viewer voor de lezer en kunt u aangeven hoe de viewer moet worden weergegeven.

![Tabblad van het dialoogvenster Bewerken van PDF Viewer Component aanpassen](/help/assets/pdf-viewer-edit-customize.png)

Het aantal beschikbare opties is afhankelijk van het type **Type** dat is geselecteerd.

* [Volledig venster](#full-window)  - Het weergavegebied wordt weergegeven in de volledige browser. Dit is het meest geschikt voor opslag- en productiviteitstoepassingen.
* [Container](#sized-container)  met grootte - Het weergavegebied wordt weergegeven in de volledige browser. Dit is het meest geschikt voor opslag- en productiviteitstoepassingen.
* [In-line](#in-line)  - Alle PDF-pagina&#39;s worden op één regel binnen een webpagina weergegeven. Dit is het meest geschikt voor het lezen van toepassingen.

#### Volledig venster {#full-window}

Het weergavegebied wordt weergegeven in de volledige browser. Dit is het meest geschikt voor opslag- en productiviteitstoepassingen.

![Optie voor het volledige venster van het dialoogvenster Bewerken van de component PDF Viewer aanpassen](/help/assets/pdf-viewer-edit-customize-full.png)

* **Standaardweergavemodus**  - Hoe de viewer op de pagina past waar deze wordt weergegeven
   * Pagina passend maken
   * Aanpassen aan breedte
* **Volledig scherm**  - Als deze optie is ingeschakeld, neemt de viewer de volledige hoogte/breedte van de viewport in beslag.
* **Annotatiegereedschappen**  - Wanneer deze optie is ingeschakeld, zijn de annotatiegereedschappen beschikbaar.
* **Deelvenster**  links - Wanneer deze optie is ingeschakeld, wordt het linkerdeelvenster weergegeven.
* **PDF**  downloaden - Wanneer deze optie is ingeschakeld, wordt de knop Downloaden weergegeven.
* **PDF**  afdrukken - Wanneer deze optie is ingeschakeld, wordt de knop Afdrukken weergegeven.
* **Besturingselementen voor**  pagina - Hiermee schakelt u het gedrag van de paginaconcentraties in of uit.
   * Koppelen
   * Loskoppelen

#### Container {#sized-container}

Het weergavegebied wordt weergegeven in de volledige browser. Dit is het meest geschikt voor opslag- en productiviteitstoepassingen.

![De containeroptie voor tabs aanpassen in het dialoogvenster Bewerken van de PDF Viewer Component](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Volledig scherm**  - Als deze optie is ingeschakeld, neemt de viewer de volledige hoogte/breedte van de viewport in beslag.
* **PDF**  downloaden - Wanneer deze optie is ingeschakeld, wordt de knop Downloaden weergegeven.
* **PDF**  afdrukken - Wanneer deze optie is ingeschakeld, wordt de knop Afdrukken weergegeven.
* **Besturingselementen voor**  pagina - Hiermee schakelt u het gedrag van de paginaconcentraties in of uit.
   * Koppelen
   * Loskoppelen

#### In-line {#in-line}

Alle PDF-pagina&#39;s worden op één regel binnen een webpagina gerenderd. Dit is het meest geschikt voor het lezen van toepassingen.

![De containeroptie voor tabs aanpassen in het dialoogvenster Bewerken van de PDF Viewer Component](/help/assets/pdf-viewer-edit-customize-inline.png)

* **PDF**  downloaden - Wanneer deze optie is ingeschakeld, wordt de knop Downloaden weergegeven.
* **PDF**  afdrukken - Wanneer deze optie is ingeschakeld, wordt de knop Afdrukken weergegeven.

## Ontwerpdialoogvenster {#design-dialog}

Er is geen dialoogvenster Ontwerpen voor de PDF Viewer-component.
