---
title: Component voor sociaal delen
description: De Core Component Social Sharing is een deelwidget Facebook en Pinterest.
role: Architect, Developer, Admin, User
exl-id: 8bd53c76-da91-479b-b416-f978682a3d43
source-git-commit: 327c239b02e0aecee878784c918bfa98d960530e
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 1%

---

# Component voor sociaal delen{#social-sharing-component}

De Core Component Social Sharing is een deelwidget Facebook en Pinterest.

>[!NOTE]
>
>De component voor sociaal delen is gedevalueerd met Core-componenten [release 2.18.0.](/help/versions.md)

## Gebruik {#usage}

Met de component Sociaal delen voegt u koppelingen naar Facebook en Pinterest voor delen toe aan de pagina. Deze wordt vaak opgenomen in kop- of voetteksten van pagina&#39;s.

In tegenstelling tot andere componenten worden de instellingen voor de component voor sociaal delen uitgevoerd door de sjabloonauteur via [Initiële pagina-eigenschappen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) en door de auteur van de inhoud via [Pagina-eigenschappen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Sociaal delen is v1, die is geïntroduceerd met versie 1.0.0 van de Core Components en wordt beschreven in dit document.

In de volgende tabel staan alle ondersteunde versies van de component en de AEM versies waarmee de versies van de component compatibel zijn.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel, afgekeurd | Compatibel, afgekeurd |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

### Technische details {#technical-details}

De meest recente technische documentatie over de delende component [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_sharing_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

![Dialoogvenster voor bewerken van component delen](/help/assets/sharing-edit.png)

* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

Omdat voor delen speciale paginakoppen vereist zijn, moet het delen op paginaniveau zijn ingeschakeld. Voor de inhoudauteur zijn daarom aanvullende bewerkingsopties voor de component voor delen beschikbaar via het tabblad Delen. [pagina-eigenschappen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Ontwerpdialoogvenster {#design-dialog}

Omdat voor delen speciale paginakoppen vereist zijn, moet het delen op paginaniveau zijn ingeschakeld. Daarom zijn voor de sjabloonauteur de ontwerpopties voor de component voor delen beschikbaar via de [eigenschappen van eerste pagina](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html).
