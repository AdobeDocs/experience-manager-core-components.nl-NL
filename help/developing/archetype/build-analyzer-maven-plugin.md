---
title: AEM as a Cloud Service SDK Build Analyzer Maven Plugin
description: Documentatie voor de lokale Maven-plug-in voor analyseprogramma's
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: de26b310-a294-42d6-a0db-91f6036a328c
source-git-commit: 60ec9c1643abce0ee75da5368269928476390440
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# AEM as a Cloud Service SDK Build Analyzer Maven Plugin {#maven-analyzer-plugin}

De AEM as a Cloud Service SDK bouwt Analyzer Maven Plugin analyseert de structuur van de diverse projecten van inhoudspakketten.

Zie de [Documentatie van Maven Plugin](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) voor informatie over de wijze waarop het in een AEM gefabriceerd project kan worden opgenomen.

>[!NOTE]
>
>U wordt aangeraden uw Maven-project bij te werken en te verwijzen naar de meest recente versie van de plug-in in de Maven Central-opslagplaats, op deze locatie: https://repo1.maven.org/maven2/com/adobe/aem/aemanalyser-maven-plugin/

De insteekmodule gebruikt de nieuwste beschikbare SDK in plaats van de SDK die in het project is geconfigureerd.

Hieronder ziet u een tabel met een beschrijving van de analyseapparaten die als onderdeel van deze stap worden uitgevoerd. <!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| Module | Functie, voorbeeld en probleemoplossing | Lokale SDK | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Controleert of alle OSGI-bundels hun import-Package-declaraties hebben die zijn voldaan aan de aangifte Export-package van andere opgenomen bundels in het Maven-project. Een fout ziet er als volgt uit: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Om problemen op te lossen, zie of is de bundel die het pakket verstrekt inbegrepen in de plaatsing, of anders bekijk manifest van de bundel die u zou verwachten om te bepalen als de verkeerde naam of de verkeerde versie werd gebruikt. | Ja | Ja |
| `bundle-unversioned-packages` | Controleert of OSGi-bundels een versie met een uitvoer-Pakket verklaring en een versiewaaier met een invoer-Pakket verklaring specificeren. Een fout ziet er als volgt uit: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is exporting package org.acme.foo without a version.`<p> </p>Om problemen op te lossen, zorg ervoor om toe te voegen `package-info.java` naar dat pakket met de te exporteren versie. | Ja | Ja |
| `requirements-capabilities` | Controleert of aan alle eisen die in de OSGI-bundels worden gesteld, wordt voldaan door de capaciteitsdeclaraties van andere bundels die in het Maven-project zijn opgenomen. Een fout ziet er als volgt uit: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Om problemen op te lossen, bekijk manifest van de bundel die u een vermogen zou verwachten te verklaren om te bepalen waarom het ontbreekt, of controleer manifest van de verplichte bundel om te zien dat het vereiste in daar correct is. | Ja | Ja |
| `bundle-content` | Geeft een waarschuwing als een bundel aanvankelijke inhoud bevat die met Sling-Initial-Content wordt gespecificeerd, die in het AEM as a Cloud Service gegroepeerde milieu problematisch is. De waarschuwing ziet er als volgt uit: <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>Zie Documentatie opnieuw aanwijzen als u problemen wilt oplossen bij het omzetten van de eerste inhoud in instructies voor het opnieuw aanwijzen. | Ja | Ja |
| `bundle-resources` | Hiermee wordt een waarschuwing gegeven als een bundel bronnen bevat die zijn opgegeven met de header Sling-Bundle-Resources. Dit is problematisch in de AEM as a Cloud Service geclusterde omgeving. De waarschuwing ziet er als volgt uit:<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Om problemen op te lossen zet de middelen om verklaringen opnieuw te richten, zie [Documentatie opnieuw plaatsen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=en#repo-init). | Ja | Ja |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Deze analysatoren controleren enkele details met betrekking tot de [inhoudspakket voor conversieproces van model](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=en#deploying) dat artefacten maakt die aan het Model van de Eigenschap van de Verkoop voldoen. Eventuele fouten moeten worden gemeld aan de Adobe Klantenondersteuning. | Ja | Ja |
| `api-regions-crossfeature-dups` | Valideert dat de klant OSGI-bundels geen declaraties voor het exporteren van pakketten hebben die de openbare API van AEM as a Cloud Service overschrijven<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>U kunt een pakket dat deel uitmaakt van de openbare API van de AEM niet meer exporteren. | Ja | Ja |
| `repoinit` | Controleert de syntaxis van alle opnieuw aanwijssecties | Ja | Ja |
| `bundle-nativecode` | Valideert dat OSGI-bundels geen native code installeren. | Ja | Ja |
| `configuration-api` | Valideert belangrijke OSGi-configuraties. <p> </p> `Configuration org.apache.felix.webconsole.internal.servlet.OsgiManager: Configuration is not allowed (com.mysite:mysite.all:1.0.0-SNAPSHOT\|com.mysite:mysite.ui.config:1.0.0-SNAPSHOT)` | Ja | Ja |
| `region-deprecated-api` | Controleert of [afgekeurde api](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-apis.html) wordt gebruikt <p> </p>`[WARNING] com.mysite:mysite.core:1.0.0-SNAPSHOT: Usage of deprecated package found : org.apache.sling.settings : Avoid these features at runtime: run modes, file system access (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | Ja | Ja |
| `artifact-rules` | Valideert afhankelijkheden zoals bundels en inhoudspakketten om bekende problemen in artefacten te voorkomen.<p> </p>`[WARNING] [artifact-rules] com.adobe.acs:acs-aem-commons-bundle:5.0.4: Use at least version 5.0.10 (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | Ja | Ja |
| `aem-env-var` | Controleert het gebruik van env vars volgens de [hulplijn voor variabele naamgeving](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#variable-naming)<p> </p>`[ERROR] Configuration org.apache.felix.webconsole.internal.servlet.OsgiManager: Value for property 'port' must not use env vars prefixed with INTERNAL_ or ADOBE_ (com.mysite1:my-site-1.all:1.0.0-SNAPSHOT\|com.mysite1:my-site-1.ui.config:1.0.0-SNAPSHOT)` | Ja | Ja |
| `content-package-validation` | Hiermee worden validators voor bestanden uitgevoerd. Door gebrek wordt jakobbit-docviewparser toegelaten die op goed gevormde inhoudssyntaxis van xml binnenpakketten controleert die tijdens plaatsing zullen worden geïnstalleerd.<p> </p>`[main] WARN org.apache.sling.feature.analyser.task.impl.CheckContentPackages - ValidationViolation: "jackrabbit-docviewparser: Invalid XML found: The reference to entity "se" must end with the ';' delimiter.", filePath=jcr_root/apps/somename/configs/com.adobe.test.Invalid.xml, nodePath=/apps/somename/configs/com.adobe.test.Invalid`<p> </p>Als u dit wilt corrigeren, controleert u het bestand dat door de analysator is benoemd op XML-problemen. | Ja | Ja |

{style="table-layout:auto"}

## Bekende problemen

Hieronder ziet u een lijst met bekende problemen wanneer u de plug-in Analysator maken gebruikt.

### Kan de plug-in Build Analyzer Maven niet uitvoeren in lokale SDK

Wanneer u de lokale SDK gebruikt met een versie van de plug-in Build Analyzer Maven die lager is dan `1.1.2`Als u de insteekmodule uitvoert, kan dit leiden tot de onderstaande fout. In dit geval werkt u uw project bij naar de meest recente versie van de plug-in.

```txt
[ERROR] Failed to execute goal com.adobe.aem:aemanalyser-maven-plugin:1.1.0:analyse (default-analyse) on project mysite.analyse: Execution default-analyse of goal com.adobe.aem:aemanalyser-maven-plugin:1.1.0:analyse failed: arraycopy: source index -1 out of bounds for char[65536] -> [Help 1]
```

Als u het AEM Archetype van het Project gebruikte om uw project te opstelling, zorg ervoor om het bezit in de wortel aan te passen Maven `pom.xml` zoals hieronder.

```xml
   ...
   <properties>
      ...
      <aemanalyser.version>1.1.2</aemanalyser.version> <!-- Make sure to use the latest release -->
      ...
   </properties>
```
