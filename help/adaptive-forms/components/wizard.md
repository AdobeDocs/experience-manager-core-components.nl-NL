---
title: Adaptive Forms Core Component - Wizard
description: De Adaptive Forms Wizard Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: fd785cd2-5ed6-4efb-997f-ce9056ed113d
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '2186'
ht-degree: 0%

---


# Wizard, component{#wizard-adaptive-forms-core-component}

Een wizardindeling in een adaptief formulier verwijst naar een formulier dat is verdeeld in meerdere stappen of pagina&#39;s, waarbij de gebruiker stap voor stap door het formulier beweegt. Deze indeling wordt een &quot;wizard&quot; genoemd omdat deze de gebruiker in een stapsgewijs proces door het formulier begeleidt.

Elke stap van de wizard bevat doorgaans een groep gerelateerde formuliervelden en een navigatiemechanisme, zoals de knoppen Volgende en Vorige, waarmee u tussen de stappen kunt navigeren. De gebruiker kan pas verdergaan naar de volgende stap nadat de huidige stap is voltooid en alle vereiste velden zijn ingevuld.

De indeling van de wizard is handig voor formulieren met veel velden of gegevens die moeten worden verzameld, omdat het formulier dan wordt opgedeeld in kleinere, beter te beheren blokken. Hiermee kunnen gebruikers zich ook op één set velden tegelijk concentreren, waardoor het invullen van het formulier minder overweldigend wordt.

Het kan echter ook de complexiteit van het formulier vergroten, omdat de gebruiker meerdere pagina&#39;s moet doorlopen om het formulier in te vullen. Het is dus noodzakelijk om de formuliervereisten en gebruikersbehoeften te evalueren voordat u besluit een wizardindeling te gebruiken.
Met de Core-component voor de wizardlay-out kunt u in een adaptief formulier de wizardlay-out maken.

{{traditional-aem}}

**Voorbeeld**

![&#x200B; voorbeeld &#x200B;](/help/adaptive-forms/assets/wizard.png)

## Gebruik {#reasons-to-use-wizard-in-an-adaptive-form}

Er zijn verscheidene redenen waarom het nuttig kan zijn om een lay-out van de Tovenaar in een AanpassingsVorm te gebruiken:

- **Eenvoud**: Het onderbreken van een vorm in veelvoudige stappen kan het voor gebruikers gemakkelijker maken om te begrijpen en te voltooien, aangezien zij zich op één reeks gebieden tegelijk kunnen concentreren.

- **Organisatie**: Een lay-out van de Tovenaar kan helpen om vormen door onderwerp of doel te organiseren, en het kan verwante gebieden ook groeperen samen, die het vorm-vullend proces kunnen logisch en efficiënt maken.

- **Bevestiging**: Een lay-out van de Tovenaar staat voor geleidelijke bevestiging toe, die gebruikers kunnen helpen fouten identificeren en verbeteren aangezien zij gaan, eerder dan het wachten tot het eind van de vorm.

- **Indicator van de Voortgang**: Een tovenaar lay-out kan de vooruitgang van de vorm tonen, die de gebruiker kan helpen begrijpen hoeveel van de vorm wordt verlaten om te voltooien.

- **Lange vormen**: Als de vorm veel gebieden heeft, kan het voor de gebruiker overweldigend zijn om hen allen in één keer te zien, zodat het breken van hen in kleinere, handelbaardere brokken het minder intimiderend kan maken.

- **het Vermijden van Afschaffing**: Een tovenaar lay-out kan ook helpen om vormvervreemding te verminderen, aangezien de gebruikers waarschijnlijker een vorm kunnen voltooien als zij vooruitgang kunnen zien en begrijpen hoeveel wordt verlaten te doen.

- **Mobiele Ervaring**: Een tovenaar lay-out kan ook voor vormen nuttig zijn die op mobiele apparaten worden betreden, aangezien het voor kleinere pagina&#39;s toestaat die sneller laden en gemakkelijker zijn te navigeren.

Over het algemeen kan een wizardindeling het invullen van formulieren overzichtelijker en efficiënter maken voor gebruikers, maar het is belangrijk om rekening te houden met de complexiteit van het formulier en de behoeften van de gebruiker voordat u besluit om dit type indeling te gebruiken.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Wizard Layout Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4. Hier volgt een tabel met alle ondersteunde versies, AEM-compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | — |
| v1 | Compatibel systeem met <br>[&#x200B; versie 2.0.4 &#x200B;](/help/adaptive-forms/version.md) en later | Compatibel | Compatibel |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het [&#128279;](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0&rbrace;.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Krijg de recentste informatie over de AanpassingsComponent van de Kern van de Tovenaar van Forms in de technische documentatie op [&#x200B; GitHub &#x200B;](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/wizard/v1/wizard). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [&#x200B; de ontwikkelaarsdocumentatie van de Componenten van de Kern &#x200B;](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de tovenaarservaring eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig wizardopties definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![&#x200B; Basis lusje &#x200B;](/help/adaptive-forms/assets/wizard-basic.png)

- **Naam** - u kunt een vormcomponent gemakkelijk met zijn unieke naam zowel in de vorm als in de regelredacteur identificeren, maar de naam moet geen ruimten of speciale karakters bevatten.

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bovenop de component.

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

<!--   **Wrap data in an object** - Choose "Wrap data in an object" to put the field data from the Wizard inside a JSON object. If not chosen, the submit data JSON has a flat structure for the Wizard's fields.

-   **Layout** - You can have either a fixed layout (Simple) or a flexible layout (Responsive Grid) for your wizard. The Simple layout keeps everything fixed in the place, while the Responsive Grid allows you to adjust the position of components to suit your needs. For example, use Responsive Grid to align "First Name", "Middle Name" and "Last Name" in a form in a single row.  -->

- **Bind verwijzing** - A bindt verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u met AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

- **read-only** - selecteer de optie om de component niet-editable te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tabblad Wizard Herhalen {#repeat-wizard-tab}

![&#x200B; herhalen tovenaar &#x200B;](/help/adaptive-forms/assets/wizard-repeat.png)

Met de opties voor herhaling kunt u de wizard en de onderliggende componenten dupliceren, een minimum- en maximumaantal herhalingen definiëren en de replicatie van vergelijkbare secties in een formulier vergemakkelijken. Wanneer het in wisselwerking staan met de component van de Tovenaar en de toegang tot van zijn montages, worden de volgende opties voorgesteld:

- **maak Tovenaar herhaalbaar**: Een kneveleigenschap die gebruikers toestaat om de herhaalbaarheidfunctionaliteit toe te laten of onbruikbaar te maken.
- **Minimale herhalingen**: Vestigt het minimumaantal tijden het paneel van de Tovenaar kan worden herhaald. De waarde nul geeft aan dat het deelvenster Wizard niet wordt herhaald; de standaardwaarde is nul.
- **Maximale herhalingen**: Plaatst het maximumaantal tijden het paneel van de Tovenaar kan worden herhaald. Deze waarde is standaard onbeperkt.

Om herhaalbare secties binnen de Tovenaar effectief te beheren, volg de stappen die in [&#x200B; worden verstrekt die vormen met herhaalbare secties &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=nl-NL) artikel creëren.

### Tabblad Items {#items-tab}

![&#x200B; Punten tabel &#x200B;](/help/adaptive-forms/assets/wizard_itemstab.png)

Met deze optie kunt u componenten Adaptief formulier toevoegen door op de knop Toevoegen te klikken. Deze knop wordt standaard weergegeven wanneer de wizard wordt toegevoegd in de bewerkingsmodus.

### Help, tabblad {#help-tab}

![&#x200B; Hulp tabel &#x200B;](/help/adaptive-forms/assets/wizard_helptab.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.

- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.


### Tabblad Toegankelijkheid {#accessibility}

![&#x200B; Toegankelijkheid tabel &#x200B;](/help/adaptive-forms/assets/wizard_accessibiltytab.png)

- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.
   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.

- **rol van HTML voor het schermlezer om** aan te kondigen - de rol van HTML is een attribuut dat wordt gebruikt om het doel van een element van HTML aan ondersteunende technologieën zoals het schermlezers te specificeren. Het rolattribuut wordt gebruikt om extra context en semantische betekenis aan een element te verstrekken, die het voor schermlezers gemakkelijker maken om de inhoud te interpreteren en aan de gebruiker aan te kondigen. In AEM Forms heeft het label van een formulierveld bijvoorbeeld de rol &quot;label&quot; en kan het invoerveld de rol &quot;textbox&quot; hebben. Hierdoor kan de schermlezer de relatie tussen het label en het invoerveld begrijpen en deze correct aan de gebruiker meedelen.


## Ontwerpdialoogvenster {#design-dialog}

De dialoog van het Ontwerp laat malplaatjemakers controleren hoe de dingen door gebrek worden getoond. Voor de component Adaptive Forms Wizard kunt u het volgende instellen:

- De kerncomponenten die een maker van het formulier aan de wizard kan toevoegen in de Adaptive Forms-editor
- Eenvoudige namen voor stijlen (CSS-klassen) die kunnen worden toegepast in het dialoogvenster met eigenschappen van de component Wizard in de Adaptive Forms-editor.

Hierdoor wordt het maken en aanpassen van formulieren eenvoudiger en efficiënter.

### Tabblad Toegestane componenten {#allowed-components-tab}

![&#x200B; Toegestane Componenten tabel &#x200B;](/help/adaptive-forms/assets/tabs-allowed-component.png)

Het **Toegestane lusje van Componenten** staat malplaatjeredacteur toe om de componenten te plaatsen die als punten aan de panelen in de tovenaarscomponent in de Aangepaste redacteur van Forms kunnen worden toegevoegd.

### Tabblad Stijlen {#styles-tab}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De adaptieve component van de de tovenaarKern van Forms steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

![&#x200B; het lusje van Stijlen &#x200B;](/help/adaptive-forms/assets/tabs-styles-tab.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de Adaptieve Component van de TovenaarKern van Forms verstrekken.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Tabblad Aangepaste eigenschappen

![&#x200B; Eigenschappen tabel van de Douane &#x200B;](/help/adaptive-forms/assets/tabs-custom-properties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de orde van de naam van het douanebezit en de waarde van het douanebezit te herschikken.

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}