---
title: Sling Context-Aware Configurations en Core Components
description: De Core Components hefboomwerking Sling contextbewuste configuraties voor bepaalde eigenschappen
translation-type: tm+mt
source-git-commit: 24a810ff634f8846881dfa0095e879476d0f16f0
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# Sling Context-Aware Configurations en Core Components {#sling-context-aware-configurations}

Contextbewuste configuraties zijn een eigenschap van het Verdelen en zijn configuraties die met een inhoudsmiddel of een middelboom verwant zijn en door de Componenten van de Kern worden gebruikt om plaats-brede configuraties toe te staan.

## Contextbewuste configuraties verkopen {#context-aware-configurations}

Uw site heeft mogelijk verschillende configuraties voor verschillende sitegebieden nodig, bijvoorbeeld waar bepaalde parameters kunnen worden gedeeld, waarvoor overerving voor geneste contexten en globale terugvalwaarden vereist is. Dit wordt mogelijk gemaakt door contextbewuste configuraties te verkopen.

Raadpleeg de documentatie bij Apache voor meer informatie over contextbewuste configuraties voor Sling. [](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html)

## In de kerncomponenten gebruiken {#core-components}

Een aantal Core Components-onderdelen maakt gebruik van contextbewuste configuraties. Al dergelijke configuraties worden gevestigd onder de volgende knoop:

* `/conf/<my-site>/sling:configs/<my-configuration>`

Individuele configuraties zijn afhankelijk van de specifieke component of functie. De eigenschappen van de Componenten van de Kern die context-bewuste configuraties gebruiken zijn:

* [PDF Viewer-component](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Gegevenslaag Adobe-client](/help/developing/data-layer/overview.md#installation-activation)
* [AMP-ondersteuning](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
