---
title: Het gebruiken van het AEM Project Archetype
description: Gedetailleerde gebruiksinstructies voor het AEM Project Archetype
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
source-git-commit: 06a620980c9cda02d1190747b12b929498fb79c2
workflow-type: tm+mt
source-wordcount: '2194'
ht-degree: 0%

---

# Projectarchetype AEM {#aem-project-archetype}

Met het AEM Project Archetype maakt u een minimaal Adobe Experience Manager-project op basis van best practices als uitgangspunt voor uw eigen AEM. De eigenschappen die moeten worden verstrekt wanneer het gebruiken van dit archetype staat u toe om de namen voor alle delen van dit project te specificeren evenals bepaalde facultatieve eigenschappen te controleren.

## Waarom het Archetype gebruiken {#why-use-the-archetype}

Het gebruiken van het AEM Archetype van het Project plaatst u op de weg naar de bouw van een op best-praktijken-gebaseerd AEM project met enkel een paar aanslagen. Door het archetype te gebruiken, zullen alle stukken reeds op zijn plaats zijn zodat terwijl het resulterende project minimaal is, het reeds alle [sleutelfuncties](#what-you-get) AEM zodat je alleen maar verder moet bouwen en uitbreiden.

Natuurlijk zijn er vele elementen die in een succesvol AEM project gaan, maar het gebruiken van het AEM Project Archetype is een correcte stichting en sterk geadviseerd voor om het even welk AEM project.

## Aan de slag {#getting-started}

Het project archetype maakt het gemakkelijk om zich op AEM te beginnen ontwikkelen. U kunt de eerste stappen op verschillende manieren uitvoeren.

* WKND-zelfstudie - Voor een grote introductie over het ontwikkelen van AEM, inclusief hoe u het archetype kunt gebruiken, raadpleegt u de [Aan de slag met AEM Sites - WKND-zelfstudie](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) voor een praktisch voorbeeld dat u door het gebruiken van archetype loopt om een eenvoudig project uit te voeren.
* Zelfstudie voor WKND-gebeurtenissen - Als u bijzonder geïnteresseerd bent in de ontwikkeling van toepassingen (SPA) op AEM voor één pagina, moet u de speciale code uitchecken [Zelfstudie over WKND-gebeurtenissen](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html).
* Download en start alleen! - U kunt het huidige project archetype gemakkelijk downloaden beschikbaar op GitHub en uw eerste project creëren door [onderstaande eenvoudige stappen volgen](#how-to-use-the-archetype).

## Wat u krijgt met Archetype {#what-you-get}

Het AEM Archetype bestaat uit modules:

* **[kern](core.md)**: is een bundel van Java die alle kernfunctionaliteit zoals de diensten OSGi, luisteraars, en planners, evenals component-verwante code van Java zoals servlets en verzoekfilters bevat.
* **[it.tests](ittests.md)**: zijn op Java gebaseerde integratietests.
* **[ui.apps](uiapps.md)**: bevat de `/apps` en `/etc` delen van het project, d.w.z. JS en CSS clientlibs, componenten, en malplaatjes.
* **[ui.content](uicontent.md)**: bevat voorbeeldinhoud met behulp van de componenten uit de module ui.apps.
* **ui.config**: bevat runtime-specifieke OSGi vormen voor het project.
* **[ui.frontend.general](uifrontend.md)**: **(optioneel)** Bevat de artefacten die worden vereist om de algemene Web-pack-Gebaseerde voorste bouwstijlmodule te gebruiken.
* **[ui.frontend.response](uifrontend-react.md)**: **(optioneel)** bevat de artefacten die wanneer het gebruiken van archetype worden vereist om een SPA tot stand te brengen die op Reageren worden gebaseerd.
* **[ui.frontend.angular](uifrontend-angular.md)**: **(optioneel)** bevat de artefacten die wanneer het gebruiken van archetype worden vereist om een SPA tot stand te brengen die projecten op Angular worden gebaseerd.
* **[ui.tests](uitests.md)**: bevat op selenium gebaseerde UI-tests.
* **alles**: is één enkel inhoudspakket dat alle gecompileerde modules (bundels en inhoudspakketten) met inbegrip van om het even welke verkopersgebiedsdelen inbedt.
* **analyseren**: stelt analyse op het project in werking, dat extra bevestiging voor het opstellen in AEM as a Cloud Service verstrekt.

![](/help/assets/archetype-structure.png)

De modules van AEM Archetype die in Maven worden vertegenwoordigd worden opgesteld aan AEM als inhoudspakketten die de toepassing, de inhoud, en de noodzakelijke bundels OSGi vertegenwoordigen.

## Het gebruiken van Archetype {#how-to-use-the-archetype}

Om archetype te gebruiken, moet u eerst een project tot stand brengen, dat de modules in een lokale dossierstructuur als produceert [eerder beschreven](#what-you-get). Als deel van projectgeneratie, kan een aantal eigenschappen voor uw project worden bepaald zoals projectnaam, versie, enz.

Het bouwen van het project met Maven leidt tot de artefacten (pakketten en bundels OSGi), die aan AEM kunnen worden opgesteld. De extra Gemaakt bevelen en de profielen kunnen worden gebruikt om de projectartefacten aan een AEM instantie op te stellen.

### Een project maken {#create-project}

Om aan de slag te gaan, kunt u het eenvoudigst de [AEM Eclipse-extensie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/eclipse.html) en volgt u de wizard Nieuw project en kiest u **AEM Monster nemen van project met meerdere modules** om een vrijgegeven versie van archetype te gebruiken.

Natuurlijk kunt u ook Maven rechtstreeks aanroepen.

```shell
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Set `XX` aan de [versienummer](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) van de nieuwste AEM Project Archetype.
* Set `aemVersion=cloud` for [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html);\
   Set `aemVersion=6.5.0` for [Beheerde services van Adobe](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)of op locatie.
De afhankelijkheid van kerncomponenten wordt alleen toegevoegd voor versies met een andere naam dan de cloud, aangezien de Core Components OTB voor AEM as a Cloud Service wordt geleverd.
* Aanpassen `appTitle="My Site"` om de titel van de website en de groepen componenten te definiëren.
* Aanpassen `appId="mysite"` om Maven artifactId, de component, config en de namen van de inhoudsomslag, evenals de namen van de cliëntbibliotheek te bepalen.
* Aanpassen `groupId="com.mysite"` om Maven groupId en het Bron Pakket van Java te bepalen.
* Zoek de lijst met beschikbare eigenschappen op om te zien of u meer eigenschappen wilt aanpassen.

>[!NOTE]
>
>Het is aan te raden de `adobe-public` profiel naar uw Maven `settings.xml` om automatisch repo.adobe.com toe te voegen aan het gemaakte buildproces.
>
>Een voorbeeld-POM [hier te vinden](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

### Eigenschappen {#properties}

De volgende eigenschappen zijn beschikbaar wanneer het creëren van een project gebruikend archetype.

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
| `frontendModule` | `general` | Omvat een vooraf ingebouwd module Webpack die de cliëntbibliotheken (kan) produceert `general` of `none` voor gewone locaties; kan `angular` of `react` voor een app voor één pagina die het [SPA Editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/editor-overview.html)). |
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

>[!NOTE]
>
> Als het archetype de eerste keer op interactieve wijze wordt uitgevoerd, kunnen de eigenschappen met standaardwaarden niet worden veranderd (zie [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) voor meer informatie ). De waarde kan worden gewijzigd wanneer de vastgoedbevestiging aan het einde wordt geweigerd en de vragenlijst wordt herhaald, of door de parameter in de opdrachtregel door te geven (bijvoorbeeld `-DoptionIncludeExamples=n`).

>[!NOTE]
>
>Wanneer het lopen op Vensters en het produceren van de dispatcherconfiguratie, zou u in een opgeheven bevelherinnering of Subsysteem van Vensters voor Linux moeten lopen (zie [uitgave 329](https://github.com/adobe/aem-project-archetype/issues/329)).

### Profielen {#profiles}

Het gegenereerde beheerde project ondersteunt verschillende implementatieprofielen bij het uitvoeren `mvn install`.

| Profiel-id | Beschrijving |
| --------------------------|------------------------------|
| `autoInstallBundle` | De kernbundel installeren met de maven-sling-plug-in op de felix-console |
| `autoInstallPackage` | Installeer het inhoudspakket ui.content en ui.apps met de insteekmodule content-package-maven naar pakketbeheer om de standaardversie van de auteur op localhost, poort 4502, te gebruiken. Hostnaam en poort kunnen worden gewijzigd met de `aem.host` en `aem.port` door de gebruiker gedefinieerde eigenschappen. |
| `autoInstallPackagePublish` | Installeer het inhoudspakket ui.content en ui.apps met de insteekmodule content-package-maven naar het pakketbeheer om standaard een publicatie-instantie te publiceren op localhost, poort 4503. Hostnaam en poort kunnen worden gewijzigd met de `aem.host` en `aem.port` door de gebruiker gedefinieerde eigenschappen. |
| `autoInstallSinglePackage` | Installeer de `all` inhoudspakket met de insteekmodule content-package-maven naar pakketbeheer om de standaardversie van de auteur op localhost, poort 4502, in te stellen. Hostnaam en poort kunnen worden gewijzigd met de `aem.host` en `aem.port` door de gebruiker gedefinieerde eigenschappen. |
| `autoInstallSinglePackagePublish` | Installeer de `all` inhoudspakket met de insteekmodule content-package-maven naar pakketbeheer om de standaardpublicatie-instantie op localhost, poort 4503, in te stellen. Hostnaam en poort kunnen worden gewijzigd met de `aem.host` en `aem.port` door de gebruiker gedefinieerde eigenschappen. |
| `integrationTests` | Hiermee worden de opgegeven integratietests uitgevoerd op de AEM instantie (alleen voor de `verify` fase) |
| `precompiledScripts` | Wordt automatisch gedefinieerd wanneer het project met de `precompiledScripts` eigenschap ingesteld op `y`. Het profiel is standaard actief en genereert een OSGi-bundel binnen `ui.apps` met de vooraf gecompileerde scripts, die in de `all` inhoudspakket. Het profiel kan worden uitgeschakeld met `-DskipScriptPrecompilation=true`. |

### Samenstellen en installeren {#building-and-installing}

Om alle modules te bouwen die in de folder van de projectwortel lopen, gebruik het volgende Gemaakt bevel.

```shell
mvn clean install
```

Als u een lopende AEM instantie hebt, kunt u het volledige project bouwen en verpakken en in AEM met het volgende Geweven bevel opstellen.

```shell
mvn clean install -PautoInstallPackage
```

Voer deze opdracht uit om de opdracht te implementeren in een publicatieinstantie.

```shell
mvn clean install -PautoInstallPackagePublish
```

U kunt ook deze opdracht uitvoeren als u wilt implementeren in een publicatieinstantie.

```shell
mvn clean install -PautoInstallPackage -Daem.port=4503
```

U kunt ook alleen de bundel naar de auteur implementeren door deze opdracht uit te voeren.

```shell
mvn clean install -PautoInstallBundle
```

## Bovenliggende POM {#parent-pom}

De `pom.xml` aan de basis van het project (`<src-directory>/<project>/pom.xml`) staat bekend als de bovenliggende POM en drijft de structuur van het project en beheert afhankelijkheden en bepaalde algemene eigenschappen van het project.

### Algemene projecteigenschappen {#global-properties}

De `<properties>` sectie van ouderPOM bepaalt verscheidene globale eigenschappen die voor de plaatsing van uw project op een AEM instantie zoals gebruikersnaam/wachtwoord, gastheernaam/haven, enz. belangrijk zijn.

Deze eigenschappen worden opstelling om aan een lokale AEM instantie op te stellen, aangezien dit de gemeenschappelijkste bouwstijl is die de ontwikkelaars zullen doen. Er zijn eigenschappen die in een auteurinstantie en een publicatieinstantie moeten worden geïmplementeerd. Dit is ook waar de geloofsbrieven worden geplaatst om met de AEM instantie voor authentiek te verklaren. De standaardreferenties voor admin:admin worden gebruikt.

Deze eigenschappen zijn opstelling zodat zij kunnen worden met voeten getreden wanneer het opstellen aan hogere niveaumilieu&#39;s. Op deze manier hoeven de POM-bestanden niet te worden gewijzigd, maar variabelen zoals `aem.host` en `sling.password` kan worden overschreven via opdrachtregelargumenten:

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Modulestructuur {#module-structure}

De `<modules>` de sectie van ouderPOM bepaalt de modules die het project zal bouwen. Standaard wordt het project gebouwd [de eerder gedefinieerde standaardmodules](#what-you-get): core, ui.apps, ui.content, ui.tests, en it.launch. Meer modules kunnen altijd worden toegevoegd aangezien een project evolueert.

### Afhankelijkheden {#dependencies}

De `<dependencyManagement>` sectie van ouderPOM bepaalt alle gebiedsdelen en versies van APIs die in het project worden gebruikt. Versies moeten worden beheerd in de bovenliggende POM. Submodules zoals core en ui.apps mogen geen versiegegevens bevatten.

#### Uber-Jar {#uber-jar}

Een van de belangrijkste afhankelijkheden is de [Java API-jar AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html). Dit omvat alle AEM APIs met enkel één enkele gebiedsdeelingang voor de versie van AEM.

>[!NOTE]
>
>Als beste praktijken zou u de uber-jar versie moeten bijwerken om de doelversie van AEM aan te passen. Bijvoorbeeld, als u van plan bent om aan AEM 6.4 op te stellen zou u de versie van uber-jar aan 6.4.0 moeten bijwerken.

#### Kernonderdelen {#core-components}

Het AEM Projectarchetype van natuurlijk hefboomwerkingen de Componenten van de Kern.

De kerncomponenten worden automatisch in AEM in de standaardrunmode geïnstalleerd en door de steekproefWKND plaats gebruikt. In een [productiestop](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#runmodes) (`nosamplecontent`) zijn de Core Components niet beschikbaar.

Daarom is het, om de Componenten van de Kern in alle plaatsingen te gebruiken, een beste praktijk om hen als deel van het Maven project te omvatten.

>[!NOTE]
>
>Elke versie van de Componenten van de Kern wordt over het algemeen gevolgd door een versie van het AEM Archetype van het Project zodat het recentste archetype de recentste versie van de kerncomponenten gebruikt.
>
>Het is echter mogelijk dat een nieuwe versie van het archetype niet direct volgt op een nieuwe versie van de Core Components, dus u wilt mogelijk de afhankelijkheid van de Core Components bijwerken naar de nieuwste versie.

>[!NOTE]
>
>core.wcm.components.examples zijn een reeks steekproefpagina&#39;s die voorbeelden van de Componenten van de Kern illustreren. Als beste praktijken, wanneer het opstellen van een project voor productiegebruik zou u deze gebiedsdeel en subpackage opneming moeten verwijderen.

## Testen {#testing}

Het project bevat drie testniveaus en omdat het verschillende typen tests zijn, worden deze op verschillende manieren of op verschillende plaatsen uitgevoerd.

* Eenheidstest in kern: Dit toont de klassieke eenheidstests van de code in de bundel. Om te testen, voer uit:
   * `mvn clean test`
* Integratietests aan serverzijde: Deze voert eenheid-als tests in de AEM-milieu, d.w.z. op de AEM server uit. Om te testen, voer uit:
   * `mvn clean verify -PintegrationTests`
* Client-side Hobbes.js-tests: Dit zijn op JavaScript gebaseerde browsertests die gedrag aan de browserzijde controleren. Testen:
   1. Laad AEM in uw browser zoals u een pagina zou schrijven.
   1. De pagina openen in [Modus Ontwikkelaar](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/developer-mode.html)
   1. Open het linkerdeelvenster en schakel over naar het **Tests** tab.
   1. De gegenereerde zoekopdracht zoeken **MyName-tests** en voert ze uit.

## Volgende stappen {#next-steps}

Dus u hebt het AEM Project Archetype gebouwd en geïnstalleerd. Wat nu? Goed, is het archetype klein, maar bestaat uit vele voorbeelden van krachtige AEM eigenschappen die volgens geadviseerde beste praktijken worden gevormd. Gebruik deze opties om aan te geven hoe u deze functies in uw project kunt gebruiken. Voor elk project moet u waarschijnlijk:

* [Componenten aanpassen door de bestaande kerncomponenten uit te breiden](/help/developing/customizing.md)
* [Extra sjablonen toevoegen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [De lokalisatiestructuur aanpassen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/preparation.html)
* [Meer informatie over de front-end build-module](uifrontend.md)
