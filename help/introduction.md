---
title: Introductie van kerncomponenten
description: 'De kerncomponenten bieden robuuste en uitbreidbare basiscomponenten die zijn gebaseerd op de nieuwste technologie en best practices. '
translation-type: tm+mt
source-git-commit: 850fbeec3cb31f4ea6873daa2555953684fd5a8d
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 3%

---


# Introductie van kerncomponenten{#core-components-introduction}

In Adobe Experience Manager zijn componenten de structuurelementen die de inhoud vormen van de pagina&#39;s die worden gemaakt. Componenten zijn altijd een fundamenteel element geweest van de AEM-ervaring. Hierdoor is het maken van pagina&#39;s eenvoudig maar krachtig voor de auteur en de ontwikkeling van componenten flexibel en uitbreidbaar voor de ontwikkelaar.

De kerncomponenten zijn een reeks gestandaardiseerde WCM-componenten (Web Content Management) voor AEM om de ontwikkelingstijd te versnellen en de onderhoudskosten van uw websites te verlagen.

## Bronnen {#resources}

* **[Componentbibliotheek:](https://www.adobe.com/go/aem_cmp_library)** een verzameling voorbeelden om de componenten in hun verschillende configuraties weer te geven.
* **Componentdocumentatie (dit document):** voor ontwikkelaars en auteurs, met details over elke component.
* **[De Bewaarplaats van GitHub van de Componenten van de kern:](https://github.com/adobe/aem-core-wcm-components)** Voor ontwikkelaardetails van elke component en projectdownload.
* Aan de slag:
   * **[Succes met de Componenten van de Kern:](/help/developing/success.md)** Richtlijnen om ruim vóór de aanvang van om het even welk project te overwegen dat de Componenten van de Kern zal gebruiken.
   * **[WKND-zelfstudie:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** een zelfstudie van twee dagen om een nieuwe site te maken.
   * **[Zelfstudie voor top:](https://expleague.azureedge.net/labs/L767/index.html)** Een zelfstudie van twee uur voor het bouwen van een nieuwe site (van een Lab op de VS-top in 2019).
   * **[Gems Webinar: ](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)** Een begeleide rondleiding door de Core Components (opgenomen in december 2018).

## Functies {#features}

|  |  |
|---|---|
| Gereed voor productie | De componenten van de Kern zijn 28 robuuste componenten die goed worden getest, wijd worden gebruikt, en die goed presteren. |
| Klaar voor cloud | Of het nu gaat om [AEM als Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html), op [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) of op locatie, ze werken alleen. |
| Veelzijdig | De componenten vertegenwoordigen generische concepten waarmee de auteurs vrijwel elke lay-out kunnen samenstellen. |
| Configureerbaar | Sjabloonniveau [inhoudsbeleid](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html#content-policies) bepaalt welke eigenschappen de paginaauteurs mogen gebruiken of niet mogen gebruiken. |
| Overtrekbaar | Met de [integratie van de gegevenslaag van de Adobe-client](/help/developing/data-layer/overview.md) kunt u alle aspecten van de ervaring van de bezoeker bijhouden. |
| Toegankelijk | Zij voldoen [WCAG 2.1 norm](https://www.w3.org/TR/WCAG21/), verstrekken ARIA etiketten, en steunen toetsenbordnavigatie ([bekende kwesties](https://github.com/adobe/aem-core-wcm-components/issues?utf8= ✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)). |
| SEO-vriendelijk | De HTML-uitvoer is semantisch en biedt microgegevensannotaties [schema.org](https://schema.org). |
| WebApp-Ready | Met de [gestroomlijnde JSON-uitvoer](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) is rendering op de client mogelijk, maar met de mogelijkheid om [in-context te bewerken](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html). |
| AMP-ondersteuning | De componenten hebben ingebouwde [ondersteuning voor de AMP-standaard,](/help/developing/amp.md) versnelt uw mobiele beleving. |
| Design Kit | Met een [UI-kit voor Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) kunnen ontwerpers draadframes maken die ze vervolgens [desgewenst kunnen opmaken](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_WKND.xd). |
| Doordrukbaar | De componenten voeren [Stijlsysteem](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/style-system.html) uit, en de prijsverhoging volgt [BEM CSS overeenkomsten](http://getbem.com/). |
| Aanpasbaar | Met verschillende patronen kunt u [gemakkelijk aanpassen](developing/customizing.md), van het aanpassen van de HTML aan geavanceerd hergebruik van de functionaliteit. |
| Versioning | Het [versieringsbeleid](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) zorgt ervoor dat de Componenten van de Kern uw plaats niet zullen breken wanneer het verbeteren van dingen die u zouden kunnen beïnvloeden. |
| Lokaliseerbaar | Met de slimme verwijzingsresolutie kunnen bepaalde componenten automatisch corresponderende gelokaliseerde inhoud zoeken en [renderen](get-started/localization.md). |
| Open Bronnen | Als iets niet zoals het zou moeten zijn, [bijdragen uw verbeteringen!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |

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

### Containercomponenten {#container-components}

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
>De Componenten van de kern zijn niet onmiddellijk beschikbaar aan auteurs, [ontwikkelingsteam moet hen eerst aan uw milieu integreren](get-started/using.md). Zodra geïntegreerd, kunnen zij via [malplaatjeredacteur](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) ter beschikking worden gesteld en worden gevormd.

>[!NOTE]
>
>Sommige versies van individuele Core Components zijn mogelijk alleen compatibel met bepaalde versies van AEM.
>
>Zie de individuele hulppagina (verbonden aan in de vorige lijst) voor de specifieke component voor verenigbaarheidsinformatie of verwijs [de Versies van de Componenten van de Kern ](versions.md) document voor meer informatie.

## Systeemvereisten {#system-requirements}

| Kernonderdelen | AEM as a Cloud Service | AEM 6,5 | AEM 6,4 | Java SE | Maven |
|---------|---------|---------|---------|---------|---------|
| [2.12.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.2) | Continu | 6.5.5.0+ * | 6.4.8.1+ * | 8, 11 | 3.3.9+ |

>[!NOTE]
>
>(*) Sinds versie 2.11.0 is `org.apache.sling.models.impl` versie 1.4.12 of hoger vereist (vanwege [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). Dit zal voor AEM 6.4 en 6.5 in een toekomstig Service Pack worden verstrekt. Tot die tijd, is de bundel van Modellen Sling inbegrepen in `core.wcm.components.all` pakket.

Voor de vereisten van vorige versies van de Component van de Kern, zie [Versies van de Componenten van de Kern](versions.md).

De Componenten van de Kern vereisen het gebruik van [editable malplaatjes](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) en steunen geen Klassieke UI noch statische malplaatjes. Indien nodig, controleer [AEM ModerniseringsHulpmiddelen](https://opensource.adobe.com/aem-modernize-tools/pages/tools.html) om uw project met deze moderne AEM eigenschappen bij te werken.

Als u uw lokale ontwikkelomgeving wilt instellen, raadpleegt u [dit overzicht voor AEM als Cloud Service SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) of dit document [voor oudere versies van AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).
