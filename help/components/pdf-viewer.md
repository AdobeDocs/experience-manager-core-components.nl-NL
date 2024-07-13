---
title: PDF Viewer-component
description: Met de PDF Viewer-component kunt u een PDF-document weergeven.
role: Architect, Developer, Admin, User
exl-id: deb635f5-2b73-4e7a-9838-3a941e39e898
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '681'
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
| v1 | Compatibel systeem met <br>[ versie 2.17.4 ](/help/versions.md) en vroeger | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Kijker van de PDF te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_pdfviewer).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Kijker van de PDF [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

>[!NOTE]
>
>De PDF Viewer Component leverages [ de Diensten APIs van het Document van de Adobe ](https://www.adobe.io/apis/documentcloud/dcsdk.html) en vereist uw beheerder om a [ context bewuste configuratie ](/help/developing/context-aware-configs.md) te vormen om deze diensten te gebruiken. Controleer de technische documentatie van de component voor [ details op deze configuratie.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud de viewer definiëren en bepalen hoe deze zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

### Tabblad Configuratie {#configuration-tab}

Het lusje van de Configuratie staat de auteur toe om te bepalen welke PDF zou moeten worden getoond. Het pad kan worden gedefinieerd als een element in AEM of als een absoluut pad naar een andere bron.

![ het lusje van de Configuratie van uitgeeft dialoog van de Component van de Kijker van de PDF ](/help/assets/pdf-viewer-edit-configuration.png)

### Tab aanpassen {#customize-tab}

Op het tabblad Aanpassen kan de auteur de opties definiëren die beschikbaar zijn in de viewer voor de lezer en kunt u aangeven hoe de viewer moet worden weergegeven.

![ pas lusje van uit uitgeeft dialoog van de Component van de Kijker van de PDF ](/help/assets/pdf-viewer-edit-customize.png) aan

Het aantal beschikbare opties hangt van het **Type** af dat wordt geselecteerd.

* [ Volledig Venster ](#full-window) - het het bekijken gebied geeft in volledige browser terug. Dit is het meest geschikt voor opslag- en productiviteitstoepassingen.
* [ Verdeelde Container ](#sized-container) - het het bekijken gebied geeft in volledige browser terug. Dit is het meest geschikt voor opslag- en productiviteitstoepassingen.
* [ In-Lijn ](#in-line) - Alle die pagina&#39;s van de PDF in lijn binnen een Web-pagina worden teruggegeven. Dit is het meest geschikt voor het lezen van toepassingen.

#### Volledig venster {#full-window}

Het weergavegebied wordt weergegeven in de volledige browser. Dit is het meest geschikt voor opslag- en productiviteitstoepassingen.

![ pas lusjevolledige vensteroptie van de uit te geven dialoog van de Component van de Kijker van de PDF ](/help/assets/pdf-viewer-edit-customize-full.png) aan

* **Modus Standaard van de Mening** - hoe de kijker aan de pagina zal worden aangepast waar het wordt getoond
   * Pagina passend maken
   * Aan breedte aanpassen
* **Volledig Scherm** - wanneer toegelaten, zal de kijker de volledige hoogte/breedte van viewport opnemen.
* **de Hulpmiddelen van de Annotatie** - wanneer toegelaten, zijn de annotatiehulpmiddelen beschikbaar.
* **Linkerhandpaneel** - wanneer toegelaten, wordt het linkerhandpaneel getoond.
* **Download PDF** - wanneer toegelaten, wordt de downloadknoop getoond.
* **PDF van de Druk** - wanneer toegelaten, wordt de drukknoop getoond.
* **Controles van de Pagina** - knevels het gedrag van de paginacontroles.
   * Koppelen
   * Loskoppelen

#### Container op maat {#sized-container}

Het weergavegebied wordt weergegeven in de volledige browser. Dit is het meest geschikt voor opslag- en productiviteitstoepassingen.

![ pas lusje rangschikte containeroptie van uit uitgeeft dialoog van de Component van de Kijker van de PDF ](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Volledig Scherm** - wanneer toegelaten, zal de kijker de volledige hoogte/breedte van viewport opnemen.
* **Download PDF** - wanneer toegelaten, wordt de downloadknoop getoond.
* **PDF van de Druk** - wanneer toegelaten, wordt de drukknoop getoond.
* **Controles van de Pagina** - knevels het gedrag van de paginacontroles.
   * Koppelen
   * Loskoppelen

#### In-line {#in-line}

Alle PDF-pagina&#39;s die op regel binnen een webpagina worden weergegeven. Dit is het meest geschikt voor het lezen van toepassingen.

![ pas lusje rangschikte containeroptie van uit uitgeeft dialoog van de Component van de Kijker van de PDF ](/help/assets/pdf-viewer-edit-customize-inline.png)

* **Download PDF** - wanneer toegelaten, wordt de downloadknoop getoond.
* **PDF van de Druk** - wanneer toegelaten, wordt de drukknoop getoond.

## Ontwerpdialoogvenster {#design-dialog}

Er is geen dialoogvenster Ontwerpen voor de PDF Viewer-component.
