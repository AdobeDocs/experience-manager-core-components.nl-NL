---
title: Webgeoptimaliseerde afbeeldingslevering
description: Leer hoe de Core Components AEM as a Cloud Service webgeoptimaliseerde functies voor het leveren van afbeeldingen kunnen gebruiken om afbeeldingen efficiënter te leveren.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: d8c8f4c3395313b21f56fd7d98175924287c367c
workflow-type: tm+mt
source-wordcount: '1023'
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

Nadat u voor het web geoptimaliseerde aflevering van afbeeldingen hebt geactiveerd, kunt u ook de configuratie van de verzender controleren om te controleren of de aanvraag voor de afbeeldingsservice niet wordt geblokkeerd. URL&#39;s van deze service hebben de volgende vorm.

```text
/adobe/dynamicmedia/deliver/dm-aid--741ed388-d5f8-4797-8095-10c896dc9f1d/skitouring.jpg?quality=80&preferwebp=true
```

Dit kan met deze regelmatige uitdrukking worden algemeen gemaakt.

```text
\/adobe\/dynamicmedia\/deliver\/([^:[]|*\/])\/([\w-])\.(gif|png|png8|jpg|pjpg|bjpg|webp|webpll|webply)(?[a-z0-9=&]*)?
```

## Weblevering controleren {#verifying}

De levering van webgeoptimaliseerde afbeeldingen is transparant voor de consument van de inhoud en heeft geen invloed op de markering. Het enige wat een eindgebruiker opmerkt, is een snellere laadtijd.

Daarom moet u de paginabron weergeven om de feitelijke gedragswijziging te kunnen observeren.

1. Bewerk in AEM een pagina die is gebaseerd op de sjabloon waarop u [geactiveerde voor het web geoptimaliseerde afbeeldingslevering](#activating) voor de component Image.
1. Selecteer in de pagina-editor de optie **Pagina-informatie** en vervolgens linksboven **Weergeven als gepubliceerd**.
1. Bekijk de bron van de pagina met de ontwikkelprogramma&#39;s van uw browsers en bekijk hoe de gerenderde markering ongewijzigd blijft, maar dat de afbeelding in de `src` kenmerkpunten naar [de URL van de nieuwe afbeeldingsservice.](#activating)

## Wanneer Web-Optimized Image Delivery niet beschikbaar is {#fallback}

Voor het web geoptimaliseerde afbeeldingslevering is alleen beschikbaar in AEM as a Cloud Service. Wanneer deze niet beschikbaar is, bijvoorbeeld wanneer AEM 6.5 op locatie of op een lokale ontwikkelingsinstantie wordt uitgevoerd, wordt de afbeelding opnieuw geleverd [de Adaptive Image Servlet.](/help/developing/adaptive-image-servlet.md)

Net zoals het inschakelen van voor het web geoptimaliseerde afbeeldingslevering geen invloed heeft op de markering, heeft het terugvallen naar de Adaptive Image Servlet ook geen invloed op de markering aangezien alleen de URL in het dialoogvenster `src` kenmerk van de `img` element is gewijzigd.

## Veelgestelde vragen {#faq}

### Waarom is er geen optie om voor het web geoptimaliseerde afbeeldingen in mijn omgeving in te schakelen? {#missing-option}

De functie is alleen beschikbaar op AEM as a Cloud Service. De afbeeldingscomponent wordt lokaal of op locatie AEM uitgevoerd [terugvallen](#fallback) op de Adaptive Image Servlet.

### Waarom werkt de service niet met de lokale SDK? {#local-sdk}

Wanneer u de AEM SDK gebruikt ingeschakeld `localhost`, is de afbeeldingsservice niet beschikbaar en wordt de afbeelding gerenderd [terugvallen](#fallback) op de Adaptive Image Servlet.

Als u de webgeoptimaliseerde service voor het leveren van afbeeldingen wilt gebruiken, implementeert u het project in een AEMaaCS-ontwikkelomgeving om te kunnen testen hoe de beeldservice zich precies gedraagt met de beeldservice.

### Waarom werkt de service niet voor bepaalde afbeeldingen op mijn pagina? {#some-images}

De afbeeldingsservice werkt alleen voor elementen onder `/content/dam` en het werkt niet voor afbeeldingen die rechtstreeks naar de pagina zijn geüpload en die zijn opgeslagen onder een `cq:Page` object. Dergelijke activa zullen nog worden geleverd met de Adaptive Image Servlet als [fallback.](#fallback)

### Waarom geeft de service een afbeelding van slechtere kwaliteit weer of beperkt deze de grootte van afbeeldingen? {#quality}

In de webgeoptimaliseerde afbeeldingsservice worden alle afbeeldingsuitvoeringen van 2048 px en kleiner beschouwd en worden de grootste uitvoeringen gebruikt als basis waarop de gewenste instellingen worden toegepast (breedte, uitsnijden, indeling, kwaliteit, enz.).

De afbeeldingsservice zal de schaal van afbeeldingen nooit verhogen. Deze vertoningen bepalen daarom de beste grootte en de kwaliteit die de beelddienst zal kunnen leveren. Zorg er daarom voor dat uw elementen allemaal de zoomuitvoering van 2048 pixels hebben en dat ze anders opnieuw worden verwerkt.

### De URL van mijn afbeeldingen eindigt nog steeds met .JPG of .PNG, niet met .WEBP, en er is geen SRCSET-kenmerk of PICTURE-element. Maakt dit echt gebruik van geoptimaliseerde webindelingen? {#content-negotiation}

Om WebP formaten te leveren, gebruikt de Web-geoptimaliseerde dienst van de beeldlevering een techniek genoemd &quot;inhoudonderhandeling&quot;. Dit bestaat uit het terugkeren van een WebP dossierformaat, zelfs wanneer het verzoeken van een JPG of PNG- dossieruitbreiding, maar slechts wanneer browser die het verzoek indient verstrekte en `image/webp` HTTP accepteert header. Browsers die deze techniek ondersteunen, kunnen deze header dan leveren en oudere browsers krijgen nog steeds de JPG- of PNG-bestandsindeling.

Het voordeel van deze techniek is dat de `img` elementen en de kenmerken ervan kunnen ongewijzigd blijven, wat zal leiden tot een optimale compatibiliteit voor bestaande sites en een zo vloeiend mogelijke overgang naar voor het web geoptimaliseerde levering van afbeeldingen garandeert.

### Kan ik voor het web geoptimaliseerde afbeeldingslevering gebruiken met mijn eigen component?

Ja, de webgeoptimaliseerde service voor het leveren van afbeeldingen kan worden gebruikt door aangepaste componenten. Adobe beveelt aan [de component Image uitbreiden](/help/developing/customizing.md) in dit geval.

Hieronder volgt een serviceinterface die kan worden gebruikt om de element-URL te genereren.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

**Houd er rekening mee dat directe URL-insluitingen in een ervaring die niet is gemaakt via Core Components die op AEM Sites CS wordt uitgevoerd, in strijd zijn met de Media Library-licentievoorwaarden.**

### Wat is de URL van een afbeelding die door de nieuwe beeldservice wordt geleverd? {#url}

Zie de vorige sectie [Webgeoptimaliseerde afbeeldingslevering activeren voor kerncomponenten](#activating) voor een voorbeeld-URL en een reguliere expressie.

### Kunnen afbeeldingen niet worden weergegeven nadat geoptimaliseerde webafbeeldingen zijn ingeschakeld?

Nee, dat mag nooit gebeuren.

* In de HTML verandert de markering niet wanneer u voor het web geoptimaliseerde afbeeldingen inschakelt, verandert alleen de waarde van het kenmerk SRC in het afbeeldingselement.
* Wanneer de nieuwe beeldservice niet beschikbaar is of de gewenste afbeelding niet kan verwerken, wordt de gegenereerde URL [fallback naar de Adaptive Image Servlet.](#fallback)
* De verzendingsregels kunnen de webgeoptimaliseerde afbeeldingsservice blokkeren en [moet worden gecontroleerd tijdens het activeren van de functie.](#activating)
