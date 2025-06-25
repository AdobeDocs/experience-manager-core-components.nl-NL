---
title: Adaptieve Forms Core-component - Bestandsbijlage
description: De Adaptive Forms-component voor bestandsbijlagen gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: 64a54fc6-db52-481f-bf5a-60c05122004d
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '2061'
ht-degree: 0%

---


# Bestandsbijlage-component {#file-attachment-adaptive-forms-core-component}

<span class="preview"> Het **type van Gegevens van voorgelegde waarde** eigenschap is beschikbaar onder vroege adopterprogramma. U kunt vanaf uw officiële e-mailadres naar aem-forms-ea@adobe.com schrijven om deel te nemen aan het programma voor vroege adoptie en toegang tot de functie te vragen. </span>

Met een bestandsbijlage in een adaptief formulier kunnen gebruikers bestanden selecteren en uploaden vanaf hun lokale computer of apparaat. De component Bestandsbijlage kan zo worden geconfigureerd dat specifieke bestandstypen, grootten en meerdere bijlagen mogelijk zijn.

{{traditional-aem}}

**Voorbeeld**

![ voorbeeld ](/help/adaptive-forms/assets/upload-image.png)


## Gebruik {#reasons-to-use-file-attachment}

Er zijn verschillende redenen waarom het nuttig is om een component voor bestandsbijlagen op te nemen in een adaptieve vorm, zoals:

- **het Verzamelen van extra informatie**: Een component van de dossiergehechtheid staat gebruikers toe om documenten, beelden, video&#39;s, of andere soorten dossiers als deel van de vormvoorlegging te uploaden. Dit kan nuttig zijn om extra informatie zoals hervatting, portefeuilles, of ondersteunende documentatie te verzamelen.

- **Gemakkelijk delen van grote dossiers**: De component van de gehechtheid van het dossier laat gebruikers toe om grote dossiers gemakkelijk te delen, zonder het moeten op de externe dossier-delende diensten vertrouwen.

- **Handigheid**: De component van de gehechtheid van het dossier staat gebruikers toe om dossiers van hun lokale computer te uploaden, zonder het moeten vanaf de vorm navigeren of andere hulpmiddelen gebruiken.

- **analyse van Gegevens**: De component van de gehechtheid van het dossier kan worden gebruikt om gegevens uit diverse bronnen te verzamelen en het te analyseren, of het als input voor verdere verwerking te gebruiken.

- **Ervaring van de Gebruiker**: De component van de gehechtheid van het dossier kan worden gebruikt om de vorm gebruikersvriendelijker te maken door een duidelijke en intuïtieve manier voor gebruikers te verstrekken om dossiers te uploaden.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms-bestandsbijlage Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 voor Cloud Service en Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM-compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/adaptive-forms/version.md) en later | Compatibel met <br>[ versie 1.1.12 ](/help/adaptive-forms/version.md) en later maar minder dan 2.0.0. |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het ](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0}.[

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Krijg de recentste informatie over de AanpassingsComponent van de Kern van de Bijlage van het Dossier van Forms in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fileinput/v1/fileinput). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de ervaring met bestandsbijlagen eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig opties voor bestandsbijlagen definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![ Basis lusje ](/help/adaptive-forms/assets/fileattachement_basictab1.png)

- **Naam** - u kunt een vormcomponent gemakkelijk met zijn unieke naam zowel in de vorm als in de regelredacteur identificeren, maar de naam moet geen ruimten of speciale karakters bevatten.

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bovenop de component. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **staat RTF voor Titel** toe - Deze eigenschappen laat gebruikers toe om gewone teksttitels te formatteren, die eigenschappen zoals vette, cursieve, onderstreepte tekst, diverse doopvonten, doopvontgrootte, kleuren, en extra optie opnemen om visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Op het selecteren van checkbox voor **staat RTF-tekst voor Titel** toe, wordt het formatteren opties zichtbaar om de titel van de component te stileren. Om tot alle beschikbare het formatteren opties toegang te hebben, kunt u op het ![ pictogram Volledig scherm ](/help/adaptive-forms/assets/fullscreen-icon.png) tabel klikken.

  ](/help/adaptive-forms/assets/richtext-support-title.png) de rijke tekststeun van 0}![

- **Verberg Titel** - selecteer de optie om de Titel van de component te verbergen.

- **titel van de Knoop** - Deze optie wordt gebruikt om het etiket van de knoop te plaatsen die op een AanpassingsVorm wordt getoond.
- **Bind Verwijzing** - A bindt verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.
- **Teken als Niet-gebonden Element van de Vorm**: Selecteer de optie om een vormgebied te vormen niet verbonden aan om het even welk schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.
- **Type van Gegevens van voorgelegde waarde**: Selecteer de optie om te bepalen hoe het in bijlage dossier aan de server wordt voorgelegd. Als u de bijlage als binaire gegevens wilt verzenden, kiest u de optie `File` . Als u de bijlage wilt verzenden als een tekenreeks met Base64-codering, kiest u de optie `String` . Als `String` wordt geselecteerd, wordt het dossier in het binaire formaat voorgelegd aan de server als gegevens URL. De server zet de gegevens-URL automatisch om in binaire indeling, zodat deze compatibel is met bestaande acties, zoals het verzenden van e-mails en het genereren van het document met records, zonder dat gebruikers wijzigingen moeten aanbrengen. Standaard is de optie `File` geselecteerd.
- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **read-only** - selecteer de optie om de component niet-editable te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **staat veelvoudige gehechtheid** toe - selecteer deze optie om veelvoudige gehechtheid te uploaden gebruikend de **knoop van de Bijlage van het Dossier**.
- **de Tekst van de Daling van de Belemmering** - het is de tekst die bij de bovenkant van de **wordt getoond** knoop vastmaken om gebruikers ertoe aan te zetten om of dossiers vast te maken of te slepen en te laten vallen. U hebt de optie om de tekst aan te passen die bij de bovenkant van de **wordt getoond** knoop van de Band. Daarnaast kunt u de tekst opmaken met het menu Rich Text.

### Tabblad Validatie {#validation-tab}

![ het lusje van de Bevestiging ](/help/adaptive-forms/assets/fileattachment_validationtab.png)

- **Vereist** - selecteer deze optie, als u de component in een Aangepaste Vorm wilt tonen. Nadat u de optie hebt geselecteerd, moet u bijlagen toevoegen voordat u verdergaat met het verzenden van een formulier. U kunt niet de **Component van de Verbergen** selecteren of **Component** in het **Basis** lusje onbruikbaar maken wanneer deze optie wordt geselecteerd.
- **Bericht van de Fout** - Deze optie staat u toe om een bericht in te gaan dat wordt getoond als **Vereiste** checkbox wordt gecontroleerd en het gebied wordt verlaten leeg.

- **Bericht van de Bevestiging van het Manuscript** - Deze optie staat u toe om een bericht in te gaan dat moet worden getoond als de manuscriptbevestiging ontbreekt.

<!--   **Minimum files error message** - This option is used to enter an error message that is displayed if you upload files lesser than the specified minimum number of files.-->

- **Maximale dossiergrootte (MB)** - deze optie staat toe om een maximumdossiergrootte te specificeren. Bestandsgrootten worden opgegeven in MB.
  <!--   **Maximum files error message** - This option is used to enter an error message that is displayed if you upload files greater than the specified maximum number of files.-->

- **Maximum de foutenmelding van de dossiergrootte** - Deze optie wordt gebruikt om een foutenmelding in te gaan die wordt getoond als u dossiers van grootte meer dan de dossiergrootte uploadt die in **wordt gespecificeerd Maximale dossiergrootte (MB)** optie.

- **Toegestane dossiertypes** - Verschillende types van dossiers die kunnen worden geupload gebruikend de **knoop van de Bijlage van het Dossier** wordt toegevoegd hier. Het staat ook toe om een nieuw dossierformaat toe te voegen door **te klikken voegt** knoop toe. Ondersteunde bestandsindelingen zijn: audio, video, afbeelding, tekst of PDF. U kunt toegestane bestandstypen ook verwijderen of opnieuw rangschikken met:
   - **Schrapping** - Tik of klik om specifieke dossiertypes te verwijderen.
   - **herschikt** - Tik of klik en sleep om de orde van toegestane dossiertypes te herschikken.

  Als u een bestand verzendt door het type te wijzigen in een indeling met toegestane bestandstypen, treedt er een fout op tijdens het verzenden van het formulier.
- **het type van Dossier foutenmelding** - Deze optie staat u toe om een foutenmelding in te gaan die wordt getoond wanneer u de dossierformaten buiten die vermeld in **toegelaten dossiertypes** optie uploadt.

### Het tabblad Help-inhoud {#help-content-tab}

![ Inhoud tabel van de Hulp ](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.

- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}


![ Toegankelijkheid tabel ](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Bestandsbijlage te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

De adaptieve Component van de Kern van de Bijlage van het Dossier van Forms steunt het systeem van de Stijl van AEM [ ](/help/get-started/authoring.md#component-styling).

![ Dialoog van het Ontwerp ](/help/adaptive-forms/assets/checkbox-style.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de AanpassingsComponent van de Kern van de Bijlage van het Dossier van Forms verstrekken.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![ de Dialoog van Eigenschappen van de Douane ](/help/adaptive-forms/assets/checkbox-customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de orde van de naam van het douanebezit en de waarde van het douanebezit te herschikken.
<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
