---
title: PDF Viewer-component
description: Met de PDF Viewer-component kunt u een PDF-document weergeven.
role: Architect, Developer, Admin, User
exl-id: deb635f5-2b73-4e7a-9838-3a941e39e898
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# PDF Viewer-component {#pdf-viewer-component}

Met de component Core Component PDF Viewer kunt u een PDF-document op een pagina opnemen.

## Gebruik {#usage}

De component Core Component PDF Viewer sluit een viewer in om PDF-bestanden weer te geven die zijn opgeslagen als elementen op de pagina.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de PDF Viewer Component is v1, die in juni 2020 is geïntroduceerd met release 2.10.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de PDF Viewer Component wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_pdfviewer).

## Technische details {#technical-details}

De meest recente technische documentatie over de PDF Viewer Component [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

>[!NOTE]
>
>De PDF Viewer-component gebruikt [API&#39;s voor Adobe](https://www.adobe.io/apis/documentcloud/dcsdk.html) en vereist uw beheerder om een [contextbewuste configuratie](/help/developing/context-aware-configs.md) om deze diensten te kunnen gebruiken. Raadpleeg de technische documentatie van het onderdeel voor [details over deze configuratie.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud de viewer definiëren en bepalen hoe deze zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

### Tabblad Configuratie {#configuration-tab}

Het lusje van de Configuratie staat de auteur toe om te bepalen welke PDF zou moeten worden getoond. Het pad kan worden gedefinieerd als een element in AEM of als een absoluut pad naar een andere bron.

![Tabblad Configuratie van het dialoogvenster Bewerken van PDF Viewer Component](/help/assets/pdf-viewer-edit-configuration.png)

### Tab aanpassen {#customize-tab}

Op het tabblad Aanpassen kan de auteur de opties definiëren die beschikbaar zijn in de viewer voor de lezer en kunt u aangeven hoe de viewer moet worden weergegeven.

![Tabblad van het dialoogvenster Bewerken van PDF Viewer Component aanpassen](/help/assets/pdf-viewer-edit-customize.png)

Het aantal beschikbare opties is afhankelijk van de **Type** geselecteerd.

* [Volledig venster](#full-window) - Het weergavegebied wordt weergegeven in de volledige browser. Dit is het meest geschikt voor opslag- en productiviteitstoepassingen.
* [Container op maat](#sized-container) - Het weergavegebied wordt weergegeven in de volledige browser. Dit is het meest geschikt voor opslag- en productiviteitstoepassingen.
* [In line](#in-line) - Alle PDF-pagina&#39;s die op één regel in een webpagina worden weergegeven. Dit is het meest geschikt voor het lezen van toepassingen.

#### Volledig venster {#full-window}

Het weergavegebied wordt weergegeven in de volledige browser. Dit is het meest geschikt voor opslag- en productiviteitstoepassingen.

![De tabbladoptie van het volledige venster van het dialoogvenster Bewerken van PDF Viewer Component aanpassen](/help/assets/pdf-viewer-edit-customize-full.png)

* **Standaardweergavemodus** - Hoe de viewer op de pagina wordt weergegeven
   * Pagina passend maken
   * Aan breedte aanpassen
* **Volledig scherm** - Als deze optie is ingeschakeld, neemt de viewer de volledige hoogte/breedte van de viewport in beslag.
* **Annotatiegereedschappen** - Als deze optie is ingeschakeld, zijn de annotatiegereedschappen beschikbaar.
* **Deelvenster Linkerhand** - Als deze optie is ingeschakeld, wordt het linkerdeelvenster weergegeven.
* **PDF downloaden** - Wanneer deze optie is ingeschakeld, wordt de knop Downloaden weergegeven.
* **PDF afdrukken** - Wanneer deze optie is ingeschakeld, wordt de knop Afdrukken weergegeven.
* **Paginabesturingselementen** - Hiermee schakelt u het gedrag van de besturingselementen voor pagina in of uit.
   * Koppelen
   * Loskoppelen

#### Container op maat {#sized-container}

Het weergavegebied wordt weergegeven in de volledige browser. Dit is het meest geschikt voor opslag- en productiviteitstoepassingen.

![De containeroptie voor tabgrootte aanpassen in het dialoogvenster Bewerken van PDF Viewer Component](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Volledig scherm** - Als deze optie is ingeschakeld, neemt de viewer de volledige hoogte/breedte van de viewport in beslag.
* **PDF downloaden** - Wanneer deze optie is ingeschakeld, wordt de knop Downloaden weergegeven.
* **PDF afdrukken** - Wanneer deze optie is ingeschakeld, wordt de knop Afdrukken weergegeven.
* **Paginabesturingselementen** - Hiermee schakelt u het gedrag van de besturingselementen voor pagina in of uit.
   * Koppelen
   * Loskoppelen

#### In line {#in-line}

Alle PDF-pagina&#39;s die op regel binnen een webpagina worden weergegeven. Dit is het meest geschikt voor het lezen van toepassingen.

![De containeroptie voor tabgrootte aanpassen in het dialoogvenster Bewerken van PDF Viewer Component](/help/assets/pdf-viewer-edit-customize-inline.png)

* **PDF downloaden** - Wanneer deze optie is ingeschakeld, wordt de knop Downloaden weergegeven.
* **PDF afdrukken** - Wanneer deze optie is ingeschakeld, wordt de knop Afdrukken weergegeven.

## Ontwerpdialoogvenster {#design-dialog}

Er is geen dialoogvenster Ontwerpen voor de PDF Viewer-component.
