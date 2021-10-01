---
title: Basiscomponenten ontwikkelen
description: De componenten van de Kern verstrekken robuuste en verlengbare basiscomponenten die eigenschap-rijke mogelijkheden, ononderbroken levering, componentenversioning, moderne implementatie, leuning prijsverhoging, en JSON de uitvoer van inhoud aanbieden.
role: Architect, Developer, Admin
exl-id: 0f79cac1-a3b0-487e-90be-0bd8263d3912
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: tm+mt
source-wordcount: '1583'
ht-degree: 1%

---

# Basiscomponenten ontwikkelen {#developing-core-components}

## Wanneer moet u de kerncomponenten gebruiken? {#when-to-use-the-core-components}

Aangezien de Componenten van de Kern allen-nieuw zijn, en veelvoudige voordelen aanbieden, wordt het geadviseerd voor nieuwe AEM projecten om hen te gebruiken. Voor bestaande projecten zou een migratie deel moeten uitmaken van een grotere projectinspanning, bijvoorbeeld een herbranding of het totale refactoring.

Daarom geeft Adobe de volgende aanbevelingen:

* **Nieuwe**
ProjectenNieuwe projecten zouden altijd moeten proberen om de Componenten van de Kern te gebruiken. Als de Componenten van de Kern niet direct of [extended](customizing.md) kunnen worden gebruikt om aan projectvereisten te voldoen, dan creeer een douanecomponent na de componentenarchitectuur die in kerncomponenten wordt vermeld. Vermijd het gebruik van [stichtingscomponenten](/help/versions.md#foundation-component-support), tenzij anders mogelijk.
* **Bestaande**
ProjectenRecommendation blijft het gebruiken van de  [stichtingscomponenten](/help/versions.md#foundation-component-support), tenzij een plaats of componentenrefactoring wordt gepland.\
   Aangezien zij zeer wijd door de meeste bestaande projecten worden gebruikt, zullen de stichtingscomponenten [blijven worden gesteund.](/help/versions.md#foundation-component-support)
* **Nieuwe aangepaste**
componentenBepaal of een bestaande  [kerncomponent kan worden aangepast](customizing.md).\
   Zo niet, dan wordt aanbevolen een nieuwe aangepaste component te maken volgens de [Componentrichtlijnen](guidelines.md).
* **Bestaande aangepaste**
componentenAls uw componenten naar behoren werken, kunt u ze op de juiste wijze houden.
\
   Als dat niet het geval is, raadpleegt u &quot;Nieuwe aangepaste componenten&quot; hierboven.

## Hoe te met de Componenten van de Kern Succes {#how-to-succeed}

De kerncomponenten zijn krachtig, flexibel en gebruiksvriendelijk. [Op basis van enkele belangrijke ](success.md) richtlijnen kunt u ervoor zorgen dat uw project met de Core Components een succes wordt.

## Migreren naar de kerncomponenten

Om het even welk nieuw project zou met de Componenten van de Kern moeten worden uitgevoerd. Nochtans zullen de bestaande projecten gewoonlijk uitgebreide implementaties van de Componenten van de Stichting hebben.

### Migreren van stichtingscomponenten {#from-foundation}

Een grotere inspanning op een bestaand project (bijvoorbeeld rebranding of het algemene refactoring) biedt vaak een kans om aan de Componenten van de Kern te migreren. Om deze migratie te vergemakkelijken, heeft Adobe een aantal migratiehulpmiddelen verstrekt om de goedkeuring van de Componenten van de Kern en de recentste AEM technologie te bevorderen.

[De ](http://opensource.adobe.com/aem-modernize-tools/) Toolsallow van de Modernisering van de AEM voor de gemakkelijke omzetting van:

* Statische sjablonen converteren naar bewerkbare sjablonen
* Ontwerpconfiguraties omzetten naar beleid
* Elementaire componenten omzetten naar kerncomponenten
* De klassieke interface converteren naar een interface met aanraakbediening

Voor meer informatie over het gebruik van deze hulpmiddelen, [zie hun documentatie](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>De AEM Moderniseren Hulpmiddelen zijn een communautaire inspanning en niet gesteund of door Adobe gewaarborgd.

## Migratie via Verplaatsen naar AEM als Cloud Service {#via-aemaacs}

Omdat AEM als Cloud Service automatisch met de recentste versie van de Componenten van de Kern komt, wanneer u zich van een op-gebouw AEM installatie beweegt, zult u om het even welke gebiedsdeel aan de Componenten van de Kern in uw projecten `pom.xml` dossier moeten verwijderen.

Uw proxycomponenten werken nog steeds zoals voorheen, omdat   proxy&#39;s verwijzen naar het vereiste supertype en het supertekstpad heeft de versie erin. Op deze manier, eenvoudig het verwijderen van de gebiedsdelen laat de Componenten van de Kern toe om in AEMaaCS te werken enkel zoals zij op-gebouw deden.

Net als bij elk ander AEMaaCS-project moet u ook een afhankelijkheid toevoegen aan de AEM SDK-jar. Dit is niet specifiek voor de Core Components, maar is vereist.

```xml
<dependency>
   <groupId>com.adobe.aem</groupId>
   <artifactId>aem-sdk-api</artifactId>
</dependency>
```

Zie het document [AEM Projectstructuur](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) voor meer informatie over projecten AEMaaCS.

## Ondersteuning van kerncomponenten {#core-component-support}

De Componenten van de kern zijn een integraal deel van AEM en gesteund zoals is, onder de zelfde voorwaarden alsof zij als deel van Quickstart werden geleverd.

De algemene regel is, net als andere AEM productkenmerken: Componenten worden eerst aangekondigd te worden vervangen en de oudste verwijderd voor de volgende AEM. Dit geeft klanten minstens één versiecyclus om naar de nieuwe versie van de component te bewegen, alvorens zijn steun te laten vallen.

In de versie van elke component worden duidelijk de AEM versies vermeld die worden ondersteund. Wanneer de steun voor een versie van AEM beëindigt, dan ook de steun van de Componenten van de Kern voor die versie van AEM.

Zie de pagina [Kerncomponenten aanpassen](customizing.md) voor meer informatie over de ondersteuning van componentaanpassingen.


## Technische mogelijkheden {#technical-capabilities}

De volgende lijst geeft een overzicht van de verschillen tussen kerncomponenten en stichtingscomponenten.

Voor details over hun auteursmogelijkheden en opties om hen pre-configureerbaar te maken, [verwijs naar de auteurspagina over hen](/help/get-started/authoring.md).

| **Capaciteit** | **Kerncomponent** | **Foundation-component** |
|-----|---|---|
| Logische implementatie | Java POJO&#39;s met [Sling Models](https://sling.apache.org/documentation/bundles/models.html) annotaties | JSP-code |
| Opmaakdefinitie | [HTML-sjabloonsyntaxis](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html)  (HTL) | JSP-code |
| XSS-ontsmetting | Geautomatiseerd door HTML | Meestal handmatig |
| Naam van CSS-klassen | Gestandaardiseerde naamgevingsconventie gebaseerd op de notatie [Blokelelement modifier](https://getbem.com/) (BEM) (vanaf release 2.0.0) | Aangepaste schema&#39;s |
| Dialoogdefinitie | [Koraal 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Koraal 2 + klassieke gebruikersinterface |
| JSON-uitvoer | [Sling Modellen Exporter met Jackson serialization](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Standaard Sling-servlet |
| Versioning | [Voor het model en het HTL](guidelines.md) | Geen |
| Testen | Eenheidstests + integratietests | Integratietests |
| Aflevering | [Via public GitHub](https://github.com/adobe/aem-core-wcm-components) | Via Quickstart |
| Licentie | [Apache-licentie](https://www.apache.org/licenses/LICENSE-2.0) | Adobe-bedrijfseigen |
| Bijdrage | Via pull request | Niet mogelijk |
| Toegankelijkheid | Volledig compatibel met de [WCAG 2.0 AA-standaard](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) | Slechts gedeeltelijk compatibel met [WCAG 2.0 AA norm](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |

## Componentlijst {#component-list}

De volgende lijst maakt een lijst van de beschikbare Componenten van de Kern, die met hun API verbinden, en wijst op welke stichtingscomponenten zij vervangen.

| Kerncomponent | Beschrijving | Vervangen basiscomponent(en) |
|---|---|---|
| [Pagina](https://adobe.com/go/aem_cmp_tech_page_v2) | Responsieve pagina werken met sjablooneditor | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Broodkruimel](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2) | Navigatie in paginahiërarchie | `/libs/foundation/components/breadcrumb` |
| [Titel](https://adobe.com/go/aem_cmp_tech_title_v2) | H1-H6-titel | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Tekst](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | RTF | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Afbeelding](https://adobe.com/go/aem_cmp_tech_image_v2) | Slim en wazig laden van optimale weergavegrootte | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Lijst](https://adobe.com/go/aem_cmp_tech_list_v2) | Lijst met pagina&#39;s | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Delen van sociale media](https://adobe.com/go/aem_cmp_tech_sharing_v1) | Delen via facebook en Pinterest widget | `-` |
| [Formuliercontainer](https://adobe.com/go/aem_cmp_tech_form_container_v2) | Responsief formulieralineasysteem | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Formuliertekst](https://adobe.com/go/aem_cmp_tech_form_text_v2) | Tekstinvoerveld | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Formulieropties](https://adobe.com/go/aem_cmp_tech_form_options_v2) | Invoerveld Meerdere opties | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Formulier verborgen](https://adobe.com/go/aem_cmp_tech_form_hidden_v2) | Verborgen invoerveld | `/libs/foundation/components/form/hidden` |
| [Formulierknop](https://adobe.com/go/aem_cmp_tech_form_button_v2) | Verzenden of aangepaste knop | `/libs/foundation/components/form/submit` |
| [Navigatie](https://adobe.com/go/aem_cmp_tech_navigation_v1) | Een sitenavigatie-component die de geneste paginahiërarchie weergeeft | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Taalnavigatie](https://adobe.com/go/aem_cmp_tech_langnav_v1) | Een taal- en landswitch die de algemene taalstructuur opsomt | `-` |
| [Snel zoeken](https://adobe.com/go/aem_cmp_tech_search_v1) | Een zoekcomponent die de resultaten als suggesties ter plaatse in een vervolgkeuzemenu weergeeft | `/libs/foundation/components/search` |
| [Teaser](https://adobe.com/go/aem_cmp_tech_teaser_v1) | Hiermee kan de auteur van de inhoud eenvoudig een gummetje maken om inhoud te verfijnen met een afbeelding, titel of RTF-tekst en een koppeling maken naar verdere inhoud of andere handelingen | `-` |
| [Tabs](https://adobe.com/go/aem_cmp_tech_tabs_v1) | Hiermee kan de auteur van de inhoud de pagina-inhoud op meerdere tabbladen ordenen | `-` |
| [Carousel](https://adobe.com/go/aem_cmp_tech_carousel_v1) | Hiermee kan de auteur van de inhoud de inhoud ordenen in een draaiende carrousel van dia&#39;s | `/libs/foundation/components/carousel` |
| [Inhoudsfragment](https://adobe.com/go/aem_cmp_tech_cf_v1) | Hiermee wordt de weergave van een inhoudsfragment toegestaan | `-` |
| [Lijst met inhoudsfragmenten](https://adobe.com/go/aem_cmp_tech_cflist_v1) | Hiermee wordt een lijst met inhoudsfragmenten weergegeven | `-` |
| [Scheidingsteken](https://adobe.com/go/aem_cmp_tech_separator_v1) | Hiermee wordt de inhoud van een pagina gescheiden | `-` |
| [Accordeon](https://adobe.com/go/aem_cmp_tech_accordion_v1) | Inhoudsdeelvensters ordenen in een inklapbare accordeon | `-` |
| [Container](https://adobe.com/go/aem_cmp_tech_container_v1) | Componenten indelen in een container | `-` |
| [Knop](https://adobe.com/go/aem_cmp_tech_button_v1) | Een knop op een pagina maken | `-` |
| [Downloaden](https://adobe.com/go/aem_cmp_tech_download_v1) | Een downloadbaar element toevoegen aan een pagina | `-` |
| [Ervaar fragment](https://adobe.com/go/aem_cmp_tech_xf_v1) | Een ervaringsfragment toevoegen aan een pagina | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [Insluiten](https://adobe.com/go/aem_cmp_tech_embed_v1) | Een externe bron in een pagina insluiten | - |
| [Voortgangsbalk](https://adobe.com/go/aem_cmp_tech_progress_v1) | Een visuele weergave geven van de voortgang in de richting van een doel | - |
| [PDF-viewer](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1) | Hiermee wordt een PDF-document op een pagina gepresenteerd | - |

### Aanstaande componenten {#upcoming-components}

Voor een overzicht van de aanstaande wegenkaart van de Component van de Kern zie [projectwiki op GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Upgrade van kerncomponenten {#upgrade-of-core-components}

Een voordeel van versioned componenten is dat het toestaat om de migratie aan een nieuwe AEM versie van de migratie aan nieuwe componentenversies te scheiden. Als er nieuwe componentversies beschikbaar zijn, is het bovendien mogelijk om elke component afzonderlijk naar de nieuwe versie te migreren.

Migraties naar een nieuwe AEM hebben geen invloed op de werking van de Core Components, op voorwaarde dat de versies ervan ook ondersteuning bieden voor de nieuwe AEM die wordt gemigreerd naar. Aanpassingen aan de Componenten van de Kern zouden ook niet moeten worden beïnvloed, zolang zij geen APIs gebruiken die [afgekeurd of verwijderd](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html) zijn.

De migraties aan nieuwe versies van de Componenten van de Kern zullen niet beïnvloeden hoe de component ook werkt, maar de nieuwe eigenschappen zouden aan paginaauteurs kunnen worden geïntroduceerd, die één of andere configuratie door een malplaatjeredacteur zouden kunnen vereisen, voor het geval dat het standaardgedrag niet wordt gewenst. Aanpassingen kunnen echter moeten worden aangepast, voor meer details zie de pagina [Kerncomponenten aanpassen](customizing.md#upgrade-compatibility-of-customizations).
