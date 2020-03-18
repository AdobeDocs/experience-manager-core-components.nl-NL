---
title: Basiscomponenten ontwikkelen
description: De componenten van de Kern verstrekken robuuste en verlengbare basiscomponenten die eigenschap-rijke mogelijkheden, ononderbroken levering, componentenversioning, moderne implementatie, leuning prijsverhoging, en JSON de uitvoer van inhoud aanbieden.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Basiscomponenten ontwikkelen {#developing-core-components}

## Overzicht {#overview}

De componenten van de Kern verstrekken robuuste en verlengbare basiscomponenten, en hun hoogtepunten zijn:

* Functiemogelijkheden
   * [Flexibele configuratieopties](/help/get-started/authoring.md) om vele gebruiksgevallen aan te passen
   * [Vooraf instelbare mogelijkheden](/help/get-started/authoring.md#pre-configuring-core-components) om te bepalen welke functies beschikbaar zijn voor auteurs van pagina&#39;s
* Doorlopende levering
   * Frequente incrementele functieverbeteringen
   * Beschikbaarheid van de [broncode op GitHub](https://github.com/adobe/aem-core-wcm-components) om de ontwikkelaarsgemeenschap toe te staan terugkoppelen en bijdragen
   * Installatie via een [apart uitgebracht inhoudspakket](https://github.com/adobe/aem-core-wcm-components/releases) voor componentupgrades die onafhankelijk van AEM-upgrades worden uitgevoerd
* [Componentversie](guidelines.md#component-versioning)
   * [Zorg voor compatibiliteit binnen een versie](#upgrade-of-core-components), maar laat de componenten toch evolueren
   * Meerdere versies van één component tegelijk toestaan in dezelfde omgeving
* Moderne uitvoering
   * Opmaak die is gedefinieerd in [HTML-sjabloontaal](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) (HTML)
   * Logica voor inhoudsmodellen die is geïmplementeerd met [verkoopmodellen](https://sling.apache.org/documentation/bundles/models.html)
* Regelafstand
   * Na [blokelement Modifier](https://getbem.com/) (BEM)-notatie vanaf release 2.0.0
      * Eerdere release volgt naamconventies [van](https://getbootstrap.com/css/) Bootstrap
   * Gebaseerd op [toegankelijkheidsrichtlijnen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)
   * Kan worden gebruikt voor responsieve en mobiele sites
* Mogelijkheid om als JSON het inhoudsmodel voor CMS-gebruiksgevallen zonder kop te serialiseren
* Toegankelijk
   * Voldoet aan de [WCAG 2.0 AA-standaard](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

>[!CAUTION]
>
>Voor kerncomponenten is AEM 6.3 of hoger en Java 8 vereist en het gebruik van [bewerkbare sjablonen is vereist](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
>
>De Componenten van de kern werken niet met Klassieke UI noch met statische malplaatjes.

## Overzicht van Gems-sessie {#gems-session-overview}

Bekijk voor een inleiding op de Core Components, de functies die ze bieden en de manier waarop ze in AEM worden gebruikt, de AEM Gems Session [AEM Core Components.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Gems on Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) is een aantal technische diepteduiken die door Adobe-experts worden geleverd. Deze reeks is een aanvulling op de productdocumentatie en alle andere technische kanalen, zodat ontwikkelaars contact kunnen opnemen en dieper kunnen gaan op een specifiek onderwerp.

## Zelfstudie voor WKND-ontwikkelaars {#wknd-developer-tutorial}

Ga aan de slag met het ontwikkelen van AEM-sites met Core Components door [deze stapsgewijze zelfstudie te volgen.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

## AEM-projectarchetype {#aem-project-archetype}

[Het AEM Project Archetype](/help/developing/archetype/overview.md) leidt tot een minimaal project van de Manager van de Ervaring van Adobe als uitgangspunt voor uw eigen projecten, met inbegrip van een voorbeeld van douaneHTML componenten met SlingModels voor de logica en juiste implementatie van de Componenten van de Kern met het geadviseerde volmachtspatroon.

## Geleverd via GitHub {#delivered-over-github}

De Componenten van de Kern worden ontwikkeld binnen en door GitHub geleverd.

CODE VOOR GITHUB

U kunt de code van deze pagina op GitHub vinden

* [Open aem-core-wcm-componentenproject op GitHub](https://github.com/adobe/aem-core-wcm-components)
* Het project downloaden als [ZIP-bestand](https://github.com/adobe/aem-core-wcm-components/archive/master.zip)

Zie de [Gebruikende de documentatiepagina van de Componenten](/help/get-started/using.md) van de Kern om te leren hoe te beginnen hen in uw project te gebruiken.

Het hebben van de Componenten van de Kern op GitHub zal toestaan om frequente updates te doen, en aan te luisteren terugkoppelen van de AEM ontwikkelaarsgemeenschap. Ook, zou dit klanten en partners moeten helpen om gelijkaardige patronen te volgen wanneer het bouwen van douanecomponenten.

>[!NOTE]
>
>Om op de recentste veranderingen in de kerncomponenten bij te houden, kunt u op de bewaarplaats [van de Componenten van de](https://github.com/adobe/aem-core-wcm-components) Kern op GitHub letten.

## Componentbibliotheek

Bekijk de [componentbibliotheek](https://adobe.com/go/aem_cmp_library), waarin de actuele release van de Core Components wordt getoond en voorbeelden van het gebruik ervan worden gegeven.

### Core Components Out-of-the-box {#out-of-the-box}

Afhankelijk van de manier waarop u AEM uitvoert, kunnen de kerncomponenten al dan niet automatisch worden geïnstalleerd.

#### AEM as a Cloud Service {#aem-cloud-service}

Hoewel de Core Components volledig compatibel zijn met [AEM als Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html), moeten de Core Components handmatig worden geïnstalleerd en zijn niet offline beschikbaar.

#### AEM On-Premise {#on-premise}

In installaties op locatie zijn de Core Components zichtbaar in de QuickStart wanneer de voorbeeldinhoud aanwezig is, omdat deze wordt gebruikt door de referentiesite [We.Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) . Nochtans, wanneer lopend in productie (op `nosamplecontent` runmode, zonder toegelaten steekproefinhoud), zullen de kerncomponenten niet meer aanwezig zijn en moeten op de instantie worden geïnstalleerd AEM.

>[!NOTE]
>
>Voer in on-premise productieomgevingen de QuickStart altijd in de `nosamplecontent` runmode uit. Volg de instructies op de documentatiepagina Core Components (Basiscomponenten `nosamplecontent` gebruiken [) om de kerncomponenten in de](/help/get-started/using.md) runmode te gebruiken.

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

### Aanstaande componenten {#upcoming-components}

Voor een overzicht van de aanstaande wegenkaart van de Component van de Kern zie de [projectwiki op GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Upgrade van kerncomponenten {#upgrade-of-core-components}

Een voordeel van versioned componenten is dat het toestaat om de migratie aan een nieuwe versie AEM van de migratie aan nieuwe componentenversies te scheiden. Als er nieuwe componentversies beschikbaar zijn, is het bovendien mogelijk om elke component afzonderlijk naar de nieuwe versie te migreren.

Migraties naar een nieuwe AEM-versie hebben geen invloed op de werking van de Core Components, op voorwaarde dat de versies ervan ook ondersteuning bieden voor de nieuwe AEM-versie waarnaar wordt gemigreerd. De aanpassingen aan de Componenten van de Kern zouden ook niet moeten worden beïnvloed, zolang zij geen APIs gebruiken die zijn [verouderd of verwijderd](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html).

De migraties aan nieuwe versies van de Componenten van de Kern zullen niet beïnvloeden hoe de component ook werkt, maar de nieuwe eigenschappen zouden aan paginaauteurs kunnen worden geïntroduceerd, die één of andere configuratie door een malplaatjeredacteur zouden kunnen vereisen, voor het geval dat het standaardgedrag niet wordt gewenst. De aanpassingen zouden echter moeten worden aangepast, voor meer details zie de het Aanpassen pagina van de Componenten [](customizing.md#upgrade-compatibility-of-customizations) van de Kern.

## Wanneer moet u de kerncomponenten gebruiken? {#when-to-use-the-core-components}

Aangezien de Componenten van de Kern allen-nieuw zijn, en veelvoudige voordelen aanbieden, wordt het geadviseerd voor nieuwe projecten AEM om hen te gebruiken. Voor bestaande projecten zou een migratie deel moeten uitmaken van een grotere projectinspanning, bijvoorbeeld een herbranding of het totale refactoring.

Daarom geeft Adobe de volgende aanbevelingen:

* **Nieuwe Projecten** Nieuwe projecten zouden altijd moeten proberen om de Componenten van de Kern te gebruiken. Als de Componenten van de Kern niet direct kunnen worden gebruikt of [uitgebreid](customizing.md) om aan projectvereisten te voldoen, dan creeer een douanecomponent na de componentenarchitectuur die in kerncomponenten wordt vermeld. Vermijd het gebruik van de [basiscomponenten](#foundation-component-support), tenzij dit anderszins mogelijk is.
* **De bestaande** Aanbeveling van Projecten [blijft het gebruiken van de](#foundation-component-support)stichtingscomponenten, tenzij een plaats of componentenrefactoring wordt gepland.\
   Aangezien de stichtingscomponenten in de meeste bestaande projecten op grote schaal worden gebruikt, [zullen zij verder worden ondersteund.](#foundation-component-support)
* **Nieuwe aangepaste componenten** bepalen of een bestaande [kerncomponent kan worden aangepast](customizing.md).\
   Zo niet, dan wordt aanbevolen een nieuwe aangepaste component te maken volgens de [Componentrichtlijnen](guidelines.md).
* **Bestaande aangepaste componenten** Als uw componenten naar behoren werken, kunt u ze op de juiste wijze houden.\
   Als dat niet het geval is, raadpleegt u &quot;Nieuwe aangepaste componenten&quot; hierboven.

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

## Ondersteuning van stichtingscomponenten {#foundation-component-support}

Aangezien de stichtingscomponenten als basis hebben gediend voor zoveel projectontwikkeling in een groot aantal AEM-versies, zullen zij in de nabije toekomst verder worden ondersteund.

De ontwikkelingsnadruk van Adobe is echter verschoven naar de kerncomponenten en er worden nieuwe functies aan toegevoegd, terwijl [bijna alle stichtingscomponenten zijn vervangen door AEM 6.5](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) en er alleen opgeloste problemen worden aangebracht in de verdere ontwikkeling van de stichtingscomponenten.

**Volgende lezen:**

* [Het gebruiken van de Componenten](/help/get-started/using.md) van de Kern - begin en loopt met de Componenten van de Kern in uw eigen project.
* [Componentrichtlijnen](guidelines.md) - voor het leren van de implementatiepatronen van de Core Components.
