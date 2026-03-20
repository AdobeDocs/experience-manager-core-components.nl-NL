---
title: Integratie en de Adobe Client Data Layer
description: Leer hoe de Adobe Client Data Layer kan worden geïntegreerd met uw aangepaste componenten en hoe integratie met Adobe Analytics en Adobe Target u kan helpen inzicht te krijgen in uw website
feature: Core Components, Adobe Client Data Layer
role: Developer, Admin
exl-id: 503dd3dc-fe95-4a17-83f5-1f0c1960993d
source-git-commit: 7ba1374bd64686c2e7ac44398d77fb187ff60949
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# Integratie met de Adobe Client Data Layer {#integrations}

De gegevenslaag van de Cliënt van Adobe vermindert de inspanning aan instrumentwebsites door een gestandaardiseerde methode te verstrekken om om het even welk soort gegevens voor om het even welk manuscript bloot te stellen en toegang te hebben.

De Adobe Client Data Layer kan worden geïntegreerd met uw aangepaste componenten en integratie met Adobe Analytics en Adobe Target kan u helpen inzicht in uw website te krijgen.

## De gegevenslaag inschakelen voor aangepaste componenten {#enabling-custom-components}

Een aangepaste component automatisch toevoegen aan de gegevenslaag:

1. Definieer de eigenschappen van het model van de aangepaste component die moeten worden bijgehouden.
1. Voeg het kenmerk `data-cmp-data-layer` toe aan de aangepaste component HTML, bijvoorbeeld `data-cmp-data-layer="${mycomponent.data.json}"`.

Als u de gegevenslaag automatisch een `cmp:click` -gebeurtenis wilt laten activeren telkens wanneer op een specifiek element van de aangepaste component wordt geklikt, voegt u het kenmerk `data-cmp-clickable` toe aan het element dat moet worden bijgehouden in de aangepaste component HTML.

Het attribuut `data-cmp-data-layer-enabled` kan client-kant worden gevraagd om te controleren of de gegevenslaag is ingeschakeld.

>[!TIP]
>
>Voor verdere technische details over de integratie van de Laag van Gegevens van de Cliënt van Adobe met de Componenten van de Kern en hoe te om de Laag van Gegevens op uw douanecomponenten toe te laten, zie het [`DATA_LAYER_INTEGRATION.md` &#x200B;](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) dossier in de bewaarplaats van de Componenten van de Kern.

## Integratie met Adobe Analytics en Adobe Target {#analytics-target}

In combinatie met Adobe Analytics en Adobe Target wordt de Adobe Client Data Layer de basis van een zeer krachtige en flexibele tool die is ingesteld om inzicht te krijgen in uw digitale ervaringen. De volgende zelfstudies leiden u door voorbeeldintegratie.

### Paginagegevens verzamelen met Adobe Analytics {#collect-page-data}

Leer de ingebouwde functies van de Adobe Client Data Layer met AEM Core Components te gebruiken om gegevens over een pagina in Adobe Experience Manager Sites te verzamelen. Experience Platform Launch en de Adobe Analytics-extensie worden gebruikt om regels te maken voor het verzenden van paginagegevens naar Adobe Analytics.

[Bekijk de zelfstudie hier.](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html?lang=nl-NL)

### Aangeklikte componenten bijhouden met Adobe Analytics {#track-clicked-components}

Gebruik de gebeurtenisgestuurde Adobe Client Data Layer met AEM Core Components om kliks van specifieke componenten op een Adobe Experience Manager-site bij te houden. Leer hoe te om regels in de Lancering van het Platform van de Ervaring te gebruiken om op klikgebeurtenissen te luisteren, filter door component te filtreren en de gegevens naar een Adobe Analytics met een baken van de spoorverbinding te verzenden.

[Bekijk de zelfstudie hier.](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html?lang=nl-NL)
