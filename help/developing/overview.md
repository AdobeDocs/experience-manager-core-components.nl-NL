---
title: Basiscomponenten ontwikkelen
description: De componenten van de Kern verstrekken robuuste en verlengbare basiscomponenten die eigenschap-rijke mogelijkheden, ononderbroken levering, componentenversioning, moderne implementatie, leuning prijsverhoging, en JSON de uitvoer van inhoud aanbieden.
translation-type: tm+mt
source-git-commit: 6f7166c46940ed451721e0760d565d58efe412ab
workflow-type: tm+mt
source-wordcount: '1425'
ht-degree: 1%

---


# Basiscomponenten ontwikkelen {#developing-core-components}

## Wanneer moet u de kerncomponenten gebruiken? {#when-to-use-the-core-components}

Aangezien de Componenten van de Kern allen-nieuw zijn, en veelvoudige voordelen aanbieden, wordt het geadviseerd voor nieuwe projecten AEM om hen te gebruiken. Voor bestaande projecten zou een migratie deel moeten uitmaken van een grotere projectinspanning, bijvoorbeeld een herbranding of het totale refactoring.

Daarom geeft Adobe de volgende aanbevelingen:

* **Nieuwe Projecten** Nieuwe projecten zouden altijd moeten proberen om de Componenten van de Kern te gebruiken. Als de Componenten van de Kern niet direct kunnen worden gebruikt of [uitgebreid](customizing.md) om aan projectvereisten te voldoen, dan creeer een douanecomponent na de componentenarchitectuur die in kerncomponenten wordt vermeld. Vermijd het gebruik van de [basiscomponenten](/help/versions.md#foundation-component-support), tenzij dit anderszins mogelijk is.
* **De bestaande** Aanbeveling van Projecten [blijft het gebruiken van de](/help/versions.md#foundation-component-support)stichtingscomponenten, tenzij een plaats of componentenrefactoring wordt gepland.\
   Aangezien de stichtingscomponenten in de meeste bestaande projecten op grote schaal worden gebruikt, [zullen zij verder worden ondersteund.](/help/versions.md#foundation-component-support)
* **Nieuwe aangepaste componenten** bepalen of een bestaande [kerncomponent kan worden aangepast](customizing.md).\
   Zo niet, dan wordt aanbevolen een nieuwe aangepaste component te maken volgens de [Componentrichtlijnen](guidelines.md).
* **Bestaande aangepaste componenten** Als uw componenten naar behoren werken, kunt u ze op de juiste wijze houden.\
   Als dat niet het geval is, raadpleegt u &quot;Nieuwe aangepaste componenten&quot; hierboven.

## Hoe te met de Componenten van de Kern Succes {#how-to-succeed}

De kerncomponenten zijn krachtig, flexibel en gebruiksvriendelijk. [Na een paar zeer belangrijke richtlijnen](success.md) zullen ervoor zorgen dat uw project met de Componenten van de Kern een succes is.

## Migreren naar de kerncomponenten

Om het even welk nieuw project zou met de Componenten van de Kern moeten worden uitgevoerd. Nochtans zullen de bestaande projecten gewoonlijk uitgebreide implementaties van de Componenten van de Stichting hebben.

Een grotere inspanning op een bestaand project (bijvoorbeeld rebranding of het algemene refactoring) biedt vaak een kans om aan de Componenten van de Kern te migreren. Om deze migratie te vergemakkelijken, heeft Adobe een aantal migratiehulpmiddelen verstrekt om de goedkeuring van de Componenten van de Kern en de recentste technologie aan te moedigen AEM.

[Met de moderniseringsinstrumenten](http://opensource.adobe.com/aem-modernize-tools/) van AEM kunt u gemakkelijk converteren naar:

* Statische sjablonen naar bewerkbare sjablonen
* Configuraties ontwerpen naar beleid
* Elementaire componenten naar kerncomponenten
* Klassieke interface naar interface met aanraakbediening

Raadpleeg de documentatie [](http://opensource.adobe.com/aem-modernize-tools/)bij deze gereedschappen voor meer informatie over het gebruik van deze gereedschappen.

>[!NOTE]
>
>De Moderniseringsgereedschappen van AEM zijn een community-inspanning en worden niet ondersteund of gegarandeerd door Adobe.

## Ondersteuning van kerncomponenten {#core-component-support}

De Componenten van de kern zijn een integraal deel van AEM en gesteund zoals is, onder de zelfde voorwaarden alsof zij als deel van Quickstart werden geleverd.

De algemene regel is, net als andere AEM-productfuncties, als volgt: Componenten worden eerst aangekondigd te worden vervangen en de oudste verwijderd voor de volgende AEM-release. Dit geeft klanten minstens één versiecyclus om naar de nieuwe versie van de component te bewegen, alvorens zijn steun te laten vallen.

De versie van elke component geeft duidelijk aan welke AEM-versies worden ondersteund. Wanneer de steun voor een versie van AEM ophoudt, dan ook de steun van de Componenten van de Kern voor die versie van AEM.

Zie de pagina Core Components [Customizing voor meer informatie over de ondersteuning van componentaanpassingen](customizing.md) .


## Technische mogelijkheden {#technical-capabilities}

De volgende lijst geeft een overzicht van de verschillen tussen kerncomponenten en stichtingscomponenten.

Voor details over hun auteursmogelijkheden en opties om hen vooraf te vormen, [verwijs naar de auteurspagina over hen](/help/get-started/authoring.md).

| **Capaciteit** | **Kerncomponent** | **Foundation-component** |
|-----|---|---|
| Logische implementatie | Java POJO&#39;s met annotaties [Sling Models](https://sling.apache.org/documentation/bundles/models.html) | JSP-code |
| Opmaakdefinitie | [HTML Template Language](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) (HTL) syntaxis | JSP-code |
| XSS-ontsmetting | Geautomatiseerd door HTML | Meestal handmatig |
| Naam van CSS-klassen | Gestandaardiseerde naamgevingsconventie gebaseerd op [blokelement Modifier](https://getbem.com/) (BEM)-notatie (vanaf release 2.0.0) | Aangepaste schema&#39;s |
| Dialoogdefinitie | [Koraal 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Koraal 2 + klassieke gebruikersinterface |
| JSON-uitvoer | [Sling Modellen Exporter met Jackson serialization](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Standaard Sling-servlet |
| Versioning | [Voor het model en het HTL](guidelines.md) | Geen |
| Testen | Eenheidstests + integratietests | Integratietests |
| Aflevering | [Via public GitHub](https://github.com/adobe/aem-core-wcm-components) | Via Quickstart |
| Licentie | [Apache-licentie](https://www.apache.org/licenses/LICENSE-2.0) | Eigendom van Adobe |
| Bijdrage | Via pull request | Niet mogelijk |
| Toegankelijkheid | Volledig compatibel met de [WCAG 2.0 AA-standaard](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html | Slechts gedeeltelijk compatibel met de norm [WCAG 2.0 AA](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |

## Componentlijst {#component-list}

De volgende lijst maakt een lijst van de beschikbare Componenten van de Kern, die met hun API verbinden, en wijst op welke stichtingscomponenten zij vervangen.

| Kerncomponent | Beschrijving | Vervangen basiscomponent(en) |
|---|---|---|
| [Pagina](https://adobe.com/go/aem_cmp_tech_page_v2) | Responsieve pagina werken met sjablooneditor | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Broodkruimel](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2) | Navigatie in paginahiërarchie | `/libs/foundation/components/breadcrumb` |
| [Titel](https://adobe.com/go/aem_cmp_tech_title_v2) | H1-H6-titel | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Tekst](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | RTF | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Afbeelding](https://adobe.com/go/aem_cmp_tech_image_v2) | Slim en wazig laden van optimale renditiegrootte | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Lijst](https://adobe.com/go/aem_cmp_tech_list_v2) | Lijst met pagina&#39;s | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Delen van sociale media](https://adobe.com/go/aem_cmp_tech_sharing_v1) | Widget Facebook en Pinterest delen | `-` |
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

### Aanstaande componenten {#upcoming-components}

Voor een overzicht van de aanstaande wegenkaart van de Component van de Kern zie de [projectwiki op GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Upgrade van kerncomponenten {#upgrade-of-core-components}

Een voordeel van versioned componenten is dat het toestaat om de migratie aan een nieuwe versie AEM van de migratie aan nieuwe componentenversies te scheiden. Als er nieuwe componentversies beschikbaar zijn, is het bovendien mogelijk om elke component afzonderlijk naar de nieuwe versie te migreren.

Migraties naar een nieuwe AEM-versie hebben geen invloed op de werking van de Core Components, op voorwaarde dat de versies ervan ook ondersteuning bieden voor de nieuwe AEM-versie waarnaar wordt gemigreerd. De aanpassingen aan de Componenten van de Kern zouden ook niet moeten worden beïnvloed, zolang zij geen APIs gebruiken die zijn [verouderd of verwijderd](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html).

De migraties aan nieuwe versies van de Componenten van de Kern zullen niet beïnvloeden hoe de component ook werkt, maar de nieuwe eigenschappen zouden aan paginaauteurs kunnen worden geïntroduceerd, die één of andere configuratie door een malplaatjeredacteur zouden kunnen vereisen, voor het geval dat het standaardgedrag niet wordt gewenst. De aanpassingen zouden echter moeten worden aangepast, voor meer details zie de het Aanpassen pagina van de Componenten [](customizing.md#upgrade-compatibility-of-customizations) van de Kern.
