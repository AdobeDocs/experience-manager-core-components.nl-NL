---
title: Component insluiten (v1)
description: Met de component Embed kunt u externe inhoud insluiten in een AEM inhoudspagina.
role: Architect, Developer, Admin, User
exl-id: 28a2d196-cc1f-4e29-a8e4-c2e0acba3bfc
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '1298'
ht-degree: 0%

---

# Component insluiten (v1) {#embed-component}

Met de component Core Components Embed kunt u externe inhoud insluiten in een AEM inhoudspagina.

## Gebruik {#usage}

Met de component Core Component Embed kan de auteur van de inhoud geselecteerde externe inhoud definiëren die moet worden ingesloten in een AEM inhoudspagina. Bovendien is er een optie om ook vrije-vorm HTML te bepalen die moet worden ingebed.

* De eigenschappen van de component kunnen worden gedefinieerd in het dialoogvenster [dialoogvenster configureren](#configure-dialog).
* De standaardwaarden voor de component wanneer deze aan een pagina wordt toegevoegd, kunnen worden gedefinieerd in het dialoogvenster [ontwerpdialoogvenster](#design-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Embed-component beschreven. Deze is in september 2019 geïntroduceerd met versie 2.7.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Embed beschreven.
>
>Voor meer informatie over de huidige versie van de component Embed raadpleegt u de [Component insluiten](/help/components/embed.md) document.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de Embed-component wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_embed).

## Technische details {#technical-details}

De meest recente technische documentatie over de component Embed [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_embed_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud de externe bron definiëren die op de pagina moet worden ingesloten. Kies eerst welk type bron moet worden ingesloten:

* [URL](#url)
* [Insluitbaar](#embeddable)
* [HTML](#html)

Voor elk type insluitbaar kunt u een advertentie definiëren **ID**. Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).

* Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
* Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
* Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### URL {#url}

De eenvoudigste insluiting is de URL. Plak gewoon de URL van de bron die u wilt insluiten in het **URL** veld. De component probeert toegang te krijgen tot de bron en als deze door een van de processors kan worden gerenderd, wordt onder de **URL** veld. Als dat niet het geval is, wordt het veld als een fout gemarkeerd.

De component Embed wordt geleverd bij processors voor de volgende typen bronnen:

* Middelen die voldoen aan de [Standaard insluiten](https://oembed.com/) inclusief Facebook Post, Instagram, SoundCloud, Twitter en YouTube
* Pinterest

Ontwikkelaars kunnen extra URL-processors toevoegen door [volgt u de ontwikkelaarsdocumentatie van de Embed Component.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Dialoogvenster voor bewerken van component insluiten voor URL](/help/assets/embed-url.png)

### Insluitbaar {#embeddable}

Met insluitbare bestanden kunt u de ingesloten bron verder aanpassen. U kunt hier parameters aan toewijzen en aanvullende informatie opnemen. Een auteur kan een keuze maken uit vooraf geconfigureerde vertrouwde insluitbare bestanden en de component wordt geleverd met een YouTube-insluitbare out-of-the-box.

De **Insluitbaar** in het veld wordt het type processor gedefinieerd dat u wilt gebruiken. In het geval van de insluitbare YouTube kunt u het volgende definiëren:

* **Video-id** - De unieke video-id van YouTube van de bron die u wilt insluiten
* **Breedte** - De breedte van de ingesloten video
* **Hoogte** - De hoogte van de ingesloten video
* **Dempen inschakelen** - Deze parameter geeft aan of de video standaard wordt gedempt. Als u deze optie inschakelt, wordt de kans dat Automatisch afspelen werkt in moderne browsers groter.
* **Automatisch afspelen inschakelen** - Deze parameter geeft aan of de eerste video automatisch wordt afgespeeld wanneer de speler wordt geladen. Dit is alleen van toepassing op de publicatie-instantie of wanneer u de opdracht **Weergeven als gepubliceerd** op de ontwerpinstantie.
* **Lus inschakelen** - Bij één video geeft deze parameter aan of de speler de eerste video herhaaldelijk moet afspelen. In het geval van een afspeellijst speelt de speler de volledige afspeellijst af en begint vervolgens opnieuw bij de eerste video.
* **Inline afspelen inschakelen (iOS)** - Deze parameter bepaalt of video&#39;s inline (ingeschakeld) of op volledig scherm (uitgeschakeld) worden afgespeeld in een HTML5-speler op iOS.
* **Onbeperkte verwante video&#39;s** - Als deze optie is uitgeschakeld, komen verwante video&#39;s van hetzelfde kanaal als de video die net is afgespeeld, anders komen ze van elk kanaal.

De opties voor inschakelen moeten worden geactiveerd via het dialoogvenster [Ontwerpdialoogvenster](#design-dialog) en kan worden ingesteld als standaardwaarden.

Andere insluitbare bestanden bieden vergelijkbare velden en kunnen door een ontwikkelaar worden gedefinieerd door [volgt u de ontwikkelaarsdocumentatie van de Embed Component.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Dialoogvenster voor bewerken van component insluiten voor insluitbare bestanden](/help/assets/embed-embeddable.png)

>[!NOTE]
>Ingesloten tabellen moeten op sjabloonniveau zijn ingeschakeld via het dialoogvenster [Ontwerpdialoogvenster](#design-dialog) beschikbaar zijn voor de auteur van de pagina.

### HTML {#html}

Met de component Embed kunt u HTML in een vrije vorm aan de pagina toevoegen.

![Dialoogvenster voor bewerken van component insluiten voor HTML](/help/assets/embed-html.png)

>[!NOTE]
>Eventuele onveilige tags, zoals scripts, worden gefilterd vanaf de ingevoerde HTML en niet weergegeven op de resulterende pagina.

#### Beveiliging {#security}

De HTML-opmaak die de auteur kan invoeren, wordt gefilterd voor beveiligingsdoeleinden om scriptaanvallen te voorkomen die verwijzen naar andere sites en waarmee auteurs bijvoorbeeld beheerdersrechten kunnen verkrijgen.

*In het algemeen:* alle script en `style` en alle `on*` en `style` kenmerken worden uit de uitvoer verwijderd.

De regels zijn echter gecompliceerder omdat de component Embed AEM algemene filterregelset van het HTML AntiSamy-sanitatieframework volgt, die u kunt vinden op `/libs/cq/xssprotection/config.xml`. Dit kan voor project-specifieke configuratie door een ontwikkelaar indien vereist worden bedekt.

Aanvullende beveiligingsinformatie vindt u in het gedeelte [AEM ontwikkelaarsdocumentatie voor installaties op locatie](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/security.html) alsmede [AEM as a Cloud Service installaties.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/home.html)

>[!NOTE]
>Hoewel de regels van het AntiSamy sanitation framework kunnen worden geconfigureerd door bedekking `/libs/cq/xssprotection/config.xml`Deze wijzigingen zijn van invloed op al het HTML- en JSP-gedrag en niet alleen op de Embed Core Component.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de inhoudauteur die de component Embed gebruikt en de standaardinstellingen die zijn ingesteld bij het plaatsen van de component Embed.

### Tabblad Insluitbare typen {#embeddable-types-tab}

![Dialoogvenster Ontwerp van component insluiten](/help/assets/embed-design.png)

* **URL uitschakelen** - Schakelt de optie **URL** optie voor de auteur van de inhoud indien geselecteerd
* **Ingesloten tabellen uitschakelen** - Schakelt de optie **Insluitbaar** als deze optie is geselecteerd, ongeacht welke insluitbare processors zijn toegestaan.
* **HTML uitschakelen** - Schakelt de optie **HTML** als deze optie is geselecteerd voor de auteur van de inhoud.
* **Toegestane insluitbare bestanden** - Multiselect die bepaalt welke insluitbare bewerkers aan de auteur van de inhoud beschikbaar zijn, op voorwaarde dat **Insluitbaar** is actief.

### YouTube Tab {#youtube-tab}

![Het tabblad YouTube van het dialoogvenster Ontwerp van de component Embed](/help/assets/embed-design-youtube.png)

* **Configuratie van dempingsgedrag toestaan** - Hiermee stelt u de auteur van de inhoud in staat de **Dempen inschakelen** in de component wanneer het YouTube-insluittype is geselecteerd
   * **Standaardwaarde van dempen** - Automatisch sets **Dempen inschakelen** als het YouTube-insluittype is geselecteerd
* **Configuratie van gedrag voor automatisch afspelen toestaan** - Hiermee stelt u de auteur van de inhoud in staat de **Automatisch afspelen inschakelen** in de component wanneer het YouTube-insluittype is geselecteerd
   * **Standaardwaarde voor automatisch afspelen** - Automatisch sets **Automatisch afspelen inschakelen** als het YouTube-insluittype is geselecteerd
* **Configuratie van lusgedrag toestaan** - Hiermee stelt u de auteur van de inhoud in staat de **Lus inschakelen** in de component wanneer het YouTube-insluittype is geselecteerd
   * **Standaardwaarde van lus** - Automatisch sets **Lus inschakelen** als het YouTube-insluittype is geselecteerd
* **Configuratie van inline afspelen toestaan (iOS)** - Hiermee stelt u de auteur van de inhoud in staat de **Inline afspelen inschakelen (iOS)** in de component wanneer het YouTube-insluittype is geselecteerd
   * **Standaardwaarde voor inline afspelen (iOS)** - Automatisch sets **Inline afspelen inschakelen (iOS)** als het YouTube-insluittype is geselecteerd
* **Configuratie van inlinevideo&#39;s toestaan** - Hiermee stelt u de auteur van de inhoud in staat de **Onbeperkte verwante video&#39;s** in de component wanneer het YouTube-insluittype is geselecteerd
   * **Standaardwaarde van onbeperkte verwante video&#39;s** - Automatisch sets **Onbeperkte verwante video&#39;s** als het YouTube-insluittype is geselecteerd
