---
title: Component voor sociaal delen
description: De Core Component Social Sharing Component is een widget voor delen via Facebook en Pinterest.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 1%

---


# Component voor sociaal delen{#social-sharing-component}

De Core Component Social Sharing Component is een widget voor delen via Facebook en Pinterest.

## Gebruik {#usage}

De component Sociaal delen voegt koppelingen voor delen via Facebook en Pinterest toe aan de pagina. Deze wordt vaak opgenomen in kop- of voetteksten van pagina&#39;s.

In tegenstelling tot andere componenten worden de instellingen voor de component Sociaal delen uitgevoerd door de sjabloonauteur via de eigenschappen [Eerste pagina en door de auteur van de inhoud via](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) Pagina-eigenschappen [](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component voor sociaal delen is v1, die is geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3. Deze versie wordt in dit document beschreven.

In de volgende tabel staan alle ondersteunde versies van de component en de AEM-versies waarmee de versies van de component compatibel zijn.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel | Compatibel | Compatibel |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_sharing)om de component voor sociaal delen te ervaren en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de het Delen Component [kan op GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster Bewerken {#edit-dialog}

![Dialoogvenster voor bewerken van component delen](/help/assets/sharing-edit.png)

* **ID** - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

Omdat voor delen speciale paginakoppen vereist zijn, moet het delen op paginaniveau zijn ingeschakeld. Voor de inhoudauteur zijn daarom aanvullende bewerkingsopties voor de component voor delen beschikbaar via het tabblad Delen in de [pagina-eigenschappen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Ontwerpdialoogvenster {#design-dialog}

Omdat voor delen speciale paginakoppen vereist zijn, moet het delen op paginaniveau zijn ingeschakeld. Daarom zijn voor de sjabloonauteur de ontwerpopties voor de component voor delen beschikbaar via de [initiële pagina-eigenschappen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).
