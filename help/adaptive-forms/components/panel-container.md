---
title: Adaptive Forms Core Component - Panel container
description: Het gebruiken van of het aanpassen van de Adaptive Forms Panel containerComponent van de Kern.
role: Architect, Developer, Admin, User
source-git-commit: 9a80b453d6a6cf7b347128654d3b5e673a063505
workflow-type: tm+mt
source-wordcount: '1503'
ht-degree: 0%

---

# Deelvenstercontainer {#panel-container-adaptive-forms-core-component}

In een adaptief formulier is een deelvenster een containerelement dat kan worden gebruikt om gerelateerde formulierelementen te groeperen. Hiermee kunt u verschillende formulierelementen op een logische en zinvolle manier groeperen en ordenen. Hierdoor kunnen de algehele structuur en leesbaarheid van het formulier worden verbeterd, zodat gebruikers het formulier eenvoudiger kunnen begrijpen en navigeren.

Deelvensters kunnen ook worden gebruikt om inklapbare secties te maken. Dit kan handig zijn voor het verbergen van complexe of minder vaak gebruikte formuliervelden, zodat het formulier eenvoudig en gebruiksvriendelijk blijft. U kunt hiermee ook andere componenten opnemen, zoals tekst, selectievakjes, knoppen, enz.

U kunt er ook gebruik van maken om verschillende op regels gebaseerde handelingen in te stellen, zoals het verzenden van een formulier, het openen van een website, het tonen/verbergen van componenten of het toevoegen van een exemplaar van een deelvenster.

**Voorbeeld**

![](/help/adaptive-forms/assets/panel-container.png)

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
| — | --- |
| v1 | Compatibel met<br>[versie 2.0.4](/help/versions.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/versions.md) document.

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

### Tab deelvenster herhalen {#repeat-panel}

![herhalingstag](/help/adaptive-forms/assets/repeat-panel.png)

Met de opties voor herhaling kunt u de container van het deelvenster en de onderliggende componenten dupliceren, een minimum- en maximumaantal herhalingen definiëren en de replicatie van vergelijkbare secties in een formulier vergemakkelijken. Wanneer u communiceert met de containercomponent van het deelvenster en de instellingen opent, worden de volgende opties weergegeven:

- **Wizard herhaalbaar maken**: Een schakelfunctie waarmee gebruikers de herhaalbaarheidsfunctionaliteit kunnen in- of uitschakelen.
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

## Verwante artikelen {#related-article}

- [Een adaptief formulier maken in AEM Sites Page of Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

- [Een zelfstandig adaptief formulier maken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)
