---
title: AEM-projectarchetype
description: Een projectmalplaatje voor op AEM-Gebaseerde toepassingen
translation-type: tm+mt
source-git-commit: 2faa092a075ab0512e9bd5654884534936c0ad53

---


# AEM-projectarchetype {#aem-project-archetype}

Het AEM Project Archetype is een Geweven malplaatje dat tot een minimaal, best-practices-gebaseerd project van de Manager van de Ervaring van Adobe (AEM) als uitgangspunt voor uw website leidt.

>[!TIP]
>
>Het recentste Archetype van het Project AEM [kan op GitHub](https://github.com/adobe/aem-project-archetype)worden gevonden.

## Bronnen {#resources}

* **Archetype Documentatie (dit document):** Overzicht van de architectuur archetype en zijn verschillende modules.
   * **[Archetype gebruiken:](using.md)**nadere bijzonderheden over het gebruik van het archetype en de beschikbare modules
   * **[ui.frontend:](uifrontend.md)**Hoe te om het vooreind te gebruiken bouwt module
* De volgende zelfstudies zijn gebaseerd op dit archetype:
   * **[WKND-site:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)**Leer hoe u een nieuwe website kunt starten.
   * **[WKND App met één pagina:](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)**Leer hoe u een React- of hoekige webapp maakt die volledig authorable is in AEM.

## Features {#features}

* **Beste praktijken:** Verhoog uw site met alle aanbevolen procedures van Adobe.
* **Lage code:** Bewerk uw sjablonen, maak inhoud, implementeer uw CSS en uw site is klaar om live te gaan.
* **Klaar voor cloud:** Gebruik indien gewenst [AEM als cloudservice](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) om binnen enkele dagen te gaan werken en de schaalbaarheid en het onderhoud te vereenvoudigen.
* **Dispatcher:** Een project is volledig slechts met een configuratie [van de](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/dispatcher.html) Verzender die snelheid en veiligheid verzekert.
* **Meerdere sites:** Indien nodig, produceert archetype de inhoudsstructuur voor een [meertalig en multi-regio opstelling](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html).
* **Kernonderdelen:** Auteurs kunnen bijna elke lay-out maken met onze veelzijdige [set gestandaardiseerde componenten](/help/introduction.md).
* **Bewerkbare sjablonen:** U kunt vrijwel elke [sjabloon zonder code](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html)samenstellen en definiëren wat de auteurs mogen bewerken.
* **Responsieve lay-out:** Voor malplaatjes of individuele pagina&#39;s, [bepaal hoe de elementen opnieuw plaatsen](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/responsive-layout.html) voor de bepaalde breekpunten.
* **Koptekst en voettekst:** U kunt ze zonder code samenstellen en lokaliseren met de [lokalisatiefuncties van de componenten](https://docs.adobe.com/content/help/en/experience-manager-core-components/using/get-started/localization.html).
* **Stijlsysteem:** Vermijd het bouwen van aangepaste componenten door auteurs toe te staan verschillende stijlen [op hen toe te](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) passen.
* **Front-end build:** Front-end devs kunnen AEM-pagina [&#39;s](uifrontend.md#webpack-dev-server) modelleren en clientbibliotheken [](uifrontend.md) bouwen met Webpack, TypeScript en SASS.
* **WebApp-Ready:** Voor plaatsen die React [of](uifrontend-react.md) Hoekig [gebruiken, gebruik het](uifrontend-angular.md)KUUROORD SDK [om](https://docs.adobe.com/content/help/en/experience-manager-64/developing/headless/spas/spa-architecture.html) in-context het schrijven van app [](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)te behouden.
* **Voorbeeldcode:** Controle uit de component HelloWorld, en de steekproefmodellen, servelets, filters, en planners.
* **Open Bronnen:** Als iets anders is dan zou moeten, [draagt](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) u uw verbeteringen bij!

## Gebruik

Om een project te produceren, pas de volgende bevellijn aan uw behoeften aan:

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.granite.archetypes \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=23 \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Set `aemVersion=cloud` for [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Stel deze optie in `aemVersion=6.5.0` voor [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)of on-premise.
De afhankelijkheid van kerncomponenten wordt alleen toegevoegd voor versies met een andere naam dan de cloud, aangezien de Core Components OTB voor AEM als CloudService wordt geleverd.
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
| `aemVersion` | `6.5.0` | Doel-AEM-versie (kan `cloud` voor [AEM als cloudservice](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)worden gebruikt; of `6.5.0`, `6.4.4`, of `6.3.3` voor [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) of on-premise). |
| `sdkVersion` | `latest` | Wanneer `aemVersion=cloud` een [SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) -versie kan worden opgegeven (bijvoorbeeld `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Bevat een configuratie van de dispatcher voor de cloud of voor AMS/on-premise, afhankelijk van de waarde van `aemVersion` (kan zijn `y` of `n`). |
| `frontendModule` | `none` | Omvat een vooraf ingebouwd module Webpack die de cliëntbibliotheken (kan `general` of `none` voor regelmatige plaatsen zijn) produceert; kan `angular` of `react` voor een Enige PaginaApp zijn die de Redacteur [van het](https://docs.adobe.com/content/help/en/experience-manager-65/developing/headless/spas/spa-overview.html)KUUROORD) uitvoert. |
| `languageCountry` | `en_us` | Taal- en landcode waarmee de inhoudsstructuur wordt gemaakt (bijvoorbeeld `en_us`). |
| `singleCountry` | `y` | Bevat een taalstramieninhoudsstructuur (kan zijn `y`, of `n`). |
| `includeExamples` | `y` | Bevat een voorbeeldsite van de [componentbibliotheek](https://www.aemcomponents.dev/) (kan `y`of `n`). |
| `includeErrorHandler` | `n` | Bevat een aangepaste 404-responspagina die globaal is voor de gehele instantie (kan zijn `y` of `n`). |

## Systeemvereisten

| Archetype | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | AEM 6.3 | Java SE | Maven |
---------|---------|---------|---------|---------|---------|---------
| [23](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-23) | Continu | 6.5.0.0+ | 6.4.4.0+ | 6.3.3.4+ | 8, 11 | 3.3.9+ |

Stel uw lokale ontwikkelomgeving voor [AEM in als een Cloud Service SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) of voor [oudere versies van AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

### Bekende problemen

Wanneer het lopen op Vensters en het produceren van de berichtcherconfiguratie, zou u in een opgeheven bevelherinnering of Subsysteem van Vensters voor Linux (zie [#329](https://github.com/adobe/aem-project-archetype/issues/329)) moeten lopen.

Wanneer het uitvoeren van archetype op interactieve wijze (zonder de `-B` parameter), kunnen de eigenschappen met standaardwaarden niet worden veranderd, tenzij de definitieve bevestiging wordt verworpen, die dan de vragen door de eigenschappen met standaardwaarden in de vragen te omvatten herhaalt (zie[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) voor details).

## Meer informatie {#further-reading}

Voor meer details over het gebruiken van archetype met inbegrip van zijn voordelen, opties, en hoe zijn modules werken, gelieve te zien het [Gebruiken van het document Archetype.](using.md)