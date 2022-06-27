---
title: Afbeeldingscomponent (v1)
description: De Core Component Image is een adaptieve beeldcomponent die ter plekke kan worden bewerkt.
index: n
role: Architect, Developer, Admin, User
exl-id: 625ce8de-5c4a-476d-b749-895493d169b1
source-git-commit: 5f25aee6ebcb7a5c6b8db0df5b8b853f15af97d0
workflow-type: tm+mt
source-wordcount: '1323'
ht-degree: 0%

---

# Afbeeldingscomponent (v1) {#image-component-v}

De Core Component Image is een adaptieve beeldcomponent die ter plekke kan worden bewerkt.

## Gebruik {#usage}

Met de component Afbeelding kunt u afbeeldingselementen eenvoudig plaatsen en op locatie bewerken. Deze functie biedt een adaptieve selectie van afbeeldingen met uitgestelde laadtijd en uitsnijden voor de auteur van de inhoud.

De toegestane afbeeldingsbreedten en uitsnijdinstellingen en aanvullende instellingen kunnen door de sjabloonauteur in het dialoogvenster [ontwerpdialoogvenster](#design-dialog). De inhoudeditor kan elementen uploaden of selecteren in het dialoogvenster [dialoogvenster configureren](#configure-dialog) en snijd de afbeelding uit in de [dialoogvenster bewerken](#edit-dialog). Voor meer gebruiksgemak is het ook mogelijk de afbeelding op een eenvoudige plaats aan te passen.

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
>Zie voor meer informatie over de huidige versie van de afbeeldingscomponent het gedeelte [Afbeeldingscomponent](/help/components/image.md) document.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende monster wordt genomen uit [Wij.Detailhandel](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Zie de [compatibiliteitsinformatie voor Core Components v1](/help/versions.md) voor meer informatie .

## Dialoogvenster configureren {#configure-dialog}

Naast de norm [dialoogvenster bewerken](#edit-dialog) en [ontwerpdialoogvenster](#design-dialog), biedt de component image een configuratiedialoogvenster waarin de afbeelding zelf wordt gedefinieerd, samen met de beschrijving en basiseigenschappen.

![](/help/assets/chlimage_1-50.png)

* **Afbeeldingselement**
   * Middelen uit het deelvenster [middelenbrowser](https://helpx.adobe.com/experience-manager/6-3/sites/authoring/using/author-environment-tools.html#main-pars_title) of tik op **doorbladeren** uploaden vanuit een lokaal bestandssysteem.
   * Tik of klik op **Wissen** om de selectie van de geselecteerde afbeelding op te heffen.
   * Tik of klik op **Bewerken** tot [de uitvoeringen van het actief beheren](https://helpx.adobe.com/experience-manager/6-3/assets/using/managing-assets-touch-ui.html#main-pars_title_19) in de middeleneditor.

* **Afbeelding is decoratief** - Controleer of het beeld door ondersteunende hulpmiddelen moet worden genegeerd en of er daarom geen alternatieve tekst nodig is. Dit geldt alleen voor decoratieve afbeeldingen.
* **Alternatieve tekst** - Textueel alternatief van de betekenis of functie van de afbeelding voor slechtzienden.
* **Koppeling**
   * Koppel de afbeelding aan een andere bron.
   * In het dialoogvenster Selecteren kunt u een koppeling maken naar een andere AEM.
   * Als u geen koppeling naar een AEM maakt, voert u de absolute URL in. Niet-absolute URL&#39;s worden geïnterpreteerd als relatief ten opzichte van AEM.

* **Bijschrift** - Standaard wordt aanvullende informatie over de afbeelding weergegeven onder de afbeelding.
* **Bijschrift weergeven als pop-up** - Als deze optie is ingeschakeld, wordt het bijschrift niet weergegeven onder de afbeelding, maar als een pop-up die door sommige browsers wordt weergegeven wanneer de muisaanwijzer op de afbeelding wordt geplaatst.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud uitsnijden, de startkaart wijzigen en inzoomen op de afbeelding.

![](/help/assets/chlimage_1-8.png)

* Uitsnijden starten

   ![](/help/assets/chlimage_1-9.png)

   Als u deze optie selecteert, wordt een vervolgkeuzelijst geopend voor vooraf gedefinieerde verhoudingen voor uitsnijden.

   * Kies de optie **Free Hand** om uw eigen uitsnijding te definiëren.
   * Kies de optie **Uitsnijden verwijderen** om het oorspronkelijke element weer te geven.

   Als een uitsnijdoptie is geselecteerd, gebruikt u de blauwe handgrepen om het uitsnijden op de afbeelding te vergroten of te verkleinen.

   ![](/help/assets/chlimage_1-10.png)

* Rechtsom roteren

   ![](/help/assets/chlimage_1-11.png)

   Gebruik deze optie als u de afbeelding 90° rechtsom wilt roteren.

* Toewijzing starten

   ![](/help/assets/chlimage_1-12.png)

   Gebruik deze optie om een startkaart toe te passen op de afbeelding. Als u deze optie selecteert, wordt een nieuw venster geopend waarin de gebruiker de vorm van de kaart kan selecteren:

   * **Rechthoekige kaart toevoegen**
   * **Cirkelvormige kaart toevoegen**
   * **Veelhoekkaart toevoegen**

      * Standaard wordt een driehoekige kaart toegevoegd. Dubbelklik op een lijn van de vorm om een nieuwe blauwe formaatgreep aan een nieuwe zijde toe te voegen.

   Als een vorm van een kaart is geselecteerd, wordt deze over de afbeelding heen geplaatst, zodat het formaat kan worden gewijzigd. Sleep de blauwe formaatgrepen om de vorm aan te passen.

   ![](/help/assets/chlimage_1-13.png)

   Nadat u de grootte van de startkaart hebt aangepast, klikt u erop om een zwevende werkbalk te openen om het pad van de koppeling te definiëren.

   * **Pad**
      * Gebruik de optie Padkiezer om een pad te selecteren in AEM
      * Als het pad niet in AEM staat, gebruikt u de absolute URL. Niet-absolute paden worden ten opzichte van AEM geïnterpreteerd.

      * **Alt-tekst**
Alternatieve beschrijving van de padbestemming
      * **Doel**
         * **Zelfde tabblad**
         * **Nieuw tabblad**
         * **Bovenliggend frame**
         * **Bovenste frame**

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

Op de **Hoofd** kunt u een lijst met toegestane breedten in pixels definiëren waarmee de afbeelding automatisch de meest geschikte breedte uit de lijst laadt.

![](/help/assets/chlimage_1-51.png)

Tik of klik op de knop Toevoegen om een andere grootte toe te voegen.

* Gebruik de grepen om de volgorde van de formaten te wijzigen.
* Gebruik het verwijderpictogram om een breedte te verwijderen.

Het laden van afbeeldingen wordt standaard uitgesteld totdat ze zichtbaar worden. Selecteer de optie **Lazy load uitschakelen** om de afbeeldingen te laden wanneer de pagina wordt geladen.

* **Geoptimaliseerde webafbeeldingen inschakelen** - Als deze optie is ingeschakeld, wordt [webgeoptimaliseerde service voor het leveren van afbeeldingen](/help/developing/web-optimized-image-delivery.md) Hiermee worden afbeeldingen in de WebP-indeling geleverd. De afbeeldingen worden gemiddeld met 25% verkleind.
   * Deze optie is alleen beschikbaar in AEMaaCS.
   * Als deze optie niet is ingeschakeld of als de service voor het leveren van afbeeldingen voor het web niet beschikbaar is, [Adaptieve afbeeldingsserver](/help/developing/adaptive-image-servlet.md) wordt gebruikt.

### Functies {#features}

Op de **Functies** kunt u opgeven welke opties beschikbaar zijn voor de auteurs van de inhoud wanneer u de component gebruikt, inclusief opties voor uploaden, richting en uitsnijden.

* **Geoptimaliseerde webafbeeldingen inschakelen** - als deze optie is ingeschakeld, levert de webgeoptimaliseerde service voor de levering van afbeeldingen afbeeldingen afbeeldingen in de WebP-indeling, waardoor de afbeeldingen gemiddeld met 25% kleiner worden.
   * Deze optie is alleen beschikbaar in AEMaaCS.
   * Als deze optie niet is ingeschakeld of als de service voor het leveren van afbeeldingen voor het web niet beschikbaar is, [Adaptieve afbeeldingsserver](/help/developing/adaptive-image-servlet.md) wordt gebruikt.

* Bron

   ![](/help/assets/chlimage_1-19.png)

   Selecteer de optie **Middelen uploaden vanuit bestandssysteem toestaan** om auteurs van inhoud toe te staan afbeeldingen te uploaden vanaf hun lokale computer. Schakel deze optie uit als u wilt dat inhoudsauteurs alleen elementen uit AEM selecteren.

* Afdrukstand

   ![](/help/assets/chlimage_1-20.png)

   * **Roteren** - Gebruik deze optie als u wilt dat de auteur van de inhoud de opdracht **Rechtsom roteren** optie.
   * **Omdraaien**
Gebruik deze optie als u wilt dat de auteur van de inhoud de opdracht 
**Horizontaal spiegelen** en **Verticaal spiegelen** opties.
   >[!CAUTION]
   >
   >De **Omdraaien** is standaard uitgeschakeld. Als u deze optie inschakelt, wordt het dialoogvenster **Verticaal spiegelen** en **Horizontaal spiegelen** in het dialoogvenster Bewerken van de afbeeldingscomponent. De functie wordt momenteel echter niet ondersteund door AEM en wijzigingen die met deze opties zijn aangebracht, blijven niet behouden.

* Uitsnijden

   ![](/help/assets/chlimage_1-21.png)

   Selecteer de optie **Uitsnijden toestaan** Hiermee kan de auteur van de inhoud de afbeelding uitsnijden in de component in het dialoogvenster Bewerken.
   * Klikken **Toevoegen** om een vooraf gedefinieerde hoogte-breedteverhouding voor uitsnijden toe te voegen.
   * Voer een beschrijvende naam in die wordt weergegeven in het dialoogvenster **Uitsnijden starten** vervolgkeuzelijst.
   * Voer de numerieke verhouding van het aspect in.
   * Gebruik de sleephandgrepen om de volgorde van de hoogte-breedteverhoudingen te wijzigen
   * Gebruik het prullenbakpictogram om een hoogte-breedteverhouding te verwijderen.

   >[!CAUTION]
   >
   >In AEM worden de hoogte-breedteverhoudingen voor uitsnijden gedefinieerd als **hoogte/breedte**. Dit verschilt van de conventionele definitie van breedte/hoogte en wordt gedaan om oude compatibiliteitsredenen. De auteurs van de inhoud zullen zich niet van enig verschil bewust zijn zolang u een duidelijke naam van de verhouding verstrekt aangezien de naam in UI en niet de verhouding zelf wordt getoond.

## Technische details {#technical-details}

De meest recente technische documentatie over de Image Component [kan op GitHub worden gevonden](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v1/image).

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).
