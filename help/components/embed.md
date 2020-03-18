---
title: Component insluiten
description: Met de component Embed kunt u externe inhoud insluiten in een AEM-inhoudspagina.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Component insluiten{#embed-component}

Met de component Core Components Embed kunt u externe inhoud insluiten in een AEM-inhoudspagina.

## Gebruik {#usage}

Met de component Core Component Embed kan de auteur van de inhoud geselecteerde externe inhoud definiëren die moet worden ingesloten in een AEM-inhoudspagina. Daarnaast is er een optie voor het definiëren van vrije HTML die ook moet worden ingesloten.

* De eigenschappen van de component kunnen in [vormen dialoog](#configure-dialog)worden bepaald.
* De standaardwaarden voor de component wanneer het toevoegen van het aan een pagina kunnen in de [ontwerpdialoog](#design-dialog)worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Embed Component is v1, die in september 2019 met versie 2.7.0 van de Componenten van de Kern werd geïntroduceerd, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v1 | Compatibel | Compatibel | Compatibel | Compatibel |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_embed)voor meer informatie over de insluitcomponent en voorbeelden van de bijbehorende configuratieopties en over HTML- en JSON-uitvoer.

## Technische details {#technical-details}

De recentste technische documentatie over de Embed Component [kan op GitHub](https://adobe.com/go/aem_cmp_tech_embed_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud de externe bron definiëren die op de pagina moet worden ingesloten. Kies eerst welk type bron moet worden ingesloten:

* [URL](#url)
* [Insluitbaar](#embeddable)
* [HTML](#html)

### URL {#url}

De eenvoudigste insluiting is de URL. Plak gewoon de URL van de bron die u wilt insluiten in het veld **URL** . De component probeert toegang te krijgen tot de bron en als deze door een van de processors kan worden gerenderd, wordt een bevestigingsbericht weergegeven onder het veld **URL** . Als dat niet het geval is, wordt het veld als een fout gemarkeerd.

De component Embed wordt geleverd bij processors voor de volgende typen bronnen:

* Bronnen die voldoen aan de [insluitingsstandaard](https://oembed.com/) , zoals Facebook Post, Instagram, SoundCloud, Twitter en YouTube
* Pinterest

Ontwikkelaars kunnen extra URL-processors toevoegen door [de ontwikkelaarsdocumentatie van de Embed Component te volgen.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](/help/assets/screen-shot-2019-09-25-10.08.29.png)

### Insluitbaar {#embeddable}

Met insluitbare bestanden kunt u de ingesloten bron verder aanpassen. U kunt hier parameters aan toewijzen en aanvullende informatie opnemen. Een auteur kan kiezen uit vooraf geconfigureerde vertrouwde insluitbare bestanden en de component wordt geleverd met een YouTube-insluitbare out-of-the-box.

Het veld **Insluitbaar** definieert het type processor dat u wilt gebruiken. In het geval van de insluitbare YouTube-modus kunt u het volgende definiëren:

* **Video-id** - De unieke video-id van YouTube van de bron die u wilt insluiten
* **Breedte** - De breedte van de ingesloten video
* **Hoogte** - De hoogte van de ingesloten video

Andere insluitbare bestanden bieden vergelijkbare velden en kunnen door een ontwikkelaar worden gedefinieerd aan de hand van de ontwikkelaarsdocumentatie van de Embed-component. [](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](/help/assets/screen-shot-2019-09-25-10.15.00.png)

>[!NOTE]
>Ingesloten tabellen moeten op sjabloonniveau via het dialoogvenster [](#design-dialog) Ontwerpen zijn ingeschakeld om beschikbaar te zijn voor de auteur van de pagina.

### HTML {#html}

Met de component Embed kunt u vrije HTML aan de pagina toevoegen.

![](/help/assets/screen-shot-2019-09-25-10.20.00.png)

>[!NOTE]
>Eventuele onveilige tags, zoals scripts, worden gefilterd vanuit de ingevoerde HTML en worden niet weergegeven op de resulterende pagina.

#### Beveiliging {#security}

De HTML-opmaak die de auteur kan invoeren, wordt voor beveiligingsdoeleinden gefilterd om scriptaanvallen te voorkomen die verwijzen naar andere sites en waarmee auteurs bijvoorbeeld beheerdersrechten kunnen verkrijgen.

*In het algemeen* worden alle script- en `style` elementen, alsmede alle `on*` en `style` kenmerken uit de uitvoer verwijderd.

De regels zijn echter gecompliceerder omdat de component Embed de algemene filterregelset van het HTML AntiSamy-sanitatieframework van AEM volgt, die u kunt vinden op `/libs/cq/xssprotection/config.xml`. Dit kan voor project-specifieke configuratie door een ontwikkelaar indien vereist worden bedekt.

Aanvullende beveiligingsinformatie vindt u in de [AEM-ontwikkelaarsdocumentatie voor on-premise installaties](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/security.html) en in AEM als installatie van [de Cloud Service.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/security/home.html)

>[!NOTE]
>Hoewel de regels van het AntiSamy- sanitatieframework door bedekking kunnen worden gevormd, beïnvloeden deze veranderingen al gedrag HTML en JSP en niet alleen de Embed Component van de Kern. `/libs/cq/xssprotection/config.xml`

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de inhoudauteur die de component Embed gebruikt en de standaardinstellingen die zijn ingesteld bij het plaatsen van de component Embed.

![](/help/assets/screen-shot-2019-09-25-10.25.28.png)

* **URL** uitschakelen - Schakelt de optie **URL** voor de auteur van de inhoud uit wanneer deze is geselecteerd
* **Uitschakelen Ingesloten** - Schakelt de optie **Insluitbaar** uit voor de auteur van de inhoud wanneer deze is geselecteerd, ongeacht welke insluitbare processors zijn toegestaan.
* **HTML** uitschakelen - Schakelt de optie **HTML** uit voor de auteur van de inhoud wanneer deze is geselecteerd.
* **Toegestane insluitbare bestanden** - Meerdere selecties die definiëren welke insluitbare processors beschikbaar zijn voor de auteur van de inhoud, op voorwaarde dat de optie **Insluitbaar** actief is.
