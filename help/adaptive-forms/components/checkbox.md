---
title: Adaptieve Forms Core-component - Selectievakje
description: De Adaptive Forms Checkbox Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: c6ca4800-bd10-4aeb-957a-fb1780cf94f3
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '1837'
ht-degree: 0%

---


# Component CheckBox{#checkbox-component}

Een selectievakje is een grafisch interface-element dat vaak wordt gebruikt in softwaretoepassingen en formulieren, zodat gebruikers een binaire keuze kunnen maken tussen twee opties: ingeschakeld (geselecteerd) of uitgeschakeld (uitgeschakeld).

Een selectievakje wordt meestal weergegeven als een klein vierkant dat in- of uitgeschakeld kan worden door erop te klikken of erop te tikken. Als een selectievakje is ingeschakeld, wordt een vinkje weergegeven om aan te geven dat de bijbehorende optie of functie actief of ingeschakeld is.

>[!NOTE]
>
> Voor AEM 6.5 Forms werd deze component geïntroduceerd met AEM 6.5 Forms Service Pack 19 (6.5.19.0). Om deze component in te schakelen, zorgt u ervoor dat de benodigde versies van zowel Forms Core Components als WCM Core Components zijn geïnstalleerd. Voor gedetailleerde informatie over de versies van de Adaptieve Componenten van de Kern van Forms, gelieve te verwijzen naar [&#x200B; Adaptieve versies van de Kern van Forms &#x200B;](/help/adaptive-forms/version.md)

{{traditional-aem}}

**Voorbeeld**

![&#x200B; checkbox groep &#x200B;](/help/adaptive-forms/assets/checkbox-example.png)

## Gebruik {#reasons-to-use-checkbox}

De algemene redenen om een selectievakje in een adaptief formulier te gebruiken zijn:

- **Versnelling van Gebruik**: De controledozen zijn visueel duidelijk en verstrekken een ongecompliceerde manier om binaire keuzen te maken. Ze zijn intuïtief en gemakkelijk te begrijpen en maken ze gebruiksvriendelijk.

- **Toestemming en Overeenkomst**: De controledozen worden gebruikt om gebruikerstoestemming voor diverse doeleinden, bijvoorbeeld het goedkeuren van voorwaarden, het intekenen op nieuwsbrieven, of het bevestigen van leeftijdscontrole te verkrijgen. Ze maken duidelijk dat de gebruiker actief met iets instemt.

- **Visuele Bevestiging**: Gecontroleerde controledozen verstrekken een visuele bevestiging aan gebruikers dat hun selectie is geregistreerd. Deze feedback helpt gebruikersfouten te voorkomen en zorgt ervoor dat gebruikers weten dat hun keuzes zijn geregistreerd.

- **Preventie van de Fout**: De controledozen verminderen de foutenwaarschijnlijkheid door gebruikers toe te staan om de keuzen vóór vormvoorlegging te herzien en te bevestigen.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Checkbox Core Component is uitgebracht als onderdeel van Core Components 2.0.52. Hier volgt een tabel met alle ondersteunde versies, AEM-compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | — |
| v1 | Compatibel systeem met <br>[&#x200B; versie 2.0.52 &#x200B;](/help/adaptive-forms/version.md) en later | Compatibel | Compatibel |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het [&#128279;](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0&rbrace;.

## Technische details {#technical-details}

Krijg de recentste informatie over de AanpassingsComponent van de Kern van Forms Checkbox in de technische documentatie op [&#x200B; GitHub &#x200B;](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkbox/v1/checkbox). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [&#x200B; de ontwikkelaarsdocumentatie van de Componenten van de Kern &#x200B;](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de ervaring in het selectievakje voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig opties voor selectievakjes definiëren voor een naadloze gebruikerservaring.

### Het tabblad Basis

![&#x200B; Basis lusje &#x200B;](/help/adaptive-forms/assets/checkbox-basic.png)

- **Naam** - u kunt een vormcomponent gemakkelijk met zijn unieke naam zowel in de vorm als in de regelredacteur identificeren, maar de naam moet geen ruimten of speciale karakters bevatten.

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bij de component. Als u geen titel toevoegt, wordt de component niet weergegeven.

- **staat RTF voor Titel** toe - Deze eigenschappen laat gebruikers toe om gewone teksttitels te formatteren, die eigenschappen zoals vette, cursieve, onderstreepte tekst, diverse doopvonten, doopvontgrootte, kleuren, en extra optie opnemen om visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Op het selecteren van checkbox voor **staat RTF-tekst voor Titel** toe, wordt het formatteren opties zichtbaar om de titel van de component te stileren. Om tot alle beschikbare het formatteren opties toegang te hebben, kunt u op het ![&#x200B; pictogram Volledig scherm &#x200B;](/help/adaptive-forms/assets/fullscreen-icon.png) tabel klikken.

  ![&#128279;](/help/adaptive-forms/assets/richtext-support-title.png) de rijke tekststeun van 0&rbrace;

- **Verberg Titel** - selecteer de optie om de Titel van de component te verbergen.

- **Bind Verwijzing** - A bindt verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u met AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

- **Teken als Niet-gebonden Element van de Vorm**: Selecteer de optie om een vormgebied te vormen niet verbonden aan om het even welk schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.

- **Type van Gegevens van voorgelegde waarde**: Deze optie specificeert het gegevenstype van de verzonden waarde wanneer om het even welke optie wordt geselecteerd. Als het **gegevenstype van voorgelegde waarde** aan `Number` wordt geplaatst en u koordgegevens aan **Waarde van Gegevens** &#x200B; &#x200B; op het **lusje van Opties** toevoegt, toont het scherm een `Value type mismatch` foutenmelding.

- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken of te sluiten. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
  <!-- - **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.-->
- **wanneer Gecontroleerd, terugkeerwaarde** - selecteer deze optie om te specificeren welke waarde met checkbox zou moeten worden geassocieerd wanneer het wordt gecontroleerd of geselecteerd. Het is de actie die voorkomt wanneer u of checkbox merkt.
- **de staatswaarde van de Oncontrole van het Behouden** - selecteer deze optie om de waarde te specificeren die moet worden teruggekeerd wanneer de checkbox component niet wordt geselecteerd. Als **Uncheck staatswaarde** wordt toegelaten of aan waar wordt geplaatst, **wanneer Ongecontroleerd, de optie van de terugkeerwaarde** verschijnt.
- **wanneer Ongecontroleerd, terugkeerwaarde** - de optie staat u toe om te specificeren welke waarde met checkbox zou moeten worden geassocieerd wanneer het in een ongecontroleerde of gedeselecteerde staat is.

- **Standaardwaarde**: Deze optie staat u toe om een standaardwaarde op een vormgebied toe te voegen. Als **Component** onbruikbaar maakt wordt geselecteerd, wordt de standaardwaarde getoond op het scherm. Als geen waarde wordt ingevoerd door de gebruiker in het formulierveld, wordt deze waarde verzonden op het moment dat het formulier wordt verzonden.

### Tabblad Validatie {#validation-tab}

![&#x200B; het lusje van de Bevestiging &#x200B;](/help/adaptive-forms/assets/checkbox-validation.png)

- **Vereist** - selecteer deze optie, als u de component in een Aangepaste Vorm wilt tonen. Nadat u de optie hebt geselecteerd, moet u een selectie maken voordat u een formulier kunt verzenden. U kunt niet de **Component van de Verbergen** selecteren of **Component** in het **Basis** lusje onbruikbaar maken wanneer deze optie wordt geselecteerd.

- **Bericht van de Fout** - Deze optie staat u toe om een bericht in te gaan dat wordt getoond als **Vereiste** checkbox wordt gecontroleerd en het vormgebied wordt verlaten leeg.
- **Bericht van de Bevestiging van het Manuscript** - Deze optie staat u toe om een bericht in te gaan dat moet worden getoond als de manuscriptbevestiging ontbreekt.

### Het tabblad Help-inhoud {#helpcontent-tab}

![&#x200B; Inhoud tabel van de Hulp &#x200B;](/help/adaptive-forms/assets/checkbox-help.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.

- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}

![&#x200B; Toegankelijkheid tabel &#x200B;](/help/adaptive-forms/assets/checkbox-accessibility.png)

- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.
   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Check-box te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

De adaptieve Component van de Kern van de Forms Checkbox steunt het systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

![&#x200B; Dialoog van het Ontwerp &#x200B;](/help/adaptive-forms/assets/checkbox-style.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de Aangepaste Component van de Kern van Forms verstrekken Checkbox.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![&#x200B; de Dialoog van Eigenschappen van de Douane &#x200B;](/help/adaptive-forms/assets/checkbox-customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de orde van de naam van het douanebezit en de waarde van het douanebezit te herschikken.

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
