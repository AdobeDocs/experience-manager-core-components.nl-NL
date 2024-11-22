---
title: Adaptive Forms Core Component - Vervolgkeuzelijst
description: De Adaptive Forms Drop-down Core Component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: 9d59d0d2-d38f-4ed5-8b43-984c45f26f27
source-git-commit: 732efc9ed450aa31078ecaad65c0c306679fe97e
workflow-type: tm+mt
source-wordcount: '2188'
ht-degree: 0%

---

# Onderdeel vervolgkeuzelijst{#drop-down-list-adaptive-forms-core-component}

Met een vervolgkeuzelijst in een adaptief formulier kunnen gebruikers een of meer opties selecteren in een lijst met vooraf gedefinieerde opties. De opties kunnen van het type String, Number of Boolean zijn. Bovendien, kan de drop-down lijstcomponent worden gevormd om verschillende bevestiging en standaardwaarden te hebben.

**Voorbeeld**
![ voorbeeld ](/help/adaptive-forms/assets/drop-down-list.png)

## Gebruik {#reasons-to-use-drop-down-list}

Er zijn verschillende redenen waarom het nuttig is om een vervolgkeuzelijst op te nemen in een adaptief formulier, zoals:

- **Lange lijst van opties**: De drop-down lijsten zijn nuttig voor situaties waar er een lange lijst van opties voor een gebied beschikbaar is. Ze nemen minder ruimte in het formulier in beslag dan een lijst met keuzerondjes of selectievakjes. De gebruikers hebben dit minder nodig.

- **Consistentie**: De drop-down lijsten verstrekken consistentie in het ontwerp en de lay-out van de vorm, makend het intuïtiever en voor gebruikers gemakkelijk om te navigeren.

- **Duidelijkheid**: De drop-down lijsten kunnen de vorm duidelijker en gemakkelijk maken te begrijpen door een duidelijke en beknopte lijst van opties te verstrekken.

- **Ervaring van de Gebruiker**: De drop-down lijsten kunnen worden gebruikt om de vorm gebruikersvriendelijker te maken door een duidelijke en intuïtieve manier voor gebruikers te verstrekken om opties te selecteren.

- **analyse van Gegevens**: De drop-down lijsten kunnen worden gebruikt om gegevens uit diverse bronnen te verzamelen en het te analyseren, of het als input voor verdere verwerking te gebruiken.

**de Dialoog van Eigenschappen**

![ eigenschappen dialoog ](/help/adaptive-forms/assets/drop-down-list-properties.png)

In dit voorbeeld wordt het element Opties gebruikt om de lijstitems te definiëren. Het **tekstelement van de Vertoning** wordt gebruikt om een etiket voor lijstpunten te verstrekken en **Waarde van Gegevens** wordt gebruikt om de waarde te specificeren die wordt verzonden naar de server wanneer de vorm wordt voorgelegd.

Elke vervolgkeuzelijst heeft een unieke waarde voor Gegevens en een uniek kenmerk voor Tekst weergeven. Als een gebruiker de optie &quot;Rood&quot; selecteert, wordt de bijbehorende waarde van Gegevens verzonden naar de server wanneer het formulier wordt verzonden. Deze gegevens kunnen vervolgens worden verwerkt door een serverscript om te bepalen welke opties door de gebruiker zijn geselecteerd en kunnen worden gebruikt om verschillende handelingen uit te voeren, zoals het bijwerken van andere velden in het formulier of het verzenden van de formuliergegevens naar een serverscript voor verdere verwerking.

Bovendien, kan de drop-down lijst worden gevormd om verschillende verwerkingswaarden voor elke optie te hebben, en dit kan worden geplaatst door de Adaptieve Redacteur van de Regel van Forms te gebruiken.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms vervolgkeuzelijst Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/adaptive-forms/version.md) en later | Compatibel met <br>[ versie 1.1.12 ](/help/adaptive-forms/version.md) en later maar minder dan 2.0.0. |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het ](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0}.[

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Krijg de recentste informatie over de AanpassingsForms drop-down component van de LijstKern in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/dropdown/v1/dropdown). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u uw ervaring in de vervolgkeuzelijst eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig opties voor vervolgkeuzelijsten definiëren voor een naadloze gebruikerservaring.

### Het tabblad Basis

![ Basis lusje ](/help/adaptive-forms/assets/dropdown_basictab.png)

- **Naam** - u kunt een vormcomponent gemakkelijk met zijn unieke naam zowel in de vorm als in de regelredacteur identificeren, maar de naam moet geen ruimten of speciale karakters bevatten.

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bovenop de component. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **staat RTF voor Titel** toe - Deze eigenschappen laat gebruikers toe om gewone teksttitels te formatteren, die eigenschappen zoals vette, cursieve, onderstreepte tekst, diverse doopvonten, doopvontgrootte, kleuren, en extra optie opnemen om visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Op het selecteren van checkbox voor **staat RTF-tekst voor Titel** toe, wordt het formatteren opties zichtbaar om de titel van de component te stileren. Om tot alle beschikbare het formatteren opties toegang te hebben, kunt u op het ![ pictogram Volledig scherm ](/help/adaptive-forms/assets/fullscreen-icon.png) tabel klikken.

  ](/help/adaptive-forms/assets/richtext-support-title.png) de rijke tekststeun van 0}![

- **Verberg Titel** - selecteer de optie om de Titel van de component te verbergen.

- **staat veelvoudige selectie** toe - selecteer deze optie om veelvoudige opties van een drop-down lijst te selecteren.
- **sparen waarde als** - deze optie specificeert het gegevenstype van de verzonden waarde wanneer om het even welke optie wordt geselecteerd. Als **sparen waarde als** aan `Number` wordt geplaatst en u koordgegevens aan **Waarde van Gegevens** &#x200B; &#x200B; op het **lusje van Opties** toevoegt, toont het scherm a `Value type mismatch` foutenmelding.

  In het **lusje van Opties**, kunt u gegevenswaarden en vertoningstekstparen toevoegen gebruikend **toevoegen** knoop. Nadat een nieuwe optie is toegevoegd, worden de volgende handelingen uitgevoerd:

   - **Waarde van Gegevens** - deze optie staat toe om de inhoud in te gaan om voor te leggen wanneer een optie wordt geselecteerd.
   - **Tekst van de Vertoning** - Deze optie staat toe om de inhoud in te gaan om in een AanpassingsVorm te tonen.
   - **Schrapping** - Tik of klik om de optie van een drop-down menu te schrappen.
   - **herschikt** - Tik of klik en sleep om de orde voor optie van een drop-down menu te herschikken.

- **Standaard optie** - deze optie staat u toe om standaardwaarden toe te voegen. Gebruik het verwijderpictogram om de toegevoegde optie te verwijderen. Als **sparen waarde als** aan `Number` wordt geplaatst en u koordgegevens aan **Standaardopties** toevoegt, toont het scherm een `Value type mismatch` foutenmelding.

- **Plaatsaanduidingstekst** - De placeholder tekst in een vormcomponent verwijst naar een kort etiket of een herinnering die binnen een inputgebied als wenk aan de gebruiker verschijnt op welk type van informatie naar verwachting op dat gebied zal zijn ingegaan. Plaatsaanduidingstekst verdwijnt wanneer de gebruiker in het veld typt en verschijnt opnieuw als het veld leeg blijft. De klasse biedt een visuele aanwijzing voor de gebruiker, maar fungeert niet als een permanent label of een permanente waarde voor het veld.

- **Opties** - u kunt gegevenswaarden en vertoningstekstparen toevoegen gebruikend **toevoegen** knoop.  Nadat een nieuwe optie is toegevoegd, kunnen de volgende acties worden uitgevoerd:
   - **Waarde van Gegevens** - deze optie staat toe om de inhoud in te gaan om voor te leggen wanneer een optie wordt geselecteerd.
   - **Tekst van de Vertoning** - Deze optie staat toe om de inhoud in te gaan om in een AanpassingsVorm te tonen.
   - **Schrapping** - Tik of klik om de optie van checkbox te schrappen.
   - **herschikt** - Tik of klik en sleep om de orde van de panelen te herschikken.

- **Bind Verwijzing** - A bindt verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.
- **Teken als Niet-gebonden Element van de Vorm**: Selecteer de optie om een vormgebied te vormen niet verbonden aan om het even welk schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.

- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **read-only** - selecteer de optie om de component niet-editable te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tabblad Validatie {#validation-tab}

![ het lusje van de Bevestiging ](/help/adaptive-forms/assets/dropdown_validationtab.png)

- **Vereist** - selecteer deze optie, als u de component in een Aangepaste Vorm wilt tonen. Nadat u de optie hebt geselecteerd, moet u een selectie maken voordat u een formulier kunt verzenden. U kunt niet de **Component van de Verbergen** selecteren of **Component** in het **Basis** lusje onbruikbaar maken wanneer deze optie wordt geselecteerd.

- **Bericht van de Fout** - Deze optie staat u toe om een bericht in te gaan dat wordt getoond als **Vereiste** checkbox wordt gecontroleerd en het vormgebied wordt verlaten leeg.

- **Bericht van de Bevestiging van het Manuscript** - Deze optie staat u toe om een bericht in te gaan dat moet worden getoond als de manuscriptbevestiging ontbreekt.

### Het tabblad Help-inhoud {#help-content-tab}

![ Inhoud tabel van de Hulp ](/help/adaptive-forms/assets/dropdown_helptab.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.

- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}

![ Toegankelijkheid tabel ](/help/adaptive-forms/assets/dropdown_accessibilitytab.png)


- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de vervolgkeuzelijstcomponent te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De adaptieve Forms drop-down component van de LijstKern steunt het AEM [ Systeem van de Stijl ](/help/get-started/authoring.md#component-styling).

![ Dialoog van het Ontwerp ](/help/adaptive-forms/assets/checkbox-style.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de Aangepaste Forms drop-down Component van de Kern verstrekken.

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
