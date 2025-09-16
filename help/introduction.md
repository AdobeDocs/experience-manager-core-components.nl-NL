---
title: Introductie van kerncomponenten
description: Oplossingen voor problemen met de Core Components en anderen toestaan elementen te ontwerpen in AEM.
role: Architect, Developer, Admin, User
exl-id: d294db22-4cb0-48a4-9366-03fda5b8bb8e
source-git-commit: b6b850237bdab1cb59a81c3162182e5b25fbdb68
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 1%

---


# Introductie van kerncomponenten{#core-components-introduction}

{{traditional-aem}}

In Adobe Experience Manager zijn componenten de structuurelementen die de inhoud vormen van de pagina&#39;s die worden gemaakt. Componenten zijn altijd een fundamenteel element geweest van de AEM-ervaring. Hierdoor is het maken van pagina&#39;s eenvoudig maar krachtig voor de auteur en de ontwikkeling van componenten flexibel en uitbreidbaar voor de ontwikkelaar.

De kerncomponenten zijn een reeks gestandaardiseerde WCM-componenten (Web Content Management) voor AEM om de ontwikkelingstijd te versnellen en de onderhoudskosten van uw websites te verlagen.

## Bronnen {#resources}

* **[Bibliotheek van de Component:](https://www.adobe.com/go/aem_cmp_library)** een inzameling van voorbeelden om de componenten in hun diverse configuraties te bekijken.
* **Documentatie van de Component (dit document):** voor ontwikkelaars en auteurs, met details over elke component.
* **[&#128279;](https://github.com/adobe/aem-core-wcm-components) voor ontwikkelaarsdetails van elke component en projectdownload.**
* Aan de slag:
   * **[Succes met de Componenten van de Kern:](/help/developing/success.md)** Richtlijnen om ruim vóór het begin van om het even welk project te overwegen dat de Componenten van de Kern zal gebruiken.
   * **[WKND Leerprogramma:](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** een tweedaagse zelfstudie voor het bouwen van een nieuwe plaats.
   * **[Leerprogramma van de Top:](https://expleague.azureedge.net/labs/L767/index.html)** Een leerprogramma van twee uur voor de bouw van een nieuwe plaats (van een Laboratorium bij de Top van de VS 2019).
   * **[Gems Webinar:](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)** Een geleide tour van de Componenten van de Kern (die op Dec 2018 wordt geregistreerd).

## Functies {#features}

|  |  |
|---|---|
| Gereed voor productie | De Componenten van de Kern zijn 30 robuuste componenten WCM die goed worden getest, wijd worden gebruikt, en die goed presteren. |
| Klaar voor cloud | Of op [ AEM as a Cloud Service ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html), op [ Managed Services van Adobe ](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams), of op-gebouw, zij enkel werken. |
| Veelzijdig | De componenten vertegenwoordigen generische concepten waarmee de auteurs vrijwel elke lay-out kunnen samenstellen. |
| Configureerbaar | Sjabloon-niveau [ inhoudsbeleid ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html#content-policies) bepaalt welke eigenschappen de paginaauteurs worden toegestaan om te gebruiken of niet te gebruiken. |
| [ Responsief ](responsive.md) | Alle Core Components zijn ontworpen om volledig te reageren, zodat alle apparaten probleemloos kunnen werken |
| Overtrekbaar | De [ integratie van de Laag van Gegevens van de Cliënt van Adobe ](/help/developing/data-layer/overview.md) staat het volgen van alle aspecten van de bezoekerservaring toe. |
| Toegankelijk | Zij voldoen aan [ norm WCAG 2.1 ](https://www.w3.org/TR/WCAG21/), verstrekken de etiketten van ARIA, en steunen toetsenbordnavigatie ([ bekende kwesties ](https://github.com/adobe/aem-core-wcm-components/issues?utf8=&lbrace;0&q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle✓)). |
| SEO-vriendelijk | De output van HTML is semantisch en verstrekt [ schema.org ](https://schema.org) microgegevensaantekeningen. |
| WebApp-Ready | De [ gestroomlijnde output JSON ](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) staat cliënt-kant het teruggeven, nog met een mogelijkheid van [ in-context het uitgeven ](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html) toe. |
| AMP-ondersteuning | De componenten hebben ingebouwde [ steun voor de norm van AMP, ](/help/developing/amp.md) het versnellen van uw mobiele ervaringen. |
| Design Kit | A [ uitrusting UI voor Adobe XD ](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd) staat ontwerpers toe om draadframes tot stand te brengen die zij [ kunnen dan stijl zoals nodig ](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-0.0.2/AEM_UI-kit-WKND.xd). |
| Doordrukbaar | De componenten voeren het [ Systeem van de Stijl ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html) uit, en de prijsverhoging volgt [ CSS van BEM overeenkomsten ](https://getbem.com/). |
| Aanpasbaar | Verscheidene patronen staan [ gemakkelijke aanpassing ](developing/customizing.md) toe, van het aanpassen van HTML aan geavanceerd functioneel hergebruik. |
| Versioning | Het [ versioning beleid ](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) zorgt ervoor dat de Componenten van de Kern uw plaats niet zullen breken wanneer het verbeteren van dingen die u zouden kunnen beïnvloeden. |
| Lokaal | De slimme verwijzingsresolutie staat bepaalde componenten toe om te vinden en [ overeenkomstige gelokaliseerde inhoud automatisch terug te geven ](get-started/localization.md). |
| Open Bronnen | Als iets niet is zoals het zou moeten, [ bijdragen uw verbeteringen!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |


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
* [ Sociale Media die ](components/sharing.md) delen (afgekeurd)
* [Scheidingsteken](components/separator.md)
* [Voortgangsbalk](components/progress-bar.md)
* [PDF Viewer](components/pdf-viewer.md)

### Containeronderdelen {#container-components}

* [Container](components/container.md)
* [Carrousel](components/carousel.md)
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
>De Componenten van de kern zijn niet onmiddellijk beschikbaar aan auteurs, moet het [ ontwikkelingsteam hen aan uw milieu ](get-started/using.md) eerst integreren. Zodra geïntegreerd, kunnen zij beschikbaar worden gemaakt en pre-gevormd via de [ malplaatjedacteur ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>Sommige versies van individuele Core Components zijn mogelijk alleen compatibel met bepaalde versies van AEM.
>
>Zie de individuele hulppagina (verbonden aan in de vorige lijst) voor de specifieke component voor verenigbaarheidsinformatie of verwijs het [ document van de Versies van de Componenten van de Kern 0&rbrace; &lbrace;voor meer informatie.](versions.md)

## Systeemvereisten {#system-requirements}

| Versie kerncomponenten | AEM as a Cloud Service | AEM 6.5 LTS | AEM 6.5 | Java SE-versie | Geweven versie |
|---|---|---|---|---|---|
| [ 2.30.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.30.0) | Continu | 6,5 LTS GA | 6.5.21.0+ | 8, 11 | 3.3.9+ |

Voor de vereisten van de vorige versies van de Component van de Kern, zie {de Versies van de Componenten van 0} Kern [.](versions.md)

De Componenten van de Kern vereisen het gebruik van [ editable malplaatjes ](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) en steunen geen Klassieke UI noch statische malplaatjes. Indien nodig, controleer de [ Hulpmiddelen van de Modernisering van AEM ](https://opensource.adobe.com/aem-modernize-tools/) om uw project met deze moderne eigenschappen van AEM bij te werken.

Om uw lokale ontwikkelomgeving op te zetten, controleer [ dit overzicht voor AEM as a Cloud Service SDK ](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) of dit document [ voor oudere versies van AEM ](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

>[!TIP]
>
>De Core Components maken automatisch deel uit van AEM as a Cloud Service en u beschikt altijd over de nieuwste versie van de Core Components.
>
>Zie [ Gebruikend het document van de Componenten van de Kern ](/help/get-started/using.md) voor meer informatie over hoe te beginnen met de Componenten van de Kern zowel in AEMaaCS als op gebouw.

## Overige onderdelen {#other-components}

Er zijn aanvullende componenten beschikbaar voor AEM-auteurs, die zijn gebaseerd op de Core Components.

* [ de Componenten van de Kern E-mail ](/help/email/introduction.md) - ontdekt componenten die bovenop de Componenten van de Kern specifiek voor gebruik met Adobe Campaign worden gebouwd.
* [ Aangepaste Componenten van de Kern van Forms ](/help/adaptive-forms/introduction.md) - Gebruikend de Aangepaste Componenten van de Kern van Forms in Adobe Experience Manager, kunt u dwingende inschrijvingservaringen tot stand brengen.
