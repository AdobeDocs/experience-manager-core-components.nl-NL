---
title: Webgeoptimaliseerde afbeeldingslevering
description: Leer hoe de Core Components de voor het web geoptimaliseerde functies voor het leveren van afbeeldingen voor AEM as a Cloud Service kunnen gebruiken om afbeeldingen efficiënter te leveren.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: eb1822cb41a849695afb5125745ed5f78e3e70a4
workflow-type: tm+mt
source-wordcount: '1061'
ht-degree: 0%

---

# Webgeoptimaliseerde afbeeldingslevering {#web-optimized-image-delivery}

Leer hoe de Core Components de voor het web geoptimaliseerde functies voor het leveren van afbeeldingen voor AEM as a Cloud Service kunnen gebruiken om afbeeldingen efficiënter te leveren.

## Overzicht {#overview}

De Web-geoptimaliseerde eigenschap van de beeldlevering van AEM als dienst van de Wolk levert beeldactiva van DAM in [&#x200B; formaat WebP.](https://developers.google.com/speed/webp) WebP kan de downloadgrootte van een afbeelding met gemiddeld ongeveer 25% verkleinen, wat leidt tot een sneller laden van pagina&#39;s.

Het activeren van voor het web geoptimaliseerde afbeeldingslevering in Core Components is eenvoudig en omdat alle algemene browsers WebP ondersteunen, is de ervaring voor de eindgebruiker transparant. Het enige verschil dat ze zullen merken, is dat inhoud sneller wordt geladen.

## Webgeoptimaliseerde afbeeldingslevering activeren voor kerncomponenten {#activating}

Om Web-geoptimaliseerde beeldlevering toe te laten, geef een paginamalplaatje uit en activeer eenvoudig de optie **laat Web Geoptimaliseerde Beelden** binnen de ontwerpdialoog van de [&#x200B; Component van het Beeld toe.](/help/components/image.md#design-dialog) Deze optie is beschikbaar voor v1, v2 en v3 van de Afbeeldingscomponent.

Als u niet vertrouwd met ontwerpdialogen en AEM paginasjablonen bent, [&#x200B; gelieve dit document te herzien.](/help/get-started/authoring.md#pre-configuring-core-components)

![&#x200B; toelatend web-geoptimaliseerde beeldlevering in de ontwerpdialoog &#x200B;](/help/assets/web-optimized-image-delivery.png)

Dat is het! Afbeeldingen worden nu door de Afbeeldingscomponent in WebP-indeling geleverd.

Nadat u voor het web geoptimaliseerde aflevering van afbeeldingen hebt geactiveerd, kunt u beter de configuratie van de verzender controleren om te controleren of de aanvraag van de service voor het leveren van de afbeelding niet wordt geblokkeerd. Gelieve te zien [&#x200B; deze ingang van FAQ &#x200B;](#failure-to-deliver) voor meer informatie.

## Weblevering controleren {#verifying}

De levering van webgeoptimaliseerde afbeeldingen is transparant voor de consument van de inhoud. Het enige wat een eindgebruiker opmerkt, is een snellere laadtijd. Als u een feitelijke gedragswijziging wilt observeren, moet u daarom het inhoudstype van de gerenderde afbeeldingen in de browser controleren. Alle moderne browsers ondersteunen WebP. U kunt naar [&#x200B; verwijzen deze plaats &#x200B;](https://caniuse.com/webp) voor details op browser steun.

1. In AEM, geef een pagina uit die van het malplaatje waar u [&#x200B; Web-geoptimaliseerde beeldlevering &#x200B;](#activating) voor de Component van het Beeld wordt gebaseerd.
1. Binnen de paginaredacteur, selecteer de **knoop van de Informatie van de Pagina** bij top-left en toen **Mening zoals Gepubliceerd**.
1. Open de ontwikkelaarsgereedschappen van uw browser en selecteer het tabblad Netwerk.
1. Laad de pagina opnieuw en zoek naar HTTP-aanvragen om de afbeeldingen te laden en controleer het inhoudstype van de afbeelding die de browser heeft ontvangen.

## Wanneer Web-Optimized Image Delivery niet beschikbaar is {#fallback}

Voor het web geoptimaliseerde afbeeldingslevering is alleen beschikbaar in AEM as a Cloud Service. In gevallen waar het niet beschikbaar zoals het runnen van AEM 6.5 op gebouw of op een lokale ontwikkelingsinstantie is, zal de beeldlevering terug naar het gebruiken van [&#x200B; de Aangepaste Servlet van het Beeld vallen.](/help/developing/adaptive-image-servlet.md)

Als u terugvalt op de Adaptive Image Server, wijzigt u het kenmerk `src` van de `img` -elementen in de paginabron.

## Veelgestelde vragen {#faq}

### Waarom is er geen optie om voor het web geoptimaliseerde afbeeldingen in mijn omgeving in te schakelen? {#missing-option}

Deze functie is alleen beschikbaar op AEM as a Cloud Service. Lopen AEM plaatselijk of op gebouw, valt de Component van het Beeld [&#x200B; terug &#x200B;](#fallback) aan het gebruiken van de Aangepaste Servlet van het Beeld.

### Waarom werkt de service niet met de lokale SDK? {#local-sdk}

Wanneer het gebruiken van AEM SDK op `localhost`, is de beelddienst niet beschikbaar, en het beeld dat [&#x200B; teruggeeft valt terug &#x200B;](#fallback) aan het gebruiken van de AanpassingsServlet van het Beeld.

Als u de webgeoptimaliseerde service voor het leveren van afbeeldingen wilt gebruiken, implementeert u het project in een AEMaaCS-ontwikkelomgeving om te kunnen testen hoe de beeldservice zich precies gedraagt met de beeldservice.

### Waarom werkt de service niet voor bepaalde afbeeldingen op mijn pagina? {#some-images}

De afbeeldingsservice werkt alleen voor elementen onder `/content/dam` en werkt niet voor afbeeldingen die rechtstreeks naar de pagina zijn geüpload en die onder een `cq:Page` -object zijn opgeslagen. Dergelijke activa zullen nog met de Adaptieve Servlet van het Beeld als a [&#x200B; reserve worden geleverd.](#fallback)

### Waarom geeft de service een afbeelding van slechtere kwaliteit weer of beperkt deze de grootte van afbeeldingen? {#quality}

Wanneer afbeeldingselementen onder `/content/dam` worden verwerkt, genereren AEM as a Cloud Service-omgevingen geoptimaliseerde uitvoeringen van verschillende afmetingen. De web-geoptimaliseerde beelddienst analyseert de breedte die door de Component van de Kern van het Beeld wordt gevraagd, beschouwt het originele beeld en alle vertoningen die 2048px en kleiner zijn, en plukt het grootste van die (binnen de grootte en de afmetingsgrenzen beelddienst kan behandelen, momenteel 50 MB en `12k` x `12k`) als basis waarop het de gevraagde montages (breedte, uitsnijding, formaat, kwaliteit, enz.) zal toepassen.

De afbeeldingsservice vergroot de schaal van afbeeldingen niet om de kwaliteit van de uitvoer te behouden. De bovenstaande uitvoeringen bepalen de beste kwaliteit die de afbeeldingsservice kan leveren. Omdat u vaak niet in staat bent de grootte en/of afmetingen van het oorspronkelijke afbeeldingselement te beïnvloeden, dient u ervoor te zorgen dat alle afbeeldingselementen een zoomuitvoering van 2048 px hebben en deze anders opnieuw te verwerken.

### De URL van mijn afbeeldingen eindigt nog steeds met .JPG of .PNG, niet met .WEBP, en er is geen SRCSET-kenmerk of PICTURE-element. Maakt dit echt gebruik van geoptimaliseerde webindelingen? {#content-negotiation}

Om formaten WebP te leveren, voert de Web-geoptimaliseerde dienst van de beeldlevering [&#x200B; server-gedreven inhoudonderhandeling uit.](https://developer.mozilla.org/en-US/docs/Web/HTTP/Content_negotiation#server-driven_content_negotiation) Hiermee kunt u de optimale uitvoerindeling voor de afbeelding selecteren op basis van de mogelijkheden die door de client worden geadverteerd, zodat de service voor het leveren van de afbeelding de bestandsextensie kan negeren.

Het voordeel van het leveraging van inhoud-onderhandeling is dat browsers die geen steun voor WebP adverteren nog het JPG van de of van PNG- dossierformaat zonder enige verandering nodig in de prijsverhoging van de pagina zullen krijgen. Dit biedt optimale compatibiliteit voor bestaande sites en garandeert een zo vloeiend mogelijk pad naar de overgang naar voor het web geoptimaliseerde levering van afbeeldingen.

### Kan ik voor het web geoptimaliseerde afbeeldingslevering gebruiken met mijn eigen component?

Ja, de web-geoptimaliseerde dienst van de beeldlevering kan door douanecomponenten worden gebruikt, die door [&#x200B; worden gebouwd uitbreidend de Component van het Beeld, &#x200B;](/help/developing/customizing.md)

Hieronder volgt een serviceinterface die kan worden gebruikt om de element-URL te genereren.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

>[!WARNING]
>
>Directe URL bedt in een ervaring in die niet door bovengenoemde SPI (beschikbaar op de Plaatsen van AEM as a Cloud Service) wordt gebouwd is in schending van de [&#x200B; termijnen van Media Library van gebruik &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/admin/medialibrary.html?lang=nl-NL#use-media-library).

### Kunnen afbeeldingen niet worden weergegeven nadat geoptimaliseerde webafbeeldingen zijn ingeschakeld? {#failure-to-deliver}

Nee, dat mag nooit gebeuren om de volgende redenen.

* In de HTML verandert de markering niet wanneer u voor het web geoptimaliseerde afbeeldingen inschakelt, verandert alleen de waarde van het kenmerk `src` in het afbeeldingselement.
* Wanneer de nieuwe beelddienst niet beschikbaar is of niet het gewenste beeld kan verwerken, zal URL geproduceerd [&#x200B; reserve aan de Adaptieve Servlet van het Beeld.](#fallback)

De verzendingsregels kunnen echter de voor het web geoptimaliseerde service voor het leveren van afbeeldingen blokkeren. URLs van de dienst van de beeldlevering begint met `/adobe`, en het onderzoeken van de verzender registreert voor verworpen verzoeken zoals [&#x200B; hier wordt beschreven &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/ams/dispatcher/common-logs.html?lang=nl-NL#filter-rejects) zou helpen om het even welke mislukkingen problemen oplossen die in het leveren van de beelden aan browser worden ontmoet.
