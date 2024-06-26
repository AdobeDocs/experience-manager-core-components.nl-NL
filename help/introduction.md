---
title: Introductie van kerncomponenten
description: Oplossingen voor problemen met de Core Components en anderen toestaan elementen te ontwerpen binnen AEM.
role: Architect, Developer, Admin, User
exl-id: d294db22-4cb0-48a4-9366-03fda5b8bb8e
source-git-commit: 39c9dd3374ea7c31b9f03cc02e883ab26f463368
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 0%

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
   * **[WKND-zelfstudie:](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** Een zelfstudie van twee dagen voor het bouwen van een nieuwe site.
   * **[Zelfstudie top:](https://expleague.azureedge.net/labs/L767/index.html)** Een zelfstudie van twee uur voor het bouwen van een nieuwe site (van een Lab op de VS-top in 2019).
   * **[Gems Webinar:](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)** Een rondleiding door de Core Components (opgenomen in december 2018).

## Functies {#features}

|  |  |
|---|---|
| Gereed voor productie | De Componenten van de Kern zijn 30 robuuste componenten WCM die goed worden getest, wijd worden gebruikt, en die goed presteren. |
| Klaar voor cloud | Of aan [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html), op [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)Op locatie werken ze gewoon. |
| Veelzijdig | De componenten vertegenwoordigen generische concepten waarmee de auteurs vrijwel elke lay-out kunnen samenstellen. |
| Configureerbaar | Sjabloonniveau [inhoudsbeleid](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html#content-policies) bepalen welke functies de auteurs van de pagina al dan niet mogen gebruiken. |
| [Responsief](responsive.md) | Alle Core Components zijn ontworpen om volledig te reageren, zodat alle apparaten probleemloos kunnen werken |
| Overtrekbaar | De [Integratie van de gegevenslaag van de client Adoben](/help/developing/data-layer/overview.md) Hiermee kunnen alle aspecten van de ervaring van de bezoeker worden bijgehouden. |
| Toegankelijk | Zij voldoen aan [WCAG 2.1-standaard](https://www.w3.org/TR/WCAG21/), biedt ARIA-labels en ondersteunt toetsenbordnavigatie ([bekende problemen](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)). |
| SEO-vriendelijk | De HTML-uitvoer is semantisch en biedt [schema.org](https://schema.org) microgegevensannotaties. |
| WebApp-Ready | De [gestroomlijnde JSON-uitvoer](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) renderen aan de clientzijde is mogelijk, maar met de mogelijkheid van [contextbewerking](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html). |
| AMP-ondersteuning | De componenten hebben ingebouwde [steun voor de AMP-norm;](/help/developing/amp.md) uw mobiele beleving versnellen. |
| Design Kit | A [UI-kit voor Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd) kunnen ontwerpers draadframes maken die ze vervolgens kunnen maken [stijl indien nodig](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-0.0.2/AEM_UI-kit-WKND.xd). |
| Doordrukbaar | De componenten implementeren de [Stijlsysteem](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html)en volgt de markering [BEM CSS-conventies](https://getbem.com/). |
| Aanpasbaar | Meerdere patronen zijn toegestaan [eenvoudig aanpassen](developing/customizing.md), van het aanpassen van de HTML aan geavanceerd hergebruik van de functionaliteit. |
| Versioning | De [versiebeleid](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) zorgt ervoor dat de componenten van de Kern uw plaats niet breken wanneer het verbeteren van dingen die u zouden kunnen beïnvloeden. |
| Lokaal | Met de slimme verwijzingsresolutie kunnen bepaalde componenten worden gevonden en [overeenkomstige gelokaliseerde inhoud automatisch renderen](get-started/localization.md). |
| Open Bronnen | Als iets anders is dan zou moeten, [bijdragen aan uw verbeteringen!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |


## De WCM-componenten {#the-wcm-components}

In de huidige versie van Core Components zijn de volgende componenten beschikbaar.

### Sjablooncomponenten {#template-components}

* [Pagina](components/page.md)
* [Navigatie](components/navigation.md)
* [Taalnavigatie](components/language-navigation.md)
* [Broodkruimel](components/breadcrumb.md)
* [Snel zoeken](components/quick-search.md)
* [Inhoudsopgave](components/tableofcontents.md)

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
* [Delen van sociale media](components/sharing.md) (afgekeurd)
* [Scheidingsteken](components/separator.md)
* [Voortgangsbalk](components/progress-bar.md)
* [PDF Viewer](components/pdf-viewer.md)

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
>De belangrijkste componenten zijn niet onmiddellijk beschikbaar aan auteurs, [ontwikkelingsteam moet deze eerst integreren in uw omgeving](get-started/using.md). Zodra geïntegreerd, kunnen zij beschikbaar worden gemaakt en vooraf gevormd via [sjablooneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>Sommige versies van individuele Core Components zijn mogelijk alleen compatibel met bepaalde versies van AEM.
>
>Zie de afzonderlijke Help-pagina (gekoppeld aan in de vorige lijst) voor de specifieke component voor compatibiliteitsinformatie of raadpleeg de [Versies van kerncomponenten](versions.md) voor meer informatie.

## Systeemvereisten {#system-requirements}

| Versie kerncomponenten | AEM as a Cloud Service | AEM 6.5 Patchniveau | Java SE-versie | Geweven versie |
|---------|---------|---------|---------|---------|
| [2,25,4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.25.4) | Continu | 6.5.21.0+ | 8, 11 | 3.3.9+ |

Voor de vereisten van eerdere versies van Core Component, zie [Versies van kerncomponenten](versions.md).

De kerncomponenten vereisen het gebruik van [bewerkbare sjablonen](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) en ondersteunen geen klassieke UI of statische sjablonen. Controleer indien nodig de [AEM moderniseringsinstrumenten](https://opensource.adobe.com/aem-modernize-tools/) om uw project bij te werken met deze moderne AEM.

Als u uw lokale ontwikkelomgeving wilt instellen, kunt u het beste uitchecken [dit overzicht voor AEM as a Cloud Service SDK](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) of dit document [voor oudere AEM](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

>[!TIP]
>
>De Core Components maken automatisch deel uit van AEM as a Cloud Service en u beschikt altijd over de nieuwste versie van de Core Components.
>
>Zie de [Basiscomponenten gebruiken](/help/get-started/using.md) document voor meer informatie over hoe u aan de slag kunt met de Core Components in AEMaaCS en in de bedrijfsruimten.

## Overige onderdelen {#other-components}

Er zijn extra componenten beschikbaar aan AEM auteurs, die op de Componenten van de Kern worden gebouwd.

* [De e-mailkerncomponenten](/help/email/introduction.md) - Ontdek componenten die bovenop de Core Components specifiek voor gebruik met Adobe Campaign zijn gebouwd.
