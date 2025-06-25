---
title: Adaptive Forms Core Component - Voorwaarden en bepalingen
description: De kerncomponent Adaptive Forms Terms and Conditions gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: c607d554-ad2d-4434-856d-91e174ef3149
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '3253'
ht-degree: 0%

---


# Onderdeel Voorwaarden en bepalingen

A **de Bepalingen en de component van de Voorwaarden** verwijst naar een sectie binnen een vorm die de termijnen, de regels, en de voorwaarden schetst die de gebruikers met moeten instemmen of voldoen wanneer het gebruiken van de dienst of de toegang tot van inhoud.

De **componenten van de Voorwaarden en van de Voorwaarden** is een samengestelde component die uit Tekst, CheckBox, en de componenten van de Verbinding bestaat. De tekstcomponent bevat een titel samen met een kort overzicht van het doel en het bereik van de voorwaarden. Het omvat ook een checkbox die wordt gebruikt om expliciete toestemming van de gebruiker te verkrijgen. U kunt een tekst met toestemming ook vervangen door koppelingen.

>[!NOTE]
>
> Voor AEM 6.5 Forms werd deze component geïntroduceerd met AEM 6.5 Forms Service Pack 19 (6.5.19.0). Om deze component in te schakelen, zorgt u ervoor dat de benodigde versies van zowel Forms Core Components als WCM Core Components zijn geïnstalleerd. Voor gedetailleerde informatie over de versies van de Adaptieve Componenten van de Kern van Forms, gelieve te verwijzen naar [ Adaptieve versies van de Kern van Forms ](/help/adaptive-forms/version.md)

{{traditional-aem}}

**Voorbeeld**

![ voorwaarden ](/help/adaptive-forms/assets/terms-and-conditions.png)

Zie [ Subcomponenten van de component van Bepalingen en van de Voorwaarden ](#sub-component) sectie, om meer over verschillende componenten van de component van Bepalingen en van de Voorwaarden te leren.

## Gebruik {#reasons-to-use-termsandconditions}

- **Overeenkomst van de Gebruiker**: De component dient als overeenkomst tussen de dienstverlener en de gebruiker. Gebruikers moeten de voorwaarden bevestigen en ermee akkoord gaan voordat ze de service of inhoud kunnen openen.

- **Juridische Naleving**: Het verzekert wettelijke naleving en bescherming voor de dienstverlener door de rechten, de verantwoordelijkheden, en de verplichtingen van beide partijen te schetsen.

- **Processen van de Registratie**: De registratie of de sign-up vormen omvatten de **Bepalingen en Voorwaarden** component, die gebruikers vereisen om met de termijnen uitdrukkelijk akkoord te gaan alvorens een rekening te creëren of de dienst te gebruiken.

- **E-commerce Transacties**: De online websites omvatten de **Bepalingen en de component van de Voorwaarden** zodat de gebruikers worden ertoe aangezet om met de voorwaarden als deel van het controleproces akkoord te gaan alvorens online aankopen te maken.

- **de Overeenkomsten van de Veiligheid en van de Privacy**: De **Bepalingen en de component van de Voorwaarden** omvat details op hoe het gebruikersgegeven wordt verzameld, opgeslagen, en gebruikt, vaak aangevuld met een afzonderlijk privacybeleid

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Terms and Conditions Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.62 voor Cloud Service en Core Components 1.1.28 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM-compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.0.62 ](/help/adaptive-forms/version.md) en later | Compatibel met <br>[ versie 1.1.28 ](/help/adaptive-forms/version.md) en later maar minder dan 2.0.0. |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het [&#128279;](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0&rbrace;.

## Technische details {#technical-details}

Krijg de recentste informatie over de AanpassingsComponent van de Kern van de Voorwaarden van Forms in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de ervaring van de component bepalingen en voorwaarden eenvoudig aanpassen voor bezoekers. U kunt de voorwaarden en bepalingen eenvoudig definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard

![ Basis lusje ](/help/adaptive-forms/assets/terms-and-conditions-basic-tab.png)

- **Naam** - de naam identificeert uniek de component in de regelredacteur. Speciale tekens en spaties zijn niet toegestaan in de naamtekenreeksen.

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bovenop de component. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **staat RTF voor Titel** toe - Deze eigenschappen laat gebruikers toe om gewone teksttitels te formatteren, die eigenschappen zoals vette, cursieve, onderstreepte tekst, diverse doopvonten, doopvontgrootte, kleuren, en extra optie opnemen om visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Op het selecteren van checkbox voor **staat RTF-tekst voor Titel** toe, wordt het formatteren opties zichtbaar om de titel van de component te stileren. Om tot alle beschikbare het formatteren opties toegang te hebben, kunt u op het ![ pictogram Volledig scherm ](/help/adaptive-forms/assets/fullscreen-icon.png) tabel klikken.

  ![&#128279;](/help/adaptive-forms/assets/richtext-support-title.png) de rijke tekststeun van 0&rbrace;

- **toon de Optie van de Goedkeuring** - selecteer de optie om toestemmingscheckbox te tonen die wordt gebruikt om expliciete toestemming van de gebruiker te verkrijgen.

- **toon als pop-up** - selecteer de optie om de termijnen en voorwaardencomponent in een pop-up venster te tonen.

- **vervangt de tekst van de Toestemming met weblink(s)**: Selecteer de optie om een toestemmingstekst met een Webverbinding te vervangen.  Als de optie is uitgeschakeld, wordt standaard de tekst voor de toestemming weergegeven.

- **Verberg Titel** - selecteer de optie om de Titel van de component te verbergen.

- **de gegevens van de Groepering van kindcomponenten over vormvoorlegging (de gegevens van de Omslag in voorwerp)** - wanneer de optie wordt geselecteerd, worden de gegevens van zijn kindcomponenten genesteld binnen het voorwerp JSON van de oudercomponent. Als de optie echter niet is geselecteerd, hebben de verzonden JSON-gegevens een platte structuur, zonder object voor de bovenliggende component. Bijvoorbeeld:

   - Wanneer de optie is geselecteerd, worden de gegevens van de onderliggende componenten (bijvoorbeeld Straat, Plaats en Postcode) genest binnen de bovenliggende component (Adres) als een JSON-object. Dit leidt tot een hiërarchische structuur, en de gegevens worden georganiseerd onder de oudercomponent.

     Structuur van de ingediende gegevens:

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - Wanneer de optie niet is geselecteerd, hebben de verzonden JSON-gegevens een platte structuur zonder object voor de bovenliggende component (Adres). Alle gegevens bevinden zich op hetzelfde niveau, zonder hiërarchische organisatie.

     Structuur van de ingediende gegevens:

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

- **Bind Verwijzing** - A bindt verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **read-only** - selecteer de optie om de component niet-editable te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Het tabblad Help-inhoud {#help-content-tab}

![ Inhoud tabel van de Hulp ](/help/adaptive-forms/assets/terms-and-conditions-help-tab.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.

- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid

![ Toegankelijkheid tabel ](/help/adaptive-forms/assets/terms-and-conditions-accessibility-tab.png)

- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.
   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.
- **rol van HTML voor het schermlezer om** aan te kondigen - de rol van HTML is een attribuut dat wordt gebruikt om het doel van een element van HTML aan ondersteunende technologieën zoals het schermlezers te specificeren. Het rolattribuut wordt gebruikt om extra context en semantische betekenis aan een element te verstrekken, die het voor schermlezers gemakkelijker maken om de inhoud te interpreteren en aan de gebruiker aan te kondigen. In AEM Forms heeft het label van een formulierveld bijvoorbeeld de rol &quot;label&quot; en kan het invoerveld de rol &quot;textbox&quot; hebben. Hierdoor kan de schermlezer de relatie tussen het label en het invoerveld begrijpen en deze correct aan de gebruiker meedelen.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Voorwaarden te definiëren en te beheren.


### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptieve Component van de Kern van de Voorwaarden van Forms steunt het systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

![ Dialoog van het Ontwerp ](/help/adaptive-forms/assets/checkbox-style.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de Aangepaste Component van de Kern van de Voorwaarden en van de Voorwaarden van Forms verstrekken.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![ de Dialoog van Eigenschappen van de Douane ](/help/adaptive-forms/assets/checkbox-customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de orde van de naam van het douanebezit en de waarde van het douanebezit te herschikken.

## Subcomponenten van de component Voorwaarden en Voorwaarden {#sub-component}

**de Bepalingen en de Component van de Voorwaarden** zijn een samengestelde component die uit de volgende subcomponenten bestaat:
- [Component Koppelen](#link)
- [Tekstcomponent](#text)
- [Component CheckBox](#checkbox)

### Component Koppelen{#link}

Deze component vervangt een of meer toestemmingsteksten door een of meer webkoppelingen. Het wordt gebruikt in een scenario, waar de gebruiker verwijzingen naar bepaalde secties, extra informatie, of externe documenten probeert aan te bieden. U kunt de **component van de Verbinding** individueel voor bezoekers met de Configure Dialoog aanpassen.

#### Tabblad Standaard

![ Basis lusje ](/help/adaptive-forms/assets/link-basic-tab.png)

- **Naam** - de naam identificeert uniek de component in de regelredacteur. Speciale tekens en spaties zijn niet toegestaan in de naamtekenreeksen.

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bovenop de component. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **staat Rijke Tekst voor Titel** toe - Deze eigenschap laat gebruikers toe om titels te formatteren gebruikend opties zoals vette, cursieve opties, doopvontstijlen, kleuren, en groepering, verbeterend visuele presentatie en aanpassing. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Op het selecteren van checkbox voor **staat RTF-tekst voor Titel** toe, wordt het formatteren opties zichtbaar om de titel van de component te stileren. Om tot alle beschikbare het formatteren opties toegang te hebben, kunt u op het ![ pictogram Volledig scherm ](/help/adaptive-forms/assets/fullscreen-icon.png) tabel klikken.

  ![&#128279;](/help/adaptive-forms/assets/richtext-support-title.png) de rijke tekststeun van 0&rbrace;

- **Verberg Titel** - selecteer de optie om de Titel van de component te verbergen.

- **Verbindingen** - specificeer de verbinding en de overeenkomstige vertoningstekst die in plaats van de toestemmingstekst wordt gebruikt. U kunt veelvoudige verbindingen toevoegen door **te klikken voegt** knoop toe.
Nadat een nieuwe optie is toegevoegd, kunnen de volgende acties worden uitgevoerd:
   - **Verbinding** - deze optie staat toe om URL in te gaan om opnieuw te richten wanneer een optie wordt geselecteerd.
   - **Tekst van de Vertoning** - Deze optie staat toe om de inhoud in te gaan om in een AanpassingsVorm te tonen.
   - **Schrapping** - Tik of klik om de optie van een radioknoop te schrappen.
   - **herschikt** - Tik of klik en sleep om de orde van de opties te herschikken.

  U kunt de opties voor checkbox groep ook formatteren gebruikend **Verrijkte Tekst voor Opties** toestaan. Zodra u checkbox voor **selecteert sta RTF voor het formatteren van Opties** toe zichtbaar worden om de opties van de component te stileren. Om tot alle beschikbare het formatteren opties toegang te hebben, kunt u op het `Fullscreen` ![ pictogram Volledig scherm ](/help/adaptive-forms/assets/fullscreen-icon.png) tabel klikken.

  ![ Rijke tekststeun voor opties ](/help/adaptive-forms/assets/link-options.png)

- **Bind Verwijzing** - A bindt verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u met AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

- **Teken als Niet-gebonden Element van de Vorm**: Selecteer de optie om een vormgebied te vormen niet verbonden aan om het even welk schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.
- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken of te sluiten. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **read-only** - selecteer de optie om de component niet-editable te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

#### Tabblad Validatie

![ het lusje van de Bevestiging ](/help/adaptive-forms/assets/link-validation-tab.png)

- **Vereist** - selecteer deze optie, als u de component in een Aangepaste Vorm wilt tonen. Nadat u de optie hebt geselecteerd, moet u een selectie maken voordat u een formulier kunt verzenden. U kunt niet de **Component van de Verbergen** selecteren of **Component** in het **Basis** lusje onbruikbaar maken wanneer deze optie wordt geselecteerd.

- **Bericht van de Fout** - Deze optie staat u toe om een bericht in te gaan dat wordt getoond als **Vereiste** checkbox wordt gecontroleerd en het vormgebied wordt verlaten leeg.

- **Bericht van de Bevestiging van het Manuscript** - Deze optie staat u toe om een bericht in te gaan dat moet worden getoond als de manuscriptbevestiging ontbreekt.

### Het tabblad Help-inhoud {#helpcontent-tab}

![ Inhoud tabel van de Hulp ](/help/adaptive-forms/assets/link-help-tab.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.

- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid

![ Toegankelijkheid tabel ](/help/adaptive-forms/assets/link-accessibilty-tab.png)

- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.
   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.

### Tekstcomponent {#text}

**de component van de Tekst** toont de tekstuele inhoud die informatie aan gebruikers verstrekt. Deze component omvat de feitelijke voorwaarden, de juridische taal of andere relevante tekstinformatie.

U kunt de [ component van de Tekst ](/help/adaptive-forms/components/text.md) gemakkelijk aanpassen individueel voor bezoekers met Configure Dialoog. Om tekstopties voor een naadloze gebruikerservaring te bepalen, gebruik [ vormt dialoog van de tekstcomponent ](/help/adaptive-forms/components/text.md#configure-dialog).


### Component CheckBox {#checkbox}

Een checkbox wordt gebruikt om gebruikerstoestemming of erkenning te verkrijgen. Het dient als visuele indicator die de gebruiker heeft gelezen en met de vermelde termijnen akkoord gegaan. Het is verplicht het selectievakje in te schakelen om de toestemming van de gebruiker aan te geven.

U kunt de [ component Checkbox ](/help/adaptive-forms/components/checkbox.md) gemakkelijk aanpassen individueel voor bezoekers met Configure Dialoog. Om de eigenschappen van checkbox voor een naadloze gebruikerservaring te bepalen, gebruik [ vormt dialoog van de checkbox component ](/help/adaptive-forms/components/checkbox.md#configure-dialog).


## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
