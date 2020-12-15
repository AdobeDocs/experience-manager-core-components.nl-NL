---
title: Het gebruiken van het AEM Project Archetype
description: Gedetailleerde gebruiksinstructies voor het AEM Project Archetype
translation-type: tm+mt
source-git-commit: 10090b836397af3c9428f99bba72313263f34596
workflow-type: tm+mt
source-wordcount: '2055'
ht-degree: 0%

---


# Projectarchetype {#aem-project-archetype} AEM

Met het AEM Project Archetype maakt u een minimaal Adobe Experience Manager-project op basis van best practices als uitgangspunt voor uw eigen AEM. De eigenschappen die moeten worden verstrekt wanneer het gebruiken van dit archetype staat u toe om de namen voor alle delen van dit project te specificeren evenals bepaalde facultatieve eigenschappen te controleren.

## Waarom Archetype {#why-use-the-archetype} gebruiken

Het gebruiken van het AEM Archetype van het Project plaatst u op de weg naar de bouw van een op best-praktijken-gebaseerd AEM project met enkel een paar aanslagen. Door archetype te gebruiken, zullen alle stukken reeds op zijn plaats zijn zodat terwijl het resulterende project minimaal is, het reeds alle [zeer belangrijke eigenschappen](#what-you-get) van AEM uitvoert zodat alles u moet doen op bovenkant bouwt en zich uitbreidt.

Natuurlijk zijn er vele elementen die in een succesvol AEM project gaan, maar het gebruiken van het AEM Project Archetype is een correcte stichting en sterk geadviseerd voor om het even welk AEM project.

## Aan de slag {#getting-started}

Het project archetype maakt het gemakkelijk om zich op AEM te beginnen ontwikkelen. U kunt de eerste stappen op verschillende manieren uitvoeren.

* WKND-zelfstudie - Voor een grote inleiding tot het ontwikkelen op AEM, inclusief hoe u het archetype optimaal kunt benutten, raadpleegt u de [Aan de slag met AEM Sites - WKND-zelfstudie](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) voor een praktisch voorbeeld waarin u het archetype gebruikt om een eenvoudig project te implementeren.
* Zelfstudie voor WKND-gebeurtenissen - Als u bijzonder geïnteresseerd bent in de ontwikkeling van toepassingen (SPA) op AEM met één pagina, moet u de speciale [WKND-gebeurtenissenzelfstudie](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html) uitchecken.
* Download en start alleen! - U kunt het huidige project archetype gemakkelijk downloaden beschikbaar op GitHub en uw eerste project door [na de eenvoudige stappen onder](#how-to-use-the-archetype) tot stand brengen.

## Wat u krijgt gebruikend Archetype {#what-you-get}

Het AEM Archetype bestaat uit modules:

* **[kern](core.md)**: is een bundel van Java die alle kernfunctionaliteit zoals de diensten OSGi, luisteraars, en planners, evenals component-verwante code van Java zoals servlets en verzoekfilters bevat.
* **[ui.apps](uiapps.md)**: bevat de  `/apps` en  `/etc` delen van het project, d.w.z. JS en CSS clientlibs, componenten, sjablonen, runmode-specifieke configuraties, en Hobbes-tests.
* **[ui.content](uicontent.md)**: bevat voorbeeldinhoud met behulp van de componenten uit de module ui.apps.
* **[ui.tests](uitests.md)**: is een Java-bundel met JUnit-tests die op de server worden uitgevoerd. Deze bundel moet niet op productie worden opgesteld.
* **ui.launch**: bevat lijm die de bundel ui.tests (en afhankelijke bundels) aan de server opstelt en de verre uitvoering JUnit teweegbrengt.
* **[ui.frontend.general](uifrontend.md)**:  **(facultatief)** bevat de artefacten die worden vereist om de algemene Web-pack-gebaseerde voorste-eind bouwstijlmodule te gebruiken.
* **[ui.frontend.response](uifrontend-react.md)**:  **(facultatief)** bevat de artefacten die wanneer het gebruiken van archetype worden vereist om tot SPA projecten te leiden die op React worden gebaseerd.
* **[ui.frontend.angular](uifrontend-angular.md)**:  **(facultatief)** bevat de artefacten die wanneer het gebruiken van archetype worden vereist om een SPA tot stand te brengen die op Hoekig worden gebaseerd.

![](/help/assets/archetype-structure.png)

De modules van AEM Archetype die in Maven worden vertegenwoordigd worden opgesteld aan AEM als inhoudspakketten die de toepassing, de inhoud, en de noodzakelijke bundels OSGi vertegenwoordigen.

## Hoe te om Archetype {#how-to-use-the-archetype} te gebruiken

Om archetype te gebruiken, moet u eerst een project tot stand brengen, dat de modules in een lokale dossierstructuur zoals [eerder beschreven ](#what-you-get) produceert. Als deel van projectgeneratie, kan een aantal eigenschappen voor uw project worden bepaald zoals projectnaam, versie, enz.

Het bouwen van het project met Maven leidt tot de artefacten (pakketten en bundels OSGi), die aan AEM kunnen worden opgesteld. De extra Gemaakt bevelen en de profielen kunnen worden gebruikt om de projectartefacten aan een AEM instantie op te stellen.

### Een project {#create-project} maken

Om begonnen te worden kunt u de [AEM uitbreiding van de Verduistering ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/eclipse.html) het eenvoudigst gebruiken en de Nieuwe tovenaar van het Project volgen en **AEM Monster Meervoudig-Module Project** kiezen om een vrijgegeven versie van archetype te gebruiken.

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

* Stel `XX` in op het [versienummer](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) van het nieuwste AEM Projectarchetype.
* `aemVersion=cloud` voor [AEM instellen als een Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Stel `aemVersion=6.5.0` in voor [Beheerde services van Adobe](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) of op locatie.
De afhankelijkheid van kerncomponenten wordt alleen toegevoegd voor versies zonder cloudnaam omdat de kerncomponenten OTB voor AEM als cloud worden geleverd
Service.
* Pas `appTitle="My Site"` aan om de titel van de website en componentengroepen te bepalen.
* Pas `appId="mysite"` aan om Maven artifactId, de component, config en de namen van de inhoudsomslag, evenals de namen van de cliëntbibliotheek te bepalen.
* Pas `groupId="com.mysite"` aan om Maven groupId en het Bron Pakket van Java te bepalen.
* Zoek de lijst met beschikbare eigenschappen op om te zien of u meer eigenschappen wilt aanpassen.

>[!NOTE]
>
>Het wordt aanbevolen om het `adobe-public`-profiel toe te voegen aan het gemaakte `settings.xml`-bestand om automatisch repo.adobe.com toe te voegen aan het gemaakte constructieproces.
>
>Een voorbeeld van POM [vindt u hier](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

### Eigenschappen {#properties}

De volgende eigenschappen zijn beschikbaar wanneer het creëren van een project gebruikend archetype.

| Naam | Standaard | Beschrijving |
--------------------------|----------------|--------------------
| `appTitle` |  | Toepassingstitel, wordt gebruikt voor de titel van de website en voor componentgroepen (bijvoorbeeld `"My Site"`). |
| `appId` |  | De technische naam, zal voor component, config en de namen van de inhoudsomslag, evenals de namen van de cliëntbibliotheek worden gebruikt (b.v. `"mysite"`). |
| `artifactId` | *`${appId}`* | Basis-Maven-artefactverwijzing (bijvoorbeeld `"mysite"`). |
| `groupId` |  | Basis-Maven-groep-id (bijvoorbeeld `"com.mysite"`). |
| `package` | *`${groupId}`* | Java-bronpakket (bijvoorbeeld `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | Projectversie (bijvoorbeeld `1.0-SNAPSHOT`). |
| `aemVersion` | `6.5.0` | AEM (kan `cloud` voor [AEM als Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) zijn; of `6.5.0`, of `6.4.4` voor [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) of on-premise). |
| `sdkVersion` | `latest` | Wanneer `aemVersion=cloud` een [SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html)-versie kan worden opgegeven (bijvoorbeeld `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Bevat een configuratie van de verzender voor cloud of voor AMS/on-premise, afhankelijk van de waarde van `aemVersion` (kan `y` of `n` zijn). |
| `frontendModule` | `none` | Omvat een vooraf gebouwde module Webpack die de cliëntbibliotheken (kan `general` of `none` voor regelmatige plaatsen zijn; kan `angular` of `react` voor een Enige Pagina zijn app die [SPA Redacteur ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/introduction.html)) uitvoert. |
| `languageCountry` | `en_us` | Taal- en landcode waarmee de inhoudsstructuur wordt gemaakt (bijvoorbeeld `en_us`). |
| `singleCountry` | `y` | Omvat een taal-master inhoudsstructuur (kan `y`, of `n` zijn). |
| `includeExamples` | `y` | Bevat een [Component Library](https://www.aemcomponents.dev/) voorbeeldsite (kan `y` of `n` zijn). |
| `includeErrorHandler` | `n` | Bevat een aangepaste 404-responspagina die globaal is voor de gehele instantie (kan `y` of `n` zijn). |

>[!NOTE]
>
> Als archetype de eerste keer op interactieve wijze wordt uitgevoerd, kunnen de eigenschappen met standaardwaarden niet worden veranderd (zie [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) voor meer details). De waarde kan worden gewijzigd wanneer de vastgoedbevestiging aan het einde wordt geweigerd en de vragenlijst wordt herhaald, of door de parameter in de opdrachtregel door te geven (bijvoorbeeld `-DoptionIncludeExamples=n`).

>[!NOTE]
>
>Wanneer het lopen op Vensters en het produceren van de verzender configuratie, zou u in een opgeheven bevelherinnering of Subsysteem van Vensters voor Linux (zie [kwestie 329](https://github.com/adobe/aem-project-archetype/issues/329)) moeten lopen.

### Profielen {#profiles}

Het gegenereerde beheerde project ondersteunt verschillende implementatieprofielen wanneer `mvn install` wordt uitgevoerd.

| Profiel-id | Beschrijving |
--------------------------|------------------------------
| `autoInstallBundle` | De kernbundel installeren met de maven-sling-plug-in op de felix-console |
| `autoInstallPackage` | Installeer het inhoudspakket ui.content en ui.apps met de insteekmodule content-package-maven naar pakketbeheer om de standaardversie van de auteur op localhost, poort 4502, te gebruiken. Hostnaam en poort kunnen worden gewijzigd met de door de gebruiker gedefinieerde eigenschappen `aem.host` en `aem.port`. |
| `autoInstallPackagePublish` | Installeer het inhoudspakket ui.content en ui.apps met de insteekmodule content-package-maven naar het pakketbeheer om standaard een publicatie-instantie te publiceren op localhost, poort 4503. Hostnaam en poort kunnen worden gewijzigd met de door de gebruiker gedefinieerde eigenschappen `aem.host` en `aem.port`. |
| `autoInstallSinglePackage` | Installeer het inhoudspakket `all` met de insteekmodule content-package-maven in het pakketbeheer om de standaardversie van de auteur op localhost, poort 4502, te gebruiken. Hostnaam en poort kunnen worden gewijzigd met de door de gebruiker gedefinieerde eigenschappen `aem.host` en `aem.port`. |
| `autoInstallSinglePackagePublish` | Installeer het `all`-inhoudspakket met de insteekmodule content-package-maven in het pakketbeheer om de standaardpublicatie-instantie op localhost, poort 4503, in te stellen. Hostnaam en poort kunnen worden gewijzigd met de door de gebruiker gedefinieerde eigenschappen `aem.host` en `aem.port`. |
| `integrationTests` | Voert de verstrekte integratietests op de AEM instantie (slechts voor de `verify` fase) in werking |

### {#building-and-installing} bouwen en installeren

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

`pom.xml` bij de wortel van het project (`<src-directory>/<project>/pom.xml`) is gekend als ouder POM en drijft de structuur van het project evenals beheert gebiedsdelen en bepaalde globale eigenschappen van het project.

### Algemene projecteigenschappen {#global-properties}

Het `<properties>` gedeelte van bovenliggende POM definieert verschillende algemene eigenschappen die belangrijk zijn voor de implementatie van uw project op een AEM instantie, zoals gebruikersnaam/wachtwoord, hostnaam/poort, enz.

Deze eigenschappen worden opstelling om aan een lokale AEM instantie op te stellen, aangezien dit de gemeenschappelijkste bouwstijl is die de ontwikkelaars zullen doen. Er zijn eigenschappen die in een auteurinstantie en een publicatieinstantie moeten worden geïmplementeerd. Dit is ook waar de geloofsbrieven worden geplaatst om met de AEM instantie voor authentiek te verklaren. De standaardreferenties voor admin:admin worden gebruikt.

Deze eigenschappen zijn opstelling zodat zij kunnen worden met voeten getreden wanneer het opstellen aan hogere niveaumilieu&#39;s. Op deze manier hoeven de POM-bestanden niet te worden gewijzigd, maar variabelen zoals `aem.host` en `sling.password` kunnen via opdrachtregelargumenten worden overschreven:

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Modulestructuur {#module-structure}

De `<modules>` sectie van ouderPOM bepaalt de modules die het project zal bouwen. Door gebrek bouwt het project [de eerder bepaalde standaardmodules](#what-you-get): core, ui.apps, ui.content, ui.tests, en it.launch. Meer modules kunnen altijd worden toegevoegd aangezien een project evolueert.

### Afhankelijkheden {#dependencies}

De `<dependencyManagement>` sectie van ouderPOM bepaalt alle gebiedsdelen en versies van APIs die in het project worden gebruikt. Versies moeten worden beheerd in de bovenliggende POM. Submodules zoals core en ui.apps mogen geen versiegegevens bevatten.

#### Uber-jar {#uber-jar}

Één van de belangrijkste gebiedsdelen is [AEM uber-jar](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/ht-projects-maven.html#ExperienceManagerAPIDependencies). Dit omvat alle AEM APIs met enkel één enkele gebiedsdeelingang voor de versie van AEM.

>[!NOTE]
>
>Als beste praktijken zou u de uber-jar versie moeten bijwerken om de doelversie van AEM aan te passen. Bijvoorbeeld, als u van plan bent om aan AEM 6.4 op te stellen zou u de versie van uber-jar aan 6.4.0 moeten bijwerken.

#### Kerncomponenten {#core-components}

Het AEM Projectarchetype van natuurlijk hefboomwerkingen de Componenten van de Kern.

De kerncomponenten worden automatisch in AEM in de standaardrunmode geïnstalleerd en door de steekproefWKND plaats gebruikt. In een [productiestroom](https://docs.adobe.com/content/help/en/experience-manager-65/administering/security/production-ready.html) (`nosamplecontent`) zijn de Componenten van de Kern niet beschikbaar.

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
   1. Open de pagina in [Modus Ontwikkelaar](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/developer-mode.html)
   1. Open het linkerdeelvenster en schakel over naar het tabblad **Tests**.
   1. Zoek de gegenereerde **MyName Tests** en voer deze uit.

## Volgende stappen {#next-steps}

Dus u hebt het AEM Project Archetype gebouwd en geïnstalleerd. Wat nu? Goed, is het archetype klein, maar bestaat uit vele voorbeelden van krachtige AEM eigenschappen die volgens geadviseerde beste praktijken worden gevormd. Gebruik deze opties om aan te geven hoe u deze functies in uw project kunt gebruiken. Voor elk project moet u waarschijnlijk:

* [Componenten aanpassen door de bestaande kerncomponenten uit te breiden](/help/developing/customizing.md)
* [Extra sjablonen toevoegen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [De lokalisatiestructuur aanpassen](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/tc-prep.html)
* [Meer informatie over de front-end build-module](uifrontend.md)
