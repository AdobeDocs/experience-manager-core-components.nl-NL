---
title: AMP-ondersteuning voor de kerncomponenten
description: De kerncomponenten ondersteunen AMP - Versnelde mobiele pagina's
translation-type: tm+mt
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---


# AMP-ondersteuning voor de kerncomponenten {#amp-support}

Vanaf [release 2.11.0](/help/versions.md) van de Core Components wordt [AMP - Versnelde mobiele pagina](https://developers.google.com/amp) - volledig ondersteund.

In dit document wordt een overzicht gegeven van de manier waarop AMP wordt ondersteund en van de manier waarop u dit voor uw sites kunt inschakelen. Nochtans voor volledige technische details, gelieve te zien de [GitHub ontwikkelaarsdocumentatie.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## Wat is AMP? {#what-is-amp}

Accelerated Mobile Pages of AMP is een opensource-framework dat oorspronkelijk door Google is ontworpen om pagina&#39;s te optimaliseren voor mobiel surfen. AMP-pagina&#39;s worden doorgaans veel sneller geladen dan standaardwebpagina&#39;s en bieden betere mobiele ervaringen.

## AMP in de kerncomponenten {#amp-in-core-components}

Ondersteuning voor AMP in de Core Components is [volledig configureerbaar.](#enabling-amp) AMP-versies van pagina&#39;s kunnen alleen worden aangeboden, naast de standaard HTML-versies, of helemaal niet.

De kerncomponenten worden gebruikt `amp` als een verkiesbare kiezer om een AMP-pagina te renderen. Zo `example.html` zou de normale pagina worden weergegeven en `example.amp.html` zou dit de AMP-versie zijn.

Individuele projecten kunnen beslissen of zij AMP al dan niet zullen benutten. Omdat AMP- en standaard HTML-pagina&#39;s parallel kunnen worden geleverd, kan een project ervoor kiezen om AMP alleen op bepaalde pagina&#39;s van het project te gebruiken.

## Aan de slag met AMP-ondersteuning in uw project {#getting-started}

Hoewel AMP-ondersteuning veel flexibiliteit biedt, zijn er slechts enkele eenvoudige stappen nodig om snel aan de slag te gaan:

1. Installeer indien nodig de extensie voor AMP-ondersteuning.
   * Voor AEM als projecten van de Cloud Service, is de uitbreiding automatisch beschikbaar met de Componenten van de Kern en geen installatie is noodzakelijk.
   * Voor on-premise en projecten van AMS, moet de uitbreiding uitdrukkelijk worden geïnstalleerd wanneer het installeren van de Componenten van de Kern.
1. Zodra de uitbreiding AMP wordt geïnstalleerd, moet de componentenauteur de componentensupertypes aan die in de uitbreiding eenvoudig richten.
1. [Schakel AMP-ondersteuning](#enabling-amp) in op sjabloonniveau of op afzonderlijke pagina&#39;s.
1. [Gebruik indien nodig inline CSS](#css-requirements) .

### AMP inschakelen voor pagina&#39;s {#enabling-amp}

Als u AMP voor een pagina wilt inschakelen, moet de **AMP-modus** zijn geselecteerd in het [paginabeleid.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-page-policy-template-author-developer)

![Opties voor AMP-paginabeleid](/help/assets/amp-policy.png)

* **Geen AMP** - De pagina wordt alleen als standaard-HTML geleverd.
* **AMP** met paden - De pagina wordt als AMP en HTML geleverd.
* **Alleen** AMP - De pagina wordt alleen als AMP geleverd.

De AMP-instellingen voor een pagina kunnen ook worden overschreven in de [Pagina-eigenschappen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) voor een afzonderlijke pagina.

![Eigenschappen van AMP-pagina](/help/assets/amp-page-properties.png)

* **Overnemen van paginasjabloon** - Dit is de standaardwaarde, waarmee de instelling kan worden overgenomen uit het beleid van de paginasjabloon.
* **Geen AMP** - De pagina wordt alleen als standaard-HTML geleverd.
* **AMP** met paden - De pagina wordt als AMP en HTML geleverd.
* **Alleen** AMP - De pagina wordt alleen als AMP geleverd.

### CSS-vereisten {#css-requirements}

Bij gebruik van AMP met de Core Components, is het belangrijkste verschil dat AMP vereist dat alle [CSS zowel in het](including-clientlibs.md#inlining) element als geoptimaliseerd worden weergegeven `<head>` .

Hiertoe wordt een aangepaste pagina-component gebruikt, die alleen de AMP-specifieke CSS laadt voor componenten die op de pagina aanwezig zijn.

Voor verdere vereisten en technische details, gelieve te zien de [GitHub ontwikkelaarsdocumentatie.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
