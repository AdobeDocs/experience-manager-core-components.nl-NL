---
title: AEM als Cloud Service SDK Build Analyzer Maven Plugin
description: Documentatie voor de lokale Maven-plug-in voor analyse van de build
translation-type: tm+mt
source-git-commit: b95515dba74486add7f50bc8984f4358090e735c
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 3%

---


# AEM als Cloud Service SDK Build Analyzer Maven Plugin {#maven-analyzer-plugin}

De AEM als Cloud Service SDK bouwt Analyzer Maven Plugin analyseert de structuur van de diverse projecten van inhoudspakketten.

Zie de [documentatie van de Geweven Insteekmodule](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) voor informatie over hoe te om het in een AEM in kaart te brengen project te omvatten.

Hieronder ziet u een tabel met een beschrijving van de analyseapparaten die als onderdeel van deze stap worden uitgevoerd. <!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| Module | Functie, voorbeeld en probleemoplossing | Lokale SDK | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Controleert of alle OSGI-bundels hun import-Package-declaraties hebben die zijn voldaan aan de aangifte Export-package van andere opgenomen bundels in het Maven-project. Een fout ziet er als volgt uit: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Om problemen op te lossen, zie of is de bundel die het pakket verstrekt inbegrepen in de plaatsing, of anders bekijk manifest van de bundel die u zou verwachten om te bepalen als de verkeerde naam of de verkeerde versie werd gebruikt. | Ja | Ja |
| `requirements-capabilities` | Controleert of aan alle eisen die in de OSGI-bundels worden gesteld, wordt voldaan door de capaciteitsdeclaraties van andere bundels die in het Maven-project zijn opgenomen. Een fout ziet er als volgt uit: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Om problemen op te lossen, bekijk manifest van de bundel die u een vermogen zou verwachten te verklaren om te bepalen waarom het ontbreekt, of controleer manifest van de verplichte bundel om te zien dat het vereiste in daar correct is. | Ja | Ja |
| `bundle-content` | Geeft een waarschuwing als een bundel aanvankelijke inhoud bevat die met Sling-Initial-Content wordt gespecificeerd, die in de AEM als Cloud Service gegroepeerde milieu problematisch is. De waarschuwing ziet er als volgt uit: <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>Zie Documentatie opnieuw aanwijzen als u problemen wilt oplossen bij het omzetten van de eerste inhoud in instructies voor het opnieuw aanwijzen. | Ja | Ja |
| `bundle-resources` | Geeft een waarschuwing als een bundel middelen bevat die met Sling-Bundle-Middelen kopbal worden gespecificeerd, die in de AEM als Cloud Service gegroepeerde milieu problematisch is. De waarschuwing ziet er als volgt uit:<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Zie [Documentatie opnieuw aanwijzen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=en#repo-init) om problemen op te lossen bij het omzetten van de bronnen naar instructies. | Ja | Ja |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Deze analysatoren controleren sommige details met betrekking tot het [inhoudspakket om model omzettingsproces te kenmerken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=en#deploying) dat artefacten tot stand brengt die aan het Model van de Eigenschap van de Verkoop aanpassen. Eventuele fouten moeten worden gemeld aan de Adobe Klantenondersteuning. | Ja | Ja |
| `api-regions-crossfeature-dups` | Valideert dat de klant-OSGI-pakketten geen declaraties voor het exporteren hebben die AEM als openbare API van een Cloud Service overschrijven<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>U kunt een pakket dat deel uitmaakt van de openbare API van de AEM niet meer exporteren. | Ja | Ja |