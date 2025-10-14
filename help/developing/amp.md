---
title: AMP-ondersteuning voor de kerncomponenten
description: De kerncomponenten ondersteunen AMP - Versnelde mobiele pagina's
role: Architect, Developer, Admin
exl-id: 1fd9b6b5-0e4d-48c7-8faa-42e0d4a6bbd0
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---

# AMP-ondersteuning voor de kerncomponenten {#amp-support}

Vanaf [&#x200B; versie 2.11.0 &#x200B;](/help/versions.md) van de Componenten van de Kern, [&#x200B; AMP - Versnelde Mobiele Pagina&#39;s &#x200B;](https://developers.google.com/amp) - volledig gesteund.

In dit document wordt een overzicht gegeven van de manier waarop AMP wordt ondersteund en van de manier waarop u dit voor uw sites kunt inschakelen. Nochtans voor volledige technische details, gelieve te zien de [&#x200B; documentatie van de ontwikkelaar GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## Wat is AMP? {#what-is-amp}

Accelerated Mobile Pages of AMP is een opensource-framework dat oorspronkelijk door Google is ontworpen om pagina&#39;s te optimaliseren voor mobiel surfen. AMP-pagina&#39;s worden doorgaans veel sneller geladen dan standaardwebpagina&#39;s en bieden betere mobiele ervaringen.

## AMP in de kerncomponenten {#amp-in-core-components}

De steun voor AMP in de Componenten van de Kern is [&#x200B; volledig configureerbaar.](#enabling-amp) AMP-versies van pagina&#39;s kunnen alleen worden weergegeven, naast de standaard HTML-versies, of helemaal niet.

De kerncomponenten gebruiken `amp` als een verkiesbare kiezer om een AMP-pagina te renderen. `example.html` geeft bijvoorbeeld de normale pagina weer en `example.amp.html` zou de AMP-versie zijn.

Individuele projecten kunnen beslissen of zij AMP al dan niet zullen benutten. Omdat AMP- en standaard HTML-pagina&#39;s parallel kunnen worden geleverd, kan een project ervoor kiezen om AMP alleen op bepaalde pagina&#39;s van het project te gebruiken.

## Aan de slag met AMP-ondersteuning in uw project {#getting-started}

Hoewel AMP-ondersteuning veel flexibiliteit biedt, zijn er slechts enkele eenvoudige stappen nodig om snel aan de slag te gaan:

1. Installeer indien nodig de extensie voor AMP-ondersteuning.
   * Voor AEM as a Cloud Service-projecten is de extensie automatisch beschikbaar met de Core Components (Basiscomponenten) en hoeft u de extensie niet te installeren.
   * Voor on-premise en projecten van AMS, moet de uitbreiding uitdrukkelijk worden geïnstalleerd wanneer het installeren van de Componenten van de Kern.
1. Zodra de uitbreiding AMP wordt geïnstalleerd, moet de componentenauteur de componentensupertypes aan die in de uitbreiding eenvoudig richten.
1. [&#x200B; laat de steun van AMP &#x200B;](#enabling-amp) op het malplaatjeniveau of op uw individuele pagina&#39;s toe.
1. [&#x200B; stelt gealigneerde CSS &#x200B;](#css-requirements) zoals vereist op.

### AMP inschakelen voor pagina&#39;s {#enabling-amp}

Om AMP voor een pagina toe te laten, moet de **Wijze van AMP** in het [&#x200B; Beleid van de Pagina worden geselecteerd.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=nl-NL#editing-a-template-page-policy-template-author-developer)

![&#x200B; de opties van het Beleid van het Beleid van de Pagina van AMP &#x200B;](/help/assets/amp-policy.png)

* **Geen AMP** - de pagina wordt geleverd als standaard slechts HTML.
* **Gepaste AMP** - de pagina wordt geleverd als AMP evenals HTML.
* **slechts AMP** - de pagina wordt geleverd als slechts AMP.

De montages van AMP voor een pagina kunnen ook in de [&#x200B; Eigenschappen van de Pagina &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html?lang=nl-NL) voor een individuele pagina worden met voeten getreden.

![&#x200B; de Eigenschappen van de Pagina van AMP &#x200B;](/help/assets/amp-page-properties.png)

* **erven van het Malplaatje van de Pagina** - dit is de standaardwaarde, die het plaatsen om van het beleid van het paginamalplaatje toestaat worden genomen.
* **Geen AMP** - de pagina wordt geleverd als standaard slechts HTML.
* **Gepaste AMP** - de pagina wordt geleverd als AMP evenals HTML.
* **slechts AMP** - de pagina wordt geleverd als slechts AMP.

### CSS-vereisten {#css-requirements}

Wanneer het gebruiken van AMP met de Componenten van de Kern, is het belangrijkste verschil dat AMP alle [&#x200B; CSS vereist om worden gealigneerd &#x200B;](including-clientlibs.md#inlining) in het `<head>` element evenals wordt geoptimaliseerd.

Hiervoor wordt een aangepaste pagina-component gebruikt, die alleen de AMP-specifieke CSS laadt voor componenten die op de pagina aanwezig zijn.

>[!NOTE]
>
>Vanwege ontwerpbeperkingen van AMP biedt Adobe geen ondersteuning voor het gebruik van het responsieve raster met de AMP-versie van uw pagina.

Voor verdere vereisten en technische details, gelieve te zien de [&#x200B; documentatie van de ontwikkelaar GitHub.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
