---
title: Core Components-versies
description: De Componenten van de kern worden gepubliceerd als versies die meer dan één versie van de zelfde kerncomponenten kunnen bevatten. In dit document wordt uitgelegd welke versies en versies beschikbaar zijn en hoe u de compatibiliteit met Core Components en AEM kunt begrijpen.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Core Components-versies {#core-components-versions}

De huidige versie van de Core Components is 2.8.0 en is compatibel met [AEM als Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) en [AEM](https://docs.adobe.com/content/help/en/experience-manager-65/user-guide/home.html) -installaties op locatie. Deze werd in december 2019 gepubliceerd als een belangrijke update voor release 2.0.0. Versie 2.0.0 introduceerde nieuwe componenten samen met v2 updates van bestaande componenten.

Zie de sectie Geschiedenis van de [Versie en Verenigbaarheid](#versions-and-releases) van dit document voor meer informatie.

U kunt ook de [componentbibliotheek](https://adobe.com/go/aem_cmp_library)uitchecken, waarin de actuele versie van de Core Components wordt weergegeven en voorbeelden van het gebruik van deze versie worden gegeven.

## Versies en releases {#versions-and-releases}

De Componenten van de kern worden verdeeld via GitHub. Op deze manier kan Adobe sneller functionaliteit toevoegen aan de componenten en kan ook community-invoer buiten de AEM-releasecyclus plaatsvinden.

De kerncomponenten worden beschikbaar gesteld met gedefinieerde AEM-versies waarmee ze compatibel zijn. Dit betekent dat één AEM-versie meerdere versies of versies van de Core Components kan ondersteunen. Dit geeft meer flexibiliteit dan de vroegere Componenten van de Stichting, die aan een specifieke versie van AEM gebonden waren.

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

## Historie en compatibiliteit vrijgeven {#release-history-and-compatibility}

De Core Components zijn voor het eerst uitgebracht met AEM 6.3 en zijn ontworpen voor flexibiliteit en compatibiliteit met alle ondersteunde AEM-versies. Daarom kan een versie van de componenten meerdere versies van dezelfde component bevatten.

De volgende lijsten illustreren de verenigbaarheid van de versies van de Componenten van de Kern samen welke componentenversies bevat zijn waarin versies.

### Historie opheffen en ondersteunde AEM-versies {#release-history-supported-aem-versions}

De volgende lijst, waarvan de inhoud op GitHub met volledige versiedetails [](https://github.com/adobe/aem-core-wcm-components/releases)beschikbaar is, geeft een overzicht van de versies van de Componenten van de Kern en hun verenigbaarheid met versies AEM en Java.

| Geen | Beschrijving | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service | Java | Releasedatum |
|---|---|---|---|---|---|---|---|
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Deze release was gericht op oplossingen met kleine verbeteringen. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | Continu | 8, 11 | 5 december 2019 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | In deze versie is de nieuwe component Embed geïntroduceerd | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | Continu | 8, 11 | 25 september 2019 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Deze release introduceerde de nieuwe Experience Fragment-component | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | Continu | 8, 11 | 6 september 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Deze versie introduceerde de nieuwe componenten Accordion, Button, Container en Download. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | Continu | 8, 11 | 25 juni 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | In deze versie is de component Lijst met inhoudsfragmenten geïntroduceerd | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | Continu | 8, 11 | 7 mei 2019 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Deze release was vooral bedoeld voor verfijningen in de componentbibliotheek, maar bevat ook enkele functieverbeteringen voor de scheidingscomponent | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | Continu | 8 | 14 maart 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Deze versie was gericht op de componentenbibliotheek en introduceerde de nieuwe separatorcomponent, maar bevat ook enkele eigenschapverhogingen voor de Component van het Beeld | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 11 februari 2019 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Deze release was vooral gericht op foutoplossingen, maar bevat ook enkele functieverbeteringen voor de Carousel-component | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 27 november 2018 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Er zijn tabs en carrouselcomponenten geïntroduceerd, verbeteringen in de afbeelding, pagina en titelcomponenten en verbeterde tekstspatiëring | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 16 oktober 2018 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Teaser Component geïntroduceerd, Image Component-verbeteringen en talrijke opgeloste problemen | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 13 juli 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Bugfix-release | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 12 juni 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Extra verbeteringen onder de wasdom, foutoplossingen en kleine verbeteringen, waaronder ondersteuning voor het spiegelen van afbeeldingen. | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 11 april 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Meestal verbeteringen onder de wasdom, foutoplossingen en enkele kleine verbeteringen in de componenten van het fragment Afbeelding, Pagina en Inhoud | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 7 maart 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Navigatie, Taalnavigatie en Snel zoeken geïntroduceerde componenten. Stijlsysteem geïmplementeerd voor alle componenten. | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 16 januari 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Implementatie van JSON-export op alle componenten, introductie van de component Content Fragment | 6.3.1.0 | 6.4.0.0+ | - | - | 8 | 10 oktober 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Verschillende correcties voor de component Image | 6.3.0.0+ | 6.4.0.0+ | - | - | 8 | 4 augustus 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Oplossingen voor pagina-component, afbeeldingscomponent, diverse algemene correcties en verbeteringen | 6.3.0.0+ | 6.4.0.0+ | - | - | 8 | 26 april 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Oplossingen voor geanimeerde GIF-afbeeldingen in de afbeeldingscomponent | 6.3.0.0+ | 6.4.0.0+ | - | - | 7 | 22 maart 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Eerste release van Core Components | 6.3.0.0+ | 6.4.0.0+ | - | - | 7 | 20 maart 2017 |

>[!NOTE]
>
>Net als bij AEM raadt Adobe ontwikkelaars aan de [nieuwste versie en versies van de beschikbare kerncomponenten](https://github.com/adobe/aem-core-wcm-components/releases/latest) te gebruiken die compatibel zijn met de versie van AEM die ze uitvoeren, zodat ze kunnen profiteren van de meest actuele oplossingen en functies.

### Componentversies en -releases {#component-versions-and-releases}

De volgende lijst specificeert welke versies van welke componenten bevat zijn waarin versies van de Componenten van de Kern.

|  | Release 1.0.0 - 1.0.6 | Release 1.1.0 | Release 2.0.0 - 2.0.8 | Release 2.1.0 | Release 2.2.0-2.2.0 | Release 2.3.0-2.3.2 | Release 2.4.0 | Release 2.5.0 | Release 2.6.0 | Release 2.7.0+ |
|---|---|---|---|---|---|---|---|---|---|---|
| **[Pagina](components/page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Titel](components/title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Afbeelding](components/image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Lijst](components/list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Broodkruimel](components/breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Delen van sociale media](components/sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Formuliercontainer](components/forms/form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formuliertekst](components/forms/form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulieropties](components/forms/form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulier verborgen](components/forms/form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulierknop](components/forms/form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Inhoudsfragment](components/content-fragment-component.md)** |  | Sandbox | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Navigatie](components/navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Taalnavigatie](components/language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Snel zoeken](components/quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Teaser](components/teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Tabs](components/tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Carousel](components/carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Scheidingsteken](components/separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[Lijst met inhoudsfragmenten](components/content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Accordeon](components/accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Knop](components/button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Container](components/container.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Downloaden](components/download.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[Ervaar fragment](components/experience-fragment.md)** |  |  |  |  |  |  |  |  | v1 | v1 |
| **[Insluiten](components/embed.md)** |  |  |  |  |  |  |  |  |  | v1 |

## Documentatie {#documentation}

[Het ontwerpen met de Componenten](get-started/authoring.md) van de Kern beschrijft het gebruik van de kerncomponenten en de eigenschappen die aan inhoudauteurs en malplaatjeauteurs worden blootgesteld. Elke component wordt in detail gedocumenteerd.

[Componentbibliotheek](https://adobe.com/go/aem_cmp_library) is een voorbeeld van de huidige versie van de meeste Core Components, waarmee u kunt zien hoe deze kunnen worden gebruikt.

[Het ontwikkelen van de Componenten](developing/overview.md) van de Kern beschrijft de technische mogelijkheden van de Componenten van de Kern, hoe te om hen in uw projecten te gebruiken, hoe te, en beste praktijken aan te passen.

[De Inleiding](introduction.md) van de Componenten van de kern geeft een overzicht van de verenigbaarheid van de Componenten van de Kern over versies, gebruiksgevallen, en steun.

[De WKND-zelfstudie](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) is een geweldige stap voor stap voor het ontwikkelen van AEM, inclusief het gebruik van de Core Components.
