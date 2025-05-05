---
title: Afbeeldingscomponent (v1)
description: De Core Component Image is een adaptieve beeldcomponent die ter plekke kan worden bewerkt.
index: n
role: Architect, Developer, Admin, User
exl-id: 625ce8de-5c4a-476d-b749-895493d169b1
source-git-commit: 5f25aee6ebcb7a5c6b8db0df5b8b853f15af97d0
workflow-type: tm+mt
source-wordcount: '1293'
ht-degree: 0%

---

# Afbeeldingscomponent (v1) {#image-component-v}

De Core Component Image is een adaptieve beeldcomponent die ter plekke kan worden bewerkt.

## Gebruik {#usage}

Met de component Afbeelding kunt u afbeeldingselementen eenvoudig plaatsen en op locatie bewerken. Deze functie biedt een adaptieve selectie van afbeeldingen met uitgestelde laadtijd en uitsnijden voor de auteur van de inhoud.

De toegestane beeldbreedten evenals het bebouwen en de extra montages kunnen door de malplaatjeauteur in de [ ontwerpdialoog ](#design-dialog) worden bepaald. De inhoudsredacteur kan activa in [ uploaden of selecteren vormt dialoog ](#configure-dialog) en bebouwt het beeld in [ uitgeeft dialoog ](#edit-dialog). Voor meer gebruiksgemak is het ook mogelijk de afbeelding op een eenvoudige plaats aan te passen.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Image Component beschreven, die oorspronkelijk is geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van versie 1 van de component Image weergegeven.

| AEM | Afbeeldingscomponent v1 |
|--- |--- |
| 6,3 | Compatibel |
| 6,4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de afbeeldingscomponent beschreven.
>
>Voor details van de huidige versie van de Component van het Beeld, zie het [&#128279;](/help/components/image.md) document van de Component van het Beeld 0&rbrace; &lbrace;.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende wordt steekproef genomen van [ We.Retail ](https://helpx.adobe.com/nl/experience-manager/6-4/sites/developing/using/we-retail.html).

### Schermafbeelding {#screenshot}

![](/help/assets/chlimage_1-7.png)

### HTML {#html}

```
<div class="cmp cmp-image aem-GridColumn aem-GridColumn--default--12">
 
        <noscript data-cmp-image="{&#34;smartImages&#34;:[],&#34;smartSizes&#34;:[],&#34;lazyEnabled&#34;:true}">
            <img src="/content/we-retail/us/en/equipment/_jcr_content/root/responsivegrid/image.img.jpg" alt="Surfboard"/>
        </noscript>

</div>
```

### JSON {#json}

```
"image": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "smartSizes": [],
              "smartImages": [],
              "lazyEnabled": true,
              "src": "/content/we-retail/us/en/equipment/equipment/jcr%3acontent/root/responsivegrid/image.img.jpeg",
              ":type": "weretail/components/content/image"
            }
```

>[!NOTE]
>
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Gelieve te zien de [ verenigbaarheidsinformatie voor de Componenten van de Kern v1 ](/help/versions.md) voor meer informatie.

## Dialoogvenster configureren {#configure-dialog}

Naast standaard [ geef dialoog ](#edit-dialog) uit en [ ontwerpdialoog ](#design-dialog), biedt de beeldcomponent een dialoog aan waar het beeld zelf samen met zijn beschrijving en basiseigenschappen wordt bepaald.

![](/help/assets/chlimage_1-50.png)

* **activa van het Beeld**
   * Daling een activa van [ activa browser ](https://helpx.adobe.com/nl/experience-manager/6-3/sites/authoring/using/author-environment-tools.html#main-pars_title) of ontvang **doorbladert** optie om van een lokaal dossiersysteem te uploaden.
   * Tik of klik **Duidelijk** om het momenteel geselecteerde beeld te deselecteren.
   * Tik of klik **uitgeven** [ om de vertoningen van de activa ](https://helpx.adobe.com/nl/experience-manager/6-3/assets/using/managing-assets-touch-ui.html#main-pars_title_19) in de activaredacteur te beheren.

* **Beeld is decoratief** - controleer als het beeld door ondersteunende technologie zou moeten worden genegeerd en daarom geen alternatieve tekst vereist. Dit geldt alleen voor decoratieve afbeeldingen.
* **Alternatieve tekst** - Textueel alternatief van de betekenis of de functie van het beeld, voor visueel gehandicapte lezers.
* **Verbinding**
   * Koppel de afbeelding aan een andere bron.
   * In het dialoogvenster Selecteren kunt u een koppeling maken naar een andere AEM.
   * Als u geen koppeling naar een AEM maakt, voert u de absolute URL in. Niet-absolute URL&#39;s worden geïnterpreteerd als relatief ten opzichte van AEM.

* **Titel** - de Extra informatie over het beeld, onder het beeld wordt getoond is gebrek.
* **titel van de Vertoning als pop-up** -   Als deze optie is ingeschakeld, wordt het bijschrift niet weergegeven onder de afbeelding, maar als een pop-up die door sommige browsers wordt weergegeven wanneer de muisaanwijzer op de afbeelding wordt geplaatst.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud uitsnijden, de startkaart wijzigen en inzoomen op de afbeelding.

![](/help/assets/chlimage_1-8.png)

* Uitsnijden starten

  ![](/help/assets/chlimage_1-9.png)

  Als u deze optie selecteert, wordt een vervolgkeuzelijst geopend voor vooraf gedefinieerde verhoudingen voor uitsnijden.

   * Kies de optie **Vrije hand** om uw eigen uitsnijding te bepalen.
   * Kies de optie **verwijdert Uitsnijden** om de originele activa te tonen.

  Als een uitsnijdoptie is geselecteerd, gebruikt u de blauwe handgrepen om het uitsnijden op de afbeelding te vergroten of te verkleinen.

  ![](/help/assets/chlimage_1-10.png)

* Rechtsom roteren

  ![](/help/assets/chlimage_1-11.png)

  Gebruik deze optie als u de afbeelding 90° rechtsom wilt roteren.

* Toewijzing starten

  ![](/help/assets/chlimage_1-12.png)

  Gebruik deze optie om een startkaart toe te passen op de afbeelding. Als u deze optie selecteert, wordt een nieuw venster geopend waarin de gebruiker de vorm van de kaart kan selecteren:

   * **voeg Rechthoekige Kaart** toe
   * **voeg Circulaire Kaart** toe
   * **voeg VeelhoekKaart** toe

      * Standaard wordt een driehoekige kaart toegevoegd. Dubbelklik op een lijn van de vorm om een nieuwe blauwe formaatgreep aan een nieuwe zijde toe te voegen.

  Als een vorm van een kaart is geselecteerd, wordt deze over de afbeelding heen geplaatst, zodat het formaat kan worden gewijzigd. Sleep de blauwe formaatgrepen om de vorm aan te passen.

  ![](/help/assets/chlimage_1-13.png)

  Nadat u de grootte van de startkaart hebt aangepast, klikt u erop om een zwevende werkbalk te openen om het pad van de koppeling te definiëren.

   * **Weg**
      * Gebruik de optie Padkiezer om een pad te selecteren in AEM
      * Gebruik de absolute URL als het pad niet in AEM is. Niet-absolute paden worden ten opzichte van AEM geïnterpreteerd.

      * **de tekst van Alt**
Alternatieve beschrijving van de padbestemming
      * **Doel**
         * **Zelfde lusje**
         * **Nieuw lusje**
         * **Bovenliggend Kader**
         * **Bovenste Kader**

  Tik of klik op het blauwe vinkje dat u wilt opslaan, de zwarte x die u wilt annuleren en de rode prullenbak om de kaart te verwijderen.

  ![](/help/assets/chlimage_1-14.png)

* Zoomen herstellen

  ![](/help/assets/chlimage_1-15.png)

  Als al op de afbeelding is ingezoomd, gebruikt u deze optie om het zoomniveau opnieuw in te stellen.

* Zoomregelaar openen

  ![](/help/assets/chlimage_1-16.png)

  Met deze optie geeft u een schuifregelaar weer om het zoomniveau van de afbeelding te bepalen.

  ![](/help/assets/chlimage_1-17.png)

U kunt de interne editor ook gebruiken om de afbeelding te wijzigen. Vanwege ruimtebeperkingen zijn alleen de basisopties online beschikbaar. Voor volledige bewerkingsopties gebruikt u de modus Volledig scherm.

![](/help/assets/chlimage_1-18.png)

>[!NOTE]
>
>Bewerkingen voor het bewerken van afbeeldingen (uitsnijden, spiegelen, roteren) worden niet ondersteund voor GIFFEN-afbeeldingen. Dergelijke wijzigingen die in de bewerkingsmodus zijn aangebracht op GIFFEN, blijven niet behouden.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de inhoud die de auteur van deze component gebruikt, uploaden en roteren, definiëren.

### Hoofd {#main}

Op het **Belangrijkste** lusje kunt u een lijst van toegestane breedten in pixel voor het beeld bepalen om de meest aangewezen breedte van de lijst automatisch te laden.

![](/help/assets/chlimage_1-51.png)

Tik of klik op de knop Toevoegen om een andere grootte toe te voegen.

* Gebruik de grepen om de volgorde van de formaten te wijzigen.
* Gebruik het verwijderpictogram om een breedte te verwijderen.

Het laden van afbeeldingen wordt standaard uitgesteld totdat ze zichtbaar worden. Selecteer de optie **maak het laden** onbruikbaar om de beelden op paginading te laden.

* **laat Web Geoptimaliseerde Beelden** toe - wanneer gecontroleerd, zal de [ Web-geoptimaliseerde dienst van de beeldlevering ](/help/developing/web-optimized-image-delivery.md) beelden in het formaat leveren WebP, die beeldgrootte door gemiddeld 25% verminderen.
   * Deze optie is alleen beschikbaar in AEMaaCS.
   * Wanneer ongecontroleerd of de web-optimized dienst van de beeldlevering niet beschikbaar is [ wordt de Aangepaste Servlet van het Beeld ](/help/developing/adaptive-image-servlet.md) gebruikt.

### Functies {#features}

Op het **lusje van Eigenschappen** kunt u bepalen welke opties aan de inhoudsauteurs beschikbaar zijn wanneer het gebruiken van de component met inbegrip van uploadt opties, richtlijn, en bebouwende opties.

* **laat Web Geoptimaliseerde Beelden** toe - wanneer gecontroleerd, zal de Web-geoptimaliseerde dienst van de beeldlevering beelden in het formaat WebP leveren, die beeldgrootte door gemiddeld 25% verminderen.
   * Deze optie is alleen beschikbaar in AEMaaCS.
   * Wanneer ongecontroleerd of de web-optimized dienst van de beeldlevering niet beschikbaar is [ wordt de Aangepaste Servlet van het Beeld ](/help/developing/adaptive-image-servlet.md) gebruikt.

* Source

  ![](/help/assets/chlimage_1-19.png)

  Selecteer de optie **activa uploaden van het dossiersysteem** toestaan om inhoudsauteurs toe te staan om beelden van zijn of haar lokale computer te uploaden. Schakel deze optie uit als u wilt dat inhoudsauteurs alleen elementen uit AEM selecteren.

* Afdrukstand

  ![](/help/assets/chlimage_1-20.png)

   * **roteer** - gebruik deze optie om de inhoudauteur toe te staan om **te gebruiken roteer Juist** optie.
   * **Omdraaien**
Gebruik deze optie om de inhoudauteur toe te staan om **Horizontaal te gebruiken Omdraaien** en **Verticaal omdraaien** opties.

  >[!CAUTION]
  >
  >De **1&rbrace; optie van de Omslag &lbrace;wordt onbruikbaar gemaakt door gebrek.** Toelatend zal het **Verticaal Omdraaien** en **Horizontaal Omdraaien** knopen in uitgeven dialoog van de beeldcomponent tonen, nochtans wordt de eigenschap momenteel niet gesteund door AEM en om het even welke veranderingen die gebruikend deze opties worden aangebracht zullen niet worden voortgeduurd.

* Uitsnijden

  ![](/help/assets/chlimage_1-21.png)

  Selecteer de optie **gewas** toestaan om de inhoudauteur toe te staan om het beeld in de component in uit te snijden uitgeeft dialoog.
   * Klik **toevoegen** om een vooraf bepaalde uitsnijdverhouding toe te voegen.
   * Ga een beschrijvende naam in, die in **1&rbrace; dropdown van het Gewas van het Begin &lbrace;zal worden getoond.**
   * Voer de numerieke verhouding van het aspect in.
   * Gebruik de sleephandgrepen om de volgorde van de hoogte-breedteverhoudingen te wijzigen
   * Gebruik het prullenbakpictogram om een hoogte-breedteverhouding te verwijderen.

  >[!CAUTION]
  >
  >Merk op dat in AEM, gewassenaspectverhoudingen als **hoogte/breedte** worden bepaald. Dit verschilt van de conventionele definitie van breedte/hoogte en wordt gedaan om oude compatibiliteitsredenen. De auteurs van de inhoud zullen zich niet van enig verschil bewust zijn zolang u een duidelijke naam van de verhouding verstrekt aangezien de naam in UI en niet de verhouding zelf wordt getoond.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van het Beeld [ kan op GitHub ](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v1/image) worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).
