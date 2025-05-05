---
title: Component E-mail
description: De component E-mailafbeelding is een adaptieve afbeeldingscomponent die op locatie kan worden bewerkt.
role: Architect, Developer, Admin, User
exl-id: f5d40047-3082-4edd-a5f6-6ab3e33997f9
source-git-commit: 91969e4956bef1a511b8d588d5290a7999bf86ec
workflow-type: tm+mt
source-wordcount: '1624'
ht-degree: 0%

---


# Component E-mail {#email-image-component}

De component E-mailafbeelding is een adaptieve afbeeldingscomponent die op locatie kan worden bewerkt.

## Gebruik {#usage}

De component E-mailafbeelding biedt een adaptieve selectie van afbeeldingen en een responsief gedrag bij het laden van de pagina voor de bezoeker van de pagina en bij het eenvoudig slepen en neerzetten van de afbeelding en de configuratie voor de auteur van de inhoud.

* De beeldbreedten en de extra montages kunnen door de malplaatjeauteur in de [ ontwerpdialoog worden bepaald.](#design-dialog)
* De inhoudsredacteur kan activa in [ uploaden of selecteren vormt dialoog.](#configure-dialog)

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de E-mailcomponent Image is v1, die in oktober 2022 is geïntroduceerd met release x van de Email Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel | - | - |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [ e-mailCore Componenten Versies ](/help/email/versions.md).

## Responsieve functies {#responsive-features}

De component E-mailafbeelding wordt geleverd met robuuste responsieve functies die direct uit de verpakking zijn te vinden. Op het niveau van het paginamalplaatje, kan de [ ontwerpdialoog ](#design-dialog) worden gebruikt om de standaardbreedten van het beeldactiva te bepalen. De component E-mail van het Beeld zal dan automatisch de correcte breedte aan vertoning afhankelijk van de grootte van het browser venster laden. Wanneer het formaat van het venster wordt gewijzigd, laadt de component E-mailafbeelding de juiste afbeeldingsgrootte dynamisch. Componentontwikkelaars hoeven zich geen zorgen te maken over het definiëren van aangepaste mediaquery&#39;s, omdat de component E-mailafbeelding al is geoptimaliseerd om uw inhoud te laden.

Daarnaast biedt de component E-mailafbeelding ondersteuning voor lui laden om het laden van het eigenlijke afbeeldingselement uit te stellen totdat dit zichtbaar is in de browser, waardoor de inhoud sneller reageert.

>[!TIP]
>
>Standaard wordt de component E-mailafbeelding aangedreven door de Adaptive Image Servlet. Gelieve te zien het document [ Adaptieve Servlet van het Beeld ](#adaptive-image-servlet) voor details op hoe het werkt.

## Ondersteuning voor dynamische media {#dynamic-media}

De component E-mail van het Beeld steunt [ Dynamische Media ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html#dynamicmedia) activa. [ wanneer toegelaten, ](#design-dialog) bieden deze eigenschappen de capaciteit aan om Dynamische het beeldactiva van Media met eenvoudige belemmering-en-daling of via activa toe te voegen browser enkel zoals u een ander beeld. Daarnaast worden ook afbeeldingsaanpassingen, voorinstellingen voor afbeeldingen en slimme gewassen ondersteund.

Uw e-mailervaring die is opgebouwd met de e-mailCore-componenten kan beschikken over uitgebreide, op Sensei gebaseerde, robuuste, krachtige, platformonafhankelijke mogelijkheden voor Dynamic Media Image.

## SVG-ondersteuning {#svg-support}

Scalable Vector Graphics (SVG) wordt ondersteund door de E-mailafbeeldingscomponent.

* Het slepen en neerzetten van een SVG-element van DAM en het uploaden van een SVG-bestandsupload vanuit een lokaal bestandssysteem worden beide ondersteund.
* Het oorspronkelijke SVG-bestand wordt gestreamd (transformaties worden overgeslagen).
* Voor een SVG-afbeelding worden de &quot;smart images&quot; en de &quot;smart sizes&quot; ingesteld op een lege array in het afbeeldingsmodel.

### Beveiliging {#security}

Vanwege beveiligingsredenen wordt de originele SVG nooit rechtstreeks aangeroepen door de Afbeeldingseditor. Deze wordt aangeroepen via `<img src=“path-to-component”>` . Hierdoor wordt voorkomen dat de browser scripts uitvoert die in het SVG-bestand zijn ingesloten.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van het Beeld E-mail [ kan op GitHub worden gevonden.](https://adobe.com/go/aem_cmp_tech_email_image_v1)

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden.](/help/developing/overview.md)

De Component van het Beeld steunt [ schema.org microdata.](https://schema.org)

## Dialoogvenster configureren {#configure-dialog}

De component E-mailafbeelding biedt een configuratievenster waarin de afbeelding zelf is gedefinieerd met een beschrijving en basiseigenschappen.

### Tabblad Element {#asset-tab}

![ het lusje van Activa van de Component van het E-mailBeeld vormt dialoog ](/help/email/assets/email-image-configure-asset.png)

* **erven geërfte beeld van pagina** - deze optie gebruikt het [ geprezen beeld van de verbonden pagina ](page.md) of het gekenmerkte beeld van de huidige pagina als het beeld niet verbonden is.

* **Alternatieve tekst voor toegankelijkheid** - Dit gebied staat u toe om een beschrijving van het beeld voor visueel gehandicapte gebruikers te bepalen.

   * **erven alternatieve tekst van pagina** - Deze optie gebruikt de alternatieve beschrijving van de verbonden activawaarde van de `dc:description` meta-gegevens in DAM of van de huidige pagina als geen activa wordt verbonden.

* **activa van het Beeld**
   * Daling een activa van [ activa browser ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of ontvang **doorbladert** optie om van een lokaal dossiersysteem te uploaden.
   * Tik of klik **Duidelijk** om het momenteel geselecteerde beeld te deselecteren.
   * Tik of klik **uitgeven** [ om de vertoningen van de activa ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in de Redacteur van Activa te beheren.

* **verstrekt geen alternatieve tekst** - Deze optie merkt het beeld dat door ondersteunende technologieën zoals het schermlezers voor gevallen wordt genegeerd waar het beeld zuiver decoratief is of anders geen extra informatie aan de pagina overbrengt.

* **maak luie lading** onbruikbaar - deze optie laadt alle beeldcomponenten zonder het laden zoals nodig vooraf.

### Tabblad Metagegevens {#metadata-tab}

![ Meta-gegevens lusje van de Component van het Beeld vormt dialoog ](/help/email/assets/email-image-configure-metadata.png)

* **vooraf ingesteld Type** - dit bepaalt de types van beeld vooraf instelt beschikbaar, of **Vooraf ingesteld Beeld** of **Slim Gewas**, en is slechts beschikbaar wanneer [ de Dynamische eigenschappen van Media ](#dynamic-meida) worden toegelaten.
   * **Vooraf ingesteld Beeld** - wanneer **Vooraf ingesteld Type** van **Vooraf ingesteld Beeld** wordt geselecteerd, is het drop-down **Beeld Vooraf ingesteld** beschikbaar, toestaand selectie van de beschikbare Dynamische Voorinstellingen van Media. Dit is alleen beschikbaar als er voorinstellingen zijn gedefinieerd voor het geselecteerde element.
   * **Slim Gewas** - wanneer **Vooraf ingesteld Type** van **Slim Gewas** wordt geselecteerd de drop-down **Vertoning** beschikbaar is, toestaand selectie van de beschikbare vertoningen van de geselecteerde activa. Dit is alleen beschikbaar als uitvoeringen zijn gedefinieerd voor het geselecteerde element.
   * **de Modifiers van het Beeld** - de Extra Dynamische beeld-dienende bevelen van Media kunnen hier worden bepaald door `&`, ongeacht welk **Vooraf ingesteld Type** wordt geselecteerd.
* **Titel** - de Extra informatie over het beeld, die onder het beeld door gebrek wordt getoond.
   * **krijgt titel van DAM** - wanneer gecontroleerd de de bijschrifttekst van het beeld zal met de waarde van de `dc:title` meta-gegevens in DAM worden bevolkt. Alleen beschikbaar wanneer een element wordt gekozen uit de DAM.
   * **titel van de Vertoning als pop-up** - wanneer gecontroleerd, zal de titel niet onder het beeld worden getoond, maar als pop-up die door sommige browsers wordt getoond wanneer het bedekken over het beeld.
* **Verbinding** - verbind het beeld met een ander middel.
   * In het dialoogvenster Selecteren kunt u een koppeling maken naar een andere AEM-bron.
   * Als u geen koppeling naar een AEM-resource wilt maken, voert u de absolute URL in. Niet-absolute URL&#39;s worden geïnterpreteerd als relatief ten opzichte van AEM.
   * **Open verbinding in nieuw lusje** - deze optie opent de verbinding in een nieuw browser venster.
* **identiteitskaart** - Deze optie staat het controleren van het unieke herkenningsteken van de component in HTML toe.
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor CSS.
* **Vast met** - deze optie bepaalt de breedte in pixel van het beeld.
* **beeld van de Schaal aan beschikbare breedte** - deze optie past `"width":"100%"` op de attributen van de beeldstijl toe.

>[!TIP]
>
>**het Slimme Gewas** en **Vooraf ingesteld Beeld** zijn wederzijds exclusieve opties. Als een auteur een beeld moet gebruiken vooraf ingesteld samen met een Slimme vertoning van het Gewas, zal de auteur de **Modifiers van het Beeld** moeten gebruiken om manueel vooraf instelt toe te voegen.

### Tabblad Stijlen {#styles-tab-edit}

![ het lusje van Stijlen van uitgeeft dialoog van de Component van het Beeld E-mail ](/help/assets/image-configure-styles.png)

De component E-mail van het Beeld steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling)

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [ ontwerpdialoog ](#design-dialog) worden gevormd opdat het lusje beschikbaar is.

## Ontwerpdialoogvenster {#design-dialog}

### Hoofdtabblad {#main-tab}

![ het belangrijkste lusje van de het ontwerpdialoog van de Component van het Beeld het ontwerp ](/help/email/assets/email-image-design-main.png)

* **laat eigenschappen DM** toe - wanneer gecontroleerd, [ de Dynamische eigenschappen van Media ](#dynamic-media) zijn beschikbaar.
   * Deze optie wordt alleen weergegeven wanneer Dynamische media is ingeschakeld in de omgeving.
* **laat Web Geoptimaliseerde Beelden** toe - wanneer gecontroleerd, [ de Web-geoptimaliseerde dienst van de beeldlevering ](/help/developing/web-optimized-image-delivery.md) zal beelden in het formaat leveren WebP, die beeldgrootte door gemiddeld 25% verminderen.
   * Deze optie is alleen beschikbaar in AEMaaCS.
   * Wanneer ongecontroleerd of wanneer de Web-geoptimaliseerde dienst van de beeldlevering niet beschikbaar is [ Aangepast Servlet van het Beeld ](/help/developing/adaptive-image-servlet.md) wordt gebruikt.
* **Beeld is decoratief** - bepaal als de decoratieve beeldoptie automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **krijgt alternatieve tekst van DAM** - bepaalt als de optie om de afwisselende tekst van DAM terug te winnen automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **krijgt titel van DAM** - bepaalt als de optie om de titel van DAM terug te winnen automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **de titel van de Vertoning als pop-up** - bepaalt als de optie om de beeldtitel als pop-up te tonen automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **resizing breedte** - deze waarde wordt gebruikt voor het resizing van de breedte van de basisbeelden die activa DAM zijn.
   * De hoogte-breedteverhouding van de afbeeldingen blijft behouden.
   * Als de waarde groter is dan de werkelijke breedte van de afbeelding, heeft deze waarde geen effect.
   * Deze waarde heeft geen effect op SVG-afbeeldingen.

U kunt een lijst van breedten in pixel voor het beeld bepalen en de component zal automatisch de meest aangewezen breedte laden die op browser grootte wordt gebaseerd. Dit is een belangrijk deel van de [ ontvankelijke eigenschappen ](#responsive-features) van de Component van het Beeld E-mail.

* **Breedten** - bepaalt een lijst van breedten in pixel voor het beeld en de component laadt automatisch de meest aangewezen breedte die op browser grootte wordt gebaseerd.
   * Tik of klik **voeg** knoop toe om een andere grootte toe te voegen.
      * Gebruik de grepen om de volgorde van de formaten te wijzigen.
      * Gebruik het **pictogram van de Schrapping** om een breedte te verwijderen.
   * Het laden van afbeeldingen wordt standaard uitgesteld totdat ze zichtbaar worden.
      * Selecteer de optie **maak het laden** onbruikbaar om de beelden op paginading te laden.
* **Kwaliteit van JPEG** - de kwaliteitsfactor (in percentage van 0 en 100) voor getransformeerde (b.v. geschraapte of bebouwde) beelden van JPEG.
* **Standaardbreedte** - de standaardbreedte van beelden in pixel die in de ontwerpdialoog zullen worden gebruikt

>[!TIP]
>
>Zie het document [ Aangepaste Servlet van het Beeld ](/help/developing/adaptive-image-servlet.md) voor uiteinden voor het optimaliseren van vertoningsselectie door uw breedten zorgvuldig te bepalen.

### Tabblad Stijlen {#styles-tab}

De component E-mail van het Beeld steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).
