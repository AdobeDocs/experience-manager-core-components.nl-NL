---
title: Basiscomponenten ontwikkelen
description: De componenten van de Kern verstrekken robuuste en verlengbare basiscomponenten die eigenschap-rijke mogelijkheden, ononderbroken levering, componentenversioning, moderne implementatie, leuning prijsverhoging, en JSON de uitvoer van inhoud aanbieden.
role: Architect, Developer, Admin
exl-id: 0f79cac1-a3b0-487e-90be-0bd8263d3912
source-git-commit: 614bc5fd01a76a6888606faa4576e1695b77ba58
workflow-type: tm+mt
source-wordcount: '1287'
ht-degree: 1%

---

# Basiscomponenten ontwikkelen {#developing-core-components}

## Wanneer moet u de kerncomponenten gebruiken? {#when-to-use-the-core-components}

Aangezien de Componenten van de Kern allen-nieuw zijn, en veelvoudige voordelen aanbieden, wordt het geadviseerd voor nieuwe AEM projecten om hen te gebruiken. Voor bestaande projecten zou een migratie deel moeten uitmaken van een grotere projectinspanning, bijvoorbeeld een herbranding of het totale refactoring.

Daarom doet de Adobe de volgende aanbevelingen:

* **Nieuwe Projecten**
De nieuwe projecten zouden altijd moeten proberen om de Componenten van de Kern te gebruiken. Als de Componenten van de Kern niet direct kunnen worden gebruikt of [ uitgebreid ](customizing.md) om aan projectvereisten te voldoen, dan creeer een douanecomponent na de componentenarchitectuur die in kerncomponenten wordt vermeld. Behalve waar anders niet mogelijk, vermijd het gebruiken van de [ stichtingscomponenten ](/help/versions.md#foundation-component-support).
* **Bestaande Projecten**
De aanbeveling houdt gebruikend de [ stichtingscomponenten ](/help/versions.md#foundation-component-support), tenzij een plaats of componentenrefactoring wordt gepland.\
  Aangezien zij zeer wijd door de meeste bestaande projecten worden gebruikt, zullen de stichtingscomponenten [ blijven worden gesteund.](/help/versions.md#foundation-component-support)
* **Nieuwe Componenten van de Douane**
Beoordeel als een bestaande [ Component van de Kern ](customizing.md) kan worden aangepast.\
  Als niet, aanbeveling een nieuwe douanecomponent na de [ Richtlijnen van de Component ](guidelines.md) moet bouwen.
* **Bestaande Componenten van de Douane**
Als uw componenten zoals verwacht werken, dan houd hen zoals zij zijn.\
  Als dat niet het geval is, raadpleegt u &quot;Nieuwe aangepaste componenten&quot; hierboven.

## Hoe te met de Componenten van de Kern Succes {#how-to-succeed}

De kerncomponenten zijn krachtig, flexibel en gebruiksvriendelijk. [ na een paar zeer belangrijke richtlijnen ](success.md) zal ervoor zorgen dat uw project met de Componenten van de Kern een succes is.

## Migreren naar de kerncomponenten

Elk nieuw project moet worden geïmplementeerd met Core Components. Nochtans zullen de bestaande projecten gewoonlijk uitgebreide implementaties van de Componenten van de Stichting hebben.

### Migreren van stichtingscomponenten {#from-foundation}

Een grotere inspanning op een bestaand project (bijvoorbeeld rebranding of het algemene refactoring) biedt vaak een kans om aan de Componenten van de Kern te migreren. Om deze migratie te vergemakkelijken, heeft Adobe een aantal migratiehulpmiddelen verstrekt om de goedkeuring van de Core Components en de recentste AEM technologie aan te moedigen.

[ de Hulpmiddelen van de Modernisering van de AEM ](https://opensource.adobe.com/aem-modernize-tools/) staan voor de gemakkelijke omzetting van toe:

* Statische sjablonen converteren naar bewerkbare sjablonen
* Ontwerpconfiguraties omzetten naar beleid
* Elementaire componenten omzetten naar kerncomponenten
* De klassieke interface converteren naar een interface met aanraakbediening

Voor verdere informatie over het gebruik van deze hulpmiddelen, [ zie hun documentatie ](https://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>De AEM Moderniseringshulpmiddelen zijn een communautaire inspanning en niet gesteund of door Adobe gewaarborgd.

## Migratie via Verplaatsen naar AEM as a Cloud Service {#via-aemaacs}

Omdat AEM as a Cloud Service automatisch de nieuwste versie van de Core Components ontvangt, moet u elke afhankelijkheid van de Core Components in uw project `pom.xml` -bestand verwijderen wanneer u van een installatie op locatie AEM de toepassing overschakelt.

Uw proxycomponenten werken nog steeds zoals voorheen, omdat   proxy&#39;s verwijzen naar het vereiste supertype en het supertekstpad heeft de versie erin. Op deze manier, eenvoudig het verwijderen van de gebiedsdelen laat de Componenten van de Kern toe om in AEMaaCS te werken enkel zoals zij op-gebouw deden.

Net als bij elk ander AEMaaCS-project moet u ook een afhankelijkheid toevoegen aan de AEM SDK-jar. Dit is niet specifiek voor de Core Components, maar is vereist.

```xml
<dependency>
   <groupId>com.adobe.aem</groupId>
   <artifactId>aem-sdk-api</artifactId>
</dependency>
```

Zie het document [ AEM de Structuur van het Project ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=nl-NL) voor meer informatie over projecten AEMaaCS.

## Ondersteuning van kerncomponenten {#core-component-support}

De Componenten van de kern zijn een integraal deel van AEM en gesteund zoals is, onder de zelfde voorwaarden alsof zij als deel van Quickstart werden geleverd.

Net als andere AEM productfuncties is de algemene regel: Componenten worden eerst aangekondigd te worden vervangen en de oudste verwijderd voor de volgende AEM. Dit geeft klanten minstens één versiecyclus om naar de nieuwe versie van de component te bewegen, alvorens zijn steun te laten vallen.

In de versie van elke component worden duidelijk de AEM versies vermeld die worden ondersteund. Wanneer de steun voor een versie van AEM beëindigt, dan ook de steun van de Componenten van de Kern voor die versie van AEM.

Voor details over de steun van componentenaanpassingen, zie de [ Aanpassende pagina van de Componenten van de Kern ](customizing.md).


## Technische mogelijkheden {#technical-capabilities}

De volgende lijst geeft een overzicht van de verschillen tussen kerncomponenten en stichtingscomponenten.

Voor details over hun auteursmogelijkheden en opties om hen pre-configureerbaar te maken, [ verwijzen naar de auteurspagina over hen ](/help/get-started/authoring.md).

| **Capability** | **Component van de Kern** | **Component van de Stichting** |
|-----|---|---|
| Logische implementatie | Java POJOs met [ Sling Models ](https://sling.apache.org/documentation/bundles/models.html) aantekeningen | JSP-code |
| Opmaakdefinitie | [ Taal van het Malplaatje van de HTML ](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=nl-NL) (HTML) syntaxis | JSP-code |
| XSS-ontsmetting | Geautomatiseerd door HTML | Meestal handmatig |
| Naam van CSS-klassen | Gestandaardiseerde noemende overeenkomst die op [ Modifier van het Element van het Blok ](https://getbem.com/) (BEM) (vanaf versie 2.0.0 wordt gebaseerd) | Aangepaste schema&#39;s |
| Dialoogdefinitie | [ Koraal 3 ](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Koraal 2 + klassieke gebruikersinterface |
| JSON-uitvoer | [ Sling Models Exporter met Jackson rangschikking ](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Standaard Sling-servlet |
| Versioning | [ voor het model en HTML ](guidelines.md) | Geen |
| Testen | Eenheidstests + integratietests | Integratietests |
| Aflevering | [ Via openbare GitHub ](https://github.com/adobe/aem-core-wcm-components) | Via Quickstart |
| Licentie | [ Vergunning Apache ](https://www.apache.org/licenses/LICENSE-2.0) | Eigen Adobe |
| Bijdrage | Via pull request | Niet mogelijk |
| Toegankelijkheid | Volledig volgzaam met de [ WCAG 2.0 norm van A ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=nl-NL) | Slechts gedeeltelijk volgzaam met de [ WCAG 2.0 norm van A ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=nl-NL) |

## Componentlijst {#component-list}

De volgende lijst maakt een lijst van de beschikbare Componenten van de Kern, die met hun API verbinden, en wijst op welke stichtingscomponenten zij vervangen.

| Kerncomponent | Beschrijving | Vervangen basiscomponent(en) |
|---|---|---|
| [ Pagina ](https://adobe.com/go/aem_cmp_tech_page_v2) | Responsieve pagina werken met sjablooneditor | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [ Breadcrumb ](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2) | Navigatie in paginahiërarchie | `/libs/foundation/components/breadcrumb` |
| [ Titel ](https://adobe.com/go/aem_cmp_tech_title_v2) | H1-H6-titel | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [ Tekst ](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | RTF | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [ Beeld ](https://adobe.com/go/aem_cmp_tech_image_v2) | Slim en wazig laden van optimale renditiegrootte | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [ Lijst ](https://adobe.com/go/aem_cmp_tech_list_v2) | Lijst met pagina&#39;s | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [ Sociale Media die ](https://adobe.com/go/aem_cmp_tech_sharing_v1) delen | Delen via facebook en Pinterest | `-` |
| [ de Container van de Vorm ](https://adobe.com/go/aem_cmp_tech_form_container_v2) | Responsief formulieralineasysteem | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [ Tekst van de Vorm ](https://adobe.com/go/aem_cmp_tech_form_text_v2) | Tekstinvoerveld | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [ Opties van de Vorm ](https://adobe.com/go/aem_cmp_tech_form_options_v2) | Invoerveld Meerdere opties | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [ Verborgen Vorm ](https://adobe.com/go/aem_cmp_tech_form_hidden_v2) | Verborgen invoerveld | `/libs/foundation/components/form/hidden` |
| [ Knop van de Vorm ](https://adobe.com/go/aem_cmp_tech_form_button_v2) | Verzenden of aangepaste knop | `/libs/foundation/components/form/submit` |
| [ Navigatie ](https://adobe.com/go/aem_cmp_tech_navigation_v1) | Een sitenavigatie-component die de geneste paginahiërarchie weergeeft | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [ Navigatie van de Taal ](https://adobe.com/go/aem_cmp_tech_langnav_v1) | Een taal- en landswitch die de algemene taalstructuur opsomt | `-` |
| [ Snel Onderzoek ](https://adobe.com/go/aem_cmp_tech_search_v1) | Een zoekcomponent die de resultaten als suggesties ter plaatse in een vervolgkeuzemenu weergeeft | `/libs/foundation/components/search` |
| [ Taser ](https://adobe.com/go/aem_cmp_tech_teaser_v1) | Hiermee kan de auteur van de inhoud eenvoudig een gummetje maken om inhoud te verfijnen met een afbeelding, titel of RTF-tekst en een koppeling maken naar verdere inhoud of andere handelingen | `-` |
| [ Lusjes ](https://adobe.com/go/aem_cmp_tech_tabs_v1) | Hiermee kan de auteur van de inhoud de pagina-inhoud op meerdere tabbladen ordenen | `-` |
| [ Carousel ](https://adobe.com/go/aem_cmp_tech_carousel_v1) | Hiermee kan de auteur van de inhoud de inhoud ordenen in een draaiende carrousel van dia&#39;s | `/libs/foundation/components/carousel` |
| [ het Fragment van de Inhoud ](https://adobe.com/go/aem_cmp_tech_cf_v1) | Hiermee kunt u een inhoudsfragment weergeven | `-` |
| [ Lijst van het Fragment van de Inhoud ](https://adobe.com/go/aem_cmp_tech_cflist_v1) | Hiermee wordt een lijst met inhoudsfragmenten weergegeven | `-` |
| [ Scheidingsteken ](https://adobe.com/go/aem_cmp_tech_separator_v1) | Hiermee wordt de inhoud van een pagina gescheiden | `-` |
| [ Accordeon ](https://adobe.com/go/aem_cmp_tech_accordion_v1) | Inhoudsdeelvensters ordenen in een inklapbare accordeon | `-` |
| [ Container ](https://adobe.com/go/aem_cmp_tech_container_v1) | Componenten indelen in een container | `-` |
| [ Knoop ](https://adobe.com/go/aem_cmp_tech_button_v1) | Een knop op een pagina maken | `-` |
| [ Download ](https://adobe.com/go/aem_cmp_tech_download_v1) | Een downloadbaar element toevoegen aan een pagina | `-` |
| [ Fragment van de Ervaring ](https://adobe.com/go/aem_cmp_tech_xf_v1) | Een ervaringsfragment toevoegen aan een pagina | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [ bed ](https://adobe.com/go/aem_cmp_tech_embed_v1) in | Een externe bron in een pagina insluiten | - |
| [ Bar van de Voortgang ](https://adobe.com/go/aem_cmp_tech_progress_v1) | Een visuele weergave geven van de voortgang in de richting van een doel | - |
| [ de Kijker van de PDF ](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1) | Hiermee wordt een PDF-document op een pagina gepresenteerd | - |

## Upgrade van kerncomponenten {#upgrade-of-core-components}

Een voordeel van versioned componenten is dat het toestaat om de migratie aan een nieuwe AEM versie van de migratie aan nieuwe componentenversies te scheiden. Als er nieuwe componentversies beschikbaar zijn, is het bovendien mogelijk om elke component afzonderlijk naar de nieuwe versie te migreren.

Migraties naar een nieuwe AEM hebben geen invloed op de werking van de Core Components, op voorwaarde dat de versies ervan ook ondersteuning bieden voor de nieuwe AEM die wordt gemigreerd naar. De aanpassingen die aan de Componenten van de Kern worden aangebracht zouden niet of moeten worden beïnvloed, zolang zij geen APIs gebruiken die [ zijn afgekeurd of ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=nl-NL) verwijderd.

De migraties aan nieuwe versies van de Componenten van de Kern zullen niet beïnvloeden hoe de component ook werkt, maar de nieuwe eigenschappen zouden aan paginaauteurs kunnen worden geïntroduceerd, die één of andere configuratie door een malplaatjeredacteur zouden kunnen vereisen, voor het geval dat het standaardgedrag niet wordt gewenst. De aanpassingen nochtans zouden moeten worden aangepast, voor meer details zie [ Aanpassend de pagina van de Componenten van de Kern ](customizing.md#upgrade-compatibility-of-customizations).
