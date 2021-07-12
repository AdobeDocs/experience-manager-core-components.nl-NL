---
title: Projectarchetype AEM
description: Een projectmalplaatje voor op AEM gebaseerde toepassingen
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 2%

---

# Projectarchetype AEM {#aem-project-archetype}

Het AEM Project Archetype is een Geweven malplaatje dat tot een minimaal, op best-praktijken-gebaseerd Adobe Experience Manager (AEM) project als uitgangspunt voor uw website leidt.

>[!TIP]
>
>Het recentste AEM Archetype van het Project [kan op GitHub worden gevonden.](https://github.com/adobe/aem-project-archetype)

## Bronnen {#resources}

* **Archetype Documentatie (dit document):** Overzicht van de architectuur archetype en zijn verschillende modules.
   * **[Het gebruiken van Archetype:](using.md)** verdere details over het gebruiken van archetype en beschikbare modules
   * **[ui.frontend:](uifrontend.md)** Hoe te om het vooreind te gebruiken bouwt module
* De volgende zelfstudies zijn gebaseerd op dit archetype:
   * **[WKND-site:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** Meer informatie over het starten van een nieuwe website.
   * **[WKND App met één pagina:](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** Leer hoe u een React- of Angular-webapp maakt die volledig in AEM kan worden geschreven.

## Functies {#features}

* **Tips en trucs:** Bootstrap uw site met alle aanbevolen Adobe.
* **Lage code:** Bewerk uw sjablonen, maak inhoud, implementeer uw CSS en uw site is klaar voor live.
* **Klaar voor cloud:** Gebruik indien gewenst  [AEM als Cloud ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) Service om binnen enkele dagen te gaan wonen en schaalbaarheid en onderhoud te vereenvoudigen.
* **Dispatcher:** Een project is volledig slechts met een  [Configuratie van de ](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/dispatcher.html) Verzender die snelheid en veiligheid verzekert.
* **Meerdere sites:** indien nodig genereert het archetype de inhoudsstructuur voor een  [meertalige en meerregionale installatie](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html).
* **Core Components:** Auteurs kunnen bijna elke lay-out maken met onze veelzijdige  [set gestandaardiseerde componenten](/help/introduction.md).
* **Bewerkbare sjablonen:** U kunt vrijwel elke  [sjabloon zonder code](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) samenstellen en definiëren wat de auteurs mogen bewerken.
* **Responsieve layout:** Definieer  [op sjablonen of afzonderlijke pagina&#39;s hoe de elementen opnieuw worden ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html) geplaatst voor de gedefinieerde onderbrekingspunten.
* **Koptekst en voettekst:deze zonder code** samenstellen en lokaliseren, met de  [lokalisatiefuncties van de componenten](https://docs.adobe.com/content/help/en/experience-manager-core-components/using/get-started/localization.html).
* **Stijlsysteem:** bouw geen aangepaste componenten door auteurs toe te staan verschillende stijlen op  [hen ](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) toe te passen.
* **Front-End Build:** Front-end ontwikkelaars kunnen  [AEM ](uifrontend.md#webpack-dev-server) pagina&#39;s modelleren en  [clientbibliotheken ](uifrontend.md) bouwen met Webpack, TypeScript en SASS.
* **WebApp-Ready:** Voor sites die  [](uifrontend-react.md) Reactor- [Angular](uifrontend-angular.md) gebruiken, gebruikt u de  [SPA ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/developing.html) SDK om het  [in-context schrijven van de app](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html) te behouden.
* **Handel ingeschakeld:** voor projecten die  [AEM ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/commerce/home.html) Handel met handelsoplossingen zoals  [](https://magento.com/) Magentousing willen integreren de Componenten [ van de Kern van de ](https://github.com/adobe/aem-core-cif-components)Handel.
* **Voorbeeldcode:** Uitchecken van de component HelloWorld en de voorbeeldmodellen, servlets, filters en planners.
* **Open Bronced:** Als iets anders is dan zou moeten,  [](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) levert dit uw verbeteringen op!

## Gebruik {#usage}

Om een project te produceren, pas de volgende bevellijn aan uw behoeften aan:

```shell
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
```

* Vervang `XX` door het laatste [archietype versienummer.](#requirements)
* `aemVersion=cloud` voor [AEM instellen als een Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Stel `aemVersion=6.5.0` in voor [Beheerde services van Adobe](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) of op locatie.
De afhankelijkheid van kerncomponenten wordt alleen toegevoegd voor versies met een andere naam dan de cloud, aangezien de Core Components OTB voor AEM als Cloud Service wordt geleverd.
* Pas `appTitle="My Site"` aan om de titel van de website en componentengroepen te bepalen.
* Pas `appId="mysite"` aan om Maven artifactId, de component, config en de namen van de inhoudsomslag, evenals de namen van de cliëntbibliotheek te bepalen.
* Pas `groupId="com.mysite"` aan om Maven groupId en het Bron Pakket van Java te bepalen.
* Zoek de lijst met beschikbare eigenschappen op om te zien of u meer eigenschappen wilt aanpassen.

## Beschikbare eigenschappen {#available-properties}

| Naam | Standaard | Beschrijving |
|---------------------------|----------------|--------------------|
| `appTitle` |  | Toepassingstitel, wordt gebruikt voor de titel van de website en voor componentgroepen (bijvoorbeeld `"My Site"`). |
| `appId` |  | De technische naam, zal voor component, config en de namen van de inhoudsomslag, evenals de namen van de cliëntbibliotheek worden gebruikt (b.v. `"mysite"`). |
| `artifactId` | *`${appId}`* | Basis-Maven-artefactverwijzing (bijvoorbeeld `"mysite"`). |
| `groupId` |  | Basis-Maven-groep-id (bijvoorbeeld `"com.mysite"`). |
| `package` | *`${groupId}`* | Java-bronpakket (bijvoorbeeld `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Projectversie (bijvoorbeeld `1.0-SNAPSHOT`). |
| `aemVersion` | `cloud` | AEM (kan `cloud` voor [AEM als Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) zijn; of `6.5.0`, of `6.4.4` voor [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) of on-premise). |
| `sdkVersion` | `latest` | Wanneer `aemVersion=cloud` een [SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html)-versie kan worden opgegeven (bijvoorbeeld `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Bevat een configuratie van de verzender voor cloud of voor AMS/on-premise, afhankelijk van de waarde van `aemVersion` (kan `y` of `n` zijn). |
| `frontendModule` | `general` | Omvat een vooraf gebouwde module Webpack die de cliëntbibliotheken (kan `general` of `none` voor regelmatige plaatsen zijn; kan `angular` of `react` voor een Enige Pagina zijn app die [SPA Redacteur ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html)) uitvoert. |
| `language` | `en` | Taalcode (ISO 639-1) waarmee de inhoudsstructuur wordt gemaakt (bijvoorbeeld `en`, `deu`). |
| `country` | `us` | Landcode (ISO 3166-1) om de inhoudsstructuur te maken op basis van (bijvoorbeeld `US`). |
| `singleCountry` | `y` | Omvat een taal-master inhoudsstructuur (kan `y`, of `n` zijn). |
| `includeExamples` | `n` | Bevat een [Component Library](https://www.aemcomponents.dev/) voorbeeldsite (kan `y` of `n` zijn). |
| `includeErrorHandler` | `n` | Bevat een aangepaste 404-responspagina die globaal is voor de gehele instantie (kan `y` of `n` zijn). |
| `includeCommerce` | `n` | Omvat [CIF Core Components](https://github.com/adobe/aem-core-cif-components) gebiedsdelen en produceert overeenkomstige artefacten. |
| `commerceEndpoint` |  | Alleen vereist voor CIF. Facultatief eindpunt van het handelssysteem te gebruiken dienst GraphQL (b.v. `https://hostname.com/grapql`). |
| `datalayer` | `y` | Activeer integratie met [Adobe Client Data Layer](/help/developing/data-layer/overview.md). |
| `amp` | `n` | Schakel [AMP](/help/developing/amp.md)-ondersteuning voor gegenereerde projectsjablonen in. |
| `enableDynamicMedia` | `n` | Laat stichting DynamicMedia componenten in de montages van het projectbeleid toe en activeert de eigenschappen van Dynamic Media in het beleid van de component van het Beeld van de Kern. |
| `enableSSR` | `n` | Optie om SSR voor het front-end project toe te laten |

## Systeemvereisten {#requirements}

| Archetype | AEM as a Cloud Service | AEM 6,5 | Java SE | Maven |
|---------|---------|---------|---------|---------|
| [28](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-28) | Continu | 6.5.7.0+ | 8, 11 | 3.3.9+ |

Stel uw lokale ontwikkelomgeving in voor [AEM als Cloud Service SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) of voor [oudere versies van AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

### Bekende problemen {#known-issues}

Wanneer het lopen op Vensters en het produceren van de berichtconfiguratie, zou u in een opgeheven bevelherinnering of Subsysteem van Vensters voor Linux (zie [#329](https://github.com/adobe/aem-project-archetype/issues/329)) moeten lopen.

Wanneer het uitvoeren van archetype op interactieve wijze (zonder de `-B` parameter), kunnen de eigenschappen met standaardwaarden niet worden veranderd, tenzij de definitieve bevestiging wordt verworpen, die dan de vragen door de eigenschappen met standaardwaarden in de vragen te omvatten herhaalt (zie
[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) voor meer informatie).

U kunt dit archetype in Eclipse niet gebruiken wanneer het beginnen van een nieuw project met `File -> New -> Maven Project` aangezien het post generatiescript `archetype-post-generate.groovy` niet wegens een [kwestie van de Verduistering zal worden uitgevoerd.](https://bugs.eclipse.org/bugs/show_bug.cgi?id=514993) De oplossing is om de bovengenoemde bevellijn en dan in Eclipse gebruik te gebruiken  `File -> Import -> Existing Maven Project`.

## Meer informatie {#further-reading}

Zie [Het Archetype-document gebruiken voor meer informatie over het gebruik van het archetype, inclusief de voordelen, opties en de manier waarop de modules werken.](using.md)
