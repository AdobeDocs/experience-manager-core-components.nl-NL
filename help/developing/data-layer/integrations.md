---
title: Integratie en de Adobe Client Data Layer
description: Leer hoe de Adobe Client Data Layer kan worden geïntegreerd met uw aangepaste componenten en hoe integratie met Adobe Analytics en Adobe Target u kan helpen inzicht in uw website te krijgen
feature: Core Components, Adobe Client Data Layer
role: Architect, Developer, Admin
exl-id: 503dd3dc-fe95-4a17-83f5-1f0c1960993d
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Integratie met de gegevenslaag Adobe Client {#integrations}

De gegevenslaag van de Cliënt van Adobe vermindert de inspanning om websites van instrumenten te voorzien door een gestandaardiseerde methode te verstrekken om om het even welk soort gegevens voor om het even welk manuscript bloot te stellen en toegang te hebben.

De Adobe Client Data Layer kan worden geïntegreerd met uw aangepaste componenten en integratie met Adobe Analytics en Adobe Target kan u helpen inzicht te krijgen in uw website.

## De gegevenslaag inschakelen voor aangepaste componenten {#enabling-custom-components}

Een aangepaste component automatisch toevoegen aan de gegevenslaag:

1. Definieer de eigenschappen van het model van de aangepaste component die moeten worden bijgehouden.
1. Voeg de `data-cmp-data-layer` aan de douanecomponent HTML. Bijv. `data-cmp-data-layer="${mycomponent.data.json}"`.

Als u de gegevenslaag automatisch wilt laten activeren door een `cmp:click` elke keer dat er op een specifiek element van de aangepaste component wordt geklikt, voegt u de `data-cmp-clickable` kenmerk aan het element dat moet worden bijgehouden in de aangepaste component HTML.

De `data-cmp-data-layer-enabled` Het attribuut kan cliënt-kant worden gevraagd om te controleren of wordt de gegevenslaag toegelaten.

>[!TIP]
>
>Voor verdere technische details over de integratie van de Laag van Gegevens van de Cliënt van Adobe met de Componenten van de Kern en hoe te om de Laag van Gegevens op uw douanecomponenten toe te laten, zie [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) in de opslagplaats voor kerncomponenten.

## Integratie met Adobe Analytics en Adobe Target {#analytics-target}

In combinatie met Adobe Analytics en Adobe Target wordt de gegevenslaag voor Adobe-clients de basis van een zeer krachtig en flexibel hulpmiddel dat is ingesteld om inzicht te krijgen in uw digitale ervaringen. De volgende zelfstudies leiden u door voorbeeldintegratie.

### Paginagegevens verzamelen met Adobe Analytics {#collect-page-data}

Leer om de ingebouwde eigenschappen van de Laag van Gegevens van de Cliënt van de Adobe met AEM Componenten van de Kern te gebruiken om gegevens over een pagina in Adobe Experience Manager Sites te verzamelen. Experience Platform Launch en de extensie Adobe Analytics worden gebruikt om regels te maken voor het verzenden van paginagegevens naar Adobe Analytics.

[Bekijk de zelfstudie hier.](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html)

### Aangeklikte componenten bijhouden met Adobe Analytics {#track-clicked-components}

Gebruik de gebeurtenisgestuurde Adobe Client Data Layer met AEM Core Components om kliks van specifieke componenten op een Adobe Experience Manager-site bij te houden. Leer hoe te om regels in Experience Platform Launch te gebruiken om op klikgebeurtenissen te luisteren, filter door component en verzend de gegevens naar een Adobe Analytics met een baken van de spoorverbinding.

[Bekijk de zelfstudie hier.](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html)
