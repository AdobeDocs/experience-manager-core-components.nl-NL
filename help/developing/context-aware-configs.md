---
title: Sling Context-Aware Configurations en Core Components
description: De Core Components hefboomwerking Sling contextbewuste configuraties voor bepaalde eigenschappen
role: Developer, Admin
exl-id: d35210f7-a65d-4768-ab9e-f12ec406da2d
source-git-commit: 7ba1374bd64686c2e7ac44398d77fb187ff60949
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Sling Context-Aware Configurations en Core Components {#sling-context-aware-configurations}

De context-bewuste configuraties zijn a [&#x200B; eigenschap van het Verdelen &#x200B;](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html). Zij zijn configuraties die met een inhoudsmiddel of een middelboom verwant zijn en door de Componenten van de Kern worden gebruikt om plaats-brede configuraties toe te staan.

## Contextbewuste configuraties verkopen {#context-aware-configurations}

Uw site heeft mogelijk verschillende configuraties voor verschillende sitegebieden nodig, bijvoorbeeld waar bepaalde parameters kunnen worden gedeeld, waarvoor overerving voor geneste contexten en globale terugvalwaarden vereist is. AEM maakt gebruik van configuraties waarbij rekening wordt gehouden met de verkoopcontext, waardoor deze mogelijkheid wordt ingeschakeld.

Voor details over configuraties in AEM, [&#x200B; zie de Browser van Configuraties en van de Configuratie documentatie.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/configurations.html)

## In de kerncomponenten gebruiken {#core-components}

Een aantal Core Components-onderdelen maakt gebruik van contextbewuste configuraties. Al dergelijke configuraties worden gevestigd onder de volgende knoop:

* `/conf/<my-site>/sling:configs/<my-configuration>`

Individuele configuraties zijn afhankelijk van de specifieke component of functie. De eigenschappen van de Componenten van de Kern die context-bewuste configuraties gebruiken omvatten:

* [&#x200B; de Component van de Pagina &#x200B;](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/page/v3/page#loading-of-context-aware-cssjs) baseert zich op context-bewuste configuratie wanneer het teruggeven `link`, `script` en `meta` markeringen.
* [PDF Viewer-component](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Adobe Client Data Layer](/help/developing/data-layer/overview.md#installation-activation)
* [AMP-ondersteuning](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
