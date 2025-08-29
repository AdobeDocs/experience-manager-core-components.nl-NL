---
title: Adaptive Forms Core Component - Krabbelhandtekening
description: De Adaptive Forms Scribble Signature Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
source-git-commit: 4218af42d947e19a65efe8839ccd4eb102fe2f21
workflow-type: tm+mt
source-wordcount: '1732'
ht-degree: 0%

---


# Ondertekeningscomponent voor krabbelen

Een krabbelcomponent van de Handtekening in een AanpassingsVorm is een gebruikersinterface element dat gebruikers toestaat om hun **handtekening** direct binnen de vorm te trekken gebruikend een muis, een stift, of touchscreen. Het zorgt ervoor dat handgeschreven toestemming, goedkeuringen, of controle in digitale werkschema&#39;s nauwkeurig worden gevangen.

**Voorbeeld**

![ voorbeeld ](/help/adaptive-forms/assets/scribble-signature.png){width=50%,align-center}

**Diverse Opties beschikbaar in het Venster van de Handtekening**

- **A:** klik **trekken** pictogram om uw handtekening op canvas te trekken.
- **B:** klik het **Duidelijke** pictogram om de handtekening op canvas te ontruimen.
- **C:** klik het **Geolocation** pictogram om geolocation samen met de handtekening toe te voegen.
- **D:** klik het **pictogram van het Toetsenbord** om uw naam op canvas te typen.

Zodra u **sparen** pictogram in het Krabbelhandtekeningsvenster selecteert, kunt u niet de handtekening uitgeven. Als u de handtekening wilt bewerken, moet u de huidige handtekening negeren en opnieuw ondertekenen met de bovenstaande optie Penseel/toetsenbord.

>[!NOTE]
>
> Handtekeningen worden altijd opgeslagen in de PNG-indeling.

## Gebruik {#reasons-to-use-scribble-signature}

Er zijn verschillende redenen waarom het nuttig is een veld voor scripthandtekening op te nemen in een formulier, zoals:

- **Digitale toestemming**: Staat gebruikers toe om wettelijk geldige handtekeningen elektronisch te verstrekken.
- **Verbeterde gebruikerservaring**: Verstrekt een natuurlijke manier om rechtstreeks op apparaten te ondertekenen zonder aftasten of het uploaden.
- **Paperless werkschema&#39;s**: Elimineert de behoefte aan druk, het ondertekenen, en het opnieuw scannen documenten.
- **Authentificatie**: Handelt als extra laag van bevestiging en goedkeuring.
- **de nauwkeurigheid van Gegevens**: Zorgt correcte vangst van de handgeschreven input van de ondertekenaar in digitale vorm.

## Versie en compatibiliteit {#version-and-compatibility}

De adaptieve Component van de Kern van de Kern van de Ondertekening van Forms Krabbelen werd vrijgegeven in **Augustus 2025** als deel van **Componenten 2.24.6 van de Kern** voor Cloud Service en later.

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.24.6 ](/help/adaptive-forms/version.md) en later | |

Voor details op versies, zie {de Versies van de Componenten van 0} Kern [.](/help/adaptive-forms/version.md)

## Technische details {#technical-details}

Krijg de recentste technische details op de Adaptieve Component van de Kern van de Kern van de Ondertekening van Forms Krabbelen op [ GitHub ](https://github.com/adobe/aem-core-forms-components). Voor meer bij het ontwikkelen van de Componenten van de Kern, zie {de ontwikkelaarsdocumentatie van de Componenten van 0} Kern [.](/help/developing/overview.md)

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kunt u de component Scripthandtekening aanpassen.

### Tabblad Standaard {#basic-tab}

![ Basis lusje ](/help/adaptive-forms/assets/scribble-signature-basictab.png)

- **Naam** - de naam identificeert uniek de component in de regelredacteur. Speciale tekens en spaties zijn niet toegestaan in de naamtekenreeksen.

- **Titel** - de Titel is een koord dat bij de bovenkant van een component in een Aangepaste Vorm verschijnt. De titel geeft de component in de boomstructuur van een adaptief formulier op unieke wijze aan. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **staat RTF voor Titel** toe - Deze eigenschappen laat gebruikers toe om gewone teksttitels te formatteren, die eigenschappen zoals vette, cursieve, onderstreepte tekst, diverse doopvonten, doopvontgrootte, kleuren, en extra optie opnemen om visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Op het selecteren van checkbox voor **staat RTF-tekst voor Titel** toe, wordt het formatteren opties zichtbaar om de titel van de component te stileren. Om tot alle beschikbare het formatteren opties toegang te hebben, kunt u op het ![ pictogram Volledig scherm ](/help/adaptive-forms/assets/fullscreen-icon.png) tabel klikken.

  ![ de rijke tekststeun van 0&rbrace;](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel van de Huid** - selecteer deze optie om titel van het componenttype in een Aangepaste Vorm te verbergen.
- **Plaatsaanduidingstekst** - De placeholder tekst in een vormcomponent verwijst naar een kort etiket of een herinnering die binnen een inputgebied als wenk aan de gebruiker verschijnt op welk type van informatie naar verwachting op dat gebied zal zijn ingegaan. Plaatsaanduidingstekst verdwijnt wanneer de gebruiker in het veld typt en verschijnt opnieuw als het veld leeg blijft. De klasse biedt een visuele aanwijzing voor de gebruiker, maar fungeert niet als een permanent label of een permanente waarde voor het veld.

- **Bind Verwijzing** - A bindt verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u met AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

- **Teken als Niet-gebonden Element van de Vorm**: Selecteer de optie om een vormgebied te vormen niet verbonden aan om het even welk schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.

- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

- **Titel van de Dialoog van de Handtekening**: De Titel van de Dialoog van de Handtekening bepaalt de tekst die bij de bovenkant van de dialoog van de handtekeningsvangst wordt getoond. Het dient als een vraag of een instructie voor de gebruiker wanneer zij worden vereist om een handtekening te verstrekken. De tekst helpt de gebruiker door het ondertekeningsproces te begeleiden, waardoor de interactie duidelijk en intuïtief wordt.

### Tabblad Validatie

![ bevestiging tabel ](/help/adaptive-forms/assets/scribble-signature-validation.png)

- **Vereist** - selecteer deze optie, als u de component in een Aangepaste Vorm wilt tonen. Nadat u de optie hebt geselecteerd, moet u een selectie maken voordat u een formulier kunt verzenden. U kunt niet de **Component van de Verbergen** selecteren of **Component** in het **Basis** lusje onbruikbaar maken wanneer deze optie wordt geselecteerd.

- **Bericht van de Fout** - Deze optie staat u toe om een bericht in te gaan dat wordt getoond als **Vereiste** checkbox wordt gecontroleerd en het vormgebied wordt verlaten leeg.

- **Bericht van de Bevestiging van het Manuscript** - Deze optie staat u toe om een bericht in te gaan dat moet worden getoond als de manuscriptbevestiging ontbreekt.

### Het tabblad Help-inhoud {#help-content-tab}

![ Inhoud tabel van de Hulp ](/help/adaptive-forms/assets/scribble-signature-helptab.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.

- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}

![ Toegankelijkheid tabel ](/help/adaptive-forms/assets/scribble-signature-accessibilitytab.png)

- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.
   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Krabbelen handtekening te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De adaptieve Component van de Kern van de Ondertekening van Forms Krabbelen steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

![ Dialoog van het Ontwerp ](/help/adaptive-forms/assets/checkbox-style.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de Aangepaste Component van de Kern van de Handtekening van Forms verstrekken Krabbelen.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![ de Dialoog van Eigenschappen van de Douane ](/help/adaptive-forms/assets/checkbox-customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de orde van de naam van het douanebezit en de waarde van het douanebezit te herschikken.

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
