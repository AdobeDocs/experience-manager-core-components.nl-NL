---
title: Webgeoptimaliseerde afbeeldingslevering
description: Leer hoe de Core Components AEM as a Cloud Service webgeoptimaliseerde functies voor het leveren van afbeeldingen kunnen gebruiken om afbeeldingen efficiënter te leveren.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: eb1822cb41a849695afb5125745ed5f78e3e70a4
workflow-type: tm+mt
source-wordcount: '1061'
ht-degree: 0%

---

# Webgeoptimaliseerde afbeeldingslevering {#web-optimized-image-delivery}

Leer hoe de Core Components AEM as a Cloud Service webgeoptimaliseerde functies voor het leveren van afbeeldingen kunnen gebruiken om afbeeldingen efficiënter te leveren.

## Overzicht {#overview}

De webgeoptimaliseerde functie voor het leveren van afbeeldingen van AEM als Cloud-service levert afbeeldingselementen van de DAM in [WebP-indeling](https://developers.google.com/speed/webp) WebP kan de downloadgrootte van een beeld met ongeveer 25% gemiddeld verminderen, die in snellere paginading resulteert.

Het activeren van voor het web geoptimaliseerde afbeeldingslevering in Core Components is eenvoudig en omdat alle algemene browsers WebP ondersteunen, is de ervaring voor de eindgebruiker transparant. Het enige verschil dat ze zullen merken, is dat inhoud sneller wordt geladen.

## Webgeoptimaliseerde afbeeldingslevering activeren voor kerncomponenten {#activating}

Als u voor het web geoptimaliseerde afbeeldingslevering wilt inschakelen, bewerkt u een paginasjabloon en activeert u gewoon de optie **Geoptimaliseerde webafbeeldingen inschakelen** in de ontwerpdialoog [Afbeeldingscomponent.](/help/components/image.md#design-dialog) Deze optie is beschikbaar voor v1, v2 en v3 van de Afbeeldingscomponent.

Als u niet bekend bent met ontwerpdialoogvensters en AEM paginasjablonen, [Controleer dit document.](/help/get-started/authoring.md#pre-configuring-core-components)

![Voor het web geoptimaliseerde afbeeldingslevering inschakelen in het dialoogvenster Ontwerpen](/help/assets/web-optimized-image-delivery.png)

Dat is het! Afbeeldingen worden nu door de Afbeeldingscomponent in WebP-indeling geleverd.

Nadat u voor het web geoptimaliseerde aflevering van afbeeldingen hebt geactiveerd, kunt u beter de configuratie van de verzender controleren om te controleren of de aanvraag van de service voor het leveren van de afbeelding niet wordt geblokkeerd. Zie [dit item voor veelgestelde vragen](#failure-to-deliver) voor meer informatie .

## Weblevering controleren {#verifying}

De levering van webgeoptimaliseerde afbeeldingen is transparant voor de consument van de inhoud. Het enige wat een eindgebruiker opmerkt, is een snellere laadtijd. Als u een feitelijke gedragswijziging wilt observeren, moet u daarom het inhoudstype van de gerenderde afbeeldingen in de browser controleren. Alle moderne browsers ondersteunen WebP. U kunt verwijzen naar [deze site](https://caniuse.com/webp) voor meer informatie over browserondersteuning.

1. Bewerk in AEM een pagina die is gebaseerd op de sjabloon waarop u [geactiveerde voor het web geoptimaliseerde afbeeldingslevering](#activating) voor de component Image.
1. Selecteer in de pagina-editor de optie **Pagina-informatie** en vervolgens linksboven **Weergeven als gepubliceerd**.
1. Open de ontwikkelaarsgereedschappen van uw browser en selecteer het tabblad Netwerk.
1. Laad de pagina opnieuw en zoek naar HTTP-aanvragen om de afbeeldingen te laden en controleer het inhoudstype van de afbeelding die de browser heeft ontvangen.

## Wanneer Web-Optimized Image Delivery niet beschikbaar is {#fallback}

Voor het web geoptimaliseerde afbeeldingslevering is alleen beschikbaar in AEM as a Cloud Service. Wanneer deze niet beschikbaar is, bijvoorbeeld wanneer AEM 6.5 op locatie of op een lokale ontwikkelingsinstantie wordt uitgevoerd, wordt de afbeelding opnieuw geleverd [de Adaptive Image Servlet.](/help/developing/adaptive-image-servlet.md)

Als u terugvalt op de Adaptive Image Servlet, verandert de optie `src` kenmerk van de `img` elementen in de paginabron.

## Veelgestelde vragen {#faq}

### Waarom is er geen optie om voor het web geoptimaliseerde afbeeldingen in mijn omgeving in te schakelen? {#missing-option}

De functie is alleen beschikbaar op AEM as a Cloud Service. De afbeeldingscomponent wordt lokaal of op locatie AEM uitgevoerd [terugvallen](#fallback) op de Adaptive Image Servlet.

### Waarom werkt de service niet met de lokale SDK? {#local-sdk}

Wanneer u de AEM SDK gebruikt ingeschakeld `localhost`, is de afbeeldingsservice niet beschikbaar en wordt de afbeelding gerenderd [terugvallen](#fallback) op de Adaptive Image Servlet.

Als u de webgeoptimaliseerde service voor het leveren van afbeeldingen wilt gebruiken, implementeert u het project in een AEMaaCS-ontwikkelomgeving om te kunnen testen hoe de beeldservice zich precies gedraagt met de beeldservice.

### Waarom werkt de service niet voor bepaalde afbeeldingen op mijn pagina? {#some-images}

De afbeeldingsservice werkt alleen voor elementen onder `/content/dam` en het werkt niet voor afbeeldingen die rechtstreeks naar de pagina zijn geüpload en die zijn opgeslagen onder een `cq:Page` object. Dergelijke activa zullen nog worden geleverd met de Adaptive Image Servlet als [fallback.](#fallback)

### Waarom geeft de service een afbeelding van slechtere kwaliteit weer of beperkt deze de grootte van afbeeldingen? {#quality}

Wanneer afbeeldingselementen onder `/content/dam` worden verwerkt, AEM as a Cloud Service omgevingen geoptimaliseerde uitvoeringen van verschillende afmetingen genereren. De webgeoptimaliseerde afbeeldingsservice analyseert de breedte die wordt gevraagd door de Image Core-component, bekijkt de oorspronkelijke afbeelding en alle uitvoeringen die 2048 px en kleiner zijn en neemt de grootste van deze vertoningen op (binnen de limiet van grootte en afmetingen die door de afbeeldingsservice kan worden verwerkt, momenteel 50 MB en `12k`x`12k`) als basis waarop de gewenste instellingen worden toegepast (breedte, uitsnijden, indeling, kwaliteit, enz.).

De afbeeldingsservice vergroot de schaal van afbeeldingen niet om de kwaliteit van de uitvoer te behouden. De bovenstaande uitvoeringen bepalen de beste kwaliteit die de afbeeldingsservice kan leveren. Omdat u vaak niet in staat bent de grootte en/of afmetingen van het oorspronkelijke afbeeldingselement te beïnvloeden, dient u ervoor te zorgen dat alle afbeeldingselementen een zoomuitvoering van 2048 px hebben en deze anders opnieuw te verwerken.

### De URL van mijn afbeeldingen eindigt nog steeds met .JPG of .PNG, niet met .WEBP, en er is geen SRCSET-kenmerk of PICTURE-element. Maakt dit echt gebruik van geoptimaliseerde webindelingen? {#content-negotiation}

Om WebP formaten te leveren, presteert de Web-geoptimaliseerde dienst van de beeldlevering [onderhandeling over servergestuurde inhoud.](https://developer.mozilla.org/en-US/docs/Web/HTTP/Content_negotiation#server-driven_content_negotiation) Hierdoor kunt u de optimale uitvoerindeling voor de afbeelding selecteren op basis van door de client geadverteerde mogelijkheden, zodat de service voor het leveren van de afbeelding de bestandsextensie kan negeren.

Het voordeel van het leveraging van inhoud-onderhandeling is dat browsers die geen steun voor WebP adverteren nog het JPG of PNG- dossierformaat zonder enige verandering nodig in de prijsverhoging van de pagina zullen krijgen. Dit biedt optimale compatibiliteit voor bestaande sites en garandeert een zo vloeiend mogelijk pad naar de overgang naar voor het web geoptimaliseerde levering van afbeeldingen.

### Kan ik voor het web geoptimaliseerde afbeeldingslevering gebruiken met mijn eigen component?

Ja, de webgeoptimaliseerde service voor het leveren van afbeeldingen kan worden gebruikt door aangepaste componenten, die zijn samengesteld door [de component Image uitbreiden,](/help/developing/customizing.md)

Hieronder volgt een serviceinterface die kan worden gebruikt om de element-URL te genereren.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

>[!WARNING]
>
>Directe URL sluit in een ervaring in die niet door bovengenoemde SPI (beschikbaar op AEM as a Cloud Service Plaatsen) wordt gebouwd in schending van [Media Library gebruiksvoorwaarden](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/admin/medialibrary.html?lang=en#use-media-library).

### Kunnen afbeeldingen niet worden weergegeven nadat geoptimaliseerde webafbeeldingen zijn ingeschakeld? {#failure-to-deliver}

Nee, dat mag nooit gebeuren om de volgende redenen.

* In de HTML verandert de markering niet wanneer u voor het web geoptimaliseerde afbeeldingen inschakelt, alleen de waarde van de `src` wijzigt het kenmerk van het afbeeldingselement.
* Wanneer de nieuwe beeldservice niet beschikbaar is of de gewenste afbeelding niet kan verwerken, wordt de gegenereerde URL [fallback naar de Adaptive Image Servlet.](#fallback)

De verzendingsregels kunnen echter de voor het web geoptimaliseerde service voor het leveren van afbeeldingen blokkeren. URL&#39;s van de service voor het leveren van afbeeldingen beginnen met `/adobe`, en het onderzoek van de verzenderslogboeken voor afgewezen aanvragen als [hier beschreven](https://experienceleague.adobe.com/docs/experience-manager-learn/ams/dispatcher/common-logs.html#filter-rejects) moet u helpen problemen op te lossen die zijn opgetreden bij het leveren van de afbeeldingen aan de browser.
