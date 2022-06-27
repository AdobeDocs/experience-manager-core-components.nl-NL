---
title: Adaptieve afbeeldingsserver
description: Leer hoe de Core Components de Adaptive Image Servlet voor beeldlevering gebruikt en hoe u het gebruik ervan kunt optimaliseren.
role: Architect, Developer, Admin, User
source-git-commit: 3ff1343ab4ef7a52f910984a0bcd8fc4201441bf
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---


# Adaptieve afbeeldingsserver {#adaptive-image-servlet}

Leer hoe de Core Components de Adaptive Image Servlet voor beeldlevering gebruikt en hoe u het gebruik ervan kunt optimaliseren.

## Aangepaste levering van imageserver of webgeoptimaliseerde levering van afbeeldingen? {#options}

De component Image Core kan twee methoden gebruiken om afbeeldingen te leveren.

* Standaard is dit de Adaptive Image Servlet.
* [Voor het web geoptimaliseerde afbeeldingslevering](/help/developing/web-optimized-image-delivery.md) is beschikbaar voor AEMaaCS en verkleint de downloadgrootte met gemiddeld 25%.

In dit document wordt de standaard adaptieve afbeeldingsserver beschreven.

## Overzicht {#overview}

Standaard gebruikt de component Image de Adaptive Image Servlet van de Core-component om afbeeldingen te leveren. [De Adaptive Image Servlet](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) is verantwoordelijk voor beeldverwerking en streaming en kan door ontwikkelaars in hun [aanpassingen van de kerncomponenten](/help/developing/customizing.md).

## Renderingsselectie optimaliseren {#optimizing-rendition-selection}

De Adaptive Image Server probeert de beste uitvoering te kiezen voor de gewenste afbeeldingsgrootte en het gewenste type. Het wordt aanbevolen dat DAM-uitvoeringen en toegestane breedten van afbeeldingscomponenten synchroon worden gedefinieerd, zodat de Adaptive Image Servlet zo weinig mogelijk verwerkt.

Hierdoor worden de prestaties verbeterd en worden sommige afbeeldingen niet correct verwerkt door de onderliggende afbeeldingsverwerkingsbibliotheek.

## Laatst gewijzigde koppen gebruiken {#last-modified}

Voorwaardelijke verzoeken via de `Last-Modified` de header wordt ondersteund door de Adaptive Image Servlet, maar het in cache plaatsen van de `Last-Modified` header [moet worden ingeschakeld in de Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=en#caching-http-response-headers).

[Het AEM Project Archetype](/help/developing/archetype/overview.md)De voorbeeldconfiguratie van Dispatcher bevat al deze configuratie.
