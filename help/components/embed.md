---
title: Component insluiten
description: Met de component Embed kunt u externe inhoud insluiten in een AEM inhoudspagina.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 2%

---


# Component insluiten{#embed-component}

Met de component Core Components Embed kunt u externe inhoud insluiten in een AEM inhoudspagina.

## Gebruik {#usage}

Met de component Core Component Embed kan de auteur van de inhoud geselecteerde externe inhoud definiëren die moet worden ingesloten in een AEM inhoudspagina. Daarnaast is er een optie voor het definiëren van vrije HTML die ook moet worden ingesloten.

* De eigenschappen van de component kunnen worden bepaald in [vorm dialoog](#configure-dialog).
* De standaardwaarden voor de component wanneer het toevoegen van het aan een pagina kunnen in [ontwerpdialoog](#design-dialog) worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Embed Component is v1, die in september 2019 met versie 2.7.0 van de Componenten van de Kern werd geïntroduceerd, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_embed) om de Embed-component te ervaren en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

## Technische details {#technical-details}

De recentste technische documentatie over de Embed Component [kan op GitHub](https://adobe.com/go/aem_cmp_tech_embed_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster {#configure-dialog} configureren

In het dialoogvenster voor configureren kan de auteur van de inhoud de externe bron definiëren die op de pagina moet worden ingesloten. Kies eerst welk type bron moet worden ingesloten:

* [URL](#url)
* [Insluitbaar](#embeddable)
* [HTML](#html)

Voor elk type insluitbaar kunt u een **ID** definiëren. Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).

* Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
* Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
* Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### URL {#url}

De eenvoudigste insluiting is de URL. Plak gewoon de URL van de bron die u wilt insluiten in het veld **URL**. De component probeert toegang te krijgen tot de bron en als deze door een van de processors kan worden gerenderd, wordt een bevestigingsbericht weergegeven onder het veld **URL**. Als dat niet het geval is, wordt het veld als een fout gemarkeerd.

De component Embed wordt geleverd bij processors voor de volgende typen bronnen:

* Bronnen die voldoen aan de [Insluiten-standaard](https://oembed.com/), waaronder Facebook Post, Instagram, SoundCloud, Twitter en YouTube
* Pinterest

Ontwikkelaars kunnen extra URL-processors toevoegen door [de ontwikkelaarsdocumentatie van de Embed Component te volgen.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Dialoogvenster voor bewerken van component insluiten voor URL](/help/assets/embed-url.png)

### Insluitbaar {#embeddable}

Met insluitbare bestanden kunt u de ingesloten bron verder aanpassen. U kunt hier parameters aan toewijzen en aanvullende informatie opnemen. Een auteur kan kiezen uit vooraf geconfigureerde vertrouwde insluitbare bestanden en de component wordt geleverd met een YouTube-insluitbare out-of-the-box.

Het veld **Insluitbaar** definieert het type processor dat u wilt gebruiken. In het geval van de insluitbare YouTube-modus kunt u het volgende definiëren:

* **Video-id** : de unieke video-id van YouTube van de bron die u wilt insluiten
* **Breedte** : de breedte van de ingesloten video
* **Hoogte**  - De hoogte van de ingesloten video

Andere insluitbare bestanden bieden vergelijkbare velden en kunnen door een ontwikkelaar worden gedefinieerd door [de ontwikkelaarsdocumentatie van de Embed-component te volgen.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Dialoogvenster voor bewerken van component insluiten voor insluitbare bestanden](/help/assets/embed-embeddable.png)

>[!NOTE]
>Ingesloten tabellen moeten op sjabloonniveau via [Ontwerpdialoogvenster](#design-dialog) zijn ingeschakeld om beschikbaar te zijn voor de auteur van de pagina.

### HTML {#html}

Met de component Embed kunt u vrije HTML aan de pagina toevoegen.

![Dialoogvenster voor bewerken van component insluiten voor HTML](/help/assets/embed-html.png)

>[!NOTE]
>Eventuele onveilige tags, zoals scripts, worden gefilterd vanuit de ingevoerde HTML en worden niet weergegeven op de resulterende pagina.

#### Beveiliging {#security}

De HTML-opmaak die de auteur kan invoeren, wordt voor beveiligingsdoeleinden gefilterd om scriptaanvallen te voorkomen die verwijzen naar andere sites en waarmee auteurs bijvoorbeeld beheerdersrechten kunnen verkrijgen.

*In het algemeen worden* alle script- en  `style` elementen, alsmede alle  `on*` en  `style` kenmerken uit de uitvoer verwijderd.

De regels zijn echter gecompliceerder omdat de Embed-component de algemene filterregelset van het HTML AntiSamy-sanitatieframework van AEM volgt, die u kunt vinden op `/libs/cq/xssprotection/config.xml`. Dit kan voor project-specifieke configuratie door een ontwikkelaar indien vereist worden bedekt.

Aanvullende beveiligingsinformatie vindt u in de [AEM ontwikkelaarsdocumentatie voor on-premise installaties](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/security.html) en [AEM als Cloud Service installaties.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/security/home.html)

>[!NOTE]
>Hoewel de regels van het AntiSamy- sanitatieframework door `/libs/cq/xssprotection/config.xml` te bedekken kunnen worden gevormd, beïnvloeden deze veranderingen al gedrag HTML en JSP en niet alleen de Embed Component van de Kern.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de inhoudauteur die de component Embed gebruikt en de standaardinstellingen die zijn ingesteld bij het plaatsen van de component Embed.

![Dialoogvenster Ontwerp van component insluiten](/help/assets/embed-design.png)

* **URL**  uitschakelen - Schakelt de  **** URL-optie voor de auteur van de inhoud uit wanneer deze is geselecteerd
* **Uitschakelen Ingesloten**  - Schakelt de optie  **** Insluitbaar voor de auteur van de inhoud uit wanneer deze is geselecteerd, ongeacht welke insluitbare processors zijn toegestaan.
* **HTML**  uitschakelen - Schakelt de  **** HTML-optie voor de auteur van de inhoud uit wanneer deze is geselecteerd.
* **Toegestane insluitbare bestanden**  - Meerdere selecties waarmee wordt gedefinieerd welke insluitbare processors beschikbaar zijn voor de auteur van de inhoud, op voorwaarde dat de optie  **** Insluitbaar actief is.
