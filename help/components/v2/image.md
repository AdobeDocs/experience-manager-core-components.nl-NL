---
title: Afbeeldingscomponent (v2)
description: De Core Component Image is een adaptieve beeldcomponent die ter plekke kan worden bewerkt.
role: Architect, Developer, Admin, User
exl-id: 3f2b93f9-c48d-43ef-a78a-accd5090fe6f
source-git-commit: 5f25aee6ebcb7a5c6b8db0df5b8b853f15af97d0
workflow-type: tm+mt
source-wordcount: '2092'
ht-degree: 0%

---

# Afbeeldingscomponent (v2) {#image-component}

De component Core Component Image is een adaptieve afbeeldingscomponent die op locatie kan worden bewerkt.

## Gebruik {#usage}

De component Afbeelding biedt een adaptieve selectie van afbeeldingen en een responsief gedrag bij het lui laden voor de bezoeker van de pagina en bij het eenvoudig plaatsen en uitsnijden van de afbeelding voor de auteur van de inhoud.

De breedte van de afbeelding en de uitsnijdbreedte en aanvullende instellingen kunnen door de sjabloonauteur in het dialoogvenster [ontwerpdialoogvenster](#design-dialog). De inhoudeditor kan elementen uploaden of selecteren in het dialoogvenster [dialoogvenster configureren](#configure-dialog) en snijd de afbeelding uit in de [dialoogvenster bewerken](#edit-dialog). Voor meer gebruiksgemak is het ook mogelijk de afbeelding op een eenvoudige plaats aan te passen.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 2 van de Image Component beschreven, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 1 van de afbeeldingscomponent beschreven.
>
>Zie voor meer informatie over de huidige versie van de afbeeldingscomponent het gedeelte [Afbeeldingscomponent](/help/components/image.md) document.

## Responsieve functies {#responsive-features}

De component Image wordt geleverd met robuuste responsieve functies die direct uit de verpakking zijn te vinden. Op het niveau van het paginasjabloon [ontwerpdialoogvenster](#design-dialog) kan worden gebruikt om de standaardbreedten van het afbeeldingselement te definiëren. De component van het Beeld zal dan automatisch de correcte breedte aan vertoning afhankelijk van de grootte van het browser venster laden. Wanneer het formaat van het venster wordt gewijzigd, laadt de component Image dynamisch de juiste afbeeldingsgrootte. Componentontwikkelaars hoeven zich geen zorgen te maken over het definiëren van aangepaste mediaquery&#39;s, aangezien de component Image al is geoptimaliseerd om uw inhoud te laden.

Bovendien ondersteunt de component Afbeelding lui laden om het laden van het eigenlijke afbeeldingselement uit te stellen totdat het element zichtbaar is in de browser, waardoor de reacties op uw pagina&#39;s sneller worden.

## Dynamic Media-ondersteuning {#dynamic-media}

De afbeeldingscomponent (vanaf [release 2.13.0](/help/versions.md)) ondersteunt [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=en#dynamicmedia) activa. [Indien ingeschakeld,](#design-dialog) Met deze functies kunt u Dynamic Media-afbeeldingselementen toevoegen met een eenvoudige sleepfunctie of via de middelenbrowser, net als met andere afbeeldingen. Daarnaast worden ook afbeeldingsaanpassingen, voorinstellingen voor afbeeldingen en slimme gewassen ondersteund.

Uw webbeleving die is gebouwd met Core Components kan geen geavanceerde, op Sensei gebaseerde, robuuste, krachtige Dynamic Media Image-mogelijkheden voor meerdere platforms bieden.

## SVG-ondersteuning {#svg-support}

Schaalbare vectorafbeeldingen (SVG) worden ondersteund door de afbeeldingscomponent.

* De belemmering-en-daling van SVG activa van DAM en het uploaden van een SVG dossier van een lokaal dossiersysteem worden allebei gesteund.
* Het oorspronkelijke SVG-bestand wordt gestreamd (transformaties worden overgeslagen).
* Voor een SVG-afbeelding worden de &quot;slimme afbeeldingen&quot; en de &quot;slimme formaten&quot; ingesteld op een lege array in het afbeeldingsmodel.

### Beveiliging {#security}

Om veiligheidsredenen wordt de originele SVG nooit direct geroepen door de Redacteur van het Beeld. Het wordt doorgeroepen `<img src=“path-to-component”>`. Hierdoor wordt voorkomen dat de browser scripts uitvoert die in het SVG-bestand zijn ingesloten.

>[!CAUTION]
>
>Voor SVG-ondersteuning is release 2.1.0 van de Core Components of hoger vereist, samen met [servicepack 2](https://experienceleague.adobe.com/docs/experience-manager-64/release-notes/sp-release-notes.html) voor AEM 6.4 of hoger [functies voor afbeeldingseditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/image-editor.html) binnen AEM.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de afbeeldingscomponent wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_image).

### Technische details {#technical-details}

De meest recente technische documentatie over de Image Component [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_image_v2).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

De component Image ondersteunt [schema.org-microgegevens](https://schema.org).

## Dialoogvenster configureren {#configure-dialog}

Naast de norm [dialoogvenster bewerken](#edit-dialog) en [ontwerpdialoogvenster](#design-dialog), biedt de component image een configuratiedialoogvenster waarin de afbeelding zelf wordt gedefinieerd, samen met de beschrijving en basiseigenschappen.

### Tabblad Element {#asset-tab}

![Tabblad Element van het dialoogvenster Configureren van Image Component](/help/assets/image-configure-asset.png)

* **Afbeeldingselement**
   * Middelen uit het deelvenster [middelenbrowser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of tik op **doorbladeren** uploaden vanuit een lokaal bestandssysteem.
   * Tik of klik op **Wissen** om de selectie van de geselecteerde afbeelding op te heffen.
   * Tik of klik op **Bewerken** tot [de uitvoeringen van het actief beheren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in de middeleneditor.

### Tabblad Metagegevens {#metadata-tab}

![Tabblad Metagegevens van het dialoogvenster Configureren van Image Component](/help/assets/image-configure-metadata.png)

* **Type voorinstelling** - Hiermee worden de typen voorinstellingen voor afbeeldingen gedefinieerd die beschikbaar zijn. **Voorinstelling afbeelding** of **Slim uitsnijden** en is alleen beschikbaar wanneer [Dynamic Media-functies](#dynamic-meida) zijn ingeschakeld.
   * **Voorinstelling afbeelding** - Wanneer **Type voorinstelling** van **Voorinstelling afbeelding** is geselecteerd, de vervolgkeuzelijst **Voorinstelling afbeelding** is beschikbaar, zodat u kunt kiezen uit de beschikbare Dynamic Media-voorinstellingen. Dit is alleen beschikbaar als er voorinstellingen zijn gedefinieerd voor het geselecteerde element.
   * **Slim uitsnijden** - Wanneer **Type voorinstelling** van **Slim uitsnijden** is geselecteerd in de vervolgkeuzelijst **Vertoning** is beschikbaar, zodat u kunt kiezen uit de beschikbare uitvoeringen van het geselecteerde element. Dit is alleen beschikbaar als uitvoeringen zijn gedefinieerd voor het geselecteerde element.
   * **Afbeeldingsaanpassingen** - U kunt hier aanvullende opdrachten voor Dynamic Media-beeldserving definiëren door `&`, ongeacht welke **Type voorinstelling** is geselecteerd.
* **Afbeelding is decoratief** - Controleer of het beeld door ondersteunende hulpmiddelen moet worden genegeerd en of er daarom geen alternatieve tekst nodig is. Dit geldt alleen voor decoratieve afbeeldingen.
* **Alternatieve tekst** - Textueel alternatief van de betekenis of functie van de afbeelding voor slechtzienden.
   * **Alternatieve tekst ophalen van DAM** - Als u deze optie inschakelt, wordt de alternatieve tekst van de afbeelding gevuld met de waarde van de optie `dc:description` metagegevens in DAM.
* **Bijschrift** - Aanvullende informatie over de afbeelding, die standaard onder de afbeelding wordt weergegeven.
   * **Bijschrift ophalen van DAM** - Als deze optie is ingeschakeld, wordt de bijschrifttekst van de afbeelding gevuld met de waarde van de optie `dc:title` metagegevens in DAM.
   * **Bijschrift weergeven als pop-up** - Als deze optie is ingeschakeld, wordt het bijschrift niet weergegeven onder de afbeelding, maar als een pop-up die door sommige browsers wordt weergegeven wanneer de muisaanwijzer op de afbeelding wordt geplaatst.
* **Koppeling** - Koppel de afbeelding aan een andere bron.
   * In het dialoogvenster Selecteren kunt u een koppeling maken naar een andere AEM.
   * Als u geen koppeling naar een AEM maakt, voert u de absolute URL in. Niet-absolute URL&#39;s worden geïnterpreteerd als relatief ten opzichte van AEM.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

>[!TIP]
>
>**Slim uitsnijden** en **Voorinstelling afbeelding** zijn opties die elkaar uitsluiten. Als een auteur een voorinstelling voor een afbeelding moet gebruiken in combinatie met een uitvoering voor slim uitsnijden, moet de auteur de opdracht **Afbeeldingsaanpassingen** om handmatig voorinstellingen toe te voegen.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud uitsnijden, de startkaart wijzigen en inzoomen op de afbeelding.

>[!NOTE]
>
>Uitsnijden, roteren en zoomen zijn niet van toepassing op Dynamic Media-elementen. Als de [Dynamic Media-functies](#dynamic-media) zijn ingeschakeld, bewerkingen naar Dynamic Media-elementen moeten worden uitgevoerd via de [Dialoogvenster configureren.](#configure-dialog)

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
>Bewerkingen voor het bewerken van afbeeldingen (uitsnijden, spiegelen, roteren) worden niet ondersteund voor GIFFEN-afbeeldingen. Dergelijke wijzigingen die in de bewerkingsmodus zijn aangebracht op GIFFEN, blijven niet behouden.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties voor uitsnijden, uploaden, roteren en uploaden definiëren die de auteur van de inhoud heeft wanneer deze component wordt gebruikt.

### Hoofdtabblad {#main-tab}

Op de **Hoofd** kunt u een lijst met breedten definiëren in pixels voor de afbeelding. De component laadt automatisch de meest geschikte breedte op basis van de browsergrootte. Dit is een belangrijk onderdeel van het [responsieve functies](#responsive-features) van de afbeeldingscomponent.

Bovendien kunt u bepalen welke algemene componentenopties automatisch of gehandicapt zijn wanneer de auteur de component aan een pagina toevoegt.

![Het hoofdtabblad van het dialoogvenster Ontwerp van de afbeeldingscomponent](/help/assets/image-design-main-v2.png)

* **DM-functies inschakelen** - Als deze optie ingeschakeld is [Dynamic Media-functies](#dynamic-media) zijn beschikbaar.
* **Geoptimaliseerde webafbeeldingen inschakelen** - Als deze optie is ingeschakeld, wordt [webgeoptimaliseerde service voor het leveren van afbeeldingen](/help/developing/web-optimized-image-delivery.md) Hiermee worden afbeeldingen in de WebP-indeling geleverd. De afbeeldingen worden gemiddeld met 25% verkleind.
   * Deze optie is alleen beschikbaar in AEMaaCS.
   * Als deze optie niet is ingeschakeld of als de service voor het leveren van afbeeldingen voor het web niet beschikbaar is, [Adaptieve afbeeldingsserver](/help/developing/adaptive-image-servlet.md) wordt gebruikt.
* **Lazy laden inschakelen** - Definieer of de uitgestelde laadoptie automatisch wordt ingeschakeld wanneer de afbeeldingscomponent aan een pagina wordt toegevoegd.
* **Afbeelding is decoratief** - Definieer of de optie Decoratieve afbeelding automatisch wordt ingeschakeld wanneer u de afbeeldingscomponent aan een pagina toevoegt.
* **Alternatieve tekst ophalen van DAM**- Definieer of de optie voor het ophalen van de alternatieve tekst van de DAM automatisch is ingeschakeld wanneer u de afbeeldingscomponent aan een pagina toevoegt.
* **Bijschrift ophalen van DAM** - Bepaal als de optie om de titel van DAM terug te winnen automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **Bijschrift weergeven als pop-up** - Definieer of de optie voor het weergeven van het bijschrift als pop-up automatisch is ingeschakeld wanneer u de afbeeldingscomponent aan een pagina toevoegt.
* **UUID-tracking uitschakelen** - Schakel deze optie in om het bijhouden van de UUID van het afbeeldingselement uit te schakelen.
* **Breedten** - Definieert een lijst met breedten in pixels voor de afbeelding en de component laadt automatisch de meest geschikte breedte op basis van de browsergrootte.
   * Tik of klik op de knop **Toevoegen** om een andere grootte toe te voegen.
      * Gebruik de grepen om de volgorde van de formaten te wijzigen.
      * Gebruik de **Verwijderen** pictogram om een breedte te verwijderen.
   * Het laden van afbeeldingen wordt standaard uitgesteld totdat ze zichtbaar worden.
      * Selecteer de optie **Lazy load uitschakelen** om de afbeeldingen te laden wanneer de pagina wordt geladen.
* **JPEG-kwaliteit** - De kwaliteitsfactor (als percentage van 0 en 100) voor getransformeerde (bijv. geschaalde of bijgesneden) JPEG-afbeeldingen.

>[!TIP]
>
>Zie het document [Adaptieve afbeeldingsserver](#adaptive-image-servlet) voor tips voor het optimaliseren van de selectie van uitvoeringen door uw breedten zorgvuldig te definiëren.

### Tabblad Functies {#features-tab}

Op de **Functies** kunt u opgeven welke opties beschikbaar zijn voor de auteurs van de inhoud wanneer u de component gebruikt, inclusief opties voor uploaden, richting en uitsnijden.

* Bron

   ![Dialoogvenster Eigenschappen van het ontwerpdialoogvenster van de component Image](/help/assets/image-design-features-source.png)

   Selecteer de optie **Middelen uploaden vanuit bestandssysteem toestaan** om auteurs van inhoud toe te staan afbeeldingen te uploaden vanaf hun lokale computer. Schakel deze optie uit als u wilt dat inhoudsauteurs alleen elementen uit AEM selecteren.

* Afdrukstand

   ![Dialoogvenster Eigenschappen van het ontwerpdialoogvenster van de component Image](/help/assets/image-design-features-orientation.png)

* **Roteren**
Gebruik deze optie als u wilt dat de auteur van de inhoud de opdracht 
**Rechtsom roteren** optie.
* **Omdraaien**
Gebruik deze optie als u wilt dat de auteur van de inhoud de opdracht 
**Horizontaal spiegelen** en **Verticaal spiegelen** opties.

   >[!CAUTION]
   >
   >De **Omdraaien** is standaard uitgeschakeld. Als u deze optie inschakelt, wordt het dialoogvenster **Verticaal spiegelen** en **Horizontaal spiegelen** in het dialoogvenster Bewerken van de afbeeldingscomponent. De functie wordt momenteel echter niet ondersteund door AEM en wijzigingen die met deze opties zijn aangebracht, blijven niet behouden.

* Uitsnijden

   ![Dialoogvenster Eigenschappen van het ontwerpdialoogvenster van de component Image](/help/assets/image-design-features-cropping.png)

   Selecteer de optie **Uitsnijden toestaan** Hiermee kan de auteur van de inhoud de afbeelding uitsnijden in de component in het dialoogvenster Bewerken.
   * Klikken **Toevoegen** om een vooraf gedefinieerde hoogte-breedteverhouding voor uitsnijden toe te voegen.
   * Voer een beschrijvende naam in die wordt weergegeven in het dialoogvenster **Uitsnijden starten** vervolgkeuzelijst.
   * Voer de numerieke verhouding van het aspect in.
   * Gebruik de sleephandgrepen om de volgorde van de hoogte-breedteverhoudingen te wijzigen
   * Gebruik het prullenbakpictogram om een hoogte-breedteverhouding te verwijderen.

   >[!CAUTION]
   >
   >In AEM worden de hoogte-breedteverhoudingen voor uitsnijden gedefinieerd als **hoogte/breedte**. Dit verschilt van de conventionele definitie van breedte/hoogte en wordt gedaan om oude compatibiliteitsredenen. De auteurs van de inhoud zullen zich niet van enig verschil bewust zijn zolang u een duidelijke naam van de verhouding verstrekt aangezien de naam in UI en niet de verhouding zelf wordt getoond.

### Tabblad Stijlen {#styles-tab-1}

De component Image ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component Image ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
