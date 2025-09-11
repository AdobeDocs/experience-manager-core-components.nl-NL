---
title: Afbeeldingscomponent (v2)
description: De Core Component Image is een adaptieve beeldcomponent die ter plekke kan worden bewerkt.
role: Architect, Developer, Admin, User
exl-id: 3f2b93f9-c48d-43ef-a78a-accd5090fe6f
index: n
source-git-commit: 3908828cf62043483a74e908204c3e9bf540300b
workflow-type: tm+mt
source-wordcount: '2048'
ht-degree: 0%

---


# Afbeeldingscomponent (v2) {#image-component}

De component Core Component Image is een adaptieve afbeeldingscomponent die op locatie kan worden bewerkt.

## Gebruik {#usage}

De component Afbeelding biedt een adaptieve selectie van afbeeldingen en een responsief gedrag bij het lui laden voor de bezoeker van de pagina en bij het eenvoudig plaatsen en uitsnijden van de afbeelding voor de auteur van de inhoud.

De beeldbreedten evenals het bebouwen en extra montages kunnen door de malplaatjeauteur in de [ ontwerpdialoog ](#design-dialog) worden bepaald. De inhoudsredacteur kan activa in [ uploaden of selecteren vormt dialoog ](#configure-dialog) en bebouwt het beeld in [ uitgeeft dialoog ](#edit-dialog). Voor meer gebruiksgemak is het ook mogelijk de afbeelding op een eenvoudige plaats aan te passen.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 2 van de Image Component beschreven, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 1 van de afbeeldingscomponent beschreven.
>
>Voor details van de huidige versie van de Component van het Beeld, zie het [ document van de Component van het Beeld 0} {.](/help/components/image.md)

## Responsieve functies {#responsive-features}

De component Image wordt geleverd met robuuste responsieve functies die direct uit de verpakking kunnen worden geleverd. Op het niveau van het paginamalplaatje, kan de [ ontwerpdialoog ](#design-dialog) worden gebruikt om de standaardbreedten van het beeldactiva te bepalen. De component van het Beeld zal dan automatisch de correcte breedte aan vertoning afhankelijk van de grootte van het browser venster laden. Wanneer het formaat van het venster wordt gewijzigd, laadt de component Image dynamisch de juiste afbeeldingsgrootte. Componentontwikkelaars hoeven zich geen zorgen te maken over het definiëren van aangepaste mediaquery&#39;s, aangezien de component Image al is geoptimaliseerd om uw inhoud te laden.

Bovendien ondersteunt de component Afbeelding lui laden om het laden van het eigenlijke afbeeldingselement uit te stellen totdat het element zichtbaar is in de browser, waardoor de reacties op uw pagina&#39;s sneller worden.

>[!TIP]
>
>De component Image wordt aangedreven door de Adaptive Image Servlet. Gelieve te zien het document [ Adaptieve Servlet van het Beeld ](/help/developing/adaptive-image-servlet.md) voor details op hoe het werkt.

## Ondersteuning voor dynamische media {#dynamic-media}

De Component van het Beeld (van [ versie 2.13.0 ](/help/versions.md)) steunt [ Dynamische Media ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=en#dynamicmedia) activa. [ wanneer toegelaten, ](#design-dialog) bieden deze eigenschappen de capaciteit aan om Dynamische het beeldactiva van Media met eenvoudige belemmering-en-daling of via activa toe te voegen browser enkel zoals u een ander beeld. Daarnaast worden ook afbeeldingsaanpassingen, voorinstellingen voor afbeeldingen en slimme gewassen ondersteund.

Uw webbeleving die is gebouwd met Core Components kan geen geavanceerde, op Sensei gebaseerde, robuuste, krachtige, platformonafhankelijke mogelijkheden voor Dynamic Media Image bieden.

## SVG-ondersteuning {#svg-support}

Scalable Vector Graphics (SVG) wordt ondersteund door de Afbeeldingscomponent.

* Het slepen en neerzetten van een SVG-element van DAM en het uploaden van een SVG-bestandsupload vanuit een lokaal bestandssysteem worden beide ondersteund.
* Het oorspronkelijke SVG-bestand wordt gestreamd (transformaties worden overgeslagen).
* Voor een SVG-afbeelding worden de &quot;smart images&quot; en de &quot;smart sizes&quot; ingesteld op een lege array in het afbeeldingsmodel.

### Beveiliging {#security}

Vanwege beveiligingsredenen wordt de originele SVG nooit rechtstreeks aangeroepen door de Afbeeldingseditor. Deze wordt aangeroepen via `<img src=“path-to-component”>` . Hierdoor wordt voorkomen dat de browser scripts uitvoert die in het SVG-bestand zijn ingesloten.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van het Beeld te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_image).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van het Beeld [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_image_v2) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

De Component van het Beeld steunt [ schema.org microdata ](https://schema.org).

## Dialoogvenster configureren {#configure-dialog}

Naast standaard [ geef dialoog ](#edit-dialog) uit en [ ontwerpdialoog ](#design-dialog), biedt de beeldcomponent een dialoog aan waar het beeld zelf samen met zijn beschrijving en basiseigenschappen wordt bepaald.

### Tabblad Element {#asset-tab}

![ het lusje van Activa van de Component van het Beeld vormt dialoog ](/help/assets/image-configure-asset.png)

* **activa van het Beeld**
   * Daling een activa van [ activa browser ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of ontvang **doorbladert** optie om van een lokaal dossiersysteem te uploaden.
   * Tik of klik **Duidelijk** om het momenteel geselecteerde beeld te deselecteren.
   * Tik of klik **uitgeven** [ om de vertoningen van de activa ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in de activaredacteur te beheren.

### Tabblad Metagegevens {#metadata-tab}

![ Meta-gegevens lusje van de Component van het Beeld vormt dialoog ](/help/assets/image-configure-metadata.png)

* **vooraf ingesteld Type** - dit bepaalt de types van beeld vooraf instelt beschikbaar, of **Vooraf ingesteld Beeld** of **Slim Gewas**, en is slechts beschikbaar wanneer [ de Dynamische eigenschappen van Media ](#dynamic-meida) worden toegelaten.
   * **Vooraf ingesteld Beeld** - wanneer **Vooraf ingesteld Type** van **Vooraf ingesteld Beeld** wordt geselecteerd, is het drop-down **Vooraf ingestelde Beeld** beschikbaar, toestaand selectie van de beschikbare Dynamische Voorinstellingen van Media. Dit is alleen beschikbaar als er voorinstellingen zijn gedefinieerd voor het geselecteerde element.
   * **Slim Gewas** - wanneer **Vooraf ingesteld Type** van **Slim Uitsnijden** wordt geselecteerd de daling onderaan **Vertoning** beschikbaar is, toestaand selectie van de beschikbare vertoningen van de geselecteerde activa. Dit is alleen beschikbaar als uitvoeringen zijn gedefinieerd voor het geselecteerde element.
   * **de Modifiers van het Beeld** - het Extra Dynamische beeld dat van Media bevelen dienen kan hier worden bepaald door `&`, ongeacht welk **Vooraf ingesteld Type** wordt geselecteerd.
* **Beeld is decoratief** - controleer als het beeld door ondersteunende technologie zou moeten worden genegeerd en daarom geen alternatieve tekst vereist. Dit geldt alleen voor decoratieve afbeeldingen.
* **Alternatieve tekst** - Textueel alternatief van de betekenis of de functie van het beeld, voor visueel gehandicapte lezers.
   * **krijgt alternatieve tekst van DAM** - wanneer gecontroleerd de alternatieve tekst van het beeld zal met de waarde van de `dc:description` meta-gegevens in DAM worden bevolkt.
* **Titel** - de Extra informatie over het beeld, die onder het beeld door gebrek wordt getoond.
   * **krijgt titel van DAM** - wanneer gecontroleerd de de bijschrifttekst van het beeld zal met de waarde van de `dc:title` meta-gegevens in DAM worden bevolkt.
   * **titel van de Vertoning als pop-up** - wanneer gecontroleerd, zal de titel niet onder het beeld worden getoond, maar als pop-up die door sommige browsers wordt getoond wanneer het bedekken over het beeld.
* **Verbinding** - verbind het beeld met een ander middel.
   * In het dialoogvenster Selecteren kunt u een koppeling maken naar een andere AEM-bron.
   * Als u geen koppeling naar een AEM-resource wilt maken, voert u de absolute URL in. Niet-absolute URL&#39;s worden geïnterpreteerd als relatief ten opzichte van AEM.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

>[!TIP]
>
>**het Slimme Gewas** en **Vooraf ingesteld Beeld** zijn wederzijds exclusieve opties. Als een auteur een beeld moet gebruiken vooraf ingesteld samen met een Slimme vertoning van het Gewas, zal de auteur de **Modifiers van het Beeld** moeten gebruiken om manueel vooraf instelt toe te voegen.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud uitsnijden, de startkaart wijzigen en inzoomen op de afbeelding.

>[!NOTE]
>
>Uitsnijden, roteren en zoomen zijn niet van toepassing op dynamische media-elementen. Als de [ Dynamische eigenschappen van Media ](#dynamic-media) worden toegelaten, zou om het even welk zulk het uitgeven aan Dynamische activa van Media door [ moeten worden uitgevoerd vormen Dialoog.](#configure-dialog)

![ de Edit dialoog van de Component van het Beeld {](/help/assets/image-edit.png)

* Uitsnijden starten

  ![ Uitsnijdpictogram van het Begin ](/help/assets/image-start-crop.png)

  Als u deze optie selecteert, wordt een vervolgkeuzelijst geopend voor vooraf gedefinieerde verhoudingen voor uitsnijden.

   * Kies de optie **Vrije hand** om uw eigen uitsnijding te bepalen.
   * Kies de optie **verwijdert Uitsnijden** om de originele activa te tonen.

  Als een uitsnijdoptie is geselecteerd, gebruikt u de blauwe handgrepen om het uitsnijden op de afbeelding te vergroten of te verkleinen.

  ![ de opties van het Gewas ](/help/assets/image-crop-options.png)

* Rechtsom roteren

  ![ roteer het juiste pictogram ](/help/assets/image-rotate-right.png)

  Gebruik deze optie als u de afbeelding 90° rechtsom wilt roteren.

* Horizontaal spiegelen

  ![ Horizontaal spiegelen pictogram ](/help/assets/image-flip-horizontal.png)

  Met deze optie kunt u de afbeelding horizontaal draaien of 180° langs de y-as draaien.

* Verticaal spiegelen

  ![ Verticaal spiegelen pictogram ](/help/assets/image-flip-vertical.png)

  Gebruik deze optie om de afbeelding 180° verticaal om te draaien of om de afbeelding 180° langs de x-as om te draaien.

* Zoomen herstellen

  ![ het gezoempictogram van het Terugstellen ](/help/assets/image-reset-zoom.png)

  Als al op de afbeelding is ingezoomd, gebruikt u deze optie om het zoomniveau opnieuw in te stellen.

* Zoomregelaar openen

  ![ Open pictogram van de gezoemschuif ](/help/assets/image-zoom.png)

  Met deze optie geeft u een schuifregelaar weer om het zoomniveau van de afbeelding te bepalen.

  ![ de schuifcontrole van het Gezoem ](/help/assets/image-zoom-slider.png)

U kunt de interne editor ook gebruiken om de afbeelding te wijzigen. Vanwege ruimtebeperkingen zijn alleen de basisopties online beschikbaar. Voor volledige bewerkingsopties gebruikt u de modus Volledig scherm.

![ Beeld op zijn plaats geeft opties uit ](/help/assets/image-in-place-edit.png)

>[!NOTE]
>
>Bewerkingen voor het bewerken van afbeeldingen (uitsnijden, spiegelen, roteren) worden niet ondersteund voor GIF-afbeeldingen. Dergelijke wijzigingen die in de bewerkingsmodus in GIF&#39;s zijn aangebracht, blijven niet behouden.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties voor uitsnijden, uploaden, roteren en uploaden definiëren die de auteur van de inhoud heeft wanneer deze component wordt gebruikt.

### Hoofdtabblad {#main-tab}

Op het **Belangrijkste** lusje kunt u een lijst van breedten in pixel voor het beeld bepalen en de component zal automatisch de meest aangewezen breedte laden die op browser grootte wordt gebaseerd. Dit is een belangrijk deel van [ ontvankelijke eigenschappen ](#responsive-features) van de Component van het Beeld.

Bovendien kunt u bepalen welke algemene componentenopties automatisch of onbruikbaar worden gemaakt wanneer de auteur de component aan een pagina toevoegt.

![ het belangrijkste lusje van de het ontwerpdialoog van de Component van het Beeld het ontwerp ](/help/assets/image-design-main-v2.png)

* **laat eigenschappen DM** toe - wanneer gecontroleerd, laat [ Dynamische eigenschappen van Media ](#dynamic-media) toe zijn beschikbaar.
* **laat Web Geoptimaliseerde Beelden** toe - wanneer gecontroleerd, zal de [ Web-geoptimaliseerde dienst van de beeldlevering ](/help/developing/web-optimized-image-delivery.md) beelden in het formaat leveren WebP, die beeldgrootte door gemiddeld 25% verminderen.
   * Deze optie is alleen beschikbaar in AEMaaCS.
   * Wanneer ongecontroleerd of de web-optimized dienst van de beeldlevering niet beschikbaar is [ wordt de Aangepaste Servlet van het Beeld ](/help/developing/adaptive-image-servlet.md) gebruikt.
* **laat luie lading** toe - bepaalt als de luie ladingsoptie automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **Beeld is decoratief** - bepaal als de decoratieve beeldoptie automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **krijgt alternatieve tekst van DAM** - bepaalt als de optie om de afwisselende tekst van DAM terug te winnen automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **krijgt titel van DAM** - bepaalt als de optie om de titel van DAM terug te winnen automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **de titel van de Vertoning als pop-up** - bepaalt als de optie om de beeldtitel als pop-up te tonen automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **onbruikbaar maken UUID het Volgen** - Controle om het volgen van UUID van het beeldelement onbruikbaar te maken.
* **Breedten** - bepaalt een lijst van breedten in pixel voor het beeld en de component laadt automatisch de meest aangewezen breedte die op browser grootte wordt gebaseerd.
   * Tik of klik **voeg** knoop toe om een andere grootte toe te voegen.
      * Gebruik de grepen om de volgorde van de formaten te wijzigen.
      * Gebruik het **pictogram van de Schrapping** om een breedte te verwijderen.
   * Het laden van afbeeldingen wordt standaard uitgesteld totdat ze zichtbaar worden.
      * Selecteer de optie **maak het laden** onbruikbaar om de beelden op paginading te laden.
* **Kwaliteit van JPEG** - de kwaliteitsfactor (in percentage van 0 en 100) voor getransformeerde (b.v. geschraapte of bebouwde) beelden van JPEG.

>[!TIP]
>
>Zie het document [ Aangepaste Servlet van het Beeld ](/help/developing/adaptive-image-servlet.md) voor uiteinden voor het optimaliseren van vertoningsselectie door uw breedten zorgvuldig te bepalen.

### Tabblad Functies {#features-tab}

Op het **lusje van Eigenschappen** kunt u bepalen welke opties aan de inhoudsauteurs beschikbaar zijn wanneer het gebruiken van de component met inbegrip van uploadt opties, richtlijn, en bebouwende opties.

* Source

  ![ het ontwerpdialoogEigenschappen van de Component van het Beeld lusje van de Eigenschappen ](/help/assets/image-design-features-source.png)

  Selecteer de optie **activa uploaden van het dossiersysteem** toestaan om inhoudsauteurs toe te staan om beelden van zijn of haar lokale computer te uploaden. Schakel deze optie uit als u wilt dat inhoudsauteurs alleen elementen uit AEM selecteren.

* Afdrukstand

  ![ het ontwerpdialoogEigenschappen van de Component van het Beeld lusje van de Eigenschappen ](/help/assets/image-design-features-orientation.png)

* **roteren**
Gebruik deze optie om de inhoudauteur toe te staan om **te gebruiken roteer Juist** optie.
* **Omdraaien**
Gebruik deze optie om de inhoudauteur toe te staan om **Horizontaal te gebruiken Omdraaien** en **Verticaal omdraaien** opties.

  >[!CAUTION]
  >
  >De **1} optie van de Omslag {wordt onbruikbaar gemaakt door gebrek.** Toelatend zal het **Verticaal Omdraaien** en **Horizontaal Omdraaien** knopen in uitgeven dialoog van de beeldcomponent tonen, nochtans wordt de eigenschap momenteel niet gesteund door AEM en om het even welke veranderingen die gebruikend deze opties worden aangebracht zullen niet worden voortgeduurd.

* Uitsnijden

  ![ het ontwerpdialoogEigenschappen van de Component van het Beeld lusje van de Eigenschappen ](/help/assets/image-design-features-cropping.png)

  Selecteer de optie **gewas** toestaan om de inhoudauteur toe te staan om het beeld in de component in uit te snijden uitgeeft dialoog.
   * Klik **toevoegen** om een vooraf bepaalde uitsnijdverhouding toe te voegen.
   * Ga een beschrijvende naam in, die in **1} dropdown van het Gewas van het Begin {zal worden getoond.**
   * Voer de numerieke verhouding van het aspect in.
   * Gebruik de sleephandgrepen om de volgorde van de hoogte-breedteverhoudingen te wijzigen
   * Gebruik het prullenbakpictogram om een hoogte-breedteverhouding te verwijderen.

  >[!CAUTION]
  >
  >Merk op dat in AEM, gewassenaspectverhoudingen als **hoogte/breedte** worden bepaald. Dit verschilt van de conventionele definitie van breedte/hoogte en wordt gedaan om oude compatibiliteitsredenen. De auteurs van de inhoud zullen zich niet van enig verschil bewust zijn zolang u een duidelijke naam van de verhouding verstrekt aangezien de naam in UI en niet de verhouding zelf wordt getoond.

### Tabblad Stijlen {#styles-tab-1}

De Component van het Beeld steunt het Systeem van de Stijl van AEM [ ](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De Component van het Beeld steunt de [ Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
