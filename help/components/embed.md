---
title: Component insluiten
description: Met de component Embed kunt u externe inhoud insluiten in een AEM-inhoudspagina.
role: Architect, Developer, Admin, User
exl-id: 985fa304-70a3-4329-957e-76d1832a06f1
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 0%

---

# Component insluiten {#embed-component}

Met de component Core Components Embed kunt u externe inhoud insluiten in een AEM-inhoudspagina.

## Gebruik {#usage}

Met de component Core Component Embed kan de auteur van de inhoud geselecteerde externe inhoud definiëren die moet worden ingesloten op een AEM-inhoudspagina. Daarnaast is er een optie voor het definiëren van HTML met vrije vorm die ook moet worden ingesloten.

* De eigenschappen van de component kunnen in [ worden bepaald vormen dialoog ](#configure-dialog).
* De gebreken voor de component wanneer het toevoegen van het aan een pagina kunnen in de [ ontwerpdialoog ](#design-dialog) worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Embed Component is v2, die in februari 2022 met versie 2.18.0 van de Componenten van de Kern werd geïntroduceerd, en in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v2 | - | Compatibel | Compatibel | Compatibel |
| [ v1 ](v1/embed.md) | Compatibel | Compatibel | - | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Embed Component te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_embed).

## Technische details {#technical-details}

De recentste technische documentatie over Embed Component [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_embed_v2) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud de externe bron definiëren die op de pagina moet worden ingesloten.

### Tabblad Eigenschappen {#properties-tab}

Kies eerst welk type bron moet worden ingesloten:

* [URL](#url)
* [Insluitbaar](#embeddable)
* [HTML](#html)

Voor elk type van ingebedd able, kunt u een **identiteitskaart** bepalen. Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens ](/help/developing/data-layer/overview.md) te controleren.

* Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
* Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
* Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

#### URL {#url}

De eenvoudigste insluiting is de URL. Plak eenvoudig URL van het middel u wenst om in het **URL** gebied in te bedden. De component zal proberen om tot het middel toegang te hebben en als het door één van de bewerkers kan worden teruggegeven, zal het een bevestigingsbericht onder het **URL** gebied tonen. Als dat niet het geval is, wordt het veld als een fout gemarkeerd.

De component Embed wordt geleverd bij processors voor de volgende typen bronnen:

* Middelen die aan de [ norm inbedden ](https://oembed.com/) met inbegrip van Post Facebook, Instagram, SoundCloud, Twitter, en YouTube voldoen
* Pinterest

De ontwikkelaars kunnen extra bewerkers URL door [ na de ontwikkelaarsdocumentatie van de Embed Component toevoegen.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![ bedt Component geeft dialoog voor URL uit ](/help/assets/embed-url.png)

#### Insluitbaar {#embeddable}

Met insluitbare bestanden kunt u de ingesloten bron verder aanpassen. U kunt hier parameters aan toewijzen en aanvullende informatie opnemen. Een auteur kan een keuze maken uit vooraf geconfigureerde vertrouwde insluitbare bestanden en de component wordt geleverd met een YouTube-insluitbare out-of-the-box.

Het **Inbeddable** gebied bepaalt het type van bewerker u wilt gebruiken. In het geval van de insluitbare YouTube kunt u het volgende definiëren:

* **Video identiteitskaart** - unieke videoidentiteitskaart van YouTube van het middel u wilt inbedden
* **Breedte** - de breedte van de ingebedde video
* **Hoogte** - de hoogte van de ingebedde video
* **laat Dempen** toe - Deze parameter specificeert of de video gedempt door gebrek zal spelen. Als u deze optie inschakelt, wordt de kans dat Automatisch afspelen werkt in moderne browsers groter.
* **laat Autoplay** toe - Deze parameter specificeert of de aanvankelijke video automatisch zal beginnen te spelen wanneer de speler laadt. Dit is slechts efficiënt op publiceer instantie of wanneer het gebruiken van de **Mening zoals Gepubliceerde** optie op de auteursinstantie.
* **laat Lijn** toe - in het geval van één enkele video, specificeert deze parameter of de speler de aanvankelijke video herhaaldelijk zou moeten spelen. In het geval van een afspeellijst speelt de speler de volledige afspeellijst af en begint vervolgens opnieuw bij de eerste video.
* **laat Inline Playback (iOS) toe** - Deze parameter controleert of video&#39;s inline (op) of volledig scherm (weg) in een speler HTML5 op iOS spelen.
* **Onbeperkte Verwante Verwante Video&#39;s** - als deze optie gehandicapt is, zullen de verwante video&#39;s uit het zelfde kanaal komen zoals de video die enkel werd gespeeld, anders zullen zij uit om het even welk kanaal komen.

Andere inbeddables zouden gelijkaardige gebieden aanbieden en kunnen door een ontwikkelaar door [ na de ontwikkelaarsdocumentatie van de Embed Component worden bepaald.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![ bedt de Edit dialoog van de Component voor ingebedde Lijsten ](/help/assets/embed-embeddable.png)

>[!NOTE]
>
>Embeddables moet op het malplaatjeniveau via de [ Dialoog van het Ontwerp ](#design-dialog) worden toegelaten om aan de paginaauteur beschikbaar te zijn.

#### HTML {#html}

Met de component Embed kunt u HTML met vrije vorm toevoegen aan uw pagina.

![ bed Component&#39;s uitgeeft dialoog voor HTML ](/help/assets/embed-html.png) in

>[!NOTE]
>Eventuele onveilige tags, zoals scripts, worden gefilterd vanaf de ingevoerde HTML en niet weergegeven op de resulterende pagina.

##### Beveiliging {#security}

De HTML-opmaakcode die de auteur kan invoeren, wordt voor beveiligingsdoeleinden gefilterd om problemen met scripts die verwijzen naar andere sites, te voorkomen. Hierdoor kunnen auteurs bijvoorbeeld administratieve rechten krijgen.

In het algemeen worden alle script- en `style` -elementen en alle `on*` - en `style` -kenmerken uit de uitvoer verwijderd.

De regels zijn echter gecompliceerder omdat de Embed-component volgt op de filterregelset van het globale HTML AntiSamy-sanitatieframework van AEM, die u kunt vinden op `/libs/cq/xssprotection/config.xml` . Dit kan voor project-specifieke configuratie door een ontwikkelaar indien vereist worden bedekt.

De extra veiligheidsinformatie kan in de [ de ontwikkelaarsdocumentatie van AEM voor op-gebouw installaties ](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/security.html) evenals [ installaties van AEM as a Cloud Service worden gevonden.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/home.html)

>[!NOTE]
>
>Hoewel de regels van het AntiSamy sanitation framework kunnen worden geconfigureerd door `/libs/cq/xssprotection/config.xml` te bedekken, zijn deze wijzigingen van invloed op al het HTML- en JSP-gedrag en niet alleen op de Embed Core Component.

### Tabblad Stijlen {#styles-tab-edit}

![ het lusje van Stijlen van uitgeeft dialoog van Embed Component ](/help/assets/embed-styles.png)

De Embed Component steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [ ontwerpdialoog ](#design-dialog) worden gevormd opdat het drop-down menu beschikbaar is.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de inhoudauteur die de component Embed gebruikt en de standaardinstellingen die zijn ingesteld bij het plaatsen van de component Embed.

### Tabblad Insluitbare typen {#embeddable-types-tab}

![ bed de het ontwerpdialoog van de Component ](/help/assets/embed-design.png) in

* **maak URL** onbruikbaar - maakt de **URL** optie voor de inhoudauteur onbruikbaar wanneer geselecteerd
* **maak Inbeddables** onbruikbaar - maakt de **Inbeddable** optie voor de inhoudauteur wanneer geselecteerd onbruikbaar, ongeacht welke ingebedde bewerkers worden toegestaan.
* **maak HTML** onbruikbaar - maakt de **HTML** optie voor de inhoudauteur onbruikbaar wanneer geselecteerd.
* **Toegestane Embeddables** - Multiselect die bepaalt welke beddable bewerkers aan de inhoudauteur beschikbaar zijn, op voorwaarde dat de **Inbeddable** optie actief is.

### YouTube Tab {#youtube-tab}

![ YouTube lusje van de Embed het ontwerpdialoog van de Component ](/help/assets/embed-design-youtube.png)

* **staat configuratie van stomme gedrag** toe - staat inhoudauteur toe om **te vormen toelaten Dempen** optie in de component wanneer YouTube inbedt type wordt geselecteerd
   * **Standaardwaarde van dempen** - plaatst automatisch **Dempen** optie toelaten wanneer YouTube inbedt type wordt geselecteerd
* **staat configuratie van autoplay gedrag** toe - staat inhoudauteur toe om **te vormen laat** optie Autoplay in de component toe wanneer YouTube inbedt type wordt geselecteerd
   * **Standaardwaarde van autoplay** - plaatst automatisch **Autoplay** optie toelaat wanneer YouTube inbedt type wordt geselecteerd
* **staat configuratie van lusgedrag** toe - staat inhoudauteur toe om **te vormen toelaten Lijn** optie in de component wanneer YouTube inbedt type wordt geselecteerd
   * **Standaardwaarde van lijn** - plaatst automatisch **Loop** optie toelaten wanneer YouTube inbedt type wordt geselecteerd
* **staat configuratie van gealigneerde playback (iOS) toe** - staat inhoudauteur toe om **te vormen laat Gealigneerde Playback (iOS)** optie in de component toe wanneer YouTube inbedt type wordt geselecteerd
   * **Standaardwaarde van gealigneerde playback (iOS)** - plaatst automatisch **laat Gealigneerde Playback (iOS) toe** optie wanneer YouTube inbed type wordt geselecteerd
* **staat configuratie van gealigneerde video&#39;s** toe - staat inhoudsauteur toe om de **Onbeperkte Verwante Verwante Video&#39;s** optie in de component te vormen wanneer YouTube inbedt type wordt geselecteerd
   * **Standaardwaarde van onbeperkte verwante video&#39;s** - plaatst automatisch **Onbeperkte Verwante Verwante Video&#39;s** optie wanneer YouTube inbedt type wordt geselecteerd
