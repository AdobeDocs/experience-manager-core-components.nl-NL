---
title: Component voor sociaal delen
description: De Core Component Social Sharing is een deelwidget Facebook en Pinterest.
role: Architect, Developer, Admin, User
exl-id: 8bd53c76-da91-479b-b416-f978682a3d43
source-git-commit: d435e82d5950336c66997399829e3baf23f170c0
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Component voor sociaal delen{#social-sharing-component}

De Core Component Social Sharing is een deelwidget Facebook en Pinterest.

## Gebruik {#usage}

Met de component Sociaal delen voegt u koppelingen naar Facebook en Pinterest voor delen toe aan de pagina. Deze wordt vaak opgenomen in kop- of voetteksten van pagina&#39;s.

In tegenstelling tot andere componenten worden de instellingen voor de component voor sociaal delen uitgevoerd door de sjabloonauteur via [Initiële pagina-eigenschappen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) en door de auteur van de inhoud via [Pagina-eigenschappen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Sociaal delen is v1, die is geïntroduceerd met versie 1.0.0 van de Core Components en wordt beschreven in dit document.

In de volgende tabel staan alle ondersteunde versies van de component en de AEM versies waarmee de versies van de component compatibel zijn.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_sharing) om de component voor sociaal delen te ervaren en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de het Delen Component [kan op GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

![Dialoogvenster voor bewerken van component delen](/help/assets/sharing-edit.png)

* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

Omdat voor delen speciale paginakoppen vereist zijn, moet het delen op paginaniveau zijn ingeschakeld. Daarom zijn voor de inhoudauteur extra bewerkingsopties voor de component voor delen beschikbaar via het tabblad Delen de [pagina-eigenschappen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Ontwerpdialoogvenster {#design-dialog}

Omdat voor delen speciale paginakoppen vereist zijn, moet het delen op paginaniveau zijn ingeschakeld. Daarom zijn voor de sjabloonauteur de ontwerpopties voor de component voor delen beschikbaar via de [eigenschappen van de startpagina](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html).
