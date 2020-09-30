---
title: Afbeeldingscomponent
description: De Core Component Image is een adaptieve beeldcomponent die ter plekke kan worden bewerkt.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '1921'
ht-degree: 0%

---


# Afbeeldingscomponent{#image-component}

De component Core Component Image is een adaptieve afbeeldingscomponent die op locatie kan worden bewerkt.

## Gebruik {#usage}

De component Afbeelding biedt een adaptieve selectie van afbeeldingen en een responsief gedrag bij het lui laden voor de bezoeker van de pagina en bij het eenvoudig plaatsen en uitsnijden van de afbeelding voor de auteur van de inhoud.

De breedte van de afbeelding en de uitsnijdbreedte en aanvullende instellingen kunnen door de sjabloonauteur in het [ontwerpdialoogvenster](#design-dialog)worden gedefinieerd. De inhoudseditor kan elementen uploaden of selecteren in het dialoogvenster [](#configure-dialog) configureren en de afbeelding uitsnijden in het dialoogvenster [](#edit-dialog)Bewerken. Voor meer gebruiksgemak is het ook mogelijk de afbeelding op een eenvoudige plaats aan te passen.

## Responsieve functies {#responsive-features}

De component Image wordt geleverd met robuuste responsieve functies die direct uit de verpakking kunnen worden geleverd. Op het niveau van het paginasjabloon kunt u het [ontwerpdialoogvenster](#design-dialog) gebruiken om de standaardbreedten van het afbeeldingselement te definiëren. De component van het Beeld zal dan automatisch de correcte breedte aan vertoning afhankelijk van de grootte van het browser venster laden. Wanneer het formaat van het venster wordt gewijzigd, laadt de component Image dynamisch de juiste afbeeldingsgrootte. Componentontwikkelaars hoeven zich geen zorgen te maken over het definiëren van aangepaste mediaquery&#39;s, aangezien de component Image al is geoptimaliseerd om uw inhoud te laden.

Bovendien ondersteunt de component Afbeelding lui laden om het laden van het eigenlijke afbeeldingselement uit te stellen totdat het element zichtbaar is in de browser, waardoor de reacties op uw pagina&#39;s sneller worden.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Image Component is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatibel | Compatibel | Compatibel |
| [v1](v1/image-v1.md) | Compatibel | Compatibel | - |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## SVG-ondersteuning {#svg-support}

SVG (Scalable Vector Graphics) wordt ondersteund door de component Image.

* Het slepen en neerzetten van een SVG-element van DAM en het uploaden van een SVG-bestandsupload vanuit een lokaal bestandssysteem worden beide ondersteund.
* De Adaptive Image Server streamt het oorspronkelijke SVG-bestand (transformaties worden overgeslagen).
* Voor een SVG-afbeelding worden de &quot;slimme afbeeldingen&quot; en de &quot;slimme formaten&quot; ingesteld op een lege array in het afbeeldingsmodel.

### Beveiliging {#security}

Vanwege beveiligingsredenen wordt de oorspronkelijke SVG nooit rechtstreeks aangeroepen door de Afbeeldingseditor. Het wordt doorgeroepen `<img src=“path-to-component”>`. Hierdoor wordt voorkomen dat de browser scripts uitvoert die in het SVG-bestand zijn ingesloten.

>[!CAUTION]
>
>Voor SVG-ondersteuning is versie 2.1.0 van de Core Components of hoger vereist, samen met [servicepack 2](https://docs.adobe.com/content/help/en/experience-manager-64/release-notes/sp-release-notes.html) voor AEM 6.4 of hoger, ter ondersteuning van de functies [voor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/image-editor.html) afbeeldingseditors in AEM.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_image)voor meer informatie over de component Image en voorbeelden van de configuratieopties ervan en over HTML- en JSON-uitvoer.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van het Beeld [kan op GitHub](https://adobe.com/go/aem_cmp_tech_image_v2)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

>[!NOTE]
>
>Vanaf versie 2.1.0 van de Componenten van de Kern, steunt de Component van het Beeld [schema.org microdata](https://schema.org).

## Dialoogvenster configureren {#configure-dialog}

Naast het standaarddialoogvenster [](#edit-dialog) Bewerken en [Ontwerpdialoogvenster](#design-dialog)biedt de component Image een configuratiedialoogvenster waarin de afbeelding zelf wordt gedefinieerd, samen met de beschrijving en basiseigenschappen.

### Tabblad Element {#asset-tab}

![Tabblad Element van het dialoogvenster Configureren van Image Component](/help/assets/image-configure-asset.png)

* **Afbeeldingselement**
   * Zet een element neer vanuit de [middelenbrowser](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of tik op de **bladeroptie** om te uploaden vanaf een lokaal bestandssysteem.
   * Tik of klik op **Wissen** om de selectie van de geselecteerde afbeelding ongedaan te maken.
   * Tik of klik op **Bewerken** om de uitvoeringen van het element [in de middeleneditor te](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) beheren.

### Tabblad Metagegevens {#metadata-tab}

![Tabblad Metagegevens van het dialoogvenster Configureren van Image Component](/help/assets/image-configure-metadata.png)

* **Afbeelding is decoratief**. Controleer of de afbeelding door hulpprogramma&#39;s moet worden genegeerd en of er daarom geen alternatieve tekst nodig is. Dit geldt alleen voor decoratieve afbeeldingen.
* **Alternatieve tekst** Alternatief tekstalternatief voor de betekenis of functie van de afbeelding, voor slechtzienden.
   * Alternatieve tekst ophalen van DAM - Bij controle wordt de alternatieve tekst van de afbeelding gevuld met de waarde van de `dc:description` metagegevens in DAM.

* **Bijschrift** Aanvullende informatie over de afbeelding die standaard onder de afbeelding wordt weergegeven.
   * **Bijschrift ophalen van DAM** Als deze optie is ingeschakeld, wordt het bijschrift van de afbeelding gevuld met de waarde van de optie 
`dc:title` metagegevens in DAM.
   * **Bijschrift weergeven als pop-up** Als deze optie is ingeschakeld, wordt het bijschrift niet weergegeven onder de afbeelding, maar als pop-up die wordt weergegeven door sommige browsers wanneer de muisaanwijzer op de afbeelding wordt geplaatst.

* **Koppeling**
   * Koppel de afbeelding aan een andere bron.
   * In het dialoogvenster Selecteren kunt u een koppeling maken naar een andere AEM.
   * Als u geen koppeling naar een AEM maakt, voert u de absolute URL in. Niet-absolute URL&#39;s worden geïnterpreteerd als relatief ten opzichte van AEM.

* **ID** - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud uitsnijden, de startkaart wijzigen en inzoomen op de afbeelding.

![Bewerkingsdialoogvenster van afbeeldingscomponent](/help/assets/image-edit.png)

* Uitsnijden starten

   ![Uitsnijdpictogram starten](/help/assets/image-start-crop.png)

   Als u deze optie selecteert, wordt een vervolgkeuzelijst geopend voor vooraf gedefinieerde verhoudingen voor uitsnijden.

   * Kies de optie **Free Hand** om uw eigen uitsnijding te definiëren.
   * Kies de optie Uitsnijden **** verwijderen om het oorspronkelijke element weer te geven.

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

Op het tabblad **Main** kunt u een lijst met breedten in pixels voor de afbeelding definiëren. De component laadt automatisch de meest geschikte breedte op basis van de browsergrootte. Dit is een belangrijk onderdeel van de [responsieve functies](#responsive-features) van de afbeeldingscomponent.

Bovendien kunt u bepalen welke algemene componentenopties automatisch of gehandicapt zijn wanneer de auteur de component aan een pagina toevoegt.

![Het hoofdtabblad van het dialoogvenster Ontwerp van de afbeeldingscomponent](/help/assets/image-design-main.png)

* **Lazy laden** Definiëren inschakelen als de luie laadoptie automatisch wordt ingeschakeld wanneer de afbeeldingscomponent aan een pagina wordt toegevoegd.
* **Afbeelding is decoratief**. Definieer of de optie Decoratieve afbeelding automatisch is ingeschakeld wanneer u de afbeeldingscomponent aan een pagina toevoegt.
* **U kunt alternatieve tekst ophalen van DAM** Define als de optie om de alternatieve tekst van de DAM op te halen automatisch is ingeschakeld wanneer de afbeeldingscomponent aan een pagina wordt toegevoegd.
* **Hiermee wordt een bijschrift opgehaald van DAM** Define als de optie om het bijschrift op te halen van de DAM automatisch is ingeschakeld wanneer de afbeeldingscomponent aan een pagina wordt toegevoegd.
* **Bijschrift weergeven als pop-up** Definiëren als de optie om het bijschrift van de afbeelding als pop-up weer te geven automatisch is ingeschakeld wanneer de afbeeldingscomponent aan een pagina wordt toegevoegd.
* **Schakel UUID-** controle van bijhouden uit om het bijhouden van de UUID van het afbeeldingselement uit te schakelen.

* **Breedten** Definieert een lijst met breedten in pixels voor de afbeelding en de component laadt automatisch de meest geschikte breedte op basis van de browsergrootte.
   * Tik of klik op de knop **Toevoegen** om een andere grootte toe te voegen.
      * Gebruik de grepen om de volgorde van de formaten te wijzigen.
      * Gebruik het pictogram **Verwijderen** om een breedte te verwijderen.
   * Het laden van afbeeldingen wordt standaard uitgesteld totdat ze zichtbaar worden.
      * Selecteer de optie **Lazy load** uitschakelen om de afbeeldingen bij het laden van de pagina te laden.
* **JPEG-kwaliteit** De kwaliteitsfactor (als percentage van 0 en 100) voor getransformeerde JPEG-afbeeldingen (bijvoorbeeld geschaald of uitgesneden).

>[!NOTE]
>
>De optie JPEG-kwaliteit is beschikbaar vanaf release 2.2.0 van de Core Components.

>[!NOTE]
>
>Vanaf release 2.2.0 van Core Components voegt de Image Component het unieke UUID-kenmerk toe `data-asset-id` aan het afbeeldingselement, zodat het aantal weergaven dat afzonderlijke elementen ontvangen kan worden bijgehouden en geanalyseerd.

### Tabblad Functies {#features-tab}

Op het tabblad **Functies** kunt u opgeven welke opties beschikbaar zijn voor de auteurs van de inhoud wanneer de component wordt gebruikt, inclusief opties voor uploaden, richting en uitsnijden.

* Bron

   ![Dialoogvenster Eigenschappen van het ontwerpdialoogvenster van de component Image](/help/assets/image-design-features-source.png)

   Selecteer de optie **Het uploaden van middelen vanaf het bestandssysteem** toestaan om auteurs van inhoud toe te staan afbeeldingen te uploaden vanaf hun lokale computer. Schakel deze optie uit als u wilt dat inhoudsauteurs alleen elementen uit AEM selecteren.

* Afdrukstand

   ![Dialoogvenster Eigenschappen van het ontwerpdialoogvenster van de component Image](/help/assets/image-design-features-orientation.png)

* **Roteren** Gebruik deze optie als de auteur van de inhoud de optie 
**Rechtsom** roteren.
* **Met deze optie spiegelen** kan de auteur van de inhoud de opdracht 
**Opties voor Horizontaal** spiegelen en **Verticaal** spiegelen.

   >[!CAUTION]
   >
   >De optie **Spiegelen** is standaard uitgeschakeld. Als u deze optie inschakelt, worden de knoppen **Verticaal** omdraaien en Horizontaal **** omdraaien weergegeven in het dialoogvenster Bewerken van de afbeeldingscomponent. De functie wordt momenteel echter niet ondersteund door AEM en wijzigingen die met deze opties zijn aangebracht, blijven niet behouden.

* Uitsnijden

   ![Dialoogvenster Eigenschappen van het ontwerpdialoogvenster van de component Image](/help/assets/image-design-features-cropping.png)

   Selecteer de optie Uitsnijden **** toestaan om de auteur van de inhoud toe te staan de afbeelding uit te snijden in de component in het dialoogvenster Bewerken.
   * Klik op **Toevoegen** om een vooraf gedefinieerde hoogte-breedteverhouding voor uitsnijden toe te voegen.
   * Voer een beschrijvende naam in, die wordt weergegeven in het vervolgkeuzemenu Uitsnijden **** starten.
   * Voer de numerieke verhouding van het aspect in.
   * Gebruik de sleephandgrepen om de volgorde van de hoogte-breedteverhoudingen te wijzigen
   * Gebruik het prullenbakpictogram om een hoogte-breedteverhouding te verwijderen.

   >[!CAUTION]
   >
   >In AEM worden de hoogte-breedteverhoudingen voor uitsnijden gedefinieerd als **hoogte/breedte**. Dit verschilt van de conventionele definitie van breedte/hoogte en wordt gedaan om oude compatibiliteitsredenen. De auteurs van de inhoud zullen zich niet van enig verschil bewust zijn zolang u een duidelijke naam van de verhouding verstrekt aangezien de naam in UI en niet de verhouding zelf wordt getoond.

### Tabblad Stijlen {#styles-tab-1}

De component van het Beeld steunt het systeem [van de](/help/get-started/authoring.md#component-styling)Stijl van het AEM.

## Adaptieve afbeeldingsserver {#adaptive-image-servlet}

De component Image maakt gebruik van de Adaptive Image Servlet van de Core-component. [De Adaptive Image Servlet](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) is verantwoordelijk voor beeldverwerking en streaming en kan door ontwikkelaars worden benut bij hun [aanpassingen van de Core Components](/help/developing/customizing.md).

>[!NOTE]
>
>Voorwaardelijke verzoeken via de `Last-Modified` header worden ondersteund door de Adaptive Image Servlet, maar het in cache plaatsen van de `Last-Modified` header [moet worden ingeschakeld in de Dispatcher](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#caching-http-response-headers).
>
>[De de steekproefconfiguratie van de Verzender van de Projectarchetype](/help/developing/archetype/overview.md)van het AEM bevat reeds deze configuratie.
