---
title: AMP-ondersteuning voor de kerncomponenten
description: De kerncomponenten ondersteunen AMP - Versnelde mobiele pagina's
role: Architect, Developer, Admin
exl-id: 1fd9b6b5-0e4d-48c7-8faa-42e0d4a6bbd0
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# AMP-ondersteuning voor de kerncomponenten {#amp-support}

Vanaf [release 2.11.0](/help/versions.md) van de kerncomponenten, [AMP - Versnelde mobiele pagina&#39;s](https://developers.google.com/amp) - volledig worden ondersteund.

In dit document wordt een overzicht gegeven van de manier waarop AMP wordt ondersteund en van de manier waarop u dit voor uw sites kunt inschakelen. Voor volledige technische details zie echter de [documentatie voor GitHub-ontwikkelaars.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## Wat is AMP? {#what-is-amp}

Accelerated Mobile Pages of AMP is een opensource-framework dat oorspronkelijk door Google is ontworpen om pagina&#39;s te optimaliseren voor mobiel surfen. AMP-pagina&#39;s worden doorgaans veel sneller geladen dan standaardwebpagina&#39;s en bieden betere mobiele ervaringen.

## AMP in de kerncomponenten {#amp-in-core-components}

Ondersteuning voor AMP in de Core Components is [volledig configureerbaar.](#enabling-amp) AMP-versies van pagina&#39;s kunnen alleen worden aangeboden, naast de standaard HTML-versies, of helemaal niet.

De kerncomponenten gebruiken `amp` als een verkiesbare selecteur om een pagina van AMP terug te geven. Bijvoorbeeld `example.html` zou de normale pagina weergeven en `example.amp.html` zou de AMP-versie zijn.

Individuele projecten kunnen beslissen of zij AMP al dan niet zullen benutten. Omdat AMP- en standaard HTML-pagina&#39;s parallel kunnen worden geleverd, kan een project ervoor kiezen om AMP alleen op bepaalde pagina&#39;s van het project te gebruiken.

## Aan de slag met AMP-ondersteuning in uw project {#getting-started}

Hoewel AMP-ondersteuning veel flexibiliteit biedt, zijn er slechts enkele eenvoudige stappen nodig om snel aan de slag te gaan:

1. Installeer indien nodig de extensie voor AMP-ondersteuning.
   * Voor AEM as a Cloud Service projecten, is de uitbreiding automatisch beschikbaar met de Componenten van de Kern en geen installatie is noodzakelijk.
   * Voor on-premise en projecten van AMS, moet de uitbreiding uitdrukkelijk worden geïnstalleerd wanneer het installeren van de Componenten van de Kern.
1. Zodra de uitbreiding AMP wordt geïnstalleerd, moet de componentenauteur de componentensupertypes aan die in de uitbreiding eenvoudig richten.
1. [Ondersteuning voor AMP inschakelen](#enabling-amp) op sjabloonniveau of op afzonderlijke pagina&#39;s.
1. [Inline CSS implementeren](#css-requirements) zoals vereist.

### AMP inschakelen voor pagina&#39;s {#enabling-amp}

Als u AMP voor een pagina wilt inschakelen, **AMP-modus** moet in [Paginabeleid.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-page-policy-template-author-developer)

![Opties voor AMP-paginabeleid](/help/assets/amp-policy.png)

* **Geen AMP** - De pagina wordt alleen geleverd als standaard-HTML.
* **Gepareerde AMP** - De pagina wordt geleverd als AMP en als HTML.
* **Alleen AMP** - De pagina wordt alleen geleverd als AMP.

De AMP-instellingen voor een pagina kunnen ook worden overschreven in het dialoogvenster [Pagina-eigenschappen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) voor een afzonderlijke pagina.

![Eigenschappen van AMP-pagina](/help/assets/amp-page-properties.png)

* **Overnemen van paginasjabloon** - Dit is de standaardwaarde, die het plaatsen om van het beleid van het paginasjabloon toestaat te worden genomen.
* **Geen AMP** - De pagina wordt alleen geleverd als standaard-HTML.
* **Gepareerde AMP** - De pagina wordt geleverd als AMP en als HTML.
* **Alleen AMP** - De pagina wordt alleen geleverd als AMP.

### CSS-vereisten {#css-requirements}

Bij het gebruik van AMP met de kerncomponenten is het belangrijkste verschil dat AMP alles vereist [CSS die moet worden omlijnd](including-clientlibs.md#inlining) in de `<head>` en geoptimaliseerd.

Hiertoe wordt een aangepaste pagina-component gebruikt, die alleen de AMP-specifieke CSS laadt voor componenten die op de pagina aanwezig zijn.

>[!NOTE]
>
>Vanwege ontwerpbeperkingen van AMP biedt Adobe geen ondersteuning voor het gebruik van het responsieve raster met de AMP-versie van uw pagina.

Voor nadere eisen en technische details raadpleegt u de [documentatie voor GitHub-ontwikkelaars.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)
