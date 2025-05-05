---
title: Adaptive Forms Core Component - Horizontale tabbladen
description: De Adaptive Forms Horizontal tabs Core Component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: fbdf330b-3b85-4f94-9dab-eea8465fba67
source-git-commit: 4c510b8fe59f4be6e1b329ee4257ab1b780fbf22
workflow-type: tm+mt
source-wordcount: '2153'
ht-degree: 0%

---

# Component Horizontale tabbladen (tabs bovenaan){#horizontal-tabs-adaptive-forms-core-component}

Horizontale tabbladen in een adaptief formulier verwijzen naar een ontwerppatroon waarbij meerdere secties van een formulier zijn gegroepeerd en worden weergegeven als afzonderlijke tabbladen, die horizontaal zijn uitgelijnd. De gebruiker kan schakelen tussen de tabbladen om toegang te krijgen tot verschillende secties van het formulier. Elk tabblad fungeert als trigger voor het weergeven en verbergen van de gerelateerde formulierinhoud. Met de horizontale tabbladen kunt u lange formulieren ordenen in hanteerbare gedeelten en de gebruikerservaring verbeteren. Tabs kunnen ertoe bijdragen dat een formulier toegankelijker wordt voor gebruikers met een handicap, aangezien ze met behulp van toetsenbordnavigatie tussen secties kunnen schakelen.

De tabbladen worden meestal gemaakt als een reeks koppelingen of knoppen, waarbij elke koppeling of knop overeenkomt met een sectie van het formulier. Wanneer een gebruiker op een tabblad klikt, wordt de formulierinhoud dynamisch bijgewerkt om de bijbehorende sectie weer te geven.

![ voorbeeld ](/help/adaptive-forms/assets/horizontal-example-new.png)

## Gebruik {#reasons-to-use-horizontal-tabs}

De algemene redenen voor het gebruik van horizontale tabbladen in een adaptieve vorm zijn:

- **Verbeterde Bruikbaarheid**: De horizontale lusjes maken het voor gebruikers gemakkelijker om door de vorm te navigeren, vooral als de vorm veelvoudige secties of een groot aantal gebieden heeft.

- **Ruimtebeheer**: De horizontale lusjes helpen het schermruimte te besparen door verwante vormsecties in lusjes te groeperen en slechts één sectie tegelijkertijd te tonen.

- **Betere Organisatie**: De lusjes verstrekken een duidelijke en georganiseerde structuur voor een vorm, die het voor gebruikers gemakkelijker maken om de vorm te begrijpen en te voltooien.

- **Verhoogde Betrokkenheid van de Gebruiker**: De horizontale lusjes kunnen een vorm visueel aantrekkelijker maken voor gebruikers, die het tarief van de vormvoltooiing kunnen verbeteren.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Horizontal tabs Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | — |
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/adaptive-forms/version.md) en later | Compatibel | Compatibel |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het [&#128279;](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0&rbrace;.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Horizontal-tabs  Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_Horizontal-tabs ). -->


## Technische details {#technical-details}

Krijg de recentste informatie over de Adaptieve Horizontale Component van de Kern van de Lusjes van Forms Horizontal in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageHorizontaltabs/v1/pageHorizontaltabs). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de ervaring van horizontale tabbladen eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig opties voor horizontale tabbladen definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![ Basis lusje ](/help/adaptive-forms/assets/tabs-on-top-basic.png)

- **Naam** - u kunt een vormcomponent gemakkelijk met zijn unieke naam zowel in de vorm als in de regelredacteur identificeren, maar de naam moet geen ruimten of speciale karakters bevatten.

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bovenop de component. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **staat RTF voor Titel** toe - Deze eigenschappen laat gebruikers toe om gewone teksttitels te formatteren, die eigenschappen zoals vette, cursieve, onderstreepte tekst, diverse doopvonten, doopvontgrootte, kleuren, en extra optie opnemen om visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Op het selecteren van checkbox voor **staat RTF-tekst voor Titel** toe, wordt het formatteren opties zichtbaar om de titel van de component te stileren. Om tot alle beschikbare het formatteren opties toegang te hebben, kunt u op het ![ pictogram Volledig scherm ](/help/adaptive-forms/assets/fullscreen-icon.png) tabel klikken.

  ![&#128279;](/help/adaptive-forms/assets/richtext-support-title.png) de rijke tekststeun van 0&rbrace;

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

<!-- **Layout** - You can have either a fixed layout (Simple) or a flexible layout (Responsive Grid) for your wizard. The Simple layout keeps everything fixed in the place, while the Responsive Grid allows you to adjust the position of components to suit your needs. For example, use Responsive Grid to align "First Name", "Middle Name" and "Last Name" in a form in a single row. -->

- **Bind Verwijzing** - A bindt verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u met AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.
- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **read-only** - selecteer de optie om de component niet-editable te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tabs boven herhalen {#repeat-tabs-on-top}

![ Toegankelijkheid tabel ](/help/adaptive-forms/assets/repeat-tabsontop.png)

Met de opties voor herhaling kunt u de component Horizontal-tabs en de onderliggende componenten dupliceren, een minimum- en maximumaantal herhalingen definiëren en de replicatie van vergelijkbare secties in een formulier vergemakkelijken. Wanneer u met de component Horizontal-tabs communiceert en de instellingen opent, worden de volgende opties weergegeven:

- **maak lusjes op bovenkant herhaalbaar**: Een kneveleigenschap die gebruikers toestaat om de herhaalbaarheidfunctionaliteit toe te laten of onbruikbaar te maken.
- **Minimale herhalingen**: Vestigt het minimumaantal tijden de horizontaal-luscomponent kan worden herhaald. De waarde nul geeft aan dat de component Horizontal-tabs niet wordt herhaald; de standaardwaarde is nul.
- **Maximale herhalingen**: Plaatst het maximumaantal tijden de horizontaal-tabs component kan worden herhaald. Deze waarde is standaard onbeperkt.
Om herhaalbare secties binnen horizontaal-lusjes effectief te beheren, volg de stappen die in [ worden verstrekt die vormen met herhaalbare secties ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=nl-NL) artikel creëren.

### Tabblad Items {#items-tab}

![ Punten tabel ](/help/adaptive-forms/assets/items-tabs-on-top.png)

**voegt** knoop toe staat u toe om een component te selecteren om als paneel van het venster van de componentenselectie toe te voegen. Nadat u de component hebt toegevoegd, kunt u de volgende opties zien:

- **Pictogram** - het pictogram identificeert de component van het paneel in de lijst. U kunt de muis boven het pictogram houden om de volledige componentnaam als knopinfo te zien.
- **Beschrijving** - de beschrijving die als tekst van het paneel wordt gebruikt. Standaard wordt de naam van de component geselecteerd voor het deelvenster.
- **Schrapping** - Tik of klik om het paneel van de horizontaal-tabs component te schrappen.
- **herschikt** - Tik of klik en sleep om de orde van de panelen te herschikken.

### Het tabblad Help-inhoud {#help-content}

![ Inhoud tabel van de Hulp ](/help/adaptive-forms/assets/helpcontent-tabs-on-top.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.
- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility}

![ Toegankelijkheid tabel ](/help/adaptive-forms/assets/accessibilty-tabs-on-top.png)

- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.
   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.

- **de rol van de HTML voor het schermlezer om** aan te kondigen - de rol van de HTML is een attribuut wordt gebruikt om het doel van een element van de HTML aan ondersteunende technologieën zoals het schermlezers te specificeren dat. Het rolattribuut wordt gebruikt om extra context en semantische betekenis aan een element te verstrekken, die het voor schermlezers gemakkelijker maken om de inhoud te interpreteren en aan de gebruiker aan te kondigen. In AEM Forms heeft het label van een formulierveld bijvoorbeeld de rol &quot;label&quot; en kan het invoerveld de rol &quot;textbox&quot; hebben. Hierdoor kan de schermlezer de relatie tussen het label en het invoerveld begrijpen en deze correct aan de gebruiker meedelen.

## Ontwerpdialoogvenster {#design-dialog}

De dialoog van het Ontwerp laat malplaatjemakers controleren hoe de dingen door gebrek worden getoond. Voor de Adaptive Forms Horizontal tabs kunt u het volgende instellen:

- De kerncomponenten die een maker van een formulier kan toevoegen aan de tabbladen Horizontaal in de Adaptieve Forms-editor
- Eenvoudige namen voor stijlen (CSS-klassen) die kunnen worden toegepast in het dialoogvenster Eigenschappen van de component Horizontale tabbladen in de Adaptieve Forms-editor.

Hierdoor wordt het maken en aanpassen van formulieren eenvoudiger en efficiënter.

### Tabblad Toegestane componenten {#allowed-components-tab}

![ Toegestane Componenten tabel ](/help/adaptive-forms/assets/tabs-allowed-component.png)

Het **Toegestane lusje van Componenten** staat malplaatjeredacteur toe om de componenten te plaatsen die als punten aan de panelen in de Horizontale lussencomponent in de Aanpassingsredacteur van Forms kunnen worden toegevoegd.

### Tabblad Stijlen {#styles-tab}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De adaptieve Horizontale component van de Lijst van de Kern van Forms steunt het AEM [ Systeem van de Stijl ](/help/get-started/authoring.md#component-styling).

![ het lusje van Stijlen ](/help/adaptive-forms/assets/tabs-styles-tab.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de Aangepaste Horizontale Component van de Lijst van de Kern van Forms verstrekken Horizontale.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Tabblad Aangepaste eigenschappen

![ Eigenschappen tabel van de Douane ](/help/adaptive-forms/assets/tabs-custom-properties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de orde van de naam van het douanebezit en de waarde van het douanebezit te herschikken.

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}