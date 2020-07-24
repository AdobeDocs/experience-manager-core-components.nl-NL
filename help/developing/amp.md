---
title: AMP-ondersteuning voor de kerncomponenten
description: De kerncomponenten ondersteunen AMP - Versnelde mobiele pagina's
translation-type: tm+mt
source-git-commit: 905096d909d4fbf624152ba3b5cbc1d80637245f
workflow-type: tm+mt
source-wordcount: '493'
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

### Vereisten {#requirements}

Wanneer u AMP gebruikt met de Core Components, is het belangrijkste verschil dat AMP vereist dat alle CSS in het `<head>` element worden gealigneerd en geoptimaliseerd.

Hiertoe wordt een aangepaste pagina-component gebruikt, die alleen de AMP-specifieke CSS laadt voor componenten die op de pagina aanwezig zijn.

Voor verdere vereisten en technische details, gelieve te zien de [GitHub ontwikkelaarsdocumentatie.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

### AMP gebruiken in de kerncomponenten {#using-amp}

Individuele projecten kunnen beslissen of zij AMP al dan niet zullen benutten. Omdat AMP- en standaard HTML-pagina&#39;s parallel kunnen worden geleverd, kan een project ervoor kiezen om AMP alleen op bepaalde pagina&#39;s van het project te gebruiken.

### AMP-ondersteuning installeren {#installing-amp}

Omdat AMP optioneel is, wordt het als een uitbreiding aan de Componenten van de Kern geleverd.

* Voor AEM als projecten van de Cloud Service, is de uitbreiding automatisch beschikbaar.
* Voor on-premise en projecten van AMS, moet de uitbreiding uitdrukkelijk worden geïnstalleerd wanneer het installeren van de Componenten van de Kern.

Nadat de extensie is geïnstalleerd, moet de auteur van de component de supertypen van de component gewoon naar de supertypen in de extensie verwijzen.

### AMP inschakelen voor pagina&#39;s {#enabling-amp}

Als u AMP voor een pagina wilt inschakelen, moet de **AMP-modus** zijn geselecteerd in het [paginabeleid.](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/templates.html#editingatemplatepagepolicies)

![Opties voor AMP-paginabeleid](/help/assets/amp-policy.png)

* **Geen AMP** - De pagina wordt alleen als standaard-HTML geleverd.
* **AMP** met paden - De pagina wordt als AMP en HTML geleverd.
* **Alleen** AMP - De pagina wordt alleen als AMP geleverd.

De AMP-instellingen voor een pagina kunnen ook worden overschreven in de [Pagina-eigenschappen](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/authoring/editing-page-properties.html) voor een afzonderlijke pagina.

![Eigenschappen van AMP-pagina](/help/assets/amp-page-properties.png)

* **Overnemen van paginasjabloon** - Dit is de standaardwaarde, waardoor de instelling kan worden overgenomen uit het beleid van de paginasjabloon.
* **Geen AMP** - De pagina wordt alleen als standaard-HTML geleverd.
* **AMP** met paden - De pagina wordt als AMP en HTML geleverd.
* **Alleen** AMP - De pagina wordt alleen als AMP geleverd.
