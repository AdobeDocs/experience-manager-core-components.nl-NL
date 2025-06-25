---
title: Adaptive Forms Core Component - Telefooninvoer, Telefoon
description: De Adaptive Forms Telephone Input Core Component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: d06179ac-04bd-4af4-b6ac-c4c78086058c
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '2197'
ht-degree: 0%

---


# Phone-component{#telephone-input-adaptive-forms-core-component}

Met de Adaptive Form Phone Core-component kunnen gebruikers een telefoonnummer invoeren. In het veld voor telefooninvoer worden toetsenborden weergegeven op mobiele apparaten die relevant zijn voor telefoonnummers. Deze kan worden aangepast met extra kenmerken, zoals &quot;patroon&quot; en &quot;plaatsaanduiding&quot;, om de notatie en beschrijving van het telefoonnummer op te geven.

Het veld voor telefooninvoer wordt vaak gebruikt in contactformulieren, registratieformulieren en andere formulieren, waarbij een telefoonnummer als contactmiddel vereist is. Het veld voor telefooninvoer kan ook worden gebruikt om ervoor te zorgen dat de gebruiker een geldig telefoonnummer invoert, omdat de browser bepaalde beperkingen kan opleggen, zoals de lengte en de indeling van het telefoonnummer, op basis van het kenmerk &quot;pattern&quot;.

![ voorbeeld ](/help/adaptive-forms/assets/emailid-example.png)

{{traditional-aem}}

## Gebruik {#reasons-to-use-telephone-input}

De algemene redenen om een veld voor telefooninvoer te gebruiken in een adaptief formulier zijn:

- **Informatie van het Contact**: Een gebied van de telefooninput wordt algemeen gebruikt om het telefoonnummer van een gebruiker als middel van contact te verzamelen.

- **Verbeterde Nauwkeurigheid van Gegevens**: Door een gebied van de telefooninput te gebruiken, kan de vorm bepaalde beperkingen op het formaat van het telefoonaantal afdwingen, dat kan helpen ervoor zorgen dat de ingevoerde gegevens nauwkeurig en volledig zijn.

- **Betere Ervaring van de Gebruiker**: Een gebied van de telefooninput verstrekt een duidelijke en intuïtieve manier voor gebruikers om hun telefoonnummer in te voeren, en kan de gebruikerservaring verbeteren door gebruikers toe te staan om hun contactinformatie snel en gemakkelijk in te gaan.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Phone Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 voor Cloud Service en Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM-compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/adaptive-forms/version.md) en later | Compatibel met <br>[ versie 1.1.12 ](/help/adaptive-forms/version.md) en later maar minder dan 2.0.0. |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het [&#128279;](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0&rbrace;.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Krijg de recentste informatie over de AanpassingsComponent van de Kern van de Telefoon van Forms in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/telephoneinput/v1/telephoneinput). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u uw telefonische invoerervaring eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig opties voor telefooninvoer definiëren voor een naadloze gebruikerservaring.

### Het tabblad Basis

![ BasisLusje ](/help/adaptive-forms/assets/telephoneinput_basictab.png)

- **Naam** - u kunt een vormcomponent gemakkelijk met zijn unieke naam zowel in de vorm als in de regelredacteur identificeren, maar de naam moet geen ruimten of speciale karakters bevatten.

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bovenop de component. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **staat RTF voor Titel** toe - Deze eigenschappen laat gebruikers toe om gewone teksttitels te formatteren, die eigenschappen zoals vette, cursieve, onderstreepte tekst, diverse doopvonten, doopvontgrootte, kleuren, en extra optie opnemen om visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Op het selecteren van checkbox voor **staat RTF-tekst voor Titel** toe, wordt het formatteren opties zichtbaar om de titel van de component te stileren. Om tot alle beschikbare het formatteren opties toegang te hebben, kunt u op het ![ pictogram Volledig scherm ](/help/adaptive-forms/assets/fullscreen-icon.png) tabel klikken.

  ![&#128279;](/help/adaptive-forms/assets/richtext-support-title.png) de rijke tekststeun van 0&rbrace;

- **Verberg Titel** - selecteer de optie om de Titel van de component te verbergen.
- **Plaatsaanduidingstekst** - De placeholder tekst in een vormcomponent verwijst naar een kort etiket of een herinnering die binnen een inputgebied als wenk aan de gebruiker verschijnt op welk type van informatie naar verwachting op dat gebied zal zijn ingegaan. Plaatsaanduidingstekst verdwijnt wanneer de gebruiker in het veld typt en verschijnt opnieuw als het veld leeg blijft. De klasse biedt een visuele aanwijzing voor de gebruiker, maar fungeert niet als een permanent label of een permanente waarde voor het veld.

- **Bind Verwijzing** - A bindt verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.
- **Teken als Niet-gebonden Element van de Vorm**: Selecteer de optie om een vormgebied te vormen niet verbonden aan om het even welk schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.

- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

- **read-only** - selecteer de optie om de component niet-editable te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

- **Standaardwaarde** - deze optie staat u toe om een standaardwaarde op een vormgebied toe te voegen. Als **Uitgeschakelde Component** of **read-only Component** wordt geselecteerd, wordt de standaardwaarde getoond op het scherm. Als geen waarde wordt ingevoerd door de gebruiker in het formulierveld, wordt deze waarde verzonden op het moment dat het formulier wordt verzonden.

- **Autofill attributen**: De optie laat gebruikers toe om een waarde in te voeren die automatisch binnen het vormgebied wordt bevolkt dat op de opgeslagen informatie wordt gebaseerd.

### Tabblad Validatie {#validation-tab}

![ het lusje van de Bevestiging ](/help/adaptive-forms/assets/telephoneinput_validationtab.png)

- **Vereist** - selecteer deze optie, als u de component in een Aangepaste Vorm wilt tonen. Nadat u de optie hebt geselecteerd, moet u een waarde invoeren voordat u verdergaat met het verzenden van een formulier. U kunt niet de **Component van de Verbergen** selecteren of **Component** in het **Basis** lusje onbruikbaar maken wanneer deze optie wordt geselecteerd.

- **Bericht van de Fout** - Deze optie staat u toe om een bericht in te gaan dat wordt getoond als **Vereiste** checkbox wordt gecontroleerd en het gebied wordt verlaten leeg.

- **Bericht van de Bevestiging van het Manuscript** - Deze optie staat u toe om een bericht in te gaan dat moet worden getoond als de manuscriptbevestiging ontbreekt.

- **Maximum Aantal karakters** - deze optie staat u toe om het maximumaantal karakters te specificeren die in de component worden toegestaan. Als u karakters groter dan de waarde ingaat die in **wordt gespecificeerd Maximum Aantal karakters**, verschijnt een foutenmelding op het scherm. Het **Maximum de dialoogvakje van de karakterfout van karakters** staat u toe om een bericht van de douanefout toe te voegen.

- **Maximum de foutenmelding van karakters** - het **Maximum de dialoogvakje van de karakterfout** staat u toe om een douanefoutenmelding toe te voegen als u karakters groter dan de waarde ingaat die in het **Maximum Aantal karakters** optie wordt gespecificeerd.

- **Minimum Aantal karakters** - Deze optie staat u toe om het minimum aantal karakters te specificeren die op het gebied worden toegestaan. Als u karakters minder dan de waarde ingaat die in **wordt gespecificeerd Minimum Aantal karakters**, verschijnt een foutenmelding op het scherm. Het **Minimale de dialoogvakje van de karakterfout** staat u toe om een bericht van de douanefout toe te voegen.

- **Minimale de foutenmelding van karakters** - het **Minimale de dialoogvakje van de karakterfout** staat u toe om een douanefoutenmelding toe te voegen als u karakters minder dan de waarde ingaat die in **MinimumAantal karakters** optie wordt gespecificeerd.

De **optie van het Patroon van de Bevestiging** staat u toe om een patroon in te gaan om het ingegaan telefoonaantal te bevestigen. Het ingegaan telefoonaantal wordt bevestigd tegen de waarde ingegaan in de **optie van het Patroon**. In het geval dat het telefoonaantal er niet in slaagt met de waarde te bevestigen ingegaan in **optie van het Patroon**, verschijnt het foutenbericht op het scherm.

- **Patroon** - Deze optie staat u toe om de toegestane verificatiepatronen voor telefoonaantal in te gaan. Reguliere expressies zijn ook toegestaan.

- **Bericht van de Fout** - Deze optie staat u toe om een bericht in te gaan dat op het scherm wordt getoond als het ingegaan telefoonaantal met de waarde niet valideert ingegaan in de **optie van het Patroon**

### Het tabblad Help-inhoud {#help-content-tab}

![ Inhoud tabel van de Hulp ](/help/adaptive-forms/assets/telephoneinput_helptab.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.
- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}

![ Toegankelijkheid tabel ](/help/adaptive-forms/assets/telephoneinput_accessibilitytab.png)

- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.
   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.

## Ontwerpdialoogvenster {#design-dialog}

Het Dialoogvenster van het ontwerp wordt gebruikt om CSS stijlen voor de telefooncomponent te bepalen en te beheren.

### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De adaptieve Component van de Kern van de Telefoon van Forms steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

![ Dialoog van het Ontwerp ](/help/adaptive-forms/assets/telephoneinput_designdialog.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de Aangepaste Component van de Kern van de Telefoon van Forms verstrekken.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![ de Dialoog van Eigenschappen van de Douane ](/help/adaptive-forms/assets/telephoneinput-customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de orde van de naam van het douanebezit en de waarde van het douanebezit te herschikken.

### Tabblad Opmaak {#format-tab}

Op het tabblad Indelingen kunt u de standaardindelingen en de aangepaste getalnotaties opgeven.

![ het Lusje van het Formaat ](/help/adaptive-forms/assets/telephoneinput_format.png)

### Tabblad Validatiepatronen {#validation-patterns-tab}

Op het tabblad Validatiepatroon kunt u waarden invoeren in een specifieke notatie of aan bepaalde criteria voldoen. Sommige opties zijn standaard beschikbaar, die u kunt selecteren door het bijbehorende selectievakje in te schakelen. Bovendien, kunt u een aangepast formaat toevoegen door **te klikken voeg** knoop toe.

![ ValidationTab ](/help/adaptive-forms/assets/telephoneinput-validationpatterns.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->


## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}