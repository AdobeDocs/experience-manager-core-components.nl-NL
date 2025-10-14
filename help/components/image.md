---
title: Afbeeldingscomponent
description: De component Core Component Image is een adaptieve afbeeldingscomponent.
role: Architect, Developer, Admin, User
exl-id: c5e57f4b-139f-40e7-8d79-be9a74360b63
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '2062'
ht-degree: 0%

---


# Afbeeldingscomponent {#image-component}

De component Core Component Image is een adaptieve afbeeldingscomponent.

{{traditional-aem}}

## Gebruik {#usage}

De component Afbeelding biedt een adaptieve selectie van afbeeldingen en een responsief gedrag bij het lui laden van de pagina voor de bezoeker van de pagina en bij het eenvoudig plaatsen van de afbeelding voor de auteur van de inhoud.

De inhoudauteur kan [&#x200B; gebruiken uitgeeft dialoog &#x200B;](#edit-dialog) om de beeldactiva uit te geven zoals het toepassen van een uitsnijding of het roteren van het beeld.

De beeldbreedten en de extra montages kunnen door de malplaatjeauteur in de [&#x200B; ontwerpdialoog &#x200B;](#design-dialog) worden bepaald. De inhoudsredacteur kan activa in [&#x200B; uploaden of selecteren vormt dialoog.](#configure-dialog)

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Image Component is v3, die in februari 2022 is geïntroduceerd met versie 2.18.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v3 | - | Compatibel | Compatibel | Compatibel |
| [&#x200B; v2 &#x200B;](v2/image.md) | Compatibel | Compatibel | - | Compatibel |
| [&#x200B; v1 &#x200B;](v1/image-v1.md) | Compatibel | Compatibel | - | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [&#x200B; Kern &#x200B;](/help/versions.md).

## Responsieve functies {#responsive-features}

De component Image wordt geleverd met robuuste responsieve functies die direct uit de verpakking kunnen worden geleverd. Op het niveau van het paginamalplaatje, kan de [&#x200B; ontwerpdialoog &#x200B;](#design-dialog) worden gebruikt om de standaardbreedten van het beeldactiva te bepalen. De component Afbeelding laadt automatisch de juiste breedte om weer te geven, afhankelijk van de grootte van het browservenster. Wanneer het formaat van het venster wordt gewijzigd, laadt de component Image dynamisch de juiste afbeeldingsgrootte. Componentontwikkelaars hoeven zich geen zorgen te maken over het definiëren van aangepaste mediaquery&#39;s, aangezien de component Image al is geoptimaliseerd om uw inhoud te laden.

Bovendien ondersteunt de component Afbeelding lui laden om het laden van het eigenlijke afbeeldingselement uit te stellen totdat het element zichtbaar is in de browser, waardoor de reacties op uw pagina&#39;s sneller worden.

>[!TIP]
>
>De component Image wordt standaard geactiveerd door de adaptieve afbeeldingsserver. Zie [&#x200B; Aangepaste Servlet van het Beeld &#x200B;](/help/developing/adaptive-image-servlet.md) voor details op hoe het werkt.

### Verschillen met v2 {#v2-differences}

In tegenstelling tot versie 2 van de Afbeeldingscomponent, gebruikt versie 3 browsereigen reactievermogen. Dit betekent dat de browser een reeks bronnen voor een afbeelding voor verschillende breedten ontvangt en dat de browser de beste bron kiest.

Meestal wordt in browsers liever lokaal een grotere breedte verkleind om een kleinere viewport te gebruiken in plaats van de afbeelding met een kleinere breedte van de server op te halen. Dit wordt verwacht en waarom de afbeeldingscomponent niet mag worden gebruikt voor illustraties (verschillende afbeeldingen/uitsnijdingen voor verschillende viewports).

[&#x200B; gelieve te zien de technische documentatie van de Component van het Beeld &#x200B;](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/image/v3/image#javascript-data-attribute-bindings) voor meer informatie.

## Ondersteuning voor dynamische media {#dynamic-media}

De Component van het Beeld (van [&#x200B; versie 2.13.0 &#x200B;](/help/versions.md)) steunt [&#x200B; Dynamische Media &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media.html?lang=nl-NL) activa. [&#x200B; wanneer toegelaten, &#x200B;](#design-dialog) bieden deze eigenschappen de capaciteit aan om Dynamische het beeldactiva van Media met eenvoudige belemmering-en-daling of via activa toe te voegen browser enkel zoals u een ander beeld. Daarnaast worden ook afbeeldingsaanpassingen, voorinstellingen voor afbeeldingen en slimme gewassen ondersteund.

Uw webbeleving die is gebouwd met Core Components kan beschikken over uitgebreide, op Sensei gebaseerde, robuuste, krachtige, platformonafhankelijke mogelijkheden voor Dynamic Media Image.

## Externe Assets-ondersteuning {#remote-assets}

De Component van het Beeld (van [&#x200B; versie 2.23.2 &#x200B;](/help/versions.md)) steunt verre activa. [&#x200B; Zodra gevormd, &#x200B;](/help/developing/remote-assets.md) kunt u activa van de verre dienst voor uw beeldcomponent selecteren.

## SVG-ondersteuning {#svg-support}

Scalable Vector Graphics (SVG) wordt ondersteund door de Afbeeldingscomponent.

* Het slepen en neerzetten van een SVG-element van DAM en het uploaden van een SVG-bestand dat vanuit een lokaal bestandssysteem is geüpload, worden beide ondersteund.
* Het oorspronkelijke SVG-bestand wordt gestreamd (transformaties worden overgeslagen).
* Voor een SVG-afbeelding worden de &quot;smart images&quot; en de &quot;smart sizes&quot; ingesteld op een lege array in het afbeeldingsmodel.

### Beveiliging {#security}

Vanwege beveiligingsredenen wordt de originele SVG nooit rechtstreeks aangeroepen door de Afbeeldingseditor. Deze wordt aangeroepen via `<img src="path-to-component">` . Hierdoor wordt voorkomen dat de browser scripts uitvoert die in het SVG-bestand zijn ingesloten.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van het Beeld te ervaren en voorbeelden van zijn configuratieopties en de output van HTML en JSON te zien, bezoek de [&#x200B; Bibliotheek van de Component &#x200B;](https://adobe.com/go/aem_cmp_library_image).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van het Beeld [&#x200B; kan op GitHub &#x200B;](https://adobe.com/go/aem_cmp_tech_image_v3) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [&#x200B; de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden &#x200B;](/help/developing/overview.md).

De Component van het Beeld steunt [&#x200B; schema.org microdata &#x200B;](https://schema.org).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de afbeelding uitsnijden en zoomen.

Afhankelijk van als u de [&#x200B; Dynamische Media &#x200B;](#dynamic-media) toegelaten hebt of [&#x200B; Verre Steun van Assets &#x200B;](#remote-assets) wordt toegelaten, verschillen de opties beschikbaar voor het uitgeven van beelden.

### Standaard bewerken van bedrijfsmiddelen {#standard-assets}

Als u standaardAEM activa uitgeeft, kunt u **klikken geeft** pictogram in het contextmenu van de beeldcomponent uit.

![&#x200B; de Edit dialoog van de Component van het Beeld &lbrace;](/help/assets/image-edit.png)

* Uitsnijden starten

  ![&#x200B; Uitsnijdpictogram van het Begin &#x200B;](/help/assets/image-start-crop.png)

  Als u deze optie selecteert, wordt een vervolgkeuzelijst geopend voor vooraf gedefinieerde verhoudingen voor uitsnijden.

   * Kies de optie **verwijdert Uitsnijden** om de originele activa te tonen.

  Als een uitsnijdoptie is geselecteerd, gebruikt u de blauwe handgrepen om het uitsnijden op de afbeelding te vergroten of te verkleinen.

  ![&#x200B; de opties van het Gewas &#x200B;](/help/assets/image-crop-options.png)

* Rechtsom roteren

  ![&#x200B; roteer het juiste pictogram &#x200B;](/help/assets/image-rotate-right.png)

  Gebruik deze optie als u de afbeelding 90° rechtsom wilt roteren.

* Zoomen herstellen

  ![&#x200B; het gezoempictogram van het Terugstellen &#x200B;](/help/assets/image-reset-zoom.png)

  Als al op de afbeelding is ingezoomd, gebruikt u deze optie om het zoomniveau opnieuw in te stellen.

* Zoomregelaar openen

  ![&#x200B; Open pictogram van de gezoemschuif &#x200B;](/help/assets/image-zoom.png)

  Met deze optie geeft u een schuifregelaar weer om het zoomniveau van de afbeelding te bepalen.

  ![&#x200B; de schuifcontrole van het Gezoem &#x200B;](/help/assets/image-zoom-slider.png)

U kunt de interne editor ook gebruiken om de afbeelding te wijzigen. Vanwege ruimtebeperkingen zijn alleen de basisopties online beschikbaar. Voor volledige bewerkingsopties gebruikt u de modus Volledig scherm.

![&#x200B; Beeld op zijn plaats geeft opties uit &#x200B;](/help/assets/image-in-place-edit.png)

>[!NOTE]
>
>Beeldbewerkingsbewerkingen worden niet ondersteund voor GIF-afbeeldingen. Dergelijke wijzigingen die in de bewerkingsmodus in GIF&#39;s zijn aangebracht, blijven niet bestaan.

### Dynamisch bewerken van media-elementen {#dynamic-media-assets}

Als u [&#x200B; Dynamische toegelaten eigenschappen van Media hebt, &#x200B;](#dynamic-media) het uitgeven van het beeld zelf moet in de activa worden uitgevoerd console.

## Dialoogvenster configureren {#configure-dialog}

De component image biedt een dialoogvenster voor configureren waarin de afbeelding zelf wordt gedefinieerd, samen met de beschrijving en basiseigenschappen.

### Tabblad Element {#asset-tab}

![&#x200B; het lusje van Activa van de Component van het Beeld vormt dialoog &#x200B;](/help/assets/image-configure-asset.png)

* **erven geërfte beeld van pagina** - deze optie gebruikt het [&#x200B; geprezen beeld van de verbonden pagina &#x200B;](page.md) of het gekenmerkte beeld van de huidige pagina als het beeld niet verbonden is.

* **activa van het Beeld** - dit wordt automatisch bevolkt als **geërft beeld van pagina** wordt geselecteerd. Schakel deze optie uit als u de afbeelding handmatig wilt definiëren door de volgende opties in te stellen.

   * Daling een activa van [&#x200B; activa browser &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html?lang=nl-NL) of ontvang **doorbladert** optie zodat kunt u van een lokaal dossiersysteem uploaden.
   * Tik of klik **Duidelijk** om het momenteel geselecteerde beeld te deselecteren.
   * Tik of klik **Keuze** om [&#x200B; activa browser &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html?lang=nl-NL) te openen zodat kunt u een beeld selecteren.
      * Als [&#x200B; de Verre Steun van Activiteiten &#x200B;](#remote-assets) wordt toegelaten, hebt u veelvoudige opties om activa te kiezen:
         * **Lokale** selecteert van de lokale de activabibliotheek van AEM.
         * **Verre** selecteert van een Dynamische bibliotheek van Media buiten uw instantie van AEM.
   * Tik of klik **uitgeven** [&#x200B; om de vertoningen van de activa &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets.html?lang=nl-NL) in de Redacteur van Activa te beheren.

* **Alternatieve tekst voor toegankelijkheid** - Dit gebied staat u toe om een beschrijving van het beeld voor visueel gehandicapte gebruikers te bepalen.

   * **erven alternatieve tekst van pagina** - Deze optie gebruikt de alternatieve beschrijving van de verbonden activawaarde van de `dc:description` meta-gegevens in DAM of van de huidige pagina als geen activa wordt verbonden.

* **verstrekt geen alternatieve tekst** - Merkt het beeld dat door ondersteunende technologieën zoals het schermlezers voor gevallen moet worden genegeerd waar het beeld zuiver decoratief is of anders geen extra informatie aan de pagina overbrengt.

### Tabblad Metagegevens {#metadata-tab}

![&#x200B; Meta-gegevens lusje van de Component van het Beeld vormt dialoog &#x200B;](/help/assets/image-configure-metadata.png)

* **vooraf ingesteld Type** - dit bepaalt de types van beeld vooraf instelt beschikbaar, of **Vooraf ingesteld Beeld** of **Slim Gewas**, en is slechts beschikbaar wanneer [&#x200B; de Dynamische eigenschappen van Media &#x200B;](#dynamic-meida) worden toegelaten.
   * **Vooraf ingesteld Beeld** - wanneer **Vooraf ingesteld Type** van **Vooraf ingesteld Beeld** wordt geselecteerd, is het drop-down **Beeld Vooraf ingesteld** beschikbaar, toestaand selectie van de beschikbare Dynamische Voorinstellingen van Media. Dit is alleen beschikbaar als er voorinstellingen zijn gedefinieerd voor het geselecteerde element.
   * **Slim Gewas** - wanneer **Vooraf ingesteld Type** van **Slim Gewas** wordt geselecteerd, is de drop-down **Vertoning** beschikbaar, toestaand selectie van de beschikbare vertoningen van het geselecteerde activa. Dit is alleen beschikbaar als uitvoeringen zijn gedefinieerd voor het geselecteerde element.
   * **de Modifiers van het Beeld** - het Extra Dynamische beeld dat van Media bevelen dienen kan hier worden bepaald door `&`, ongeacht welk **Vooraf ingesteld Type** wordt geselecteerd.
* **Titel** - de Extra informatie over het beeld, die onder het beeld door gebrek wordt getoond.
   * **krijgt titel van DAM** - wanneer gecontroleerd de de titeltekst van het beeld wordt bevolkt met de waarde van de `dc:title` meta-gegevens in DAM.
   * **titel van de Vertoning als pop-up** - wanneer gecontroleerd, wordt de titel niet getoond onder het beeld, maar als pop-up die door sommige browsers wordt getoond wanneer het bedekken over het beeld.
* **Verbinding** - verbind het beeld met een ander middel.
   * In het dialoogvenster Selecteren kunt u een koppeling maken naar een andere AEM-bron.
   * Als u geen koppeling naar een AEM-resource wilt maken, voert u de absolute URL in. Niet-absolute URL&#39;s worden geïnterpreteerd als relatief ten opzichte van AEM.
   * **Open verbinding in nieuw lusje** - deze optie opent de verbinding in een nieuw browser venster.
* **identiteitskaart** - Deze optie laat u het unieke herkenningsteken van de component in HTML en in de [&#x200B; Laag van Gegevens controleren &#x200B;](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

>[!TIP]
>
>**het Slimme Gewas** en **Vooraf ingesteld Beeld** zijn wederzijds exclusieve opties. Als een auteur een beeld moet gebruiken vooraf ingesteld samen met een Slimme vertoning van het Gewas, moet de auteur de **Modifiers van het Beeld** gebruiken om manueel vooraf instelt toe te voegen.

### Tabblad Stijlen {#styles-tab-edit}

![&#x200B; het lusje van Stijlen van uitgeeft dialoog van de Component van het Beeld &#x200B;](/help/assets/image-configure-styles.png)

De Component van het Beeld steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [&#x200B; ontwerpdialoog &#x200B;](#design-dialog) voor het drop-down menu worden gevormd om beschikbaar te zijn.

## Ontwerpdialoogvenster {#design-dialog}

### Hoofdtabblad {#main-tab}

![&#x200B; het belangrijkste lusje van de het ontwerpdialoog van de Component van het Beeld het ontwerp &#x200B;](/help/assets/image-design-main.png)

* **laat eigenschappen DM** toe - wanneer gecontroleerd, [&#x200B; de Dynamische eigenschappen van Media &#x200B;](#dynamic-media) zijn beschikbaar.
   * Deze optie wordt alleen weergegeven wanneer Dynamische media is ingeschakeld in de omgeving.
* **laat Web Geoptimaliseerde Beelden** toe - wanneer gecontroleerd, [&#x200B; de Web-geoptimaliseerde dienst van de beeldlevering &#x200B;](/help/developing/web-optimized-image-delivery.md) levert beelden in het formaat WebP, die beeldgrootte door gemiddeld 25% verminderen.
   * Deze optie is alleen beschikbaar in AEMaaCS.
   * Wanneer ongecontroleerd, of de Web-geoptimaliseerde dienst van de beeldlevering niet beschikbaar is, wordt de [&#x200B; Aangepaste Servlet van het Beeld &#x200B;](/help/developing/adaptive-image-servlet.md) gebruikt.
* **maak luie lading** onbruikbaar - wanneer gecontroleerd, laadt de component alle beelden zonder luie lading vooraf.
* **Beeld is decoratief** - bepaal als de decoratieve beeldoptie automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **krijgt alternatieve tekst van DAM** - bepaalt als de optie om de afwisselende tekst van DAM terug te winnen automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **krijgt titel van DAM** - bepaalt als de optie om de titel van DAM terug te winnen automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **de titel van de Vertoning als pop-up** - bepaalt als de optie om de beeldtitel als pop-up te tonen automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **resizing breedte** - deze waarde wordt gebruikt voor het resizing van de breedte van de basisbeelden die activa DAM zijn.
   * De hoogte-breedteverhouding van de afbeeldingen blijft behouden.
   * Als de waarde groter is dan de werkelijke breedte van de afbeelding, heeft deze waarde geen effect.
   * Deze waarde heeft geen effect op SVG-afbeeldingen.

U kunt een lijst van breedten in pixel voor het beeld bepalen, en de component laadt automatisch de meest aangewezen breedte gebaseerd op browser grootte. Dit is een belangrijk deel van [&#x200B; ontvankelijke eigenschappen &#x200B;](#responsive-features) van de Component van het Beeld.

* **Breedten** - bepaalt een lijst van breedten in pixel voor het beeld en de component laadt automatisch de meest aangewezen breedte die op browser grootte wordt gebaseerd.
   * Tik of klik **voeg** knoop toe om een andere grootte toe te voegen.
      * Gebruik de handgrepen om de grootte te wijzigen.
      * Gebruik het **pictogram van de Schrapping** om een breedte te verwijderen.
   * Het laden van afbeeldingen wordt standaard uitgesteld totdat ze zichtbaar worden.
      * Selecteer de optie **maak het laden** onbruikbaar zodat kunt u de beelden op paginading laden.
* **de Kwaliteit van JPEG** - de kwaliteitsfactor (in percentage van 0 en 100) voor getransformeerde (bijvoorbeeld, geschraapte of bebouwde) beelden van JPEG.

>[!TIP]
>
>Zie het document [&#x200B; Aangepaste Servlet van het Beeld &#x200B;](/help/developing/adaptive-image-servlet.md) voor uiteinden voor het optimaliseren van vertoningsselectie door uw breedten zorgvuldig te bepalen.

### Tabblad Stijlen {#styles-tab}

De Component van het Beeld steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De Component van het Beeld steunt de [&#x200B; Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
