---
title: Sling Context-Aware Configurations en Core Components
description: De Core Components hefboomwerking Sling contextbewuste configuraties voor bepaalde eigenschappen
role: Architect, Developer, Admin
exl-id: d35210f7-a65d-4768-ab9e-f12ec406da2d
source-git-commit: b72defe1bbe6cb286730ac3f508f7d6c14b3fc33
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Sling Context-Aware Configurations en Core Components {#sling-context-aware-configurations}

Contextbewuste configuraties zijn een [onderdeel van verkoop](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html). Zij zijn configuraties die met een inhoudsmiddel of een middelboom verwant zijn en door de Componenten van de Kern worden gebruikt om plaats-brede configuraties toe te staan.

## Contextbewuste configuraties verkopen {#context-aware-configurations}

Uw site heeft mogelijk verschillende configuraties voor verschillende sitegebieden nodig, bijvoorbeeld waar bepaalde parameters kunnen worden gedeeld, waarvoor overerving voor geneste contexten en globale terugvalwaarden vereist is. AEM gebruikmaakt van contextbewuste configuraties die deze mogelijkheid mogelijk maken.

Voor details over configuraties in AEM, [Zie de documentatie van Configurations en Browser van de Configuratie.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/configurations.html)

## In de kerncomponenten gebruiken {#core-components}

Een aantal Core Components-onderdelen maakt gebruik van contextbewuste configuraties. Al dergelijke configuraties worden gevestigd onder de volgende knoop:

* `/conf/<my-site>/sling:configs/<my-configuration>`

Individuele configuraties zijn afhankelijk van de specifieke component of functie. De eigenschappen van de Componenten van de Kern die context-bewuste configuraties gebruiken omvatten:

* [De component Pagina](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/page/v3/page#loading-of-context-aware-cssjs) vertrouwt op context-bewuste configuratie wanneer het teruggeven `link`, `script` en `meta` -tags.
* [PDF Viewer-component](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Gegevenslaag client-Adobe](/help/developing/data-layer/overview.md#installation-activation)
* [AMP-ondersteuning](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
