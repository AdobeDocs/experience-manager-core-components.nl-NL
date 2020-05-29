---
title: AEM-projectarchetype gebruiken
description: Gedetailleerde gebruiksinstructies voor het AEM Project Archetype
translation-type: tm+mt
source-git-commit: 6f7166c46940ed451721e0760d565d58efe412ab
workflow-type: tm+mt
source-wordcount: '2057'
ht-degree: 0%

---


# AEM-projectarchetype {#aem-project-archetype}

Het AEM Project Archetype leidt tot een minimaal, op best-praktijken-gebaseerd project van de Manager van de Ervaring van Adobe als uitgangspunt voor uw eigen projecten AEM. De eigenschappen die moeten worden verstrekt wanneer het gebruiken van dit archetype staat u toe om de namen voor alle delen van dit project te specificeren evenals bepaalde facultatieve eigenschappen te controleren.

## Waarom het Archetype gebruiken {#why-use-the-archetype}

Met het AEM Project Archetype kunt u een AEM-project op basis van best practices bouwen met slechts een paar toetsaanslagen. Door het archetype te gebruiken, zullen alle stukken reeds op zijn plaats zijn zodat terwijl het resulterende project minimaal is, het reeds alle [belangrijkste eigenschappen](#what-you-get) van AEM uitvoert zodat alles u moet doen voortbouwen en zich uitbreiden.

Natuurlijk zijn er vele elementen die in een succesvol AEM- project gaan, maar het gebruiken van het Archieftype van het Project AEM is een correcte stichting en sterk geadviseerd voor om het even welk AEM- project.

## Aan de slag {#getting-started}

Met het projectarchetype is het gemakkelijk om aan de slag te gaan met de ontwikkeling van AEM. U kunt de eerste stappen op verschillende manieren uitvoeren.

* WKND-zelfstudie - Voor een geweldige introductie van het ontwikkelen op AEM, inclusief hoe u het archetype optimaal kunt benutten, raadpleegt u de [Getting Started with AEM Sites - WKND-zelfstudie](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) voor een praktisch voorbeeld waarin u het archetype gebruikt om een eenvoudig project te implementeren.
* WKND-gebeurtenissenzelfstudie - Als u bijzonder geïnteresseerd bent in de ontwikkeling van één pagina (SPA) voor toepassingen op AEM, moet u de speciale [WKND-gebeurtenissenzelfstudie](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)uitchecken.
* Download en start alleen! - U kunt het huidige project archetype gemakkelijk downloaden beschikbaar op GitHub en uw eerste project tot stand brengen door de eenvoudige hieronder [stappen te](#how-to-use-the-archetype)volgen.

## Wat u krijgt met Archetype {#what-you-get}

Het AEM Archetype bestaat uit modules:

* **[kern](core.md)**: is een bundel van Java die alle kernfunctionaliteit zoals de diensten OSGi, luisteraars, en planners, evenals component-verwante code van Java zoals servlets en verzoekfilters bevat.
* **[ui.apps](uiapps.md)**: bevat de`/apps`en`/etc`delen van het project, d.w.z. JS en CSS clientlibs, componenten, sjablonen, runmode-specifieke configuraties, en Hobbes-tests.
* **[ui.content](uicontent.md)**: bevat voorbeeldinhoud met behulp van de componenten uit de module ui.apps.
* **[ui.tests](uitests.md)**: is een Java-bundel met JUnit-tests die op de server worden uitgevoerd. Deze bundel moet niet op productie worden opgesteld.
* **ui.launch**: bevat lijm die de bundel ui.tests (en afhankelijke bundels) aan de server opstelt en de verre uitvoering JUnit teweegbrengt.
* **[ui.frontend.general](uifrontend.md)**:**(facultatief)**bevat de artefacten die worden vereist om de algemene Web-pack-gebaseerde voorste-eind bouwstijlmodule te gebruiken.
* **[ui.frontend.response](uifrontend-react.md)**:**(facultatief)**bevat de artefacten die wanneer het gebruiken van archetype worden vereist om tot een projecten van het KUUROORD te leiden die op Reageren worden gebaseerd.
* **[ui.frontend.angular](uifrontend-angular.md)**:**(facultatief)**bevat de artefacten die wanneer het gebruiken van archetype worden vereist om tot een projecten van het KUUROORD te leiden die op Hoekig worden gebaseerd.

![](/help/assets/archetype-structure.png)

De modules van het Archetype van AEM in Maven worden vertegenwoordigd opgesteld aan AEM als inhoudspakketten die de toepassing, de inhoud, en de noodzakelijke OSGi bundels vertegenwoordigen.

## Het gebruiken van Archetype {#how-to-use-the-archetype}

Om archetype te gebruiken, moet u eerst een project tot stand brengen, dat de modules in een lokale dossierstructuur zoals [eerder beschreven](#what-you-get)produceert. Als deel van projectgeneratie, kan een aantal eigenschappen voor uw project worden bepaald zoals projectnaam, versie, enz.

Het bouwen van het project met Maven leidt tot de artefacten (pakketten en bundels OSGi), die aan AEM kunnen worden opgesteld. De extra Gemaakt bevelen en de profielen kunnen worden gebruikt om de projectartefacten aan een instantie op te stellen AEM.

### Een project maken {#create-project}

Om begonnen te worden kunt u de uitbreiding [van de Verduistering van](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/aem-eclipse.html) AEM het eenvoudigst gebruiken en de Nieuwe tovenaar van het Project volgen en **AEM Monster van de Steekproef van de Module Project** kiezen om een vrijgegeven versie van archetype te gebruiken.

Natuurlijk kunt u ook Maven rechtstreeks aanroepen.

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.granite.archetypes \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Stel dit in `XX` op het [versienummer](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) van het nieuwste AEM-projecttype.
* Set `aemVersion=cloud` for [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Stel deze optie in `aemVersion=6.5.0` voor [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)of on-premise.
De afhankelijkheid van kerncomponenten wordt alleen toegevoegd voor versies met een andere naam dan de cloud, aangezien de Core Components OTB voor AEM als CloudService wordt geleverd.
* Pas `appTitle="My Site"` de titel van de website en de groepen componenten aan.
* Pas `appId="mysite"` aan om Maven artifactId, de component, config en de namen van de inhoudsomslag, evenals de namen van de cliëntbibliotheek te bepalen.
* Pas `groupId="com.mysite"` aan om Maven groupId en het Bron Pakket van Java te bepalen.
* Zoek de lijst met beschikbare eigenschappen op om te zien of u meer eigenschappen wilt aanpassen.

>[!NOTE]
>
>U kunt het beste het `adobe-public` profiel toevoegen aan uw Maven- `settings.xml` bestand om automatisch repo.adobe.com toe te voegen aan het gemaakte buildproces.
>
>Hier [vindt](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html)u een voorbeeld van een POM.

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
| `aemVersion` | `6.5.0` | Doel-AEM-versie (kan `cloud` voor [AEM als cloudservice](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)worden gebruikt; of `6.5.0`, `6.4.4`, of `6.3.3` voor [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) of on-premise). |
| `sdkVersion` | `latest` | Wanneer `aemVersion=cloud` een [SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) -versie kan worden opgegeven (bijvoorbeeld `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | Bevat een configuratie van de dispatcher voor de cloud of voor AMS/on-premise, afhankelijk van de waarde van `aemVersion` (kan zijn `y` of `n`). |
| `frontendModule` | `none` | Omvat een vooraf ingebouwd module Webpack die de cliëntbibliotheken (kan `general` of `none` voor regelmatige plaatsen zijn) produceert; kan `angular` of `react` voor een Enige PaginaApp zijn die de Redacteur [van het](https://docs.adobe.com/content/help/en/experience-manager-65/developing/headless/spas/spa-overview.html)KUUROORD) uitvoert. |
| `languageCountry` | `en_us` | Taal- en landcode waarmee de inhoudsstructuur wordt gemaakt (bijvoorbeeld `en_us`). |
| `singleCountry` | `y` | Bevat een taalstramieninhoudsstructuur (kan zijn `y`, of `n`). |
| `includeExamples` | `y` | Bevat een voorbeeldsite van de [componentbibliotheek](https://www.aemcomponents.dev/) (kan `y`of `n`). |
| `includeErrorHandler` | `n` | Bevat een aangepaste 404-responspagina die globaal is voor de gehele instantie (kan zijn `y` of `n`). |

>[!NOTE]
> Als het archetype de eerste keer op interactieve wijze wordt uitgevoerd, kunnen de eigenschappen met standaardwaarden niet worden veranderd (zie [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) voor meer details). De waarde kan worden gewijzigd wanneer de vastgoedbevestiging aan het einde wordt geweigerd en de vragenlijst wordt herhaald, of door de parameter in de opdrachtregel door te geven (bijvoorbeeld `-DoptionIncludeExamples=n`).

>[!NOTE]
>Wanneer het lopen op Vensters en het produceren van de berichtcherconfiguratie, zou u in een opgeheven bevelherinnering of Subsysteem van Vensters voor Linux (zie [kwestie 329](https://github.com/adobe/aem-project-archetype/issues/329)) moeten lopen.

### Profielen {#profiles}

Het gegenereerde beheerde project ondersteunt verschillende implementatieprofielen wanneer het wordt uitgevoerd `mvn install`.

| Profiel-id | Beschrijving |
--------------------------|------------------------------
| `autoInstallBundle` | De kernbundel installeren met de maven-sling-plug-in op de felix-console |
| `autoInstallPackage` | Installeer het inhoudspakket ui.content en ui.apps met de insteekmodule content-package-maven naar pakketbeheer om de standaardversie van de auteur op localhost, poort 4502, te gebruiken. Hostnaam en poort kunnen worden gewijzigd met de eigenschappen `aem.host` en `aem.port` door de gebruiker gedefinieerd. |
| `autoInstallPackagePublish` | Installeer het inhoudspakket ui.content en ui.apps met de insteekmodule content-package-maven naar het pakketbeheer om standaard een publicatie-instantie te publiceren op localhost, poort 4503. Hostnaam en poort kunnen worden gewijzigd met de eigenschappen `aem.host` en `aem.port` door de gebruiker gedefinieerd. |
| `autoInstallSinglePackage` | Installeer het `all` inhoudspakket met de insteekmodule content-package-maven in het pakketbeheer om de standaardversie van de auteur op localhost, poort 4502, in te stellen. Hostnaam en poort kunnen worden gewijzigd met de eigenschappen `aem.host` en `aem.port` door de gebruiker gedefinieerd. |
| `autoInstallSinglePackagePublish` | Installeer het `all` inhoudspakket met de insteekmodule content-package-maven in het pakketbeheer om de standaardpublicatie-instantie op localhost, poort 4503, in te stellen. Hostnaam en poort kunnen worden gewijzigd met de eigenschappen `aem.host` en `aem.port` door de gebruiker gedefinieerd. |
| `integrationTests` | Voert de verstrekte integratietests op de instantie AEM (slechts voor de `verify` fase) uit |

### Samenstellen en installeren {#building-and-installing}

Om alle modules te bouwen die in de folder van de projectwortel lopen, gebruik het volgende Gemaakt bevel.

```
mvn clean install
```

Als u een lopende instantie AEM hebt, kunt u het volledige project bouwen en verpakken en in AEM met het volgende Geweven bevel opstellen.

```
mvn clean install -PautoInstallPackage
```

Voer deze opdracht uit om de opdracht te implementeren in een publicatieinstantie.

```
mvn clean install -PautoInstallPackagePublish
```

U kunt ook deze opdracht uitvoeren als u wilt implementeren in een publicatieinstantie.

```
mvn clean install -PautoInstallPackage -Daem.port=4503
```

U kunt ook alleen de bundel naar de auteur implementeren door deze opdracht uit te voeren.

```
mvn clean install -PautoInstallBundle
```

## Bovenliggende POM {#parent-pom}

De `pom.xml` basis van het project (`<src-directory>/<project>/pom.xml`) wordt de bovenliggende POM genoemd en drijft de structuur van het project aan en beheert afhankelijkheden en bepaalde algemene eigenschappen van het project.

### Algemene projecteigenschappen {#global-properties}

De `<properties>` sectie van ouderPOM bepaalt verscheidene globale eigenschappen die voor de plaatsing van uw project op een instantie AEM zoals gebruikersnaam/wachtwoord, gastheernaam/haven, enz. belangrijk zijn.

Deze eigenschappen worden opstelling om aan een lokale instantie AEM op te stellen, aangezien dit de gemeenschappelijkste bouwstijl is die de ontwikkelaars zullen doen. Er zijn eigenschappen die in een auteurinstantie en een publicatieinstantie moeten worden geïmplementeerd. Dit is ook waar de geloofsbrieven worden geplaatst om met de instantie van AEM voor authentiek te verklaren. De standaardreferenties voor admin:admin worden gebruikt.

Deze eigenschappen zijn opstelling zodat zij kunnen worden met voeten getreden wanneer het opstellen aan hogere niveaumilieu&#39;s. Op deze manier hoeven de POM-bestanden niet te worden gewijzigd, maar variabelen zoals `aem.host` en `sling.password` kunnen via opdrachtregelargumenten worden overschreven:

```
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### Modulestructuur {#module-structure}

De `<modules>` sectie van ouderPOM bepaalt de modules die het project zal bouwen. Door gebrek bouwt het project [de eerder bepaalde](#what-you-get)standaardmodules: core, ui.apps, ui.content, ui.tests, en it.launch. Meer modules kunnen altijd worden toegevoegd aangezien een project evolueert.

### Afhankelijkheden {#dependencies}

De `<dependencyManagement>` sectie van ouderPOM bepaalt alle gebiedsdelen en versies van APIs die in het project worden gebruikt. Versies moeten worden beheerd in de bovenliggende POM. Submodules zoals core en ui.apps mogen geen versiegegevens bevatten.

#### Uber-Jar {#uber-jar}

Een van de belangrijkste afhankelijkheden is de [AEM-uber-jar](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/ht-projects-maven.html#ExperienceManagerAPIDependencies). Dit omvat alle AEM APIs met enkel één enkel gebiedsdeelingang voor de versie van AEM.

>[!NOTE]
>
>U kunt het beste de Auto-Jar versie bijwerken zodat deze overeenkomt met de doelversie van AEM. Bijvoorbeeld, als u van plan bent om aan AEM 6.4 op te stellen zou u de versie van uber-jar aan 6.4.0 moeten bijwerken.

#### Kernonderdelen {#core-components}

Het AEM Project Archetype maakt natuurlijk gebruik van de Core Components.

De componenten van de Kern worden geïnstalleerd in AEM automatisch op de standaardrunmode en gebruikt door de steekproefWij.Retail plaats. In een [productiestroom](https://docs.adobe.com/content/help/en/experience-manager-65/administering/security/production-ready.html) (`nosamplecontent`) zijn de Core Components niet beschikbaar.

Daarom is het, om de Componenten van de Kern in alle plaatsingen te gebruiken, een beste praktijk om hen als deel van het Maven project te omvatten.

>[!NOTE]
>
>Elke versie van de Core Components wordt over het algemeen gevolgd door een versie van het AEM Project Archetype zodat het recentste archetype de recentste versie van de kerncomponenten gebruikt.
>
>Het is echter mogelijk dat een nieuwe versie van het archetype niet direct volgt op een nieuwe versie van de Core Components, dus u wilt mogelijk de afhankelijkheid van de Core Components bijwerken naar de nieuwste versie.

>[!NOTE]
>
>core.wcm.components.examples zijn een reeks steekproefpagina&#39;s die voorbeelden van de Componenten van de Kern illustreren. Als beste praktijken, wanneer het opstellen van een project voor productiegebruik zou u deze gebiedsdeel en subpackage opneming moeten verwijderen.

## Testen {#testing}

Het project bevat drie testniveaus en omdat het verschillende typen tests zijn, worden deze op verschillende manieren of op verschillende plaatsen uitgevoerd.

* Eenheidstest in kern: Dit toont de klassieke eenheidstests van de code in de bundel. U test als volgt:
   * `mvn clean test`
* Integratietests aan serverzijde: Deze voert eenheid-als tests in het milieu AEM, d.w.z. op de server AEM uit. U test als volgt:
   * `mvn clean verify -PintegrationTests`
* Client-side Hobbes.js-tests: Dit zijn op JavaScript gebaseerde browsertests die gedrag aan de browserzijde controleren. Testen:
   1. Laad AEM in uw browser zoals u een pagina zou ontwerpen.
   1. De pagina openen in de modus [Ontwikkelaar](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/developer-mode.html)
   1. Open het linkerdeelvenster en schakel over naar het tabblad **Tests** .
   1. Vind de geproduceerde Tests **MyName** en stel hen in werking.

## Volgende stappen {#next-steps}

Dus u hebt het AEM Project Archetype gebouwd en geïnstalleerd. Wat nu? Goed, is het archetype klein, maar bestaat uit vele voorbeelden van krachtige eigenschappen AEM die volgens geadviseerde beste praktijken worden gevormd. Gebruik deze opties om aan te geven hoe u deze functies in uw project kunt gebruiken. Voor elk project moet u waarschijnlijk:

* [Componenten aanpassen door de bestaande kerncomponenten uit te breiden](/help/developing/customizing.md)
* [Extra sjablonen toevoegen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [De lokalisatiestructuur aanpassen](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/tc-prep.html)
* [Meer informatie over de front-end build-module](uifrontend.md)
