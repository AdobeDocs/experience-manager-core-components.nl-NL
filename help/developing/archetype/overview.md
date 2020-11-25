---
title: Projectarchetype AEM
description: Een projectmalplaatje voor op AEM gebaseerde toepassingen
translation-type: tm+mt
source-git-commit: e32521f35f33897cd72892de393073b01ad963f1
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 3%

---


# Projectarchetype AEM {#aem-project-archetype}

Het AEM Project Archetype is een Geweven malplaatje dat tot een minimaal, op best-praktijken-gebaseerd Adobe Experience Manager (AEM) project als uitgangspunt voor uw website leidt.

>[!TIP]
>
>Het recentste AEM Archetype van het Project [kan op GitHub](https://github.com/adobe/aem-project-archetype)worden gevonden.

## Bronnen {#resources}

* **Archetype Documentatie (dit document):** Overzicht van de architectuur archetype en zijn verschillende modules.
   * **[Archetype gebruiken:](using.md)** nadere bijzonderheden over het gebruik van het archetype en de beschikbare modules
   * **[ui.frontend:](uifrontend.md)** Hoe te om het vooreind te gebruiken bouwt module
* De volgende zelfstudies zijn gebaseerd op dit archetype:
   * **[WKND-site:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** Leer hoe u een nieuwe website kunt starten.
   * **[WKND App met één pagina:](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** Leer hoe u een React- of Angular-webapp maakt die volledig in AEM kan worden geschreven.

## Features {#features}

* **Beste praktijken:** Bootstrap uw site met alle aanbevolen Adobe.
* **Lage code:** Bewerk uw sjablonen, maak inhoud, implementeer uw CSS en uw site is klaar om live te gaan.
* **Klaar voor cloud:** Indien gewenst kunt u [AEM gebruiken als Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) om binnen enkele dagen te gaan leven en schaalbaarheid en onderhoud te vereenvoudigen.
* **Dispatcher:** Een project is volledig slechts met een configuratie [van de](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/dispatcher.html) Verzender die snelheid en veiligheid verzekert.
* **Meerdere sites:** Indien nodig, produceert archetype de inhoudsstructuur voor een [meertalig en multi-regio opstelling](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html).
* **Kernonderdelen:** Auteurs kunnen bijna elke lay-out maken met onze veelzijdige [set gestandaardiseerde componenten](/help/introduction.md).
* **Bewerkbare sjablonen:** U kunt vrijwel elke [sjabloon zonder code](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html)samenstellen en definiëren wat de auteurs mogen bewerken.
* **Responsieve lay-out:** Voor malplaatjes of individuele pagina&#39;s, [bepaal hoe de elementen voor de bepaalde breekpunten opnieuw plaatsen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html) .
* **Koptekst en voettekst:** U kunt ze zonder code samenstellen en lokaliseren met de [lokalisatiefuncties van de componenten](https://docs.adobe.com/content/help/en/experience-manager-core-components/using/get-started/localization.html).
* **Stijlsysteem:** Vermijd het bouwen van aangepaste componenten door auteurs toe te staan verschillende stijlen [op hen toe te](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) passen.
* **Front-end build:** Ontwikkelaars aan de voorzijde kunnen [AEM pagina](uifrontend.md#webpack-dev-server) &#39;s modelleren en clientbibliotheken [](uifrontend.md) bouwen met Webpack, TypeScript en SASS.
* **WebApp-Ready:** Voor sites die gebruikmaken van [React](uifrontend-react.md) of [Angular](uifrontend-angular.md), gebruikt u de [SPA SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/developing.html) om het [in-context ontwerpen van de app](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)te behouden.
* **Handel ingeschakeld:** Voor projecten die [AEM Handel](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/commerce/home.html) met handelsoplossingen zoals [Magento](https://magento.com/) willen integreren gebruikend de Componenten [van de Kern van de](https://github.com/adobe/aem-core-cif-components)Handel.
* **Voorbeeldcode:** Controle uit de component HelloWorld, en de steekproefmodellen, servlets, filters, en planners.
* **Open Bronnen:** Als iets anders is dan zou moeten, [draagt](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) u uw verbeteringen bij!

## Gebruik

Om een project te produceren, pas de volgende bevellijn aan uw behoeften aan:

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=24 \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
```

* Set `aemVersion=cloud` for [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Stel deze optie in `aemVersion=6.5.0` voor [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)of on-premise.
De afhankelijkheid van kerncomponenten wordt alleen toegevoegd voor versies met een andere naam dan de cloud, aangezien de Core Components OTB voor AEM als Cloud Service wordt geleverd.
* Pas `appTitle="My Site"` de titel van de website en de groepen componenten aan.
* Pas `appId="mysite"` aan om Maven artifactId, de component, config en de namen van de inhoudsomslag, evenals de namen van de cliëntbibliotheek te bepalen.
* Pas `groupId="com.mysite"` aan om Maven groupId en het Bron Pakket van Java te bepalen.
* Zoek de lijst met beschikbare eigenschappen op om te zien of u meer eigenschappen wilt aanpassen.

## Beschikbare eigenschappen

| Naam | Standaard | Beschrijving |
--------------------------|----------------|--------------------
| `appTitle` |  | Toepassingstitel, wordt gebruikt voor de titel van de website en voor componentgroepen (bijvoorbeeld `"My Site"`). |
| `appId` |  | De technische naam, zal voor component, config en de namen van de inhoudsomslag, evenals de namen van de cliëntbibliotheek worden gebruikt (b.v. `"mysite"`). |
| `artifactId` | *`${appId}`* | Basis-Maven-artefactverwijzing (bijvoorbeeld `"mysite"`). |
| `groupId` |  | Basis-Maven-groep-id (bijvoorbeeld `"com.mysite"`). |
| `package` | *`${groupId}`* | Java-bronpakket (bijvoorbeeld `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Projectversie (bijvoorbeeld `1.0-SNAPSHOT`). |
| `aemVersion` | `cloud` | AEM (kan `cloud` voor [AEM als Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)zijn; of `6.5.0`, of `6.4.4` voor [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) of on-premise). |
| `sdkVersion` | `latest` | Wanneer `aemVersion=cloud` een [SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) -versie kan worden opgegeven (bijvoorbeeld `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Bevat een configuratie van de dispatcher voor de cloud of voor AMS/on-premise, afhankelijk van de waarde van `aemVersion` (kan zijn `y` of `n`). |
| `frontendModule` | `general` | Omvat een vooraf ingebouwd module Webpack die de cliëntbibliotheken (kan `general` of `none` voor regelmatige plaatsen zijn) produceert; kan `angular` of `react` voor een app van één pagina zijn die de [SPA Editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html)implementeert). |
| `language` | `en` | Taalcode (ISO 639-1) waarmee de inhoudsstructuur wordt gemaakt (bijvoorbeeld `en`, `deu`). |
| `country` | `us` | Landcode (ISO 3166-1) om de inhoudsstructuur te maken op basis van (bijvoorbeeld `US`). |
| `singleCountry` | `y` | Omvat een taal-master inhoudsstructuur (kan zijn, `y`of `n`). |
| `includeExamples` | `n` | Bevat een voorbeeldsite van de [componentbibliotheek](https://www.aemcomponents.dev/) (kan `y`of `n`). |
| `includeErrorHandler` | `n` | Bevat een aangepaste 404-responspagina die globaal is voor de gehele instantie (kan zijn `y` of `n`). |
| `includeCommerce` | `n` | Omvat de [eigenschappen van de Componenten](https://github.com/adobe/aem-core-cif-components) van de Kern CIF en produceert overeenkomstige artefacten. |
| `commerceEndpoint` |  | Alleen vereist voor CIF. Facultatief eindpunt van het handelssysteem te gebruiken dienst GraphQL (b.v. `https://hostname.com/grapql`). |
| `datalayer` | `y` | Activeer integratie met de Gegevenslaag [van de Cliënt van](/help/developing/data-layer/overview.md)Adobe. |
| `amp` | `n` | Schakel [AMP](/help/developing/amp.md) -ondersteuning voor gegenereerde projectsjablonen in. |

## Systeemvereisten

| Archetype | AEM as a Cloud Service | AEM 6,5 | AEM 6,4 | Java SE | Maven |
|---------|---------|---------|---------|---------|---------|
| [24](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-24) | Continu | 6.5.5.0+ | 6.4.8.1+ | 8, 11 | 3.3.9+ |

Opstelling uw lokale ontwikkelomgeving voor [AEM als Cloud Service SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) of voor [oudere versies van AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

### Bekende problemen

Wanneer het lopen op Vensters en het produceren van de berichtcherconfiguratie, zou u in een opgeheven bevelherinnering of Subsysteem van Vensters voor Linux (zie [#329](https://github.com/adobe/aem-project-archetype/issues/329)) moeten lopen.

Wanneer het uitvoeren van archetype op interactieve wijze (zonder de `-B` parameter), kunnen de eigenschappen met standaardwaarden niet worden veranderd, tenzij de definitieve bevestiging wordt verworpen, die dan de vragen door de eigenschappen met standaardwaarden in de vragen te omvatten herhaalt (zie[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) voor details).

## Meer informatie {#further-reading}

Voor meer details over het gebruiken van archetype met inbegrip van zijn voordelen, opties, en hoe zijn modules werken, gelieve te zien het [Gebruiken van het document Archetype.](using.md)
