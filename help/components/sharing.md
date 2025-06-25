---
title: Component voor sociaal delen
description: De Core Component Social Sharing Component is een widget voor delen via Facebook en Pinterest.
role: Architect, Developer, Admin, User
exl-id: 8bd53c76-da91-479b-b416-f978682a3d43
index: false
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 1%

---


# Component voor sociaal delen{#social-sharing-component}

De Core Component Social Sharing Component is een widget voor delen via Facebook en Pinterest.

>[!NOTE]
>
>De sociale het Delen Component werd afgeschreven met de Componenten van de Kern [ versie 2.18.0.](/help/versions.md)

{{traditional-aem}}

## Gebruik {#usage}

Met de component Sociaal delen voegt u koppelingen voor delen via Facebook en Pinterest toe aan de pagina. Deze wordt vaak opgenomen in kop- of voetteksten van pagina&#39;s.

In tegenstelling tot andere componenten, worden de montages voor de Sociale Delende Component gedaan door de malplaatjeauteur via [ Oorspronkelijke eigenschappen van de Pagina ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=nl-NL) en door de inhoudauteur via [ Eigenschappen van de Pagina ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=nl-NL).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Sociaal delen is v1, die is geïntroduceerd met versie 1.0.0 van de Core Components en wordt beschreven in dit document.

In de volgende tabel staan alle ondersteunde versies van de component en de AEM-versies waarmee de versies van de component compatibel zijn.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v1 | Compatibel systeem met <br>[ versie 2.17.4 ](/help/versions.md) en vroeger | Compatibel, afgekeurd | Compatibel, afgekeurd | Compatibel, afgekeurd |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

### Technische details {#technical-details}

De recentste technische documentatie over de het Delen Component [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_sharing_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

![ het Delen van Component geeft dialoog uit ](/help/assets/sharing-edit.png)

* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

Omdat voor delen speciale paginakoppen vereist zijn, moet het delen op paginaniveau zijn ingeschakeld. Daarom voor de inhoudauteur geeft de extra opties voor de het delen component uit beschikbaar door het delen lusje de [ pagina eigenschappen ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=nl-NL) uit.

## Ontwerpdialoogvenster {#design-dialog}

Omdat voor delen speciale paginakoppen vereist zijn, moet het delen op paginaniveau zijn ingeschakeld. Daarom voor de malplaatjeauteur zijn de ontwerpopties voor de het delen component beschikbaar door de [ aanvankelijke paginaeigenschappen ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=nl-NL).
