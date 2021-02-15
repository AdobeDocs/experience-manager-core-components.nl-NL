---
title: Afbeeldingscomponent
description: De Core Component Image is een adaptieve beeldcomponent die ter plekke kan worden bewerkt.
translation-type: tm+mt
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: tm+mt
source-wordcount: '2170'
ht-degree: 0%

---


# Afbeeldingscomponent{#image-component}

De component Core Component Image is een adaptieve afbeeldingscomponent die op locatie kan worden bewerkt.

## Gebruik {#usage}

De component Afbeelding biedt een adaptieve selectie van afbeeldingen en een responsief gedrag bij het lui laden voor de bezoeker van de pagina en bij het eenvoudig plaatsen en uitsnijden van de afbeelding voor de auteur van de inhoud.

De breedte van de afbeelding en de uitsnijdbreedte en aanvullende instellingen kunnen door de sjabloonauteur worden gedefinieerd in het dialoogvenster [ontwerp](#design-dialog). De inhoudeditor kan elementen uploaden of selecteren in het [dialoogvenster configureren](#configure-dialog) en de afbeelding uitsnijden in het [dialoogvenster Bewerken](#edit-dialog). Voor meer gebruiksgemak is het ook mogelijk de afbeelding op een eenvoudige plaats aan te passen.

## Responsieve functies {#responsive-features}

De component Image wordt geleverd met robuuste responsieve functies die direct uit de verpakking kunnen worden geleverd. Op het niveau van het paginasjabloon kunt u het [ontwerpdialoogvenster](#design-dialog) gebruiken om de standaardbreedten van het afbeeldingselement te definiëren. De component van het Beeld zal dan automatisch de correcte breedte aan vertoning afhankelijk van de grootte van het browser venster laden. Wanneer het formaat van het venster wordt gewijzigd, laadt de component Image dynamisch de juiste afbeeldingsgrootte. Componentontwikkelaars hoeven zich geen zorgen te maken over het definiëren van aangepaste mediaquery&#39;s, aangezien de component Image al is geoptimaliseerd om uw inhoud te laden.

Bovendien ondersteunt de component Afbeelding lui laden om het laden van het eigenlijke afbeeldingselement uit te stellen totdat het element zichtbaar is in de browser, waardoor de reacties op uw pagina&#39;s sneller worden.

## Dynamic Media-ondersteuning {#dynamic-media}

De component Image (vanaf [versie 2.13.0](/help/versions.md)) ondersteunt [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=en#dynamicmedia)-elementen. [Als deze functies zijn ingeschakeld, kunt ](#design-dialog) u Dynamic Media-afbeeldingselementen toevoegen met een eenvoudige sleepfunctie of via de middelenbrowser, net als elke andere afbeelding. Daarnaast worden ook afbeeldingsaanpassingen, voorinstellingen voor afbeeldingen en slimme gewassen ondersteund.

Uw webervaringen die zijn gemaakt met Core Components kunnen geen geavanceerde, op Sensei gebaseerde, robuuste, krachtige Dynamic Media Image-mogelijkheden voor meerdere platforms bieden.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Image Component is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatibel | Compatibel | Compatibel |
| [v1](v1/image-v1.md) | Compatibel | Compatibel | - |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## SVG-ondersteuning {#svg-support}

SVG (Scalable Vector Graphics) wordt ondersteund door de component Image.

* Het slepen en neerzetten van een SVG-element van DAM en het uploaden van een SVG-bestandsupload vanuit een lokaal bestandssysteem worden beide ondersteund.
* De Adaptive Image Server streamt het oorspronkelijke SVG-bestand (transformaties worden overgeslagen).
* Voor een SVG-afbeelding worden de &quot;slimme afbeeldingen&quot; en de &quot;slimme formaten&quot; ingesteld op een lege array in het afbeeldingsmodel.

### Beveiliging {#security}

Vanwege beveiligingsredenen wordt de oorspronkelijke SVG nooit rechtstreeks aangeroepen door de Afbeeldingseditor. Het wordt geroepen door `<img src=“path-to-component”>`. Hierdoor wordt voorkomen dat de browser scripts uitvoert die in het SVG-bestand zijn ingesloten.

>[!CAUTION]
>
>Voor SVG-ondersteuning is versie 2.1.0 van de Core Components of hoger vereist, samen met [servicepack 2](https://docs.adobe.com/content/help/en/experience-manager-64/release-notes/sp-release-notes.html) voor AEM 6.4 of hoger, ter ondersteuning van de [functies voor afbeeldingseditors](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/image-editor.html) in AEM.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_image) om de Image Component te bekijken en voorbeelden van de configuratieopties en de HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van het Beeld [kan op GitHub](https://adobe.com/go/aem_cmp_tech_image_v2) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

De component van het Beeld steunt [schema.org microdata](https://schema.org).

## Dialoogvenster {#configure-dialog} configureren

Naast de standaard [bewerkingsdialoog](#edit-dialog) en [ontwerpdialoog](#design-dialog), biedt de component van het beeld een configuratievenster waarin het beeld zelf met zijn beschrijving en basiseigenschappen wordt bepaald.

### Tabblad Elementen {#asset-tab}

![Tabblad Element van het dialoogvenster Configureren van Image Component](/help/assets/image-configure-asset.png)

* **Afbeeldingselement**
   * Zet een element neer vanuit de [assetbrowser](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of tik op de optie **browse** om te uploaden vanaf een lokaal bestandssysteem.
   * Tik of klik op **Wissen** om de selectie van de geselecteerde afbeelding ongedaan te maken.
   * Tik of klik op **Bewerken** om de uitvoeringen van het element te beheren](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in de elementeneditor.[

### Tabblad Metagegevens {#metadata-tab}

![Tabblad Metagegevens van het dialoogvenster Configureren van Image Component](/help/assets/image-configure-metadata.png)

* **Type**  voorinstelling - Hiermee definieert u de typen voorinstellingen voor afbeeldingen die beschikbaar zijn,  **Voorinstelling** afbeelding of  **Slim uitsnijden**. Deze voorinstelling is alleen beschikbaar wanneer  [Dynamic Media-](#dynamic-meida) functies zijn ingeschakeld.
   * **Voorinstelling**  afbeelding - Wanneer  **Voorinstelling** voor type  **voorinstelling** afbeelding is geselecteerd, kunt u de keuzelijst met  **voorinstellingen** voor afbeelding openen, zodat u kunt kiezen uit de beschikbare Dynamic Media-voorinstellingen. Dit is alleen beschikbaar als er voorinstellingen zijn gedefinieerd voor het geselecteerde element.
   * **Slim uitsnijden**  - Als  **Voorinstelling** voor  **slim** uitsnijden is geselecteerd, is de vervolgkeuzelijst  **** Vertoning beschikbaar, zodat u kunt kiezen uit de beschikbare uitvoeringen van het geselecteerde element. Dit is alleen beschikbaar als uitvoeringen zijn gedefinieerd voor het geselecteerde element.
   * **Image Modifiers** : extra opdrachten voor Dynamic Media-beeldserving kunnen hier worden gedefinieerd door  `&`, ongeacht welk  **type** voorinstelling is geselecteerd.
* **Afbeelding is decoratief** . Controleer of de afbeelding door hulpprogramma&#39;s moet worden genegeerd en of er daarom geen alternatieve tekst nodig is. Dit geldt alleen voor decoratieve afbeeldingen.
* **Alternatieve tekst** : een tekstalternatief met de betekenis of functie van de afbeelding voor slechtzienden.
   * **Alternatieve tekst ophalen van DAM**  - Bij controle wordt de alternatieve tekst van de afbeelding gevuld met de waarde van de  `dc:description` metagegevens in DAM.
* **Bijschrift**  - Aanvullende informatie over de afbeelding die standaard onder de afbeelding wordt weergegeven.
   * **Bijschrift ophalen van DAM**  - Bij controle wordt de waarde van de  `dc:title` metagegevens in DAM ingevuld bij de bijschrifttekst van de afbeelding.
   * **Bijschrift weergeven als pop-up**  - Als dit selectievakje is ingeschakeld, wordt het bijschrift niet weergegeven onder de afbeelding, maar als een pop-up die wordt weergegeven door sommige browsers wanneer de muisaanwijzer op de afbeelding wordt geplaatst.
* **Koppeling**  - Koppel de afbeelding aan een andere bron.
   * In het dialoogvenster Selecteren kunt u een koppeling maken naar een andere AEM.
   * Als u geen koppeling naar een AEM maakt, voert u de absolute URL in. Niet-absolute URL&#39;s worden geïnterpreteerd als relatief ten opzichte van AEM.
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

>[!TIP]
>
>**De optie Slim** uitsnijden en  **Voorinstelling** afbeelding sluiten elkaar uit. Als een auteur een vooraf ingestelde afbeelding samen met een uitvoering voor Slim uitsnijden moet gebruiken, moet de auteur de **Voorinstellingen voor afbeeldingen** handmatig toevoegen.

## Dialoogvenster {#edit-dialog} bewerken

In het dialoogvenster Bewerken kan de auteur van de inhoud uitsnijden, de startkaart wijzigen en inzoomen op de afbeelding.

>[!NOTE]
>
>Uitsnijden, roteren en zoomen zijn niet van toepassing op Dynamic Media-elementen. Als de [Dynamic Media-functies](#dynamic-media) zijn ingeschakeld, moet het bewerken van Dynamic Media-elementen worden uitgevoerd via het [Dialoogvenster configureren.](#configure-dialog)

![Bewerkingsdialoogvenster van afbeeldingscomponent](/help/assets/image-edit.png)

* Uitsnijden starten

   ![Uitsnijdpictogram starten](/help/assets/image-start-crop.png)

   Als u deze optie selecteert, wordt een vervolgkeuzelijst geopend voor vooraf gedefinieerde verhoudingen voor uitsnijden.

   * Kies de optie **Free Hand** om uw eigen uitsnijding te definiëren.
   * Kies de optie **Uitsnijden verwijderen** om het oorspronkelijke element weer te geven.

   Als een uitsnijdoptie is geselecteerd, gebruikt u de blauwe handgrepen om het uitsnijden op de afbeelding te vergroten of te verkleinen.

   ![Opties voor uitsnijden](/help/assets/image-crop-options.png)

* Rechtsom roteren

   ![Pictogram rechtsom roteren](/help/assets/image-rotate-right.png)

   Gebruik deze optie als u de afbeelding 90° rechtsom wilt roteren.

* Horizontaal spiegelen

   ![Pictogram Horizontaal spiegelen](/help/assets/image-flip-horizontal.png)

   Met deze optie kunt u de afbeelding horizontaal draaien of 180° langs de y-as draaien.

* Verticaal spiegelen

   ![Pictogram verticaal spiegelen](/help/assets/image-flip-vertical.png)

   Gebruik deze optie om de afbeelding 180° verticaal om te draaien of om de afbeelding 180° langs de x-as om te draaien.

* Zoomen herstellen

   ![Zoompictogram opnieuw instellen](/help/assets/image-reset-zoom.png)

   Als al op de afbeelding is ingezoomd, gebruikt u deze optie om het zoomniveau opnieuw in te stellen.

* Zoomregelaar openen

   ![Pictogram van zoomregelaar openen](/help/assets/image-zoom.png)

   Met deze optie geeft u een schuifregelaar weer om het zoomniveau van de afbeelding te bepalen.

   ![Besturing van zoomregelaar](/help/assets/image-zoom-slider.png)

U kunt de interne editor ook gebruiken om de afbeelding te wijzigen. Vanwege ruimtebeperkingen zijn alleen de basisopties online beschikbaar. Voor volledige bewerkingsopties gebruikt u de modus Volledig scherm.

![Opties voor Op plaats bewerken van afbeeldingen](/help/assets/image-in-place-edit.png)

>[!NOTE]
>
>Bewerkingen voor het bewerken van afbeeldingen (uitsnijden, spiegelen, roteren) worden niet ondersteund voor GIF-afbeeldingen. Dergelijke wijzigingen die in de bewerkingsmodus in GIF&#39;s zijn aangebracht, blijven niet behouden.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties voor uitsnijden, uploaden, roteren en uploaden definiëren die de auteur van de inhoud heeft wanneer deze component wordt gebruikt.

### Hoofdtabblad {#main-tab}

Op het **Main** lusje kunt u een lijst van breedten in pixel voor het beeld bepalen en de component zal automatisch de meest aangewezen breedte laden die op browser grootte wordt gebaseerd. Dit is een belangrijk onderdeel van de [responsieve functies](#responsive-features) van de component Image.

Bovendien kunt u bepalen welke algemene componentenopties automatisch of gehandicapt zijn wanneer de auteur de component aan een pagina toevoegt.

![Het hoofdtabblad van het dialoogvenster Ontwerp van de afbeeldingscomponent](/help/assets/image-design-main.png)

* **Functies**  voor DM inschakelen - Als deze optie is ingeschakeld, zijn de functies voor  [Dynamic Media inschakelen ](#dynamic-media) beschikbaar.
* **Lazy laden**  inschakelen - Definieer of de luie laadoptie automatisch is ingeschakeld wanneer u de afbeeldingscomponent aan een pagina toevoegt.
* **Afbeelding is decoratief** . Definieer of de optie Decoratieve afbeelding automatisch is ingeschakeld wanneer u de afbeeldingscomponent aan een pagina toevoegt.
* **Alternatieve tekst ophalen van DAM** - Definiëren of de optie voor het ophalen van de alternatieve tekst van de DAM automatisch is ingeschakeld wanneer de afbeeldingscomponent aan een pagina wordt toegevoegd.
* **Bijschrift ophalen van DAM**  - Definieer of de optie om het bijschrift op te halen van de DAM automatisch is ingeschakeld wanneer u de afbeeldingscomponent aan een pagina toevoegt.
* **Bijschrift weergeven als pop-up**  - Definieer of de optie om het bijschrift van de afbeelding als pop-up weer te geven automatisch is ingeschakeld wanneer u de afbeeldingscomponent aan een pagina toevoegt.
* **UUID-tracking**  uitschakelen - Schakel deze optie in om het bijhouden van de UUID van het afbeeldingselement uit te schakelen.
* **Breedten**  - Definieert een lijst met breedten in pixels voor de afbeelding en de component laadt automatisch de meest geschikte breedte op basis van de browsergrootte.
   * Tik of klik op de knop **Toevoegen** om een andere grootte toe te voegen.
      * Gebruik de grepen om de volgorde van de formaten te wijzigen.
      * Gebruik het pictogram **Delete** om een breedte te verwijderen.
   * Het laden van afbeeldingen wordt standaard uitgesteld totdat ze zichtbaar worden.
      * Selecteer de optie **Uitgestelde laadbewerking** uitschakelen om de afbeeldingen te laden bij het laden van de pagina.
* **JPEG-kwaliteit** : de kwaliteitsfactor (als percentage van 0 en 100) voor getransformeerde JPEG-afbeeldingen (bijvoorbeeld geschaald of uitgesneden).

### Tabblad Functies {#features-tab}

Op het tabblad **Functies** kunt u bepalen welke opties beschikbaar zijn voor de auteurs van de inhoud wanneer u de component gebruikt, inclusief opties voor uploaden, richting en uitsnijden.

* Bron

   ![Dialoogvenster Eigenschappen van het ontwerpdialoogvenster van de component Image](/help/assets/image-design-features-source.png)

   Selecteer de optie **Het uploaden van elementen vanuit het bestandssysteem toestaan** om auteurs van inhoud toe te staan afbeeldingen te uploaden vanaf hun lokale computer. Schakel deze optie uit als u wilt dat inhoudsauteurs alleen elementen uit AEM selecteren.

* Afdrukstand

   ![Dialoogvenster Eigenschappen van het ontwerpdialoogvenster van de component Image](/help/assets/image-design-features-orientation.png)

* **RoterenGebruik deze optie**
als u wilt dat de auteur van de inhoud de opdracht 
**Roteer** de optie.
* ****
FlipUse this option to allow the content ontwerper to use the 
**Opties voor** Horizontaal spiegelen en  **Verticaal** spiegelen.

   >[!CAUTION]
   >
   >De optie **Flip** is standaard uitgeschakeld. Als u deze functie inschakelt, worden de knoppen **Verticaal spiegelen** en **Horizontaal spiegelen** weergegeven in het dialoogvenster Bewerken van de afbeeldingscomponent. De functie wordt momenteel echter niet ondersteund door AEM en wijzigingen die met deze opties zijn aangebracht, blijven niet behouden.

* Uitsnijden

   ![Dialoogvenster Eigenschappen van het ontwerpdialoogvenster van de component Image](/help/assets/image-design-features-cropping.png)

   Selecteer de optie **Uitsnijden toestaan** om de auteur van de inhoud toe te staan om de afbeelding uit te snijden in de component in het dialoogvenster Bewerken.
   * Klik **Toevoegen** om een vooraf gedefinieerde hoogte-breedteverhouding voor uitsnijden toe te voegen.
   * Voer een beschrijvende naam in, die wordt weergegeven in het vervolgkeuzemenu **Uitsnijden starten**.
   * Voer de numerieke verhouding van het aspect in.
   * Gebruik de sleephandgrepen om de volgorde van de hoogte-breedteverhoudingen te wijzigen
   * Gebruik het prullenbakpictogram om een hoogte-breedteverhouding te verwijderen.

   >[!CAUTION]
   >
   >In AEM worden de hoogte-breedteverhoudingen voor uitsnijden gedefinieerd als **hoogte/breedte**. Dit verschilt van de conventionele definitie van breedte/hoogte en wordt gedaan om oude compatibiliteitsredenen. De auteurs van de inhoud zullen zich niet van enig verschil bewust zijn zolang u een duidelijke naam van de verhouding verstrekt aangezien de naam in UI en niet de verhouding zelf wordt getoond.

### Tabblad Stijlen {#styles-tab-1}

De component van het Beeld steunt het AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Adaptieve afbeeldingsserver {#adaptive-image-servlet}

De component Image maakt gebruik van de Adaptive Image Servlet van de Core-component. [De Adaptive Image ](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) Servletis verantwoordelijk voor beeldverwerking en het stromen en kan door ontwikkelaars in hun  [aanpassingen van de Componenten](/help/developing/customizing.md) van de Kern worden gebruikt.

>[!NOTE]
>
>Voorwaardelijke aanvragen via de `Last-Modified`-header worden ondersteund door de Adaptive Image Servlet, maar het in cache plaatsen van de `Last-Modified`-header [moet worden ingeschakeld in de Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=en#caching-http-response-headers).
>
>[De de steekproefconfiguratie van de Verzender van de Projectarchetype](/help/developing/archetype/overview.md) van het AEM bevat reeds deze configuratie.

## Adobe-gegevenslaag client {#data-layer}

De component van het Beeld steunt de [Laag van de Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
