---
title: Adaptieve afbeeldingsserver
description: Leer hoe de Core Components de Adaptive Image Servlet voor beeldlevering gebruikt en hoe u het gebruik ervan kunt optimaliseren.
role: Architect, Developer, Admin, User
exl-id: d9199d51-6f09-4000-9525-afc30474437e
source-git-commit: 785aa82930e3bcf6ef16d7a1cdc614d230e8daa8
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# Adaptieve afbeeldingsserver {#adaptive-image-servlet}

Leer hoe de Core Components de Adaptive Image Servlet voor beeldlevering gebruikt en hoe u het gebruik ervan kunt optimaliseren.

## Adaptive Image Servlet of Web-Optimized Image Delivery? {#options}

De component Image Core kan twee methoden gebruiken om afbeeldingen te leveren.

* Standaard is dit de Adaptive Image Servlet.
* [ Web-geoptimaliseerde beeldlevering ](/help/developing/web-optimized-image-delivery.md) is beschikbaar aan AEMaaCS en vermindert downloadgrootte door gemiddeld 25%.

In dit document wordt de standaard adaptieve afbeeldingsserver beschreven.

## Overzicht {#overview}

Standaard gebruikt de component Image de Adaptive Image Servlet van de Core-component om afbeeldingen te leveren. [ de Adaptieve Servlet van het Beeld ](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) is verantwoordelijk voor beeldverwerking en het stromen en kan door ontwikkelaars in hun [ aanpassingen van de Componenten van de Kern ](/help/developing/customizing.md) worden leveraged.

## Selectie van vertoning {#rendition-selection}

De Adaptive Image Server selecteert automatisch de meest geschikte vertoning op basis van de grootte van de container waarin deze wordt weergegeven. Het selectieproces van de vertoning ziet er als volgt uit.

1. De Adaptive Image Server controleert bij alle beschikbare uitvoeringen van het afbeeldingselement.
1. Alleen elementen met dezelfde mime/hetzelfde type als het oorspronkelijke element waarnaar wordt verwezen, worden geselecteerd.
   * Als het oorspronkelijke element bijvoorbeeld een PNG-bestand was, wordt alleen rekening gehouden met PNG-uitvoeringen.
1. Van deze uitvoeringen worden de afmetingen in overweging genomen en worden deze vergeleken met de grootte van de container waarin de afbeelding moet worden weergegeven.
   1. Als de vertoning >= de containergrootte is, wordt het toegevoegd aan een lijst van kandidaatvertoningen.
   1. Als de vertoning kleiner is dan de containergrootte, wordt deze genegeerd.
   1. Deze criteria zorgen ervoor dat de vertoning niet wordt vergroot, wat van invloed is op de beeldkwaliteit.
1. De adaptieve server van het Beeld selecteert dan de vertoning met de kleinste dossiergrootte van de kandidaatlijst.

## Renderingsselectie optimaliseren {#optimizing-rendition-selection}

De Adaptive Image Server probeert de beste uitvoering te kiezen voor de gewenste afbeeldingsgrootte en het gewenste type. Het wordt aanbevolen dat DAM-uitvoeringen en toegestane breedten van afbeeldingscomponenten synchroon worden gedefinieerd, zodat de Adaptive Image Servlet zo weinig mogelijk verwerkt.

Dit verbetert de prestaties en voorkomt dat sommige afbeeldingen niet correct worden verwerkt door de onderliggende afbeeldingsverwerkingsbibliotheek.

## Laatst gewijzigde koppen gebruiken {#last-modified}

Voorwaardelijke verzoeken via de `Last-Modified` kopbal worden gesteund door de Adaptieve Servlet van het Beeld, maar het in het voorgeheugen onderbrengen van de `Last-Modified` kopbal [ moet in Dispatcher ](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=en#caching-http-response-headers) worden toegelaten.

[ het AEM Archetype van het Project ](/help/developing/archetype/overview.md) de configuratie van steekproefDispatcher bevat reeds deze configuratie.
