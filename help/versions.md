---
title: Core Components-versies
description: De Componenten van de kern worden gepubliceerd als versies die meer dan één versie van de zelfde kerncomponenten kunnen bevatten. In dit document wordt uitgelegd welke versies en versies beschikbaar zijn en hoe u de compatibiliteit met Core Components en AEM begrijpt.
translation-type: tm+mt
source-git-commit: a35054397619e3efe051e557951e2d62634c678a
workflow-type: tm+mt
source-wordcount: '1783'
ht-degree: 11%

---


# Core Components-versies {#core-components-versions}

De huidige versie van de Core Components is 2.12.0 en is compatibel met [AEM als Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) en [op-gebouw AEM](https://docs.adobe.com/content/help/en/experience-manager-65/user-guide/home.html) installaties. Deze werd in oktober 2020 gepubliceerd als een belangrijke update voor release 2.0.0. Versie 2.0.0 introduceerde nieuwe componenten samen met v2 updates van bestaande componenten.

## Historie en compatibiliteit vrijgeven {#release-history-and-compatibility}

De Core Components zijn ontworpen om flexibel te zijn en compatibel met alle ondersteunde AEM versies. Daarom kan een versie van de componenten meerdere versies van dezelfde component bevatten.

De volgende lijsten illustreren de verenigbaarheid van de versies van de Componenten van de Kern samen welke componentenversies bevat zijn waarin versies.

### Historie en vereisten vrijgeven {#release-history-requirements}

De volgende lijst, waarvan de inhoud op GitHub met volledige versiedetails [](https://github.com/adobe/aem-core-wcm-components/releases)beschikbaar is, geeft een overzicht van de versies van de Componenten van de Kern en hun verenigbaarheid met AEM versies en van Java.

| Geen | Beschrijving | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service | Java | Releasedatum |
|---|---|---|---|---|---|---|
| [2.12.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | Deze versie introduceerde [een nieuwe POST vormmanager;](/help/components/forms/form-container.md#post-data) de mogelijkheid om aangepaste CSS-, JavaScript- en metagegevenstags op te nemen via een contextbewuste configuratie; [](/help/developing/including-clientlibs.md#context-aware-loading) en een `DataLayerBuilder` nut om de integratie van de gegevenslaag in douanecomponenten te [vereenvoudigen.](/help/developing/data-layer/integrations.md#enabling-custom-components) | 6.4.8.1+ | 6.5.5.0+ | Continu | 8, 11 | 27 oktober 2020 |
| [2.11.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | Deze release introduceerde ondersteuning voor [AMP.](/help/developing/amp.md) | 6.4.8.1+ | 6.5.5.0+ | Continu | 8, 11 | 20 juli 2020 |
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | In deze versie is de component [PDF Viewer geïntroduceerd.](/help/components/pdf-viewer.md) | 6.4.8.1+ | 6.5.5.0+ | Continu | 8, 11 | 17 juni 2020 |
| [2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | Deze versie liet integratie met de Laag [van Gegevens van de Cliënt van](/help/developing/data-layer/overview.md) Adobe toe en introduceerde de component van de Bar van de [Voortgang.](/help/components/progress-bar.md) | 6.4.8.0+ | 6.5.4.0+ | Continu | 8, 11 | 29 mei 2020 |
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Deze release was gericht op oplossingen met kleine verbeteringen. | 6.4.4.0+ | 6.5.0.0+ | Continu | 8, 11 | 5 december 2019 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | In deze versie is de nieuwe component [Embed geïntroduceerd.](/help/components/embed.md) | 6.4.4.0+ | 6.5.0.0+ | Continu | 8, 11 | 25 september 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | In deze versie is de nieuwe component [Experience Fragment geïntroduceerd.](/help/components/experience-fragment.md) | 6.4.4.0+ | 6.5.0.0+ | Continu | 8, 11 | 6 september 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Deze versie introduceerde de nieuwe componenten [Accordion,](/help/components/accordion.md) [Button,](/help/components/button.md) [Container,](/help/components/container.md) en [Download.](/help/components/download.md) | 6.4.2.0+ | 6.5.0.0+ | Continu | 8, 11 | 25 juni 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | In deze versie werd de component [Lijst met inhoudsfragmenten geïntroduceerd.](/help/components/content-fragment-list.md) | 6.4.2.0+ | 6.5.0.0+ | Continu | 8, 11 | 7 mei 2019 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Deze release was gericht op verfijningen in de [componentbibliotheek,](https://aemcomponents.dev) maar bevat ook enkele functieverbeteringen voor de [scheidingscomponent.](/help/components/separator.md) | 6.4.2.0+ | 6.5.0.0+ | Continu | 8 | 14 maart 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Deze release was gericht op de [componentbibliotheek](https://aemcomponents.dev) en introduceerde de nieuwe [scheidingscomponent,](/help/components/separator.md) maar bevat ook enkele functieverbeteringen voor de [afbeeldingscomponent.](/help/components/image.md) | 6.4.2.0+ | - | - | 8 | 11 februari 2019 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Deze release was vooral gericht op foutoplossingen, maar bevat ook enkele functieverbeteringen voor de [Carousel-component.](/help/components/carousel.md) | 6.4.2.0+ | - | - | 8 | 27 november 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | In deze release werden de [tabs Component](/help/components/tabs.md) en de [Carousel Component](/help/components/carousel.md) geïntroduceerd, evenals verbeteringen in de [Image Component,](/help/components/image.md) [Page Component,](/help/components/page.md) en de [Title Component](/help/components/title.md) en verbeterde tekstspatiëring. | 6.4.2.0+ | - | - | 8 | 16 oktober 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | In deze versie werd de [Taser-component](/help/components/teaser.md) geïntroduceerd, samen met verbeteringen in de [afbeeldingscomponent](/help/components/image.md) en een groot aantal foutoplossingen. | 6.4.2.0+ | - | - | 8 | 13 juli 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Dit was een foutopsporingsversie. | 6.4.0.0+ | - | - | 8 | 12 juni 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Deze release heeft verbeteringen onder de kap, foutoplossingen en kleine verbeteringen toegevoegd, waaronder ondersteuning voor het spiegelen van afbeeldingen in de [afbeeldingscomponent.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 11 april 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Deze release was vooral gericht op verbeteringen onder de wasdom, foutoplossingen en enkele kleine verbeteringen in de component [Afbeelding,](/help/components/image.md) [Paginacomponent](/help/components/page.md) en de component [Inhoudsfragment.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 7 maart 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Deze versie introduceerde de Component van de [Navigatie,](/help/components/navigation.md) de Component van de Navigatie van de [Taal,](/help/components/language-navigation.md) en de Component [van het](/help/components/quick-search.md) Snel Onderzoek en voerde het Systeem [van de](/help/get-started/authoring.md#component-styling) Stijl voor alle componenten uit. | 6.4.0.0+ | - | - | 8 | 16 januari 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Deze release implementeert JSON-export op alle componenten en introduceert de [Content Fragment-component.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 10 oktober 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Met deze release worden verschillende correcties toegevoegd voor de [afbeeldingscomponent.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 4 augustus 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | In deze release worden correcties toegevoegd voor de [pagina-component,](/help/components/page.md) de [afbeeldingscomponent,](/help/components/image.md) en diverse algemene correcties en verbeteringen. | 6.4.0.0+ | - | - | 8 | 26 april 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Met deze release voegt u correcties toe voor geanimeerde GIF-afbeeldingen in [Afbeeldingscomponent.](/help/components/image.md) | 6.4.0.0+ | - | - | 7 | 22 maart 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Eerste release van Core Components. | 6.4.0.0+ | - | - | 7 | 20 maart 2017 |

>[!NOTE]
>
>Net als bij AEM raadt Adobe ontwikkelaars aan de [nieuwste versie en versies van de beschikbare Core Components](https://github.com/adobe/aem-core-wcm-components/releases/latest) te gebruiken die compatibel zijn met de versie van AEM die ze uitvoeren om te profiteren van de meest actuele oplossingen en functies.

### Componentversies en -releases {#component-versions-and-releases}

De volgende lijst specificeert welke versies van welke componenten bevat zijn waarin versies van de Componenten van de Kern.

|  | Release 1.0.0 - 1.0.6 | Release 1.1.0 | Release 2.0.0 - 2.0.8 | Release 2.1.0 | Release 2.2.0-2.2.0 | Release 2.3.0-2.3.2 | Release 2.4.0 | Release 2.5.0 | Release 2.6.0 | Release 2.7.0-2.8.0 | Release 2.9.0+ |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **[Pagina](components/page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Titel](components/title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Afbeelding](components/image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Lijst](components/list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Broodkruimel](components/breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Delen van sociale media](components/sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Formuliercontainer](components/forms/form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formuliertekst](components/forms/form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulieropties](components/forms/form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulier verborgen](components/forms/form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulierknop](components/forms/form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Inhoudsfragment](components/content-fragment-component.md)** |  | Sandbox | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 |
| **[Navigatie](components/navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Taalnavigatie](components/language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Snel zoeken](components/quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Teaser](components/teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Tabs](components/tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Carousel](components/carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Scheidingsteken](components/separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Lijst met inhoudsfragmenten](components/content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[Accordeon](components/accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Knop](components/button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Container](components/container.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Downloaden](components/download.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Ervaar fragment](components/experience-fragment.md)** |  |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Insluiten](components/embed.md)** |  |  |  |  |  |  |  |  |  | v1 | v1 |
| **[Voortgangsbalk](components/progress-bar.md)** |  |  |  |  |  |  |  |  |  |  | v1 |
| **[PDF-viewer](components/pdf-viewer.md)** |  |  |  |  |  |  |  |  |  |  | v1 |

## Versies en releases {#versions-and-releases}

De Componenten van de kern worden verdeeld via GitHub. Hierdoor kan Adobe sneller functionaliteit toevoegen aan de componenten en kan ook gemeenschapsinvoer buiten de AEM releasecyclus plaatsvinden.

De Core Components worden beschikbaar gesteld met bepaalde AEM versies waarmee zij compatibel zijn. Dit betekent dat één AEM versie meerdere versies of versies van de Componenten van de Kern kan steunen. Dit geeft meer flexibiliteit dan de vroegere Componenten van de Stichting, die aan een specifieke versie van AEM gebonden waren.

### Versies {#versions}

De belangrijkste herhaling van de Componenten van de Kern zijn de **versies**. Elke component heeft een versie. Versies worden aangeduid met **v** , aangevuld met een positief geheel getal dat niet gelijk is aan nul, zoals v1 en v2. Versies worden alleen verhoogd voor wijzigingen die niet compatibel zijn met oudere versies, wat normaal gesproken het geval is bij de introductie van nieuwe functies en functionaliteit.

De ontwikkelaars en de beheerders kunnen versies van de kerncomponenten door een aantal in hun middeltypepaden, en in volledig gekwalificeerde de klassennamen van Java van hun implementaties erkennen. Dit versienummer vertegenwoordigt een hoofdversie zoals gedefinieerd door [semantische versierichtlijnen](https://semver.org/).

Raadpleeg de documentatie voor [ontwikkelaars van Core Components](developing/guidelines.md)voor meer informatie over kerncomponentversies.

### Uitstoot {#releases}

De kerncomponenten worden ter beschikking gesteld door **versies** en [vertegenwoordigen de daadwerkelijke gepubliceerde artefacten beschikbaar op GitHub](https://github.com/adobe/aem-core-wcm-components/releases). De versies worden aangegeven met een decimaal aantal van formaat X.Y.Z en verzamelen alle kerncomponenten samen als te leveren pakket.

* **De grote versies** kunnen nieuwe versies van bestaande componenten samen met volledig nieuwe componenten evenals standaardinsectenmoeilijke situaties introduceren. Dit wordt vertegenwoordigd door een toename in de component X van het versieaantal.
* **De belangrijke versies** kunnen nieuwe functionaliteit aan bestaande versies van componenten samen met insectenmoeilijke situaties introduceren. Dit wordt vertegenwoordigd door een toename in de component Y van het versieaantal.
* **Kleine versies** bevatten alleen opgeloste problemen. Dit wordt vertegenwoordigd door een verhoging in de component van Z van het versieaantal.

>[!NOTE]
>
>De versies kunnen veelvoudige versies van de zelfde component bevatten.
>
>Dezelfde versie van een component kan in meerdere releases worden weergegeven.

## Ondersteuning voor kerncomponenten {#core-components-support}

De Componenten van de kern zijn een integraal deel van AEM en gesteund zoals is, onder de zelfde voorwaarden alsof zij als deel van Quickstart werden geleverd.

Net als andere productkenmerken is de algemene regel van het einde van de levensduur:

* Componenten worden eerst aangekondigd te worden vervangen voordat ze worden verwijderd
* Op zijn vroegst worden ze na de aankondiging uit de AEM gehaald.

Dit geeft klanten minstens één versiecyclus om naar de nieuwe versie van de component te bewegen, alvorens steun beëindigt.

In de versie van elke component worden duidelijk de AEM versies vermeld die worden ondersteund. Wanneer de steun voor een versie van AEM beëindigt, dan ook de steun van de Componenten van de Kern voor die versie van AEM.

Meer informatie over de ondersteuning van componentaanpassingen vindt u op de pagina Core Components [Customizing](developing/customizing.md) (Kerncomponenten aanpassen) van de relevante versie van Core Components.

## Ondersteuning van stichtingscomponenten {#foundation-component-support}

De nadruk op Adobe is verschoven naar de kerncomponenten en er worden nieuwe functies toegevoegd.

[Bijna zijn alle Componenten van de Stichting verouderd met AEM 6.5](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) en slechts zullen de belangrijkste insectenmoeilijke situaties voor de Componenten van de Stichting in de toekomst worden overwogen.
