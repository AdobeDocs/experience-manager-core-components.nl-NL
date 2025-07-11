---
title: Adaptive Forms Core Component - E-mailinvoer
description: De Adaptive Forms Email input Core Component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: f6a2974b-991e-4cea-9ef8-0b03e8975eeb
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '2111'
ht-degree: 0%

---


# E-mailcomponent {#Email-input-adaptive-forms-core-component}

De Adaptive Form Email input Core Component wordt gebruikt om e-mailadressen van gebruikers te verzamelen. In het veld voor e-mailinvoer kan de browser controleren of de ingevoerde gegevens een geldige indeling voor e-mailadressen zijn. De naam wordt meestal weergegeven als een tekstvak en heeft patroonvalidaties om alleen geldige e-mailadressen te accepteren. Het veld voor e-mailinvoer kan verder worden aangepast met extra kenmerken zoals &quot;vereist&quot;, &quot;plaatsaanduiding&quot; en &quot;patroon&quot; om validaties voor de invoergegevens in te stellen.

{{traditional-aem}}

**Voorbeeld**

![ voorbeeld ](/help/adaptive-forms/assets/emailid-example.png)

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

Er zijn verschillende redenen waarom het nuttig is om een e-mailinvoercomponent op te nemen in een adaptief formulier, zoals:

- **Gebruikerservaring van de Gebruiker**: Een e-mailinput maakt het voor gebruikers gemakkelijker om hun e-mailadressen in te gaan aangezien het een duidelijke aanwijzing van de gegevens verstrekt die op het gebied worden verwacht.

- **Gepersonaliseerde Communicatie**: Het verzamelen van e-mailadressen van gebruikers door een vorm staat voor gepersonaliseerde mededeling toe, zoals het verzenden van bevestigingse-mails of nieuwsbrieven.

- **de Generatie van de Lood**: Door e-mailadressen door een vorm te verzamelen, kunnen de ondernemingen hun e-maillijst bouwen en het voor loodgeneratie gebruiken.

- **Authentificatie van de Gebruiker**: De e-mailadressen kunnen als middel van authentificatie voor de toegang tot van beperkte inhoud of de diensten worden gebruikt.

- **de Inzameling van de Terugkoppeling**: Een e-mailinput in een feedbackvorm staat de zaken toe om met de gebruiker voor follow-up of verduidelijking op hun te communiceren terugkoppelen.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Email Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 voor Cloud Service en Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM-compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/adaptive-forms/version.md) en later | Compatibel met <br>[ versie 1.1.12 ](/help/adaptive-forms/version.md) en later maar minder dan 2.0.0. |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het [&#128279;](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0&rbrace;.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Krijg de recentste informatie over de Adaptieve Component van de Invoerkern van de Forms E-mail in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/emailinput/v1/emailinput). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u uw e-mailinvoerervaring eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig opties voor e-mailinvoer definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![ Basis lusje ](/help/adaptive-forms/assets/email_basictab.png)

- **Naam** - de naam identificeert uniek de component in de regelredacteur.De speciale karakters en de ruimten worden niet toegestaan in de naamkoorden.

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

- **Standaardwaarde** - deze optie staat u toe om een standaardwaarde op een vormgebied toe te voegen. Als **Uitgeschakelde Component** of **read-only Component** wordt geselecteerd, wordt de standaardwaarde getoond op het scherm. Als er geen waarde wordt ingevoerd door de gebruiker in het formulierveld, wordt deze waarde verzonden op het moment dat het formulier wordt verzonden
- **Autofill attributen**: De optie laat gebruikers toe om een waarde in te voeren die automatisch binnen het vormgebied wordt bevolkt dat op de opgeslagen informatie wordt gebaseerd.

### Tabblad Validatie {#validation-tab}

![ het lusje van de Bevestiging ](/help/adaptive-forms/assets/email_validationtab.png)

- **Vereist** - selecteer deze optie, als u de component in een Aangepaste Vorm wilt tonen. Na het selecteren van de optie, moet u een waarde ingaan alvorens met een vorm voorlegging te werk te gaan.U kunt niet de **Component van de Verbergen** selecteren of **Component** op het **Basis** lusje onbruikbaar maken wanneer deze optie wordt geselecteerd.

- **Bericht van de Fout** - Deze optie staat u toe om een bericht in te gaan dat wordt getoond als **Vereiste** checkbox wordt gecontroleerd en het vormgebied wordt verlaten leeg.

- **Bericht van de Bevestiging van het Manuscript** - Deze optie staat u toe om een bericht in te gaan dat moet worden getoond als de manuscriptbevestiging ontbreekt.

- **Maximum Aantal karakters** - Deze optie staat u toe om het maximumaantal karakters te specificeren die op het gebied worden toegestaan. Als u karakters groter dan de waarde ingaat die in **wordt gespecificeerd Maximum Aantal karakters**, verschijnt een foutenmelding op het scherm. Het **Maximum de dialoogvakje van de karakterfout van karakters** staat u toe om een bericht van de douanefout toe te voegen.

- **Maximum de foutenmelding van karakters** - het **Maximum de dialoogvakje van de karakterfout** staat u toe om een douanefoutenmelding toe te voegen als u karakters groter dan de waarde ingaat die in het **Maximum Aantal karakters** optie wordt gespecificeerd.

- **Minimum Aantal karakters** - Deze optie staat u toe om het minimum aantal karakters te specificeren die op het gebied worden toegestaan. Als u karakters minder dan de waarde ingaat die in **wordt gespecificeerd Minimum Aantal karakters**, verschijnt een foutenmelding op het scherm. Het **Minimale de dialoogvakje van de karakterfout** staat u toe om een bericht van de douanefout toe te voegen.

- **Minimale de foutenmelding van karakters** - het **Minimale de dialoogvakje van de karakterfout** staat u toe om een douanefoutenmelding toe te voegen als u karakters minder dan de waarde ingaat die in **MinimumAantal karakters** optie wordt gespecificeerd.
<br>

De **optie van het Patroon van de Bevestiging** staat u toe om een patroon in te gaan om ingevoerde e-mailidentiteitskaart te bevestigen. In het geval dat e-mailidentiteitskaart er niet in slaagt met de waarde in **ingevoerde optie van het Patroon** te bevestigen, verschijnt het foutenbericht op het scherm.

- **Patroon** - deze optie staat u toe om de toegestane verificatiepatronen voor e-mail in te gaan. Reguliere expressies zijn ook toegestaan.
- **Bericht van de Fout** - Deze optie staat u toe om een bericht in te gaan dat op het scherm wordt getoond als e-mailidentiteitskaart met de waarde ontbreekt te bevestigen ingegaan in de **optie van het Patroon**

### Het tabblad Help-inhoud {#help-content-tab}

![ Inhoud tabel van de Hulp ](/help/adaptive-forms/assets/email_helptab.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.

- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}

![ Toegankelijkheid tabel ](/help/adaptive-forms/assets/email_accessibilitytab.png)

- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de invoercomponent E-mail te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De adaptieve Forms E-mail inputcomponent van de Kern steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

![ lusje van de Stijl ](/help/adaptive-forms/assets/datepicker_styletab.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de Adaptieve Component van de Kern van de E-mailInput van Forms verstrekken.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![ de Dialoog van Eigenschappen van de Douane ](/help/adaptive-forms/assets/datepicker_customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de orde van de naam van het douanebezit en de waarde van het douanebezit te herschikken.

### Tabblad Opmaak {#formats-tab}

Op het tabblad Indelingen kunt u standaard- en aangepaste datumnotaties opgeven.

![ Formattab ](/help/adaptive-forms/assets/emailinput_formattab.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=nl-NL)

-->

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
