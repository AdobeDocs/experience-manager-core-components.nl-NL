---
title: Basiscomponenten ontwikkelen
description: De componenten van de Kern verstrekken robuuste en verlengbare basiscomponenten die eigenschap-rijke mogelijkheden, ononderbroken levering, componentenversioning, moderne implementatie, leuning prijsverhoging, en JSON de uitvoer van inhoud aanbieden.
role: Architect, Developer, Admin
exl-id: 0f79cac1-a3b0-487e-90be-0bd8263d3912
source-git-commit: 5994133947ff697f7c866fe61598c58e37e77008
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 2%

---

# Basiscomponenten ontwikkelen {#developing-core-components}

De componenten van de Kern verstrekken robuuste en verlengbare basiscomponenten die eigenschap-rijke mogelijkheden, ononderbroken levering, componentenversioning, moderne implementatie, leuning prijsverhoging, en JSON de uitvoer van inhoud aanbieden.

{{traditional-aem}}

## Hoe te met de Componenten van de Kern Succes {#how-to-succeed}

De kerncomponenten zijn krachtig, flexibel en gebruiksvriendelijk. [&#x200B; na een paar zeer belangrijke richtlijnen &#x200B;](success.md) zal ervoor zorgen dat uw project met de Componenten van de Kern een succes is.

## Migreren naar de kerncomponenten

Elk nieuw project moet worden geïmplementeerd met Core Components. Nochtans zullen de bestaande projecten gewoonlijk uitgebreide implementaties van de Componenten van de Stichting hebben.

### Migreren van stichtingscomponenten {#from-foundation}

Een grotere inspanning op een bestaand project (bijvoorbeeld rebranding of het algemene refactoring) biedt vaak een kans om aan de Componenten van de Kern te migreren. Om deze migratie te vergemakkelijken, heeft Adobe een aantal migratiehulpmiddelen verstrekt om de goedkeuring van de Core Components en de recentste technologie van AEM aan te moedigen.

[&#x200B; de Moderniseringshulpmiddelen van AEM &#x200B;](https://opensource.adobe.com/aem-modernize-tools/) staan voor de gemakkelijke omzetting van toe:

* Statische sjablonen converteren naar bewerkbare sjablonen
* Ontwerpconfiguraties omzetten naar beleid
* Elementaire componenten omzetten naar kerncomponenten
* De klassieke interface converteren naar een interface met aanraakbediening

Voor verdere informatie over het gebruik van deze hulpmiddelen, [&#x200B; zie hun documentatie &#x200B;](https://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>De Moderniseringsgereedschappen van AEM zijn een gemeenschapsinspanning en worden niet ondersteund of gegarandeerd door Adobe.

## Migratie via Verplaatsen naar AEM as a Cloud Service {#via-aemaacs}

Omdat AEM as a Cloud Service automatisch de nieuwste versie van de Core Components ontvangt, moet u, wanneer u van een AEM-installatie op locatie overschakelt, elke afhankelijkheid van de Core Components in uw project `pom.xml` -bestand verwijderen.

Uw proxycomponenten werken nog steeds zoals voorheen, omdat   proxy&#39;s verwijzen naar het vereiste supertype en het supertekstpad heeft de versie erin. Op deze manier, eenvoudig het verwijderen van de gebiedsdelen laat de Componenten van de Kern toe om in AEMaaCS te werken enkel zoals zij op-gebouw deden.

Net als bij elk ander AEMaaCS-project moet u ook een afhankelijkheidsrelatie toevoegen aan de AEM SDK jar. Dit is niet specifiek voor de Core Components, maar is vereist.

```xml
<dependency>
   <groupId>com.adobe.aem</groupId>
   <artifactId>aem-sdk-api</artifactId>
</dependency>
```

Zie het document [&#x200B; Structuur van het Project van AEM &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=nl-NL) voor meer informatie over projecten AEMaaCS.

## Ondersteuning van kerncomponenten {#core-component-support}

De Componenten van de kern zijn een integraal deel van AEM en gesteund zoals is, onder de zelfde voorwaarden alsof zij als deel van Quickstart werden geleverd.

De algemene regel is, net als bij andere AEM-productfuncties, dat componenten eerst worden aangekondigd om te worden vervangen en dat de oudste wordt verwijderd voor de volgende AEM-release. Dit geeft klanten minstens één versiecyclus om naar de nieuwe versie van de component te bewegen, alvorens zijn steun te laten vallen.

De versie van elke component geeft duidelijk aan welke AEM-versies worden ondersteund. Als een versie van AEM geen ondersteuning meer biedt, biedt dit ook ondersteuning voor de Core Components voor die versie van AEM.

Voor details over de steun van componentenaanpassingen, zie de [&#x200B; Aanpassende pagina van de Componenten van de Kern &#x200B;](customizing.md).


## Technische mogelijkheden {#technical-capabilities}

De volgende lijst geeft een overzicht van de verschillen tussen kerncomponenten en stichtingscomponenten.

Voor details over hun auteursmogelijkheden en opties om hen pre-configureerbaar te maken, [&#x200B; verwijzen naar de auteurspagina over hen &#x200B;](/help/get-started/authoring.md).

| **Capability** | **Component van de Kern** | **Component van de Stichting** |
|-----|---|---|
| Logische implementatie | Java POJOs met [&#x200B; Sling Models &#x200B;](https://sling.apache.org/documentation/bundles/models.html) aantekeningen | JSP-code |
| Opmaakdefinitie | [&#x200B; de syntaxis van de Taal van het Malplaatje van HTML &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=nl-NL) (HTML) | JSP-code |
| XSS-ontsmetting | Geautomatiseerd door HTML | Meestal handmatig |
| Naam van CSS-klassen | Gestandaardiseerde noemende overeenkomst die op [&#x200B; Modifier van het Element van het Blok &#x200B;](https://getbem.com/) (BEM) (vanaf versie 2.0.0 wordt gebaseerd) | Aangepaste schema&#39;s |
| Dialoogdefinitie | [&#x200B; Koraal 3 &#x200B;](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Koraal 2 + klassieke gebruikersinterface |
| JSON-uitvoer | [&#x200B; Sling Models Exporter met Jackson rangschikking &#x200B;](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Standaard Sling-servlet |
| Versioning | [&#x200B; voor het model en HTML &#x200B;](guidelines.md) | Geen |
| Testen | Eenheidstests + integratietests | Integratietests |
| Aflevering | [&#x200B; Via openbare GitHub &#x200B;](https://github.com/adobe/aem-core-wcm-components) | Via Quickstart |
| Licentie | [&#x200B; Vergunning Apache &#x200B;](https://www.apache.org/licenses/LICENSE-2.0) | Eigendom van Adobe |
| Bijdrage | Via pull request | Niet mogelijk |
| Toegankelijkheid | Volledig volgzaam met de [&#x200B; WCAG 2.0 norm van A &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=nl-NL) | Slechts gedeeltelijk volgzaam met de [&#x200B; WCAG 2.0 norm van A &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=nl-NL) |

## Componentlijst {#component-list}

De volgende lijst maakt een lijst van de beschikbare Componenten van de Kern, die met hun API verbinden, en wijst op welke stichtingscomponenten zij vervangen.

| Kerncomponent | Beschrijving | Vervangen basiscomponent(en) |
|---|---|---|
| [&#x200B; Pagina &#x200B;](https://adobe.com/go/aem_cmp_tech_page_v2) | Responsieve pagina werken met sjablooneditor | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [&#x200B; Breadcrumb &#x200B;](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2) | Navigatie in paginahiërarchie | `/libs/foundation/components/breadcrumb` |
| [&#x200B; Titel &#x200B;](https://adobe.com/go/aem_cmp_tech_title_v2) | H1-H6-titel | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [&#x200B; Tekst &#x200B;](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | RTF | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [&#x200B; Beeld &#x200B;](https://adobe.com/go/aem_cmp_tech_image_v2) | Slim en wazig laden van optimale renditiegrootte | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [&#x200B; Lijst &#x200B;](https://adobe.com/go/aem_cmp_tech_list_v2) | Lijst met pagina&#39;s | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [&#x200B; Sociale Media die &#x200B;](https://adobe.com/go/aem_cmp_tech_sharing_v1) delen | Widget voor delen via Facebook en Pinterest | `-` |
| [&#x200B; de Container van de Vorm &#x200B;](https://adobe.com/go/aem_cmp_tech_form_container_v2) | Responsief formulieralineasysteem | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [&#x200B; Tekst van de Vorm &#x200B;](https://adobe.com/go/aem_cmp_tech_form_text_v2) | Tekstinvoerveld | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [&#x200B; Opties van de Vorm &#x200B;](https://adobe.com/go/aem_cmp_tech_form_options_v2) | Invoerveld Meerdere opties | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [&#x200B; Verborgen Vorm &#x200B;](https://adobe.com/go/aem_cmp_tech_form_hidden_v2) | Verborgen invoerveld | `/libs/foundation/components/form/hidden` |
| [&#x200B; Knop van de Vorm &#x200B;](https://adobe.com/go/aem_cmp_tech_form_button_v2) | Verzenden of aangepaste knop | `/libs/foundation/components/form/submit` |
| [&#x200B; Navigatie &#x200B;](https://adobe.com/go/aem_cmp_tech_navigation_v1) | Een sitenavigatie-component die de geneste paginahiërarchie weergeeft | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [&#x200B; Navigatie van de Taal &#x200B;](https://adobe.com/go/aem_cmp_tech_langnav_v1) | Een taal- en landswitch die de algemene taalstructuur opsomt | `-` |
| [&#x200B; Snel Onderzoek &#x200B;](https://adobe.com/go/aem_cmp_tech_search_v1) | Een zoekcomponent die de resultaten als suggesties ter plaatse in een vervolgkeuzemenu weergeeft | `/libs/foundation/components/search` |
| [&#x200B; Taser &#x200B;](https://adobe.com/go/aem_cmp_tech_teaser_v1) | Hiermee kan de auteur van de inhoud eenvoudig een gummetje maken om inhoud te verfijnen met een afbeelding, titel of RTF-tekst en een koppeling maken naar verdere inhoud of andere handelingen | `-` |
| [&#x200B; Lusjes &#x200B;](https://adobe.com/go/aem_cmp_tech_tabs_v1) | Hiermee kan de auteur van de inhoud de pagina-inhoud op meerdere tabbladen ordenen | `-` |
| [&#x200B; Carousel &#x200B;](https://adobe.com/go/aem_cmp_tech_carousel_v1) | Hiermee kan de auteur van de inhoud de inhoud ordenen in een draaiende carrousel van dia&#39;s | `/libs/foundation/components/carousel` |
| [&#x200B; het Fragment van de Inhoud &#x200B;](https://adobe.com/go/aem_cmp_tech_cf_v1) | Hiermee kunt u een inhoudsfragment weergeven | `-` |
| [&#x200B; Lijst van het Fragment van de Inhoud &#x200B;](https://adobe.com/go/aem_cmp_tech_cflist_v1) | Hiermee wordt een lijst met inhoudsfragmenten weergegeven | `-` |
| [&#x200B; Scheidingsteken &#x200B;](https://adobe.com/go/aem_cmp_tech_separator_v1) | Hiermee wordt de inhoud van een pagina gescheiden | `-` |
| [&#x200B; Accordeon &#x200B;](https://adobe.com/go/aem_cmp_tech_accordion_v1) | Inhoudsdeelvensters ordenen in een inklapbare accordeon | `-` |
| [&#x200B; Container &#x200B;](https://adobe.com/go/aem_cmp_tech_container_v1) | Componenten indelen in een container | `-` |
| [&#x200B; Knoop &#x200B;](https://adobe.com/go/aem_cmp_tech_button_v1) | Een knop op een pagina maken | `-` |
| [&#x200B; Download &#x200B;](https://adobe.com/go/aem_cmp_tech_download_v1) | Een downloadbaar element toevoegen aan een pagina | `-` |
| [&#x200B; Fragment van de Ervaring &#x200B;](https://adobe.com/go/aem_cmp_tech_xf_v1) | Een ervaringsfragment toevoegen aan een pagina | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [&#x200B; bed &#x200B;](https://adobe.com/go/aem_cmp_tech_embed_v1) in | Een externe bron in een pagina insluiten | - |
| [&#x200B; Bar van de Voortgang &#x200B;](https://adobe.com/go/aem_cmp_tech_progress_v1) | Een visuele weergave geven van de voortgang in de richting van een doel | - |
| [&#x200B; de Kijker van PDF &#x200B;](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1) | Hiermee wordt een PDF-document op een pagina gepresenteerd | - |

## Upgrade van kerncomponenten {#upgrade-of-core-components}

Een voordeel van versioned componenten is dat het toestaat om de migratie aan een nieuwe versie van AEM van de migratie aan nieuwe componentenversies te scheiden. Als er nieuwe componentversies beschikbaar zijn, is het bovendien mogelijk om elke component afzonderlijk naar de nieuwe versie te migreren.

Migraties naar een nieuwe AEM-versie hebben geen invloed op de werking van de Core Components, op voorwaarde dat de versies ervan ook ondersteuning bieden voor de nieuwe AEM-versie waarnaar wordt gemigreerd. De aanpassingen die aan de Componenten van de Kern worden aangebracht zouden niet of moeten worden beïnvloed, zolang zij geen APIs gebruiken die [&#x200B; zijn afgekeurd of &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=nl-NL) verwijderd.

De migraties aan nieuwe versies van de Componenten van de Kern zullen niet beïnvloeden hoe de component ook werkt, maar de nieuwe eigenschappen zouden aan paginaauteurs kunnen worden geïntroduceerd, die één of andere configuratie door een malplaatjeredacteur zouden kunnen vereisen, voor het geval dat het standaardgedrag niet wordt gewenst. De aanpassingen nochtans zouden moeten worden aangepast, voor meer details zie [&#x200B; Aanpassend de pagina van de Componenten van de Kern &#x200B;](customizing.md#upgrade-compatibility-of-customizations).
