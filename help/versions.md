---
title: Versies van kerncomponenten
description: De Componenten van de kern worden gepubliceerd als versies die meer dan één versie van de zelfde kerncomponenten kunnen bevatten. In dit document wordt uitgelegd welke versies en versies worden uitgebracht en hoe u de compatibiliteit met Core Components en AEM begrijpt.
role: Architect, Developer, Admin, User
exl-id: 7d4dbe46-4013-4217-b815-cdb1462072c6
source-git-commit: 821530ce1958566f0a2c1fb88c5017572057f88f
workflow-type: tm+mt
source-wordcount: '3056'
ht-degree: 0%

---

# Versies van kerncomponenten {#core-components-versions}

De Componenten van de Kern zijn compatibel met [ AEM as a Cloud Service ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=nl-NL) en [ op-gebouwAEM ](https://experienceleague.adobe.com/docs/experience-manager-65/user-guide/home.html?lang=nl-NL) installaties.

## Historie en compatibiliteit vrijgeven {#release-history-and-compatibility}

De Core Components zijn ontworpen om flexibel te zijn en compatibel met alle ondersteunde AEM-versies. Daarom kan een versie van de componenten meerdere versies van dezelfde component bevatten.

De volgende lijsten illustreren de verenigbaarheid van de versies van de Componenten van de Kern samen welke componentenversies bevat zijn waarin versies.

### Historie en vereisten vrijgeven {#release-history-requirements}

De volgende lijst, waarvan de inhoud [ op GitHub met volledige versiedetails ](https://github.com/adobe/aem-core-wcm-components/releases) beschikbaar is, geeft een overzicht van de versies van de Componenten van de Kern en hun verenigbaarheid met de versies van AEM en van Java.

| Geen | Beschrijving | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service | Java | Releasedatum |
|---|---|---|---|---|---|---|---|
| [ 2.29.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.29.0) | In deze release werd ondersteuning toegevoegd voor het ontwerpen van voorvertoningsversies van elementen in de kerncomponent van sites en worden talrijke opgeloste problemen opgelost. | - | 6.5.21.0+ | 6,5 LTS GA | Continu | 8, 11 | 21 april 2025 |
| [ 2.28.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.28.0) | Deze versie is bedoeld voor een groot aantal opgeloste problemen. | - | 6.5.21.0+ | 6,5 LTS GA | Continu | 8, 11 | 17 maart 2025 |
| [ 2.27.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.27.0) | Deze versie is bedoeld voor een groot aantal opgeloste problemen. | - | 6.5.21.0+ | - | Continu | 11 | 10 september 2024 |
| [ 2.26.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.26.0) | Deze versie is bedoeld voor een groot aantal opgeloste problemen. | - | 6.5.21.0+ | - | Continu | 11 | 31 juli 2024 |
| [ 2.25.4 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.25.4) | Dit is een kleine release die enkele IT-fouten corrigeert. | - | 6.5.21.0+ | - | Continu | 8, 11 | 10 mei 2024 |
| [ 2.25.2 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.25.2) | Dit is een kleine release die enkele IT-fouten corrigeert. | - | 6.5.21.0+ | - | Continu | 8, 11 | 9 mei 2024 |
| [ 2.25.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.25.0) | Met deze release wordt ondersteuning toegevoegd voor benoemde smartcrop in Dynamic Media, inclusief verbetering van prestaties en toegankelijkheid en verschillende opgeloste problemen. | - | 6.5.21.0+ | - | Continu | 8, 11 | 2 mei 2024 |
| [ 2.24.6 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.24.6) | Deze patchrelease bevat verbeteringen voor de initialisatie van de datalaag. | - | 6.5.21.0+ | - | Continu | 8, 11 | 22 april 2024 |
| [ 2.24.4 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.24.4) | Met deze patchrelease wordt een initialisatie van het verkoopmodel opgelost. | - | 6.5.21.0+ | - | Continu | 8, 11 | 1 april 2024 |
| [ 2.24.2 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.24.2) | Deze pleisterafgifte verbetert de stabiliteit van integratietests. | - | 6.5.21.0+ | - | Continu | 8, 11 | 22 februari 2024 |
| [ 2.24.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.24.0) | Deze release biedt extra ondersteuning voor de gegevenslaag van Google Tag Manager en bevat verschillende oplossingen voor problemen. | - | 6.5.21.0+ | - | Continu | 8, 11 | 14 februari 2024 |
| [ 2.23.4 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.23.4) | Deze patchrelease bevatte verschillende foutoplossingen. | - | 6.5.17.0+ | - | Continu | 8, 11 | 15 september 2023 |
| [ 2.23.2 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.23.2) | Dit flard voegde Dynamische Slimme uitsnijding van Media voor verre activa aan het [ Beeld ](/help/components/image.md) toe en [ Componenten van het Taser ](/help/components/teaser.md) en bevond een aantal insecten. | - | 6.5.17.0+ | - | Continu | 8, 11 | 4 augustus 2023 |
| [ 2.23.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.23.0) | Deze versie voegde steun voor [ Dynamische de verre activa van Media van de Volgende Generatie toe.](/help/developing/remote-assets.md) | - | 6.5.17.0+ | - | Continu | 8, 11 | 6 juni 2023 |
| [ 2.22.12 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.12) | Deze patchrelease verhelpt twee problemen. | - | 6.5.14.0+ | - | Continu | 8, 11 | 25 mei 2023 |
| [ 2.22.10 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.10) | Deze patchrelease verhelpt twee regressies. | - | 6.5.14.0+ | - | Continu | 8, 11 | 11 mei 2023 |
| [ 2.22.8 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.8) | Deze patchrelease biedt functies die per ongeluk zijn verwijderd uit de vorige release. | - | 6.5.14.0+ | - | Continu | 8, 11 | 9 mei 2023 |
| [ 2.22.6 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.6) | Deze flardversie bevestigt een regressie in de [ Component van de Container.](/help/components/container.md) | - | 6.5.14.0+ | - | Continu | 8, 11 | 21 april 2023 |
| [ 2.22.4 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.4) | Dit is een flardversie om een kwesties in de [ Component van de Lijst van het Fragment van de Inhoud te bevestigen.](/help/components/content-fragment-list.md) | - | 6.5.14.0+ | - | Continu | 8, 11 | 5 april 2023 |
| [ 2.22.2 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.2) | Dit is een onderhoudsrelease om twee problemen op te lossen die zijn geïntroduceerd in 2.2.0 | - | 6.5.14.0+ | - | Continu | 8, 11 | 31 maart 2023 |
| [ 2.22.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.0) | Deze versie introduceert een nieuwe versie van de [ Component van de Lijst ](/help/components/list.md) samen met verbeteringen aan [ Taser ](/help/components/teaser.md) en update van de [ Kijker van PDF ](/help/components/pdf-viewer.md) en [ Carousel ](/help/components/carousel.md) | - | 6.5.14.0+ | - | Continu | 8, 11 | 9 februari 2023 |
| [ 2.21.2 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.21.2) | Dit is een flardversie die een kwestie met v1 en v2 [ de Componenten van het Taser bevestigen.](/help/components/teaser.md) | - | 6.5.13.0+ | - | Continu | 8, 11 | 12 september 2022 |
| [ 2.21.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.21.0) | Deze versie omvat een aantal verhogingen met inbegrip van publicatie van LinkHandler API, verbeteringen aan de [ Component van het Beeld ](/help/components/image.md) en [ Laag van Gegevens, ](/help/developing/data-layer/overview.md) evenals verbeteringen aan multi-paneelcomponenten. | - | 6.5.13.0+ | - | Continu | 8, 11 | 12 september 2022 |
| [ 2.20.8 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.8) | Deze release verhelpt een probleem met de levering van SVG-afbeeldingen via AdaptiveImageServer. | - | 6.5.13.0+ | - | Continu | 8, 11 | 4 augustus 2022 |
| [ 2.20.6 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.6) | Deze flardversie lost een kwestie met de nieuwe [ Component van de Inhoudslijst op.](/help/components/tableofcontents.md) | - | 6.5.13.0+ | - | Continu | 8, 11 | 7 juli 2022 |
| [ 2.20.4 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.4) | Deze flardversie lost een kwestie met de nieuwe [ Component van de Inhoudslijst op.](/help/components/tableofcontents.md) | - | 6.5.13.0+ | - | Continu | 8, 11 | 29 juni 2022 |
| [ 2.20.2 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.2) | Dit is een flardversie die een kwestie in de nieuwe AEMaaCS [ Web-geoptimaliseerde dienst van de activalevering bevestigt.](/help/developing/web-optimized-image-delivery.md) | - | 6.5.13.0+ | - | Continu | 8, 11 | 20 juni 2022 |
| [ 2.20.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.0) | Deze versie voegt een nieuwe [ Component van de Inhoudsopgave ](/help/components/tableofcontents.md) toe, voegt steun voor de [ Web-geoptimaliseerde dienst van de activalevering AEMaaCS, ](/help/developing/web-optimized-image-delivery.md) toe en omvat insectenmoeilijke situaties. | - | 6.5.13.0+ | - | Continu | 8, 11 | 9 juni 2022 |
| [ 2.19.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.19.0) | Deze versie voegt een nieuwe versie aan de [ Component van het Onderzoek ](/help/components/quick-search.md) en eigenschappen aan de [ Component van de Knoop ](/help/components/button.md) evenals vele toegankelijkheidsverbeteringen en insectenmoeilijke situaties toe. | - | 6.5.10.0+ | - | Continu | 8, 11 | 7 april 2022 |
| [ 2.18.8 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.8) | Deze release verhelpt een probleem met AEMaaCS. | - | 6.5.10.0+ | - | Continu | 8, 11 | 17 maart 2022 |
| [ 2.18.6 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.6) | Dit is een patchrelease. | - | 6.5.10.0+ | - | Continu | 8, 11 | 3 maart 2022 |
| [ 2.18.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.0) | Deze belangrijke versie van de kerncomponenten ziet de introductie van een nieuwe verbindingsmanager over nieuwe versies van veelvoudige componenten samen met vele toegankelijkheidsverbeteringen en insectenmoeilijke situaties. | - | 6.5.10.0+ * | - | Continu | 8, 11 | 16 februari 2022 |
| [ 2.17.14 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.12) | Dit is een patchrelease. | 6.4.8.4+ | 6.5.6.0+ | - | Continu | 8, 11 | 13 december 2021 |
| [ 2.17.12 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.12) | Dit is een patchrelease die een regressie verhelpt die bij de vorige release werd geïntroduceerd. | 6.4.8.4+ | 6.5.6.0+ | - | Continu | 8, 11 | 1 oktober 2021 |
| [ 2.17.10 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.10) | Dit flard verbetert de [ Lijst ](/help/components/list.md) en [ de componenten van de Navigatie ](/help/components/navigation.md) om externe URL voor omleidingsdoelstellingen te tonen, laat paginabeelden overerving voor aanstaande v2 van de [ 5&rbrace; component van het Taser &lbrace;toe, en bevat extra insectenmoeilijke situaties.](/help/components/teaser.md) | 6.4.8.4+ | 6.5.6.0+ | - | Continu | 8, 11 | 31 augustus 2021 |
| [ 2.17.8 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.8) | Deze flardversie Dit is een flardversie om een achterwaartse onverenigbare verandering te bevestigen die eerder werd geïntroduceerd. | 6.4.8.4+ | 6.5.6.0+ | - | Continu | 8, 11 | 2 augustus 2021 |
| [ 2.17.6 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.6) | Deze patchrelease biedt ondersteuning voor site maps voor pagina&#39;s en bevat verschillende toegankelijkheidsverbeteringen. | 6.4.8.4+ | 6.5.6.0+ | - | Continu | 8, 11 | 29 juli 2021 |
| [ 2.17.2 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.2) | Deze flardversie omvat een moeilijke situatie voor de [ Laag van Gegevens ](/help/developing/data-layer/overview.md) het werken niet met AEMaaCS. | 6.4.8.4+ | 6.5.6.0+ | - | Continu | 8, 11 | 8 juli 2021 |
| [ 2.17.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.0) | Deze versie omvat technische voorproeven van vele nieuwe componentenversies die verbindingshandlereigenschappen evenals een technologievoorproef van een gekenmerkte beeldeigenschap voor de [ Component van de Pagina steunen.](/help/components/page.md) Verschillende opgeloste problemen zijn ook opgenomen. | 6.4.8.4+ | 6.5.6.0+ | - | Continu | 8, 11 | 16 juni 2021 |
| [ 2.16.4 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.4) | Dit is een flardversie om een kwestie met de nieuwe manager van de Verbinding te bevestigen. | 6.4.8.1+ | 6.5.5.0+ | - | Continu | 8, 11 | 19 mei 2021 |
| [ 2.16.2 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.2) | Dit was een flardversie hoofdzakelijk die een kwestie met de nieuwe manager van de Verbinding bevestigen en een verhoging toevoegde om multi-page toepassingen voor [ PWA te steunen.](/help/components/page.md#pwa-support) | 6.4.8.1+ | 6.5.5.0+ | - | Continu | 8, 11 | 15 mei 2021 |
| [ 2.16.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.0) | Deze versie concentreerde zich op toegankelijkheidsverbeteringen en introduceerde een nieuwe Handler van de Verbinding aan bestaande componenten. | 6.4.8.1+ | 6.5.5.0+ | - | Continu | 8, 11 | 22 april 2021 |
| [ 2.15.2 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.2) | Dit was een flardversie hoofdzakelijk die kwesties met [ Laag van Gegevens ](/help/developing/data-layer/overview.md) achterwaartse verenigbaarheid en de tests van IT vastzetten die in bepaalde situaties ontbreken. | 6.4.8.1+ | 6.5.5.0+ | - | Continu | 8, 11 | 16 maart 2021 |
| [ 2.15.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.0) | Deze versie omvat steun voor [ progressieve Web apps (PWA) in de Component van de Pagina ](/help/components/page.md#pwa-support) en steunt versie 2.0.0 van de [ Gegevens van Adobe Laag.](/help/developing/data-layer/overview.md) | 6.4.8.1+ | 6.5.5.0+ | - | Continu | 8, 11 | 23 februari 2021 |
| [ 2.14.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.14.0) | Deze versie omvat nieuwe opties voor [ bedt Component ](/help/components/embed.md) in en introduceert het Merk Slug op het [ pagina ](/help/components/page.md) niveau evenals het richten van vele kwesties. | 6.4.8.1+ | 6.5.5.0+ | - | Continu | 8, 11 | 9 februari 2021 |
| [ 2.13.2 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.2) | Dit was een flardversie richtend een kwestie met RTE wanneer gebruikt op AEMaaCS | 6.4.8.1+ | 6.5.5.0+ | - | Continu | 8, 11 | 16 december 2020 |
| [ 2.13.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.0) | Deze versie omvat nieuwe Dynamische eigenschappen van Media voor de [ Component van het Beeld.](/help/components/image.md) | 6.4.8.1+ | 6.5.5.0+ | - | Continu | 8, 11 | 4 december 2020 |
| [ 2.12.2 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.2) | Dit was een patchrelease voor 2.12.0 inclusief kleine correcties. | 6.4.8.1+ | 6.5.5.0+ | - | Continu | 8, 11 | 11 november 2020 |
| [ 2.12.1 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.1) | Dit was een flardversie voor 2.12.0 die een belangrijke insect in de [ Component van het Beeld bevestigt.](/help/components/image.md) | 6.4.8.1+ | 6.5.5.0+ | - | Continu | 8, 11 | 5 november 2020 |
| [ 2.12.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.0) | Deze versie introduceerde [ een nieuwe POST vormmanager;](/help/components/forms/form-container.md#post-data) de capaciteit om douane CSS, Javascript, en meta-gegevens [ markeringen via context bewuste configuratie te omvatten;](/help/developing/including-clientlibs.md#context-aware-loading) en a `DataLayerBuilder` nut om [ de integratie van de gegevenslaag in douanecomponenten te vereenvoudigen.](/help/developing/data-layer/integrations.md#enabling-custom-components) | 6.4.8.1+ | 6.5.5.0+ | - | Continu | 8, 11 | 29 oktober 2020 |
| [ 2.11.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | Deze versie introduceerde [ steun van AMP.](/help/developing/amp.md) | 6.4.8.1+ | 6.5.5.0+ | - | Continu | 8, 11 | 20 juli 2020 |
| [ 2.10.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | Deze versie introduceerde de [ component van de Kijker van PDF.](/help/components/pdf-viewer.md) | 6.4.8.1+ | 6.5.5.0+ | - | Continu | 8, 11 | 17 juni 2020 |
| [ 2.9.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | Deze versie liet integratie met de [ Gegevens van de Cliënt van Adobe ](/help/developing/data-layer/overview.md) toe en introduceerde de [ component van de Bar van de Voortgang.](/help/components/progress-bar.md) | 6.4.8.0+ | 6.5.4.0+ | - | Continu | 8, 11 | 29 mei 2020 |
| [ 2.8.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | Deze release was gericht op oplossingen met kleine verbeteringen. | 6.4.4.0+ | 6.5.0.0+ | - | Continu | 8, 11 | 5 december 2019 |
| [ 2.7.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | Deze versie introduceerde nieuwe [ bed component in.](/help/components/embed.md) | 6.4.4.0+ | 6.5.0.0+ | - | Continu | 8, 11 | 25 september 2019 |
| [ 2.6.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Deze versie introduceerde de nieuwe [ component van het Fragment van de Ervaring.](/help/components/experience-fragment.md) | 6.4.4.0+ | 6.5.0.0+ | - | Continu | 8, 11 | 6 september 2019 |
| [ 2.5.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Deze versie introduceerde nieuwe [ Accordeon, ](/help/components/accordion.md) [ Knoop, ](/help/components/button.md) [ Container, ](/help/components/container.md) en [ componenten van de Download.](/help/components/download.md) | 6.4.2.0+ | 6.5.0.0+ | - | Continu | 8, 11 | 25 juni 2019 |
| [ 2.4.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Deze versie introduceerde de [ Component van de Lijst van het Fragment van de Inhoud.](/help/components/content-fragment-list.md) | 6.4.2.0+ | 6.5.0.0+ | - | Continu | 8, 11 | 7 mei 2019 |
| [ 2.3.2 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Deze versie concentreerde zich op verfijningen aan de [ Bibliotheek van de Component, ](https://aemcomponents.dev) maar bevat ook sommige eigenschapverhogingen voor de [ Component van de Scheiding.](/help/components/separator.md) | 6.4.2.0+ | 6.5.0.0+ | - | Continu | 8 | 14 maart 2019 |
| [ 2.3.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Deze versie concentreerde zich op de [ Bibliotheek van de Component ](https://aemcomponents.dev) evenals introducerend de nieuwe [ Component van de Scheiding, ](/help/components/separator.md) maar bevat ook sommige eigenschapverhogingen voor de [ Component van het Beeld.](/help/components/image.md) | 6.4.2.0+ | - | - | - | 8 | 11 februari 2019 |
| [ 2.2.2 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Deze versie concentreerde zich hoofdzakelijk op insectenmoeilijke situaties, maar bevat ook sommige eigenschapverhogingen voor de [ Component van Carousel.](/help/components/carousel.md) | 6.4.2.0+ | - | - | - | 8 | 27 november 2018 |
| [ 2.2.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Deze versie introduceerde de [ Component van Lusjes ](/help/components/tabs.md) en de [ Component van Carousel ](/help/components/carousel.md) evenals verbeteringen aan de [ Component van het Beeld, ](/help/components/image.md) [ Component van de Pagina, ](/help/components/page.md) en [ Component van de Titel ](/help/components/title.md) en verbeterde het volgen. | 6.4.2.0+ | — |  | - | 8 | 16 oktober 2018 |
| [ 2.1.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Deze versie introduceerde de [ Component van het Taser ](/help/components/teaser.md) samen met verbeteringen aan de [ Component van het Beeld ](/help/components/image.md) en talrijke insectenmoeilijke situaties. | 6.4.2.0+ | — |  | - | 8 | 13 juli 2018 |
| [ 2.0.8 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Dit was een foutopsporingsversie. | 6.4.0.0+ | — |  | - | 8 | 12 juni 2018 |
| [ 2.0.6 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Deze versie voegde verbeteringen onder-de-zijn toe, insectenmoeilijke situaties, en kleine verbeteringen met inbegrip van steun van beeld in de [ Component van het Beeld.](/help/components/image.md) | 6.4.0.0+ | - | - | - | 8 | 11 april 2018 |
| [ 2.0.4 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Deze versie concentreerde zich hoofdzakelijk op verbeteringen onder-de-zijn, insectenmoeilijke situaties, plus sommige minder belangrijke verbeteringen aan de [ Component van het Beeld, ](/help/components/image.md) [ Component van de Pagina, ](/help/components/page.md) en [ Component van het Fragment van de Inhoud.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 7 maart 2018 |
| [ 2.0.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Deze versie introduceerde de [ Component van de Navigatie, ](/help/components/navigation.md) [ Component van de Navigatie van de Taal, ](/help/components/language-navigation.md) en de [ Snelle Component van het Onderzoek ](/help/components/quick-search.md) en voerde het [ Systeem van de Stijl ](/help/get-started/authoring.md#component-styling) voor alle componenten uit. | 6.4.0.0+ | - | - | - | 8 | 16 januari 2018 |
| [ 1.1.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Deze versie voert de uitvoer JSON op alle componenten uit en introduceert de [ Component van het Fragment van de Inhoud.](/help/components/content-fragment-component.md) | 6.4.0.0+ | — |  | - | 8 | 10 oktober 2017 |
| [ 1.0.6 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Deze versie voegt verscheidene moeilijke situaties voor de [ Component van het Beeld toe.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 4 augustus 2017 |
| [ 1.0.4 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Deze versie voegt moeilijke situaties voor de [ Component van de Pagina toe, ](/help/components/page.md) [ Component van het Beeld, ](/help/components/image.md) en diverse globale moeilijke situaties en verbeteringen. | 6.4.0.0+ | — |  | - | 8 | 26 april 2017 |
| [ 1.0.2 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Deze versie voegt moeilijke situaties voor geanimeerde beelden van GIF in [ Component van het Beeld toe.](/help/components/image.md) | 6.4.0.0+ | - | - | - | 7 | 22 maart 2017 |
| [ 1.0.0 ](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Eerste release van Core Components. | 6.4.0.0+ | - | - | - | 7 | 20 maart 2017 |

>[!TIP]
>
>Zoals met AEM, adviseert Adobe dat de ontwikkelaars de [ recentste versie en versies van de beschikbare Componenten van de Kern gebruiken ](https://github.com/adobe/aem-core-wcm-components/releases/latest) die met de versie van AEM compatibel zijn die zij lopen om van de meest bijgewerkte moeilijke situaties en de eigenschappen te profiteren.

### Componentversies en -releases {#component-versions-and-releases}

In de volgende tabel wordt aangegeven in welke versies van de Core Components de componenten zijn uitgebracht.

|  | Release 1.0.0 - 1.0.6 | Release 1.1.0 | Release 2.0.0 - 2.0.8 | Release 2.1.0 | Release 2.2.0-2.2.0 | Release 2.3.0-2.3.2 | Release 2.4.0 | Release 2.5.0 | Release 2.6.0 | Release 2.7.0-2.8.0 | Release 2.9.0-2.17.14 | Release 2.18.0 | Release 2.19.0 | Release 2.20.0-2.21.2 | Release 2.2.0+ |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **[Pagina](components/page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Titel](components/title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Beeld](components/image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Lijst](components/list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3, v4 |
| **[Breadcrumb](components/breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[Sociale Media die](components/sharing.md)** delen | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, afgekeurd | v1, afgekeurd | v1, afgekeurd | v1, afgekeurd |
| **[de Container van de Vorm](components/forms/form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Tekst van de Vorm](components/forms/form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Opties van de Vorm](components/forms/form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Verborgen Vorm](components/forms/form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Knop van de Vorm](components/forms/form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[het Fragment van de Inhoud](components/content-fragment-component.md)** |  | Sandbox | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Navigatie](components/navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Navigatie van de Taal](components/language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Snel Onderzoek](components/quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 |
| **[Taser](components/teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Lusjes](components/tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Carousel](components/carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Scheidingsteken](components/separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Lijst van het Fragment van de Inhoud](components/content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Accordeon](components/accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Knoop](components/button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Container](components/container.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Download](components/download.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Fragment van de Ervaring](components/experience-fragment.md)** |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[bed](components/embed.md)** in |  |  |  |  |  |  |  |  |  | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[Bar van de Voortgang](components/progress-bar.md)** |  |  |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[de Kijker van PDF](components/pdf-viewer.md)** |  |  |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[Inhoudsopgave](components/tableofcontents.md)** |  |  |  |  |  |  |  |  |  |  |  |  |  | v1 | v1 |

## Versies en releases {#versions-and-releases}

De Componenten van de kern worden verdeeld via GitHub. Op deze manier kan Adobe sneller functionaliteit toevoegen aan de componenten en ook buiten de releasecyclus van AEM invoer uit de gebruikersgemeenschap mogelijk maken.

De Core Components worden beschikbaar gesteld met gedefinieerde AEM-versies waarmee ze compatibel zijn. Dit betekent dat één AEM-versie meerdere versies of versies van de Core Components kan ondersteunen.

### Versies {#versions}

De belangrijkste herhaling van de Componenten van de Kern is de **versies**. Elke component heeft een versie. De versies worden aangeduid met **v** die met een nonzero, positief geheel zoals v1 en v2 wordt toegevoegd. Versies worden alleen verhoogd voor wijzigingen die niet compatibel zijn met oudere versies, wat normaal gesproken het geval is bij de introductie van nieuwe functies en functionaliteit.

De ontwikkelaars en de beheerders kunnen versies van de kerncomponenten door een aantal in hun middeltypepaden, en in volledig gekwalificeerde de klassennamen van Java van hun implementaties erkennen. Dit versieaantal vertegenwoordigt een belangrijke versie zoals die door [ semantische versieringsrichtlijnen ](https://semver.org/) wordt bepaald.

Voor meer details over kerncomponentenversies, zie de [ ontwikkelaarsdocumentatie van de Componenten van de Kern ](developing/guidelines.md).

### Uitstoot {#releases}

De kerncomponenten worden ter beschikking gesteld door **versies** en [ vertegenwoordigen de daadwerkelijke gepubliceerde artefacten beschikbaar op GitHu.](https://github.com/adobe/aem-core-wcm-components/releases) In releases wordt een decimaal getal in de notatie `X.Y.Z` aangegeven en worden alle kerncomponenten samen verzameld als een leverbaar pakket.

* **Belangrijke versies** introduceren volledig nieuwe componenten, verbeteringen aan bestaande versie van componenten, evenals standaardinsectenmoeilijke situaties. Dit wordt vertegenwoordigd door een toename in de `X` component van het versieaantal.
* **Kleine versies** introduceren nieuwe componenten, nieuwe functionaliteit aan bestaande versies van componenten, evenals insectenmoeilijke situaties. Dit wordt vertegenwoordigd door een toename in de `Y` component van het versieaantal.
* **de versies van het Patch** bevatten slechts insectenmoeilijke situaties. Dit wordt vertegenwoordigd door een toename in de `Z` component van het versieaantal.

>[!NOTE]
>
>De versies kunnen veelvoudige versies van de zelfde component bevatten.
>
>Dezelfde versie van een component kan in meerdere releases worden weergegeven.

## Ondersteuning voor kerncomponenten {#core-components-support}

De Componenten van de kern zijn een integraal deel van AEM en worden gesteund onder de zelfde voorwaarden alsof zij als deel van Quickstart werden geleverd.

Net als andere productkenmerken is de algemene regel van het einde van de levensduur:

* Componenten worden eerst aangekondigd te worden vervangen voordat ze worden verwijderd
* Op zijn vroegst worden ze na de aankondiging uit de AEM-versie verwijderd.

Dit geeft klanten minstens één versiecyclus om naar de nieuwe versie van de component te bewegen, alvorens steun beëindigt.

De versie van elke component geeft duidelijk aan welke AEM-versies worden ondersteund. Als een versie van AEM geen ondersteuning meer biedt, biedt dit ook ondersteuning voor de Core Components voor die versie van AEM.

Voor details over de steun van componentenaanpassingen, zie de [ Aanpassende pagina van de Componenten van de Kern ](developing/customizing.md) van de relevante Versie van de Componenten van de Kern.

## Ondersteuning van stichtingscomponenten {#foundation-component-support}

Adobe-ontwikkelingsnadruk is verschoven naar Core Components en er zullen nieuwe functies worden toegevoegd.

[ bijna zijn alle Componenten van de Stichting verouderd met AEM 6.5 ](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/siteandpage/default-components-foundation.html?lang=nl-NL) en slechts zullen de belangrijkste insectenmoeilijke situaties voor de Componenten van de Stichting die door:gaan worden overwogen.
