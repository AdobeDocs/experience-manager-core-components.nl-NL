---
title: Aangepaste formulieraccordeon
description: Gebruik accordeon om een lange of complexe vorm te ordenen en te vereenvoudigen door deze op te splitsen in kleinere, beter te beheren gedeelten.
role: Architect, Developer, Admin, User
exl-id: 0ed38eee-fc22-4708-82eb-3fb1839b1ff2
source-git-commit: 8388de05c86641d4887b48a9fd10901cb5a19998
workflow-type: tm+mt
source-wordcount: '2174'
ht-degree: 0%

---

# Accordeoncomponent {#accordion-component-adaptive-forms-core-component}

Met de Accordion Core-component kunnen gebruikers uitbreidbare en inklapbare secties maken in een adaptief formulier. Het wordt vaak gebruikt om lange of complexe vormen te organiseren en te vereenvoudigen door hen in kleinere, handelbaardere secties op te splitsen. Elke sectie van een accordeon wordt meestal vertegenwoordigd door een koptekst, waarop de gebruiker kan klikken om de bijbehorende inhoud uit of samen te vouwen. De inhoud kan elke Core-component bevatten.

![voorbeeld](/help/adaptive-forms/assets/example-accordion.png)

## Gebruik {#usage}

Er zijn verschillende redenen waarom het nuttig is een accordeon in een adaptieve vorm op te nemen, zoals:

- **Ruimtebesparing**: Met een accordeon kunnen gebruikers delen van een formulier uit- en samenvouwen, waardoor er minder ruimte is voor de weergave van alle formuliervelden tegelijk.

- **Navigatie**: Een accordeon kan worden gebruikt om een hiërarchische navigatiestructuur te maken, zodat gebruikers gemakkelijker de formuliervelden kunnen vinden die ze nodig hebben.

- **Gebruikerservaring**: Met Accordeon kunt u het formulier gebruiksvriendelijker maken door gebruikers een duidelijke en intuïtieve manier te bieden om formuliervelden te openen en in te vullen.

- **Long Forms**: Accordeon is een ideale component voor het verwerken van lange formulieren, aangezien gebruikers zich hierdoor op één sectie tegelijk kunnen concentreren in plaats van een hoop informatie tegelijk te verwerken.

U kunt het volgende gebruiken:

- De [dialoogvenster configureren](#configure-dialog) om eigenschappen van de accordeoncomponent op te geven.

- De [Pop-upmenu van deelvenster selecteren](#select-panel-popover)  om de volgorde van de panelen van de accordeon te bepalen. Hierdoor kan de auteur de deelvensters rangschikken in de volgorde waarin de deelvensters moeten worden weergegeven.

- Opties voor de auteur van een formulier om bepaalde functies in het deelvenster [ontwerpdialoogvenster](#design-dialog). Een auteur kan er bijvoorbeeld voor kiezen om bepaalde velden of secties van een formulier uit te schakelen. Met deze opties heeft de auteur meer controle over het ontwerp en de functionaliteit van het formulier, waardoor het eenvoudiger wordt om formulieren te maken die zijn toegesneden op de specifieke behoeften van de organisatie.

Het dialoogvenster Configureren en de deelvensterpop-up en het dialoogvenster Ontwerp selecteren maken allemaal deel uit van de kerncomponenten die zijn ontworpen om het ontwerpen van de formulieren eenvoudig te maken en een efficiënte manier te bieden om complexe formulieren te maken.

## Versie en compatibiliteit {#version-and-compatibility}


De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | — |
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Ga voor de meest recente informatie over de Accordion-component naar de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de accordeonervaring voor bezoekers eenvoudig aanpassen. U kunt accordeonitems, deelvensters, gedrag en vormgeving eenvoudig definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![Het tabblad Basis](/help/adaptive-forms/assets/acc-basic.png)

- **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

- **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.

- **Gegevens van onderliggende componenten groeperen over het verzenden van formulieren (gegevens laten teruglopen in object)** - Wanneer de optie is geselecteerd, worden de gegevens van de onderliggende componenten genest in het JSON-object van de bovenliggende component. Als de optie echter niet is geselecteerd, hebben de verzonden JSON-gegevens een platte structuur, zonder object voor de bovenliggende component. Bijvoorbeeld:

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

- **Layout** - U kunt een vaste lay-out (Eenvoudig) of een flexibele lay-out (Responsief raster) voor uw wizard gebruiken. De eenvoudige lay-out houdt alles vast op de plaats, terwijl het Responsieve Net u toestaat om de positie van componenten aan uw behoeften aan te passen. Gebruik bijvoorbeeld Responsief raster om &quot;Voornaam&quot;, &quot;Tweede naam&quot; en &quot;Achternaam&quot; in één rij uit te lijnen in een formulier.

- **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

- **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

- **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Accordeon herhalen {#repeat-accordion}

![herhalen-accordeon](/help/adaptive-forms/assets/repeat-accordion.png)

Met de opties voor herhaling kunt u accordeondeelvensters en onderliggende componenten dupliceren, een minimum- en maximumaantal herhalingen definiëren en de replicatie van vergelijkbare secties in een formulier vergemakkelijken. Wanneer u communiceert met de accordeoncomponent en de instellingen opent, worden de volgende opties weergegeven:

- **Accordeon herhaalbaar maken**: Een schakelfunctie waarmee gebruikers de herhaalbaarheidsfunctionaliteit kunnen in- of uitschakelen.
- **Minimale herhalingen**: Hiermee stelt u in hoe vaak het accordeonvenster minimaal kan worden herhaald. De waarde nul geeft aan dat het accordeonvenster niet wordt herhaald; de standaardwaarde is nul.
- **Maximale herhalingen**: Hiermee stelt u in hoe vaak het accordeonvenster maximaal kan worden herhaald. Deze waarde is standaard onbeperkt.

Om herhaalbare secties binnen de accordeon effectief te beheren, voert u de stappen uit die in de [Formulieren maken met herhaalbare secties](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html) artikel.

### Tabblad Items {#items-tab}

![Tabblad Items](/help/adaptive-forms/assets/acc-items.png)

Met de knop Toevoegen kunt u een component selecteren die u als deelvenster wilt toevoegen in het selectievenster van de component. Nadat u de component hebt toegevoegd, kunt u de volgende opties zien:

- **Pictogram** - Het pictogram geeft de component van het deelvenster in de lijst aan. U kunt de muis boven het pictogram houden om de volledige componentnaam als knopinfo te zien.
- **Beschrijving** - De beschrijving die wordt gebruikt als de tekst van het deelvenster. Standaard is de naam van de component geselecteerd voor het deelvenster.
- **Verwijderen** - Tik of klik om het deelvenster uit de accordeoncomponent te verwijderen.
- **Opnieuw rangschikken** - Tik of klik en sleep om de volgorde van de deelvensters te wijzigen.

### Het tabblad Help-inhoud {#help-content}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/acc-helpcontent.png)

- **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de achtergrondafbeelding onder de component weer te geven.

- **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

- **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/acc-accessisbilty.png)

Op de **Toegankelijkheid** tab, waarden worden ingesteld voor [Toegankelijkheid ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) labels voor de component. Er zijn verschillende opties beschikbaar voor het gebruik van de tekst voor schermlezers:

- **Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.


   - **Aangepaste tekst**: Selecteer deze optie als u de aangepaste tekst voor toegankelijkheidslabels in ARIA wilt gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie als u de beschrijving voor toegankelijkheidslabels van ARIA wilt gebruiken.
   - **Titel**: Selecteer deze optie als u de titel voor toegankelijkheidslabels in ARIA wilt gebruiken.
   - **Naam**: Selecteer deze optie als u de naam voor toegankelijkheidslabels van ARIA wilt gebruiken.
   - **Geen**: Selecteer deze optie als u geen toegankelijkheidslabels voor ARIA wilt toevoegen.

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

- Het type HTML-kopelementen dat is toegestaan en ingesteld als standaard (zoals H1, H2, H3, enz.)
- De kerncomponenten die een maker van het formulier aan de accordeon kan toevoegen in de Adaptive Forms Editor
- Eenvoudige namen voor stijlen (CSS-klassen) die kunnen worden toegepast in het dialoogvenster met eigenschappen van de accordeoncomponent in de Adaptieve Forms-editor.

Hierdoor wordt het maken en aanpassen van formulieren eenvoudiger en efficiënter.

### Tabblad Eigenschappen {#properties-tab-design}

Op het tabblad Eigenschappen kunnen sjabloonauteurs de standaardelementen en toegestane HTML-kopelementen voor formulierauteurs instellen:

![Dialoogvenster Ontwerp, tabblad](/help//adaptive-forms/assets/accordion-design-properties.png)

- **Toegestane kopelementen**: Een vervolgkeuzelijst met meerdere opties waarmee de sjabloonauteur kan kiezen welke koppen de auteur van het formulier voor accordeon kan gebruiken.

- **Standaardkopelement**: In een vervolgkeuzelijst wordt het standaardelement Kop voor de accordeoncomponent ingesteld.

### Tabblad Toegestane componenten {#allowed-components-tab}

![Dialoogvenster Toegestaan component, tabblad](/help//adaptive-forms/assets/accordion-allowed-components.png)

De **Toegestane componenten** kunt u in de sjablooneditor de componenten instellen die als items kunnen worden toegevoegd aan de deelvensters in de component Accordeon in de Adaptieve Forms-editor.

### Tabblad Stijlen {#styles-tab}

![Tabblad Stijl ontwerpdialoogvenster](/help/adaptive-forms/assets/accordion-styles-tab.png)

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Accordion Core-component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

- **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de accordeoncomponent.

- **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![accordion-custom-properties-tab](/help/adaptive-forms/assets/accordion-custom-properties-tab.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Groepsnaam**: U kunt een naam opgeven om de groep met aangepaste eigenschappen te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **Belangrijke paren**: U kunt meerdere aangepaste eigenschapnamen en aangepaste eigenschapswaarden toevoegen door op de knop **Toevoegen** knop voor elke aangepaste groep eigenschappen.

   - **Verwijderen**: Tik of klik om de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te verwijderen.

   - **Opnieuw rangschikken**: Tik of klik en sleep om de volgorde van de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te wijzigen.

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}