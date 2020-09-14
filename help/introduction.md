---
title: Introductie van kerncomponenten
description: 'De kerncomponenten bieden robuuste en uitbreidbare basiscomponenten die zijn gebaseerd op de nieuwste technologie en best practices. '
translation-type: tm+mt
source-git-commit: f94b9e8757295ba25f11a0e60fc864a85db5c765
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 3%

---


# Introductie van kerncomponenten{#core-components-introduction}

In Adobe Experience Manager zijn componenten de structuurelementen die de inhoud vormen van de pagina&#39;s die worden gemaakt. Componenten zijn altijd een fundamenteel element geweest van de AEM-ervaring. Hierdoor is het maken van pagina&#39;s eenvoudig maar krachtig voor de auteur en de ontwikkeling van componenten flexibel en uitbreidbaar voor de ontwikkelaar.

De kerncomponenten zijn een reeks gestandaardiseerde WCM-componenten (Web Content Management) voor AEM om de ontwikkelingstijd te versnellen en de onderhoudskosten van uw websites te verlagen.

## Bronnen {#resources}

* **[Componentbibliotheek:](https://www.adobe.com/go/aem_cmp_library)** Een inzameling van voorbeelden om de componenten in hun diverse configuraties te bekijken.
* **Componentdocumentatie (dit document):** Voor ontwikkelaars en auteurs, met details over elke component.
* **[De Bewaarplaats van GitHub van de Componenten van de kern:](https://github.com/adobe/aem-core-wcm-components)** Voor de details van de ontwikkelaar van elke component en projectdownload.
* Aan de slag:
   * **[Succes met de kerncomponenten:](/help/developing/success.md)** Richtlijnen die ruim vóór de aanvang van om het even welk project moeten overwegen dat de Componenten van de Kern zal gebruiken.
   * **[WKND-zelfstudie:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** Een zelfstudie van twee dagen voor het bouwen van een nieuwe site.
   * **[Zelfstudie top:](https://expleague.azureedge.net/labs/L767/index.html)** Een zelfstudie van twee uur voor het bouwen van een nieuwe site (van een Lab op de VS-top in 2019).
   * **[Gems Webinar:](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)** Een rondleiding door de Core Components (opgenomen in december 2018).

## Features {#features}

|  |  |
|---|---|
| Gereed voor productie | De componenten van de Kern zijn 28 robuuste componenten die goed worden getest, wijd worden gebruikt, en die goed presteren. |
| Klaar voor cloud | Of het nu gaat om [AEM als Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html), op [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)of op locatie, ze werken gewoon. |
| Veelzijdig | De componenten vertegenwoordigen generische concepten waarmee de auteurs vrijwel elke lay-out kunnen samenstellen. |
| Configureerbaar | In het inhoudsbeleid [](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/page-templates-editable.html#content-policies) op sjabloonniveau wordt gedefinieerd welke functies de auteurs van de pagina al dan niet mogen gebruiken. |
| Overtrekbaar | De integratie [van de Laag van Gegevens van de Cliënt van](/help/developing/data-layer/overview.md) Adobe staat het volgen van alle aspecten van de bezoekerservaring toe. |
| Toegankelijk | Ze voldoen aan de [WCAG 2.1-standaard](https://www.w3.org/TR/WCAG21/), bieden ARIA-labels en ondersteunen toetsenbordnavigatie ([bekende problemen](https://github.com/adobe/aem-core-wcm-components/issues?utf8= ✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)). |
| SEO-vriendelijk | De HTML-uitvoer is semantisch en biedt [schema.org](https://schema.org) -microgegevensannotaties. |
| WebApp-Ready | Met de [gestroomlijnde JSON-uitvoer](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) is rendering op de client mogelijk, maar [in de context nog steeds](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html). |
| AMP-ondersteuning | De componenten hebben ingebouwde [ondersteuning voor de AMP-standaard,](/help/developing/amp.md) waardoor uw mobiele ervaring sneller wordt. |
| Design Kit | Met een [UI-kit voor Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) kunnen ontwerpers draadframes maken die zij vervolgens naar wens [kunnen](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_WKND.xd)opmaken. |
| Doordrukbaar | De componenten voeren het Systeem [van de](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/style-system.html)Stijl uit, en de prijsverhoging volgt [BEM CSS overeenkomsten](http://getbem.com/). |
| Aanpasbaar | Met verschillende patronen kunt u de HTML [eenvoudig aanpassen](developing/customizing.md), van het aanpassen van de HTML tot het hergebruik van de geavanceerde functionaliteit. |
| Versioning | Het [versiebeleid](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) zorgt ervoor dat de Componenten van de Kern uw plaats niet breken wanneer het verbeteren van dingen die u zouden kunnen beïnvloeden. |
| Lokaliseerbaar | Met slimme verwijzingsresolutie kunnen bepaalde componenten automatisch [corresponderende gelokaliseerde inhoud zoeken en](get-started/localization.md)renderen. |
| Open Bronnen | Als iets anders is dan zou moeten, [draagt u bij aan uw verbeteringen!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |

## De componenten {#the-components}

In de huidige versie van Core Components zijn de volgende componenten beschikbaar.

### Sjablooncomponenten {#template-components}

* [Pagina](components/page.md)
* [Navigatie](components/navigation.md)
* [Taalnavigatie](components/language-navigation.md)
* [Broodkruimel](components/breadcrumb.md)
* [Snel zoeken](components/quick-search.md)

### Componenten voor paginaontwerp {#page-authoring-components}

* [Titel](components/title.md)
* [Tekst](components/text.md)
* [Afbeelding](components/image.md)
* [Knop](components/button.md)
* [Teaser](components/teaser.md)
* [Downloaden](components/download.md)
* [Lijst](components/list.md)
* [Ervaar fragment](components/experience-fragment.md)
* [Inhoudsfragment](components/content-fragment-component.md)
* [Lijst met inhoudsfragmenten](components/content-fragment-list.md)
* [Insluiten](components/embed.md)
* [Delen van sociale media](components/sharing.md)
* [Scheidingsteken](components/separator.md)
* [Voortgangsbalk](components/progress-bar.md)
* [PDF-viewer](components/pdf-viewer.md)

### Containeronderdelen {#container-components}

* [Container](components/container.md)
* [Carousel](components/carousel.md)
* [Tabs](components/tabs.md)
* [Accordeon](components/accordion.md)

### Formuliercomponenten {#form-components}

* [Formuliercontainer](components/forms/form-container.md)
* [Formuliertekst](components/forms/form-text.md)
* [Formulieropties](components/forms/form-options.md)
* [Formulier verborgen](components/forms/form-hidden.md)
* [Formulierknop](components/forms/form-button.md)

>[!NOTE]
>
>De Componenten van de kern zijn niet onmiddellijk beschikbaar aan auteurs, moet het [ontwikkelingsteam hen aan uw milieu](get-started/using.md)eerst integreren. Zodra geïntegreerd, kunnen zij beschikbaar worden gemaakt en via de [malplaatjeredacteur](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)worden gevormd.

>[!NOTE]
>
>Sommige versies van individuele Core Components zijn mogelijk alleen compatibel met bepaalde versies van AEM.
>
>Zie de afzonderlijke Help-pagina (die is gekoppeld aan de vorige lijst) voor de specifieke component voor compatibiliteitsinformatie of raadpleeg het document [Core Components Versions](versions.md) voor meer informatie.

## Systeemvereisten {#system-requirements}

| Kernonderdelen | AEM as a Cloud Service | AEM 6,5 | AEM 6,4 | Java SE | Maven |
|---------|---------|---------|---------|---------|---------|
| [2.11.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | Continu | 6.5.5.0+ | 6.4.8.1+ | 8, 11 | 3.3.9+ |

Zie [Core Components Versions](versions.md)voor de vereisten van eerdere versies van Core Component.

De componenten van de Kern vereisen het gebruik van [editable malplaatjes](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) en steunen geen Klassieke UI noch statische malplaatjes. Controleer indien nodig de [AEM moderniseringsgereedschappen](https://opensource.adobe.com/aem-modernize-tools/pages/tools.html) om uw project bij te werken met deze moderne AEM.

Als u uw lokale ontwikkelomgeving wilt instellen, raadpleegt u [dit overzicht voor AEM als Cloud Service-SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) of dit document [voor oudere versies van AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).
