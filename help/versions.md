---
title: Core Components-versies
description: De Componenten van de kern worden gepubliceerd als versies die meer dan één versie van de zelfde kerncomponenten kunnen bevatten. In dit document wordt uitgelegd welke versies en versies beschikbaar zijn en hoe u de compatibiliteit met Core Components en AEM begrijpt.
role: Architect, Developer, Admin, User
exl-id: 7d4dbe46-4013-4217-b815-cdb1462072c6
source-git-commit: 6fd0fd045846da0d8e6f9c4753d172a9af101ba2
workflow-type: tm+mt
source-wordcount: '2780'
ht-degree: 12%

---

# Core Components-versies {#core-components-versions}

De huidige versie van de Core Components is 2.20.6 en is compatibel met [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html) en [AEM op locatie](https://experienceleague.adobe.com/docs/experience-manager-65/user-guide/home.html) installaties.

## Historie en compatibiliteit vrijgeven {#release-history-and-compatibility}

De Core Components zijn ontworpen om flexibel te zijn en compatibel met alle ondersteunde AEM versies. Daarom kan een versie van de componenten meerdere versies van dezelfde component bevatten.

De volgende lijsten illustreren de verenigbaarheid van de versies van de Componenten van de Kern samen welke componentenversies bevat zijn waarin versies.

### Historie en vereisten vrijgeven {#release-history-requirements}

De volgende tabel, waarvan de inhoud [beschikbaar op GitHub met volledige versiedetails](https://github.com/adobe/aem-core-wcm-components/releases), geeft een overzicht van de versies van de Core Components en hun verenigbaarheid met AEM versies en versies van Java.

| Geen | Beschrijving | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service | Java | Releasedatum |
|---|---|---|---|---|---|---|
| [2.21.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.21.2) | Dit is een patchrelease die een probleem met v1 en v2 verhelpt [Taser-componenten.](/help/components/teaser.md) | - | 6.5.13.0+ * | Continu | 8, 11 | 12 september 2022 |
| [2.21.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.21.0) | Deze release bevat een aantal verbeteringen, waaronder publicatie van de LinkHandler-API, verbeteringen voor de [Afbeeldingscomponent](/help/components/image.md) en [Gegevenslaag,](/help/developing/data-layer/overview.md) en verbeteringen aan componenten met meerdere deelvensters. | - | 6.5.13.0+ * | Continu | 8, 11 | 12 september 2022 |
| [2.20.8.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.8) | Deze release verhelpt een probleem met de levering van SVG-afbeeldingen via AdaptiveImageServlet. | - | 6.5.13.0+ * | Continu | 8, 11 | 4 augustus 2022 |
| [2.20.6.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.6) | Deze patchrelease verhelpt een probleem met de nieuwe [Component Inhoudsopgave.](/help/components/tableofcontents.md) | - | 6.5.13.0+ * | Continu | 8, 11 | 7 juli 2022 |
| [2.20.4.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.4) | Deze patchrelease verhelpt een probleem met de nieuwe [Component Inhoudsopgave.](/help/components/tableofcontents.md) | - | 6.5.13.0+ * | Continu | 8, 11 | 29 juni 2022 |
| [2.20.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.2) | Dit is een patchrelease die een probleem in de nieuwe AEMaaCS verhelpt [voor het web geoptimaliseerde service voor het leveren van bedrijfsmiddelen.](/help/developing/web-optimized-image-delivery.md) | - | 6.5.13.0+ * | Continu | 8, 11 | 20 juni 2022 |
| [2.20.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.0) | Deze release voegt een nieuwe versie toe [Component Inhoudsopgave](/help/components/tableofcontents.md), voegt ondersteuning voor AEMaaCS toe [voor internet geoptimaliseerde service voor de levering van bedrijfsmiddelen;](/help/developing/web-optimized-image-delivery.md) en bevat foutoplossingen. | - | 6.5.13.0+ * | Continu | 8, 11 | 9 juni 2022 |
| [2.19.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.19.0) | Deze versie voegt een nieuwe versie toe aan de [Zoekcomponent](/help/components/quick-search.md) en functies voor de [Component Button](/help/components/button.md) en veel verbeteringen op gebied van toegankelijkheid en foutoplossingen. | - | 6.5.10.0+ * | Continu | 8, 11 | 7 april 2022 |
| [2.18.8.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.8) | Deze release verhelpt een probleem met AEMaaCS. | - | 6.5.10.0+ * | Continu | 8, 11 | 17 maart 2022 |
| [2.18.6.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.6) | Dit is een patchrelease. | - | 6.5.10.0+ * | Continu | 8, 11 | 3 maart 2022 |
| [2.18.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.0) | Deze belangrijke versie van de kerncomponenten ziet de introductie van een nieuwe verbindingsmanager over nieuwe versies van veelvoudige componenten samen met vele toegankelijkheidsverbeteringen en insectenmoeilijke situaties. | - | 6.5.10.0+ * | Continu | 8, 11 | 16 februari 2022 |
| [2.17.14.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.12) | Dit is een patchrelease. | 6.4.8.4+ * | 6.5.6.0+ * | Continu | 8, 11 | 13 december 2021 |
| [2.17.12.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.12) | Dit is een patchrelease die een regressie verhelpt die bij de vorige release werd geïntroduceerd. | 6.4.8.4+ * | 6.5.6.0+ * | Continu | 8, 11 | 1 oktober 2021 |
| [2.17.10.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.10) | Deze patch verbetert de [Lijst](/help/components/list.md) en [Navigatie](/help/components/navigation.md) componenten om de externe URL voor omleidingsdoelen weer te geven, schakelt paginaafbeeldingsovererving in voor de komende v2 van de [Teaser](/help/components/teaser.md) en bevat aanvullende opgeloste problemen. | 6.4.8.4+ * | 6.5.6.0+ * | Continu | 8, 11 | 31 augustus 2021 |
| [2.17.8.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.8) | Deze flardversie Dit is een flardversie om een achterwaartse onverenigbare verandering te bevestigen die eerder werd geïntroduceerd. | 6.4.8.4+ * | 6.5.6.0+ * | Continu | 8, 11 | 2 augustus 2021 |
| [2.17.6.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.6) | Deze patchrelease biedt ondersteuning voor site maps voor pagina&#39;s en bevat verschillende toegankelijkheidsverbeteringen. | 6.4.8.4+ * | 6.5.6.0+ * | Continu | 8, 11 | 29 juli 2021 |
| [2.17.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.2) | Deze patchrelease bevat een oplossing voor de [Gegevenslaag](/help/developing/data-layer/overview.md) werkt niet met AEMaaCS. | 6.4.8.4+ * | 6.5.6.0+ * | Continu | 8, 11 | 8 juli 2021 |
| [2.17.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.0) | Deze release bevat technische voorvertoningen van veel nieuwe componentversies die ondersteuning bieden voor functies van de koppelingsafhandeling en een technische voorvertoning van een functie voor aanbevolen afbeeldingen voor de [Paginacomponent.](/help/components/page.md) Verschillende opgeloste problemen zijn ook opgenomen. | 6.4.8.4+ * | 6.5.6.0+ * | Continu | 8, 11 | 16 juni 2021 |
| [2.16.4.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.4) | Dit is een flardversie om een kwestie met de nieuwe manager van de Verbinding te bevestigen. | 6.4.8.1+ * | 6.5.5.0+ * | Continu | 8, 11 | 19 mei 2021 |
| [2.16.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.2) | Dit was een patchrelease die voornamelijk een probleem verhelpt met de nieuwe koppelingshandler en een uitbreiding toevoegde ter ondersteuning van toepassingen met meerdere pagina&#39;s voor [PWA.](/help/components/page.md#pwa-support) | 6.4.8.1+ * | 6.5.5.0+ * | Continu | 8, 11 | 15 mei 2021 |
| [2.16.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.0) | Deze versie concentreerde zich op toegankelijkheidsverbeteringen en introduceerde een nieuwe Handler van de Verbinding aan bestaande componenten. | 6.4.8.1+ * | 6.5.5.0+ * | Continu | 8, 11 | 22 april 2021 |
| [2.15.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.2) | Dit was een patchrelease die voornamelijk problemen verholpen met [Gegevenslaag](/help/developing/data-layer/overview.md) achterwaartse compatibiliteit en IT-tests mislukken in bepaalde situaties. | 6.4.8.1+ * | 6.5.5.0+ * | Continu | 8, 11 | 16 maart 2021 |
| [2.15.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.0) | Deze release bevat ondersteuning voor [progressieve web-apps (PWA) in de paginacomponent](/help/components/page.md#pwa-support) en ondersteunt versie 2.0.0 van de [Gegevenslaag Adobe.](/help/developing/data-layer/overview.md) | 6.4.8.1+ * | 6.5.5.0+ * | Continu | 8, 11 | 23 februari 2021 |
| [2.14.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.14.0) | Deze release bevat nieuwe opties voor de [Component insluiten](/help/components/embed.md) en introduceert de Brand Slug in de [page](/help/components/page.md) en veel kwesties aan te pakken. | 6.4.8.1+ * | 6.5.5.0+ * | Continu | 8, 11 | 9 februari 2021 |
| [2.13.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.2) | Dit was een flardversie richtend een kwestie met RTE wanneer gebruikt op AEMaaCS | 6.4.8.1+ * | 6.5.5.0+ * | Continu | 8, 11 | 16 december 2020 |
| [2.13.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.0) | Deze release bevat nieuwe Dynamic Media-functies voor de [Afbeeldingscomponent.](/help/components/image.md) | 6.4.8.1+ * | 6.5.5.0+ * | Continu | 8, 11 | 4 december 2020 |
| [2.12.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.2) | Dit was een patchrelease voor 2.12.0 inclusief kleine correcties. | 6.4.8.1+ * | 6.5.5.0+ * | Continu | 8, 11 | 11 november 2020 |
| [2.12.1.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.1) | Dit was een flardversie voor 2.12.0 die een belangrijke insect in [Afbeeldingscomponent.](/help/components/image.md) | 6.4.8.1+ * | 6.5.5.0+ * | Continu | 8, 11 | 5 november 2020 |
| [2.12.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.0) | Deze release is geïntroduceerd [een nieuwe POST-formulierhandler;](/help/components/forms/form-container.md#post-data) de mogelijkheid om aangepaste CSS, JavaScript en metagegevens op te nemen [tags via contextbewuste configuratie;](/help/developing/including-clientlibs.md#context-aware-loading) en `DataLayerBuilder` nut aan [vereenvoudigt de integratie van gegevenslagen in aangepaste componenten.](/help/developing/data-layer/integrations.md#enabling-custom-components) | 6.4.8.1+ * | 6.5.5.0+ * | Continu | 8, 11 | 29 oktober 2020 |
| [2.11.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | Deze release is geïntroduceerd [Ondersteuning voor AMP.](/help/developing/amp.md) | 6.4.8.1+ * | 6.5.5.0+ * | Continu | 8, 11 | 20 juli 2020 |
| [2.10.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | Deze release introduceert de [PDF Viewer-component.](/help/components/pdf-viewer.md) | 6.4.8.1+ | 6.5.5.0+ | Continu | 8, 11 | 17 juni 2020 |
| [2.9.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | Deze release maakt integratie met de [Gegevenslaag Adobe-client](/help/developing/data-layer/overview.md) en de [component ProgressBar.](/help/components/progress-bar.md) | 6.4.8.0+ | 6.5.4.0+ | Continu | 8, 11 | 29 mei 2020 |
| [2.8.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Deze release was gericht op oplossingen met kleine verbeteringen. | 6.4.4.0+ | 6.5.0.0+ | Continu | 8, 11 | 5 december 2019 |
| [2.7.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | Deze release introduceert de nieuwe versie [Component insluiten.](/help/components/embed.md) | 6.4.4.0+ | 6.5.0.0+ | Continu | 8, 11 | 25 september 2019 |
| [2.6.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Deze release introduceert de nieuwe versie [Ervaar de fragmentcomponent.](/help/components/experience-fragment.md) | 6.4.4.0+ | 6.5.0.0+ | Continu | 8, 11 | 6 september 2019 |
| [2.5.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Deze release introduceert de nieuwe versie [Accordeon](/help/components/accordion.md) [Button,](/help/components/button.md) [Container](/help/components/container.md) en [Download componenten.](/help/components/download.md) | 6.4.2.0+ | 6.5.0.0+ | Continu | 8, 11 | 25 juni 2019 |
| [2.4.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Deze release introduceert de [Component lijst met inhoudsfragmenten.](/help/components/content-fragment-list.md) | 6.4.2.0+ | 6.5.0.0+ | Continu | 8, 11 | 7 mei 2019 |
| [2.3.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Deze release was gericht op verfijningen van de [Componentbibliotheek,](https://aemcomponents.dev) maar bevat ook enkele functieverbeteringen voor de [Scheidingscomponent.](/help/components/separator.md) | 6.4.2.0+ | 6.5.0.0+ | Continu | 8 | 14 maart 2019 |
| [2.3.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Deze release was gericht op de [Componentbibliotheek](https://aemcomponents.dev) en de invoering van de nieuwe [Scheidingscomponent](/help/components/separator.md) maar bevat ook enkele functieverbeteringen voor de [Afbeeldingscomponent.](/help/components/image.md) | 6.4.2.0+ | - | - | 8 | 11 februari 2019 |
| [2.2.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Deze release was vooral gericht op foutoplossingen, maar bevat ook enkele functieverbeteringen voor de [Carousel-component.](/help/components/carousel.md) | 6.4.2.0+ | - | - | 8 | 27 november 2018 |
| [2.2.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Deze release introduceert de [Component Tabs](/help/components/tabs.md) en de [Carousel-component](/help/components/carousel.md) alsmede verbeteringen van de [Afbeeldingscomponent,](/help/components/image.md) [Paginacomponent,](/help/components/page.md) en [Component Title](/help/components/title.md) en verbeterde tekstspatiëring. | 6.4.2.0+ | - | - | 8 | 16 oktober 2018 |
| [2.1.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Deze release introduceert de [Teaser-component](/help/components/teaser.md) samen met verbeteringen van de [Afbeeldingscomponent](/help/components/image.md) en een groot aantal opgeloste problemen. | 6.4.2.0+ | - | - | 8 | 13 juli 2018 |
| [2.0.8.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Dit was een foutopsporingsversie. | 6.4.0.0+ | - | - | 8 | 12 juni 2018 |
| [2.0.6.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | In deze release zijn verbeteringen aangebracht die onder de wasdom stonden, oplossingen voor problemen en kleine verbeteringen, waaronder ondersteuning voor het omdraaien van afbeeldingen in de [Afbeeldingscomponent.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 11 april 2018 |
| [2.0.4.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Deze release was vooral gericht op verbeteringen onder de wasdom, foutoplossingen en enkele kleine verbeteringen in de [Afbeeldingscomponent,](/help/components/image.md) [Paginacomponent,](/help/components/page.md) en [Component Inhoudsfragment.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 7 maart 2018 |
| [2.0.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Deze release introduceert de [Navigatiecomponent,](/help/components/navigation.md) [Taalnavigatiecomponent,](/help/components/language-navigation.md) en de [Component Snel zoeken](/help/components/quick-search.md) en de [Stijlsysteem](/help/get-started/authoring.md#component-styling) voor alle componenten. | 6.4.0.0+ | - | - | 8 | 16 januari 2018 |
| [1.1.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Deze release implementeert JSON-export op alle componenten en introduceert de [Component Inhoudsfragment.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 10 oktober 2017 |
| [1.0.6.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | In deze release zijn verschillende oplossingen toegevoegd voor de [Afbeeldingscomponent.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 4 augustus 2017 |
| [1.0.4.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Deze release voegt oplossingen toe voor de [Paginacomponent,](/help/components/page.md) [Afbeeldingscomponent,](/help/components/image.md) en diverse mondiale oplossingen en verbeteringen. | 6.4.0.0+ | - | - | 8 | 26 april 2017 |
| [1.0.2.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | In deze release worden correcties toegevoegd voor afbeeldingen van geanimeerde GIFFEN in [Afbeeldingscomponent.](/help/components/image.md) | 6.4.0.0+ | - | - | 7 | 22 maart 2017 |
| [1.0.0.](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Eerste release van Core Components. | 6.4.0.0+ | - | - | 7 | 20 maart 2017 |

>[!NOTE]
>
>(*) Sinds versie 2.11.0, `org.apache.sling.models.impl` versie 1.4.12 of hoger is vereist (vanwege [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). Dit zal voor AEM 6.4 en 6.5 in een toekomstig Service Pack worden verstrekt. Tot die tijd is de bundel Sling Models opgenomen in de `core.wcm.components.all` pakket.

>[!TIP]
>
>Net als bij AEM raadt Adobe ontwikkelaars aan de [nieuwste versie en versies van de Core Components](https://github.com/adobe/aem-core-wcm-components/releases/latest) beschikbaar is die compatibel is met de versie van AEM die zij in werking stellen om van de meest bijgewerkte moeilijke situaties en de eigenschappen te profiteren.

### Componentversies en -releases {#component-versions-and-releases}

De volgende lijst specificeert welke versies van welke componenten bevat zijn waarin versies van de Componenten van de Kern.

|  | Release 1.0.0 - 1.0.6 | Release 1.1.0 | Release 2.0.0 - 2.0.8 | Release 2.1.0 | Release 2.2.0-2.2.0 | Release 2.3.0-2.3.2 | Release 2.4.0 | Release 2.5.0 | Release 2.6.0 | Release 2.7.0-2.8.0 | Release 2.9.0-2.17.14 | Release 2.18.0 | Release 2.19.0 | Release 2.20.0+ |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **[Pagina](components/page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Titel](components/title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Afbeelding](components/image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Lijst](components/list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Broodkruimel](components/breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Delen van sociale media](components/sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, afgekeurd | v1, afgekeurd | v1, afgekeurd |
| **[Formuliercontainer](components/forms/form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formuliertekst](components/forms/form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulieropties](components/forms/form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulier verborgen](components/forms/form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Formulierknop](components/forms/form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Inhoudsfragment](components/content-fragment-component.md)** |  | Sandbox | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Navigatie](components/navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Taalnavigatie](components/language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Snel zoeken](components/quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 |
| **[Teaser](components/teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Tabs](components/tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Carousel](components/carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Scheidingsteken](components/separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Lijst met inhoudsfragmenten](components/content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Accordeon](components/accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Knop](components/button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Container](components/container.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Downloaden](components/download.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Ervaar fragment](components/experience-fragment.md)** |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Insluiten](components/embed.md)** |  |  |  |  |  |  |  |  |  | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Voortgangsbalk](components/progress-bar.md)** |  |  |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[PDF Viewer](components/pdf-viewer.md)** |  |  |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[Inhoudsopgave](components/tableofcontents.md)** |  |  |  |  |  |  |  |  |  |  |  |  |  | v1 |

## Versies en releases {#versions-and-releases}

De Componenten van de kern worden verdeeld via GitHub. Hierdoor kan Adobe sneller functionaliteit toevoegen aan de componenten en kan ook gemeenschapsinvoer buiten de AEM releasecyclus plaatsvinden.

De Core Components worden beschikbaar gesteld met bepaalde AEM versies waarmee zij compatibel zijn. Dit betekent dat één AEM versie meerdere versies of versies van de Componenten van de Kern kan steunen.

### Versies {#versions}

De belangrijkste iteratie van de Core Components is de **versies**. Elke component heeft een versie. Versies worden aangeduid met **v** toegevoegd met een positief geheel getal dat niet gelijk is aan nul, zoals v1 en v2. Versies worden alleen verhoogd voor wijzigingen die niet compatibel zijn met oudere versies, wat normaal gesproken het geval is bij de introductie van nieuwe functies en functionaliteit.

De ontwikkelaars en de beheerders kunnen versies van de kerncomponenten door een aantal in hun middeltypepaden, en in volledig gekwalificeerde de klassennamen van Java van hun implementaties erkennen. Dit versienummer vertegenwoordigt een hoofdversie zoals gedefinieerd door [semantische versierichtlijnen](https://semver.org/).

Voor meer informatie over kerncomponentenversies, zie [ontwikkelaarsdocumentatie van de Core Components](developing/guidelines.md).

### Uitstoot {#releases}

De kerncomponenten worden beschikbaar gesteld via **lozingen** en [vertegenwoordigen de feitelijke gepubliceerde artefacten die beschikbaar zijn op GitHu.](https://github.com/adobe/aem-core-wcm-components/releases) De versies worden aangeduid met een decimaal aantal van het formaat `X.Y.Z` en verzamel alle kerncomponenten samen als een te leveren pakket.

* **Grote introducties** introduceer volledig nieuwe componenten, verbeteringen aan bestaande versie van componenten, evenals standaardinsectenmoeilijke situaties. Dit wordt vertegenwoordigd door een toename in de `X` component van het releasenummer.
* **Kleine introducties** introduceer nieuwe componenten, nieuwe functionaliteit aan bestaande versies van componenten, evenals insectenmoeilijke situaties. Dit wordt vertegenwoordigd door een toename in de `Y` component van het releasenummer.
* **Patchreleases** bevat alleen opgeloste problemen. Dit wordt vertegenwoordigd door een toename in de `Z` component van het releasenummer.

>[!NOTE]
>
>De versies kunnen veelvoudige versies van de zelfde component bevatten.
>
>Dezelfde versie van een component kan in meerdere releases worden weergegeven.

## Ondersteuning voor kerncomponenten {#core-components-support}

De Componenten van de kern zijn een integraal deel van AEM en worden gesteund onder de zelfde voorwaarden alsof zij als deel van QuickStart werden geleverd.

Net als andere productkenmerken is de algemene regel van het einde van de levensduur:

* Componenten worden eerst aangekondigd te worden vervangen voordat ze worden verwijderd
* Op zijn vroegst worden ze na de aankondiging uit de AEM gehaald.

Dit geeft klanten minstens één versiecyclus om naar de nieuwe versie van de component te bewegen, alvorens steun beëindigt.

In de versie van elke component worden duidelijk de AEM versies vermeld die worden ondersteund. Wanneer de steun voor een versie van AEM beëindigt, dan ook de steun van de Componenten van de Kern voor die versie van AEM.

Raadpleeg voor meer informatie over de ondersteuning van componentaanpassingen de [Kerncomponenten aanpassen](developing/customizing.md) pagina van de relevante versie van de Componenten van de Kern.

## Ondersteuning van stichtingscomponenten {#foundation-component-support}

De nadruk op Adobe is verschoven naar de kerncomponenten en er worden nieuwe functies toegevoegd.

[Bijna zijn alle Componenten van de Stichting verouderd met AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/siteandpage/default-components-foundation.html) en slechts zullen de belangrijkste insectenmoeilijke situaties voor de Componenten van de Stichting in overweging worden genomen die verder gaan.
