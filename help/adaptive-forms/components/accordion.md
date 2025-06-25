---
title: Aangepaste formulieraccordeon
description: Gebruik accordeon om een lange of complexe vorm te ordenen en te vereenvoudigen door deze op te splitsen in kleinere, beter te beheren gedeelten.
role: Architect, Developer, Admin, User
exl-id: 0ed38eee-fc22-4708-82eb-3fb1839b1ff2
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '2237'
ht-degree: 0%

---


# Accordion-component {#accordion-component-adaptive-forms-core-component}

Met de Accordion Core-component kunnen gebruikers uitbreidbare en inklapbare secties maken in een adaptief formulier. Het wordt vaak gebruikt om lange of complexe vormen te organiseren en te vereenvoudigen door hen in kleinere, handelbaardere secties op te splitsen. Elke sectie van een accordeon wordt meestal vertegenwoordigd door een koptekst, waarop de gebruiker kan klikken om de bijbehorende inhoud uit of samen te vouwen. De inhoud kan elke Core-component bevatten.

![ voorbeeld ](/help/adaptive-forms/assets/example-accordion.png)

{{traditional-aem}}

## Gebruik {#usage}

Er zijn verschillende redenen waarom het nuttig is een accordeon in een adaptieve vorm op te nemen, zoals:

- **ruimtebesparing**: Een accordeon staat gebruikers toe om secties van een vorm uit te breiden en samen te vouwen, die de hoeveelheid ruimte verminderen nodig om alle vormgebieden in één keer te tonen.

- **Navigatie**: Een accordeon kan worden gebruikt om een hiërarchische navigatiestructuur tot stand te brengen, die het voor gebruikers gemakkelijker maken om de vormgebieden te vinden zij nodig hebben.

- **Ervaring van de Gebruiker**: De accordeon kan worden gebruikt om de vorm gebruikersvriendelijker te maken door een duidelijke en intuïtieve manier voor gebruikers te verstrekken om tot vormgebieden toegang te hebben en in te vullen.

- **Lange Forms**: De Accordeon is een ideale component om lange vormen te behandelen, aangezien het gebruikers toestaat om zich op één sectie tegelijkertijd te concentreren, eerder dan het proberen om veel informatie allen in één keer te verwerken.

U kunt het volgende gebruiken:

- [ vormt dialoog ](#configure-dialog) om eigenschappen van de accordeoncomponent te specificeren.

- [ Uitgezochte paneel popover ](#select-panel-popover) om de orde van de panelen van de accordeon te bepalen. Hierdoor kan de auteur de deelvensters rangschikken in de volgorde waarin de deelvensters moeten worden weergegeven.

- Opties voor een vormauteur om bepaalde eigenschappen in de [ ontwerpdialoog ](#design-dialog) toe te laten of onbruikbaar te maken. Een auteur kan er bijvoorbeeld voor kiezen om bepaalde velden of secties van een formulier uit te schakelen. Met deze opties heeft de auteur meer controle over het ontwerp en de functionaliteit van het formulier, waardoor het eenvoudiger wordt om formulieren te maken die zijn toegesneden op de specifieke behoeften van de organisatie.

Het dialoogvenster Configureren en de deelvensterpop-up en het dialoogvenster Ontwerp selecteren maken allemaal deel uit van de kerncomponenten die zijn ontworpen om het ontwerpen van de formulieren eenvoudig te maken en een efficiënte manier te bieden om complexe formulieren te maken.

## Versie en compatibiliteit {#version-and-compatibility}


De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4. Hier volgt een tabel met alle ondersteunde versies, AEM-compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | — |
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/adaptive-forms/version.md) en later | Compatibel | Compatibel |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het [&#128279;](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0&rbrace;.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Krijg de recentste informatie over de Component van de Accordeon in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de accordeonervaring voor bezoekers eenvoudig aanpassen. U kunt accordeonitems, deelvensters, gedrag en vormgeving eenvoudig definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![ Basis lusje ](/help/adaptive-forms/assets/acc-basic.png)

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

<!--  **Layout** - You can have either a fixed layout (Simple) or a flexible layout (Responsive Grid) for your wizard. The Simple layout keeps everything fixed in the place, while the Responsive Grid allows you to adjust the position of components to suit your needs. For example, use Responsive Grid to align "First Name", "Middle Name" and "Last Name" in a form in a single row. -->

- **Bind Verwijzing** - A bindt verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

- **read-only** - selecteer de optie om de component niet-editable te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Accordeon herhalen {#repeat-accordion}

![ herhalen-accordeon ](/help/adaptive-forms/assets/repeat-accordion.png)

Met de opties voor herhaling kunt u accordeondeelvensters en onderliggende componenten dupliceren, een minimum- en maximumaantal herhalingen definiëren en de replicatie van vergelijkbare secties in een formulier vergemakkelijken. Wanneer u communiceert met de accordeoncomponent en de instellingen opent, worden de volgende opties weergegeven:

- **maak accordeon herhaalbaar**: Een kneveleigenschap die gebruikers toestaat om de herhaalbaarheidfunctionaliteit toe te laten of onbruikbaar te maken.
- **Minimale herhalingen**: Vestigt het minimumaantal tijden het accordeonpaneel kan worden herhaald. De waarde nul geeft aan dat het accordeonvenster niet wordt herhaald; de standaardwaarde is nul.
- **Maximale herhalingen**: Plaatst het maximumaantal tijden het accordeonpaneel kan worden herhaald. Deze waarde is standaard onbeperkt.

Om herhaalbare secties binnen de accordeon effectief te beheren, volg de stappen die in [ worden verstrekt die vormen met herhaalbare secties ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html) artikel creëren.

### Tabblad Items {#items-tab}

![ Punten tabel ](/help/adaptive-forms/assets/acc-items.png)

Met de knop Toevoegen kunt u een component selecteren die u als deelvenster wilt toevoegen in het selectievenster van de component. Nadat u de component hebt toegevoegd, kunt u de volgende opties zien:

- **Pictogram** - het pictogram identificeert de component van het paneel in de lijst. U kunt de muis boven het pictogram houden om de volledige componentnaam als knopinfo te zien.
- **Beschrijving** - de beschrijving die als tekst van het paneel wordt gebruikt. Standaard is de naam van de component geselecteerd voor het deelvenster.
- **Schrapping** - Tik of klik om het paneel van de accordeoncomponent te schrappen.
- **herschikt** - Tik of klik en sleep om de orde van de panelen te herschikken.

### Het tabblad Help-inhoud {#help-content}

![ Inhoud tabel van de Hulp ](/help/adaptive-forms/assets/acc-helpcontent.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.

- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility}

![ Toegankelijkheid tabel ](/help/adaptive-forms/assets/acc-accessisbilty.png)

Op het **lusje van de Toegankelijkheid**, worden de waarden geplaatst voor [ toegankelijkheid ARIA ](https://www.w3.org/WAI/standards-guidelines/aria/) etiketten voor de component. Er zijn verschillende opties beschikbaar voor het gebruik van de tekst voor schermlezers:

- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.

<!--

### Properties Tab {#properties-tab}

![Properties tab of the edit dialog of the Accordion Component](/help/assets/accordion-edit-properties.png)

*   **Single item expansion** - When selected, this option forces a single accordion item to be expanded at a time. Expanding one item will then collapse all others.
*   **Expanded items** - This option defines the items that are expanded by default when the page is loaded.
    * When **Single item expansion** is selected, one panel must be selected. By default the first panel is selected.
    * When **Single item expansion** is not selected, this option is a multi-select and is optional.
*   **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
    * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
    * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
    * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Select Panel Popover {#select-panel-popover}

The **Select Panel** option (![Select panel icon](/help/assets/select-panel-icon.png)) on the component toolbar enables content authors to modify the panels in an accordion with ease. By selecting this option, the author can switch to a different panel for editing and rearrange the order of the panels in the accordion. The configured panels will be displayed in a drop-down menu for the author to choose from. This feature optimizes the editing process and makes it user-friendly for content authors.

![Select panel popover](/help/assets/select-panel-popover.png)


* The panels are displayed in a numbered list, reflecting the assigned arrangement.
* Each panel is listed with its component type in bold, followed by a brief description in lighter font.
* By clicking or tapping on a panel in the drop-down, you can easily switch the view in the editor to that specific panel.
* To rearrange the panels, simply use the drag handles to move them into the desired order. -->

## Ontwerpdialoogvenster {#design-dialog}

De dialoog van het Ontwerp laat malplaatjemakers controleren hoe de dingen door gebrek worden getoond. Voor de Adaptieve Forms Accordion-component kunt u het volgende instellen:

- Het type HTML-kopelementen dat is toegestaan en als standaard is ingesteld (zoals H1, H2, H3, enz.)
- De kerncomponenten die een maker van het formulier aan de accordeon kan toevoegen in de Adaptive Forms Editor
- Eenvoudige namen voor stijlen (CSS-klassen) die kunnen worden toegepast in het dialoogvenster met eigenschappen van de accordeoncomponent in de Adaptieve Forms-editor.

Hierdoor wordt het maken en aanpassen van formulieren eenvoudiger en efficiënter.

### Tabblad Eigenschappen {#properties-tab-design}

Op het tabblad Eigenschappen kunnen sjabloonauteurs de standaardelementen en toegestane HTML-kopelementen voor formulierauteurs instellen:

![ de dialoogeigenschappen tabel van het Ontwerp ](/help//adaptive-forms/assets/accordion-design-properties.png)

- **Toegestane Elementen van de Kop**: Een drop-down lijst met veelvoudige opties die de malplaatjeauteur laat kiezen welke rubrieken auteur voor accordeon kunnen gebruiken.

- **Standaard het Element van de Kop**: Een drop-down lijst plaatst het standaardelement van de Kop voor accordeoncomponent.

### Tabblad Toegestane componenten {#allowed-components-tab}

![ dialoog van het Ontwerp stond componentenlusje ](/help//adaptive-forms/assets/accordion-allowed-components.png) toe

Het **Toegestane lusje van Componenten** staat malplaatjeredacteur toe om de componenten te plaatsen die als punten aan de panelen in de component van de Accordeon in de Aangepaste redacteur van Forms kunnen worden toegevoegd.

### Tabblad Stijlen {#styles-tab}

![ lusje van de de dialoogvakje van het Ontwerp ](/help/adaptive-forms/assets/accordion-styles-tab.png)

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De adaptieve Component van de Kern van de Accordion van Forms steunt het systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de accordeoncomponent verstrekken.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![ accordeon-douane-eigenschappen-lusje ](/help/adaptive-forms/assets/accordion-custom-properties-tab.png)
Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de orde van de naam van het douanebezit en de waarde van het douanebezit te herschikken.

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}