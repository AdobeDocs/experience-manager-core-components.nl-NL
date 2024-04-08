---
title: Adaptive Forms Core Component - Panel container
description: Het gebruiken van of het aanpassen van de Adaptive Forms Panel containerComponent van de Kern.
role: Architect, Developer, Admin, User
exl-id: 104836fe-8325-47de-978d-1ff2d6a9dd15
source-git-commit: f1fce5f661bc7581f7c6c6905f34e9954d1d4f70
workflow-type: tm+mt
source-wordcount: '2052'
ht-degree: 0%

---

# Deelvenstercontainer {#panel-container-adaptive-forms-core-component}

In een adaptief formulier is een deelvenster een containerelement dat kan worden gebruikt om gerelateerde formulierelementen te groeperen. Hiermee kunt u verschillende formulierelementen op een logische en zinvolle manier groeperen en ordenen. Hierdoor kunnen de algehele structuur en leesbaarheid van het formulier worden verbeterd, zodat gebruikers het formulier eenvoudiger kunnen begrijpen en navigeren.

Deelvensters kunnen ook worden gebruikt om inklapbare secties te maken. Dit kan handig zijn voor het verbergen van complexe of minder vaak gebruikte formuliervelden, zodat het formulier eenvoudig en gebruiksvriendelijk blijft. U kunt hiermee ook andere componenten opnemen, zoals tekst, selectievakjes, knoppen, enz.

U kunt er ook gebruik van maken om verschillende op regels gebaseerde handelingen in te stellen, zoals het verzenden van een formulier, het openen van een website, het tonen/verbergen van componenten of het toevoegen van een exemplaar van een deelvenster.

**Voorbeeld**

![voorbeeld](/help/adaptive-forms/assets/panel-container.png)

## Gebruik {#reasons-to-use-panel-container}

Er zijn verschillende redenen om een deelvenster in een formulier te gebruiken, zoals:

- **Formulierelementen ordenen**: Met een deelvenster kunt u gerelateerde formulierelementen groeperen, zodat gebruikers het formulier eenvoudiger kunnen begrijpen en navigeren.

- **Formulierstructuur verbeteren**: Door formulierelementen in deelvensters te groeperen, kunt u de algehele structuur en leesbaarheid van het formulier verbeteren, zodat u het formulier eenvoudiger kunt begrijpen.

- **Inklapbare secties maken**: Met deelvensters kunt u inklapbare secties maken. Dit kan handig zijn voor het verbergen van complexe of minder vaak gebruikte formuliervelden, zodat het formulier eenvoudig en gebruiksvriendelijk blijft.

- **Verbeterde bruikbaarheid**: Door deelvensters te gebruiken om formulierelementen te ordenen, kunt u het formulier gebruiksvriendelijker en gebruiksvriendelijker maken. Dit kan leiden tot hogere voltooiingssnelheden.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Panel Container Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | — |
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Lees de meest recente informatie over de Adaptive Forms Panel Container Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/panelcontainer/v1/panelcontainer). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de containerervaring van het deelvenster eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig containeropties voor deelvensters definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![Het tabblad Basis](/help/adaptive-forms/assets/basic-panel.png)

- **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
<!-- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png) -->

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

- **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.
- **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
- **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tab deelvenster herhalen {#repeat-panel}

![herhalingstag](/help/adaptive-forms/assets/repeat-panel.png)

Met de opties voor herhaling kunt u de container van het deelvenster en de onderliggende componenten dupliceren, een minimum- en maximumaantal herhalingen definiëren en de replicatie van vergelijkbare secties in een formulier vergemakkelijken. Wanneer u communiceert met de containercomponent van het deelvenster en de instellingen opent, worden de volgende opties weergegeven:

- **Deelvenster herhaalbaar maken**: Een schakelfunctie waarmee gebruikers de herhaalbaarheidsfunctionaliteit kunnen in- of uitschakelen.
- **Minimale herhalingen**: Hiermee stelt u in hoe vaak de container van het deelvenster minimaal kan worden herhaald. De waarde nul geeft aan dat het deelvenster Wizard niet wordt herhaald; de standaardwaarde is nul.
- **Maximale herhalingen**: Hiermee stelt u in hoe vaak de container van het deelvenster kan worden herhaald. Deze waarde is standaard onbeperkt.

Voer de stappen uit in het dialoogvenster [Formulieren maken met herhaalbare secties](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html) artikel.

### Het tabblad Help-inhoud {#help-content}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/helpcontent-panel.png)


- **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de achtergrondafbeelding onder de component weer te geven.

- **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

- **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/accessibilty-panel.png)


- **Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

- **HTML-rol voor schermlezer om aan te kondigen** - De rol HTML is een kenmerk dat wordt gebruikt om het doel van een element HTML aan ondersteunende hulpmiddelen, zoals schermlezers, op te geven. Het rolattribuut wordt gebruikt om extra context en semantische betekenis aan een element te verstrekken, die het voor schermlezers gemakkelijker maken om de inhoud te interpreteren en aan de gebruiker aan te kondigen. In AEM Forms heeft het label van een formulierveld bijvoorbeeld de rol &quot;label&quot; en kan het invoerveld de rol &quot;textbox&quot; hebben. Hierdoor kan de schermlezer de relatie tussen het label en het invoerveld begrijpen en deze correct aan de gebruiker meedelen.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Form Container te definiëren en te beheren.

### Tabblad Toegestane componenten {#allowed-components-tab}

![Dialoogvenster Toegestaan component, tabblad](/help/adaptive-forms/assets/panel-container-allowed-component.png)

De **Toegestane componenten** kunt u in de sjablooneditor de componenten instellen die als items kunnen worden toegevoegd aan de deelvensters in de component in de Adaptieve Forms-editor.

### Tabblad Standaardcomponenten {#default-components-tab}

![Standaardtabblad van dialoogvenster Ontwerp](/help/adaptive-forms/assets/panel-container-default-component.png)

De **Standaardcomponenten** kunt u in de sjablooneditor opgeven welke componenten standaard zichtbaar zijn als items in de formuliercontainercomponent in de Adaptive Forms-editor.

### Tab Instellingen voor responsief {#responsive-tab}

![Instellingen tabblad van dialoogvenster Ontwerpen](/help/adaptive-forms/assets/panel-container-responsive-style-tab.png)

De **Instellingen voor responsie** kunt u in de sjablooneditor het aantal kolommen in het raster opgeven dat zich in de formuliercontainercomponent van de Adaptieve Forms-editor bevindt.

### Containerinstellingen, tabblad

![Containerinstellingen, tabblad](/help/adaptive-forms/assets/panel-container-container-settings.png)

- **Layout** - U kunt een vaste lay-out (Eenvoudig) of een flexibele lay-out (Responsief raster) voor uw wizard gebruiken. De eenvoudige lay-out houdt alles vast op de plaats, terwijl het Responsieve Net u toestaat om de positie van componenten aan uw behoeften aan te passen. Gebruik bijvoorbeeld Responsief raster om &quot;Voornaam&quot;, &quot;Tweede naam&quot; en &quot;Achternaam&quot; in één rij uit te lijnen in een formulier.

- **Lay-out uitschakelen**: Selecteer deze optie om de lay-outselectie uit te schakelen in het dialoogvenster Bewerken van een component.

- **Achtergrondafbeelding inschakelen**: Met deze optie kan de gebruiker de instellingen van het deelvenster zodanig configureren dat een visuele achtergrond wordt opgenomen om het visuele aspect te verbeteren.

- **Achtergrondkleur inschakelen**: Met deze optie kunt u de achtergrondkleur van het deelvenster instellen of wijzigen. Deze functie wordt doorgaans gebruikt in het ontwerp van de gebruikersinterface om de weergave van deelvensters in een grotere interface aan te passen. Wanneer u **Achtergrondkleur inschakelen** de **Alleen stalen** wordt weergegeven. De **Alleen stalen** kunt u kleuren voor de achtergrond, tekst of andere visuele elementen in het deelvenster opgeven of kiezen met behulp van het **Toevoegen** knop

### Tabblad Stijlen {#styles-tab}

De Adaptive Forms File Attachment Core-component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Ontwerpdialoogvenster](/help/adaptive-forms/assets/panel-container-styles-tab.png)

- **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Panel Container Core Component.

- **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Tabblad Aangepaste eigenschappen

![Dialoogvenster Aangepaste eigenschappen](/help/adaptive-forms/assets/panel-container-custom-properties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Groepsnaam**: U kunt een naam opgeven om de groep met aangepaste eigenschappen te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **Belangrijke paren**: U kunt meerdere aangepaste eigenschapnamen en aangepaste eigenschapswaarden toevoegen door op de knop **Toevoegen** knop voor elke aangepaste groep eigenschappen.

   - **Verwijderen**: Tik of klik om de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te verwijderen.

   - **Opnieuw rangschikken**: Tik of klik en sleep om de volgorde van de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te wijzigen.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}