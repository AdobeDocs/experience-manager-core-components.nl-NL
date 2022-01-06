---
title: Projectarchetype AEM
description: Een projectmalplaatje voor op AEM gebaseerde toepassingen
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: 9ae35572f7ef60ea5140a7b48be087f34e39ce3a
workflow-type: tm+mt
source-wordcount: '1148'
ht-degree: 1%

---

# Projectarchetype AEM {#aem-project-archetype}

Het AEM Project Archetype is een Geweven malplaatje dat tot een minimaal, op best-praktijken-gebaseerd Adobe Experience Manager (AEM) project als uitgangspunt voor uw website leidt.

>[!TIP]
>
>De nieuwste AEM Project Archetype [kan op GitHub worden gevonden.](https://github.com/adobe/aem-project-archetype)

## Bronnen {#resources}

* **Archetype Documentatie (dit document):** Overzicht van de architectuur archetype en zijn verschillende modules.
   * **[Archetype gebruiken:](using.md)** nadere bijzonderheden over het gebruik van het archetype en de beschikbare modules
   * **[ui.frontend:](uifrontend.md)** Hoe te om het vooreind te gebruiken bouwt module
* **De volgende zelfstudies zijn gebaseerd op dit archetype:**
   * **[WKND-site:](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** Leer hoe u een nieuwe website kunt starten.
   * **[WKND App met één pagina:](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** Leer hoe u een React- of Angular-webapp ontwikkelt die volledig in AEM kan worden geschreven.

## Functies {#features}

* **Beste praktijken:** Bootstrap uw site met alle aanbevolen Adobe.
* **Lage code:** Bewerk uw sjablonen, maak inhoud, implementeer uw CSS en uw site is klaar om live te gaan.
* **Klaar voor cloud:** Indien gewenst, gebruik [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html) om binnen enkele dagen te gaan wonen en schaalbaarheid en onderhoud te vergemakkelijken.
* **Dispatcher:** Een project is alleen voltooid met een [Dispatcher-configuratie](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html) dat snelheid en veiligheid verzekert.
* **Meerdere sites:** Indien nodig genereert het archetype de inhoudsstructuur voor een [meertalige installatie en installatie voor meerdere regio&#39;s](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html).
* **Kernonderdelen:** Auteurs kunnen bijna elke lay-out maken met onze veelzijdige [reeks gestandaardiseerde componenten](/help/introduction.md).
* **Bewerkbare sjablonen:** Bijna alles samenstellen [sjabloon zonder code](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html)en definieert wat de auteurs mogen bewerken.
* **Responsieve lay-out:** Op sjablonen of afzonderlijke pagina&#39;s [definiëren hoe de elementen opnieuw worden geplaatst](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html) voor de gedefinieerde onderbrekingspunten.
* **Koptekst en voettekst:** U kunt ze samenstellen en lokaliseren zonder code, met de opdracht [lokalisatiefuncties van de componenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html).
* **Stijlsysteem:** Vermijd het bouwen van aangepaste componenten door auteurs toe te staan om [verschillende stijlen toepassen](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html) aan hen.
* **Front-end build:** Ontwikkelaars aan de voorzijde kunnen [AEM](uifrontend.md#webpack-dev-server) en [build-clientbibliotheken](uifrontend.md) met Webpack, TypeScript en SASS.
* **WebApp-Ready:** Voor sites die [Reageren](uifrontend-react.md) of [Angular](uifrontend-angular.md), gebruikt u de [SPA SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/headless/spa/developing.html) behouden [contextontwerp van de app](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html).
* **Handel ingeschakeld:** Voor projecten die willen integreren [AEM Commerce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html) met handelsoplossingen zoals [Magento](https://magento.com/) met de [Core Components](https://github.com/adobe/aem-core-cif-components).
* **Voorbeeldcode:** Controle uit de component HelloWorld, en de steekproefmodellen, servlets, filters, en planners.
* **Open Bronnen:** Als iets anders is dan zou moeten, [bijdragen](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) uw verbeteringen!

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

* Vervangen `XX` uiterlijk [archietype versienummer.](#requirements)
* Set `aemVersion=cloud` for [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html);\
   Set `aemVersion=6.5.0` for [Beheerde services van Adobe](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)of op locatie.
De afhankelijkheid van kerncomponenten wordt alleen toegevoegd voor versies met een andere naam dan de cloud, aangezien de Core Components OTB voor AEM as a Cloud Service wordt geleverd.
* Aanpassen `appTitle="My Site"` om de titel van de website en de groepen componenten te definiëren.
* Aanpassen `appId="mysite"` om Maven artifactId, de component, config en de namen van de inhoudsomslag, evenals de namen van de cliëntbibliotheek te bepalen.
* Aanpassen `groupId="com.mysite"` om Maven groupId en het Bron Pakket van Java te bepalen.
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
| `aemVersion` | `cloud` | AEM (kan `cloud` for [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html); of `6.5.0`, of `6.4.4` for [Beheerde services van Adobe](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) of op locatie). |
| `sdkVersion` | `latest` | Wanneer `aemVersion=cloud` een [SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) versie kan worden opgegeven (bijvoorbeeld `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Bevat een configuratie van de verzender voor cloud of voor AMS/on-premise, afhankelijk van de waarde van `aemVersion` (kan `y` of `n`). |
| `frontendModule` | `general` | Omvat een vooraf ingebouwd module Webpack die de cliëntbibliotheken (kan) produceert `general` of `none` voor gewone locaties; kan `angular` of `react` voor een app voor één pagina die het [SPA Editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html)). |
| `language` | `en` | Taalcode (ISO 639-1) waarmee de inhoudsstructuur wordt gemaakt (bijvoorbeeld `en`, `deu`). |
| `country` | `us` | Landcode (ISO 3166-1) om de inhoudsstructuur te maken op basis van (bijvoorbeeld `US`). |
| `singleCountry` | `y` | Omvat een taal-master inhoudsstructuur (kan `y`, of `n`). |
| `includeExamples` | `n` | Bevat een [Componentbibliotheek](https://www.aemcomponents.dev/) voorbeeldsite (kan `y`, of `n`). |
| `includeErrorHandler` | `n` | Bevat een aangepaste 404-responspagina die globaal is voor de gehele instantie (kan `y` of `n`). |
| `includeCommerce` | `n` | Inclusief [CIF Core-componenten](https://github.com/adobe/aem-core-cif-components) afhankelijkheden en genereert overeenkomstige artefacten. |
| `commerceEndpoint` |  | Alleen vereist voor CIF. Facultatief eindpunt van het handelssysteem te gebruiken dienst GraphQL (b.v. `https://hostname.com/grapql`). |
| `datalayer` | `y` | Integratie activeren met [Gegevenslaag Adobe-client](/help/developing/data-layer/overview.md). |
| `amp` | `n` | Inschakelen [AMP](/help/developing/amp.md) ondersteuning voor gegenereerde projectsjablonen. |
| `enableDynamicMedia` | `n` | Laat stichting DynamicMedia componenten in de montages van het projectbeleid toe en activeert de eigenschappen van Dynamic Media in het beleid van de component van het Beeld van de Kern. |
| `enableSSR` | `n` | Optie om SSR voor het front-end project toe te laten |
| `precompiledScripts` | `n` | Optie naar [vooraf compileren](/help/developing/archetype/precompiled-bundled-scripts.md) de serverscripts van `ui.apps` en als secundair bundelartefact aan het gebouw koppelen in het `ui.apps` project. `aemVersion` moet worden ingesteld op `cloud`. |
| `includeFormscommunications` | `n` | Inclusief [Forms Core-componenten](https://github.com/adobe/aem-core-forms-components) afhankelijkheden, sjablonen, formuliergegevensmodellen, thema&#39;s en genereert overeenkomstige artefacten voor Forms Communications-programma&#39;s. |
| `includeFormsenrollment` | `n` | Inclusief [Forms Core-componenten](https://github.com/adobe/aem-core-forms-components) afhankelijkheden, sjablonen, formuliergegevensmodellen, thema&#39;s en genereert overeenkomstige artefacten voor Forms-inschrijvingsprogramma&#39;s. |

## Systeemvereisten {#requirements}

| Archetype | AEM as a Cloud Service | AEM 6,5 | Java SE | Maven |
|---------|---------|---------|---------|---------|
| [34](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-34) | Continu | 6.5.7.0+ | 8, 11 | 3.3.9+ |

Stel uw lokale ontwikkelomgeving in voor [as a Cloud Service SDK AEM](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) of voor [oudere versies van AEM](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

### Bekende problemen {#known-issues}

Wanneer het lopen op Vensters en het produceren van de dispatcherconfiguratie, zou u in een opgeheven bevelherinnering of Subsysteem van Vensters voor Linux moeten lopen (zie [#329](https://github.com/adobe/aem-project-archetype/issues/329)).

Als u het archetype uitvoert in de interactieve modus (zonder de `-B` parameter), kunnen de eigenschappen met standaardwaarden niet worden veranderd, tenzij de definitieve bevestiging wordt verworpen, die dan de vragen door de eigenschappen met standaardwaarden in de vragen te omvatten herhaalt (zie
[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) voor meer informatie).

U kunt dit archetype in Eclipse niet gebruiken wanneer het beginnen van een nieuw project met `File -> New -> Maven Project` sinds het script voor na de generatie `archetype-post-generate.groovy` wordt niet uitgevoerd vanwege een [Eclipse-probleem.](https://bugs.eclipse.org/bugs/show_bug.cgi?id=514993) Als tussenoplossing kunt u de bovenstaande opdrachtregel gebruiken en daarna in Eclipse `File -> Import -> Existing Maven Project`.

## Meer informatie {#further-reading}

Voor meer details over het gebruiken van archetype met inbegrip van zijn voordelen, opties, en hoe zijn modules werken, gelieve te zien [Het Archetype-document gebruiken.](using.md)
