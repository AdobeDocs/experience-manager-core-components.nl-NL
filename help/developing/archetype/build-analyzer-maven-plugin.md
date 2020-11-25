---
title: AEM als Cloud Service SDK Build Analyzer Maven Plugin
description: Documentatie voor de lokale Maven-plug-in voor analyse van de build
translation-type: tm+mt
source-git-commit: a58434ebf7ae72472989f2e55d40bfa22fd99208
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 3%

---


# AEM als Cloud Service SDK Build Analyzer Maven Plugin {#maven-analyzer-plugin}

De AEM analyzer Maven plugin analyseert de structuur van de diverse projecten van inhoudspakketten.

Raadpleeg de documentatie [van de plug-in](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) AEM Analyzer Maven voor informatie over het opnemen van de plug-in in een AEM project.

Hieronder ziet u een tabel met een beschrijving van de analyseapparaten die als onderdeel van deze stap worden uitgevoerd. Sommige worden uitgevoerd in de lokale SDK, terwijl andere alleen worden uitgevoerd tijdens de implementatie van de Cloud Manager-pijplijn.

| Module | Functie, voorbeeld en probleemoplossing | Lokale SDK | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Controleert of alle OSGI-bundels hun import-Package-declaraties hebben die zijn voldaan aan de aangifte Export-package van andere opgenomen bundels in het Maven-project. Een fout ziet er als volgt uit: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Om problemen op te lossen, zie of is de bundel die het pakket verstrekt inbegrepen in de plaatsing, of anders bekijk manifest van de bundel die u zou verwachten om te bepalen als de verkeerde naam of de verkeerde versie werd gebruikt. | Ja | Ja |
| `requirements-capabilities` | Controleert of aan alle eisen die in de OSGI-bundels worden gesteld, wordt voldaan door de capaciteitsdeclaraties van andere bundels die in het Maven-project zijn opgenomen. Een fout ziet er als volgt uit: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Om problemen op te lossen, bekijk manifest van de bundel die u een vermogen zou verwachten te verklaren om te bepalen waarom het ontbreekt, of controleer manifest van de verplichte bundel om te zien dat het vereiste in daar correct is. | Ja | Ja |
| `bundle-content` | Geeft een waarschuwing als een bundel aanvankelijke inhoud bevat die met Sling-Initial-Content wordt gespecificeerd, die in de AEM als Cloud Service gegroepeerde milieu problematisch is. De waarschuwing ziet er als volgt uit: <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>Zie Documentatie opnieuw aanwijzen als u problemen wilt oplossen bij het omzetten van de eerste inhoud in instructies voor het opnieuw aanwijzen. | Ja | Ja |
| `bundle-resources` | Geeft een waarschuwing als een bundel middelen bevat die met Sling-Bundle-Middelen kopbal worden gespecificeerd, die in de AEM als Cloud Service gegroepeerde milieu problematisch is. De waarschuwing ziet er als volgt uit:<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Om problemen op te lossen zet de middelen om verklaringen opnieuw te richten, zie Documentatie [opnieuw richten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=en#repo-init). | Ja | Ja |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Deze analysatoren controleren enkele details over de instelling van de API-gebieden in de functies. Voor klanten wordt de configuratie van API-gebieden gegenereerd en niet rechtstreeks door hen opgegeven, worden deze analysatoren ingeschakeld omdat ze ook zijn ingeschakeld in AEMaaCS. Een fout die door een van deze fouten wordt gemaakt, geeft echter aan dat er in het inhoudspakket een fout is opgetreden tijdens het conversieproces van het model. | Ja | Ja |
| `api-regions-crossfeature-dups` | Valideert dat de klant-OSGI-pakketten geen declaraties voor het exporteren hebben die AEM als openbare API van een Cloud Service overschrijven<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>U kunt een pakket dat deel uitmaakt van de openbare API van de AEM niet meer exporteren. | Ja | Ja |