---
title: Adaptive Forms Core Component - Panel container
description: Het gebruiken van of het aanpassen van de Adaptive Forms Panel containerComponent van de Kern.
role: Architect, Developer, Admin, User
exl-id: 104836fe-8325-47de-978d-1ff2d6a9dd15
source-git-commit: 4c510b8fe59f4be6e1b329ee4257ab1b780fbf22
workflow-type: tm+mt
source-wordcount: '2225'
ht-degree: 0%

---

# Deelvenstercomponent{#panel-container-adaptive-forms-core-component}

In een adaptief formulier is een deelvenster een containerelement dat kan worden gebruikt om gerelateerde formulierelementen te groeperen. Hiermee kunt u verschillende formulierelementen op een logische en zinvolle manier groeperen en ordenen. Hierdoor kunnen de algehele structuur en leesbaarheid van het formulier worden verbeterd, zodat gebruikers het formulier eenvoudiger kunnen begrijpen en navigeren.

Deelvensters kunnen ook worden gebruikt om inklapbare secties te maken. Dit kan handig zijn voor het verbergen van complexe of minder vaak gebruikte formuliervelden, zodat het formulier eenvoudig en gebruiksvriendelijk blijft. U kunt hiermee ook andere componenten opnemen, zoals tekst, selectievakjes, knoppen, enz.

U kunt er ook gebruik van maken om verschillende op regels gebaseerde handelingen in te stellen, zoals het verzenden van een formulier, het openen van een website, het tonen/verbergen van componenten of het toevoegen van een exemplaar van een deelvenster.

**Voorbeeld**

![ voorbeeld ](/help/adaptive-forms/assets/panel-container.png)

## Gebruik {#reasons-to-use-panel-container}

Er zijn verschillende redenen om een deelvenster in een formulier te gebruiken, zoals:

- **het Organiseren van vormelementen**: Een paneel kan worden gebruikt om verwante vormelementen samen te groeperen, die het voor gebruikers gemakkelijker maken om de vorm te begrijpen en te navigeren.

- **verbeterend vormstructuur**: Door vormelementen in panelen te groeperen, kan het de algemene structuur en leesbaarheid van de vorm verbeteren, die het gemakkelijker maken te begrijpen.

- **Creërend doen ineenstorten secties**: De panelen kunnen worden gebruikt om doen ineenstorten secties tot stand te brengen, die voor het verbergen van complexe of minder vaak gebruikte vormgebieden nuttig kunnen zijn, waarbij de vorm eenvoudig en gemakkelijk te gebruiken houdt.

- **Verbeterend bruikbaarheid**: Door panelen te gebruiken om vormelementen te organiseren, kan het vorm gebruikersvriendelijker en gemakkelijker maken te gebruiken, die tot hogere voltooiingstarieven kunnen leiden.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Panel Container Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | — |
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/adaptive-forms/version.md) en later | Compatibel | Compatibel |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het [&#128279;](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0&rbrace;.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Krijg de recentste informatie over de AanpassingsComponent van de Kern van de Container van het Comité van Forms in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de containerervaring van het deelvenster eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig containeropties voor deelvensters definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![ Basis lusje ](/help/adaptive-forms/assets/basic-panel.png)

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

- **Bind Verwijzing** - A bindt verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.
- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **read-only** - selecteer de optie om de component niet-editable te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tab deelvenster herhalen {#repeat-panel}

![ herhalingslusje ](/help/adaptive-forms/assets/repeat-panel.png)

Met de opties voor herhaling kunt u de container van het deelvenster en de onderliggende componenten dupliceren, een minimum- en maximumaantal herhalingen definiëren en de replicatie van vergelijkbare secties in een formulier vergemakkelijken. Wanneer u communiceert met de containercomponent van het deelvenster en de instellingen opent, worden de volgende opties weergegeven:

- **maak paneel herhaalbaar**: Een kneveleigenschap die gebruikers toestaat om de herhaalbaarheidfunctionaliteit toe te laten of onbruikbaar te maken.
- **Minimale herhalingen**: Vestigt het minimumaantal tijden de paneelcontainer kan worden herhaald. De waarde nul geeft aan dat het deelvenster Wizard niet wordt herhaald; de standaardwaarde is nul.
- **Maximale herhalingen**: Plaatst het maximumaantal tijden de paneelcontainer kan worden herhaald. Deze waarde is standaard onbeperkt.

Om herhaalbare secties binnen de paneelcontainer effectief te beheren, volg de stappen die in [ worden verstrekt die vormen met herhaalbare secties ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html) artikel creëren.

### Het tabblad Help-inhoud {#help-content}

![ Inhoud tabel van de Hulp ](/help/adaptive-forms/assets/helpcontent-panel.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.

- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility}

![ Toegankelijkheid tabel ](/help/adaptive-forms/assets/accessibilty-panel.png)


- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.
   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.

- **de rol van de HTML voor het schermlezer om** aan te kondigen - de rol van de HTML is een attribuut wordt gebruikt om het doel van een element van de HTML aan ondersteunende technologieën zoals het schermlezers te specificeren dat. Het rolattribuut wordt gebruikt om extra context en semantische betekenis aan een element te verstrekken, die het voor schermlezers gemakkelijker maken om de inhoud te interpreteren en aan de gebruiker aan te kondigen. In AEM Forms heeft het label van een formulierveld bijvoorbeeld de rol &quot;label&quot; en kan het invoerveld de rol &quot;textbox&quot; hebben. Hierdoor kan de schermlezer de relatie tussen het label en het invoerveld begrijpen en deze correct aan de gebruiker meedelen.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de deelvenstercomponent te definiëren en te beheren.

### Tabblad Toegestane componenten {#allowed-components-tab}

![ dialoog van het Ontwerp stond componentenlusje ](/help/adaptive-forms/assets/panel-container-allowed-component.png) toe

Het **Toegestane lusje van Componenten** staat malplaatjeredacteur toe om de componenten te plaatsen die als punten aan de panelen in de component in de Aangepaste redacteur van Forms kunnen worden toegevoegd.

### Tabblad Standaardcomponenten {#default-components-tab}

![ de dialoog standaardcomponentenlusje van het Ontwerp &lbrace;](/help/adaptive-forms/assets/panel-container-default-component.png)

Het **Standaardlusje van Componenten** staat de malplaatjeredacteur toe om de componenten te specificeren die door gebrek als punten in de component van de vormcontainer in de Aangepaste redacteur van Forms zichtbaar zijn.

### Tab Instellingen voor responsief {#responsive-tab}

![ de dialoog van het Ontwerp ontvankelijke montages tabel ](/help/adaptive-forms/assets/panel-container-responsive-style-tab.png)

Het **Responsieve lusje van Montages** staat de malplaatjeredacteur toe om het aantal kolommen in het net binnen de component van de vormcontainer in de Adaptieve redacteur van Forms te specificeren.

### Containerinstellingen, tabblad

![ het lusje van de Montages van de Container ](/help/adaptive-forms/assets/panel-container-container-settings.png)

- **Lay-out** - u kunt of een vaste lay-out (Eenvoudig) of een flexibele lay-out (het Responsieve Net) voor uw tovenaar hebben. De eenvoudige lay-out houdt alles vast op de plaats, terwijl het Responsieve Net u toestaat om de positie van componenten aan uw behoeften aan te passen. Gebruik bijvoorbeeld Responsief raster om &quot;Voornaam&quot;, &quot;Tweede naam&quot; en &quot;Achternaam&quot; in één rij uit te lijnen in een formulier.

- **maak Lay-out** onbruikbaar: Selecteer deze optie om lay-outselectie in uit te schakelen uitgeven dialoog van een component.

- **laat achtergrondbeeld** toe: Deze optie staat gebruiker toe om de montages van het paneel te vormen om een visuele achtergrond voor het verbeteren van het visuele beroep te omvatten.

- **laat achtergrondkleur** toe: Deze optie staat u toe om de achtergrondkleur van het paneel te plaatsen of te veranderen. Deze functie wordt doorgaans gebruikt in het ontwerp van de gebruikersinterface om de weergave van deelvensters in een grotere interface aan te passen. Wanneer u **selecteert laat achtergrondkleur** optie toe, verschijnt de **slechts optie van Monsters**. De **slechts optie van Monsters** staat u toe om kleuren voor de achtergrond, de tekst, of andere visuele elementen binnen het paneel te specificeren of te kiezen gebruikend **voeg** knoop toe

### Tabblad Stijlen {#styles-tab}

De adaptieve Component van de Kern van de Bijlage van het Dossier van Forms steunt het AEM [ Systeem van de Stijl ](/help/get-started/authoring.md#component-styling).

![ Dialoog van het Ontwerp ](/help/adaptive-forms/assets/panel-container-styles-tab.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de AanpassingsComponent van de Kern van de Container van het Comité van Forms verstrekken.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Tabblad Aangepaste eigenschappen

![ de Dialoog van Eigenschappen van de Douane ](/help/adaptive-forms/assets/panel-container-custom-properties.png)

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