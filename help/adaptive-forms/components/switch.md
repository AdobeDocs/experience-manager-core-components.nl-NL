---
title: Adaptieve Forms Core-component - Switch-component
description: De Adaptive Forms Switch Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: 6ff2ca76-1514-42eb-bde3-60259af2d187
source-git-commit: e4274194026c3370b52be17171776847374a86b5
workflow-type: tm+mt
source-wordcount: '1689'
ht-degree: 0%

---

# Component wisselen{#switch-adaptive-forms-core-component}

De component switch is een grafische gebruikersinterface die in formulieren wordt gebruikt en die gebruikers in staat stelt uit twee opties te kiezen. Het is meestal een schakeloptie met twee statussen waarmee gebruikers kunnen kiezen tussen twee statussen, waarbij een functie, instelling of functionaliteit wordt in- of uitgeschakeld. De schakelaarcomponent wordt ontworpen om de huidige staat en vertoning visueel te vertegenwoordigen of een bepaalde eigenschap wordt aangezet of weg.

De schakelaarcomponent is een booleaanse controleelement dat de waarde aan waar of vals plaatst. Het wordt bijvoorbeeld gebruikt om een functie in of uit te schakelen, zoals geluid dempen of dempen, of Bluetooth of WiFi in- of uitschakelen.

![Componentvoorbeeld wijzigen](/help/adaptive-forms/assets/switch-example.png)

## Gebruik {#reasons-to-use-switch}

De algemene redenen om over te schakelen in een adaptieve vorm zijn:

- **Gebruikersinteractie**: De gebruikers kunnen met de schakelaarcomponent in wisselwerking staan door op het te klikken of te tikken.

- **Staten**: De component switch heeft twee statussen: AAN en UIT. De aanvankelijke staat van de schakelaarcomponent hangt van het gebrek af dat of de huidige status van de eigenschap plaatst die het controleert.

- **Visuele vertegenwoordiging**: De schakelcomponent geeft visueel de huidige toestand door de kleur of positie te wijzigen.

- **Functie voor besturing**: De component switch wordt gebruikt om specifieke functionaliteit in een AEM vorm in of uit te schakelen. Zo kunnen gebruikers bijvoorbeeld een functie in- of uitschakelen.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Switch Core Component is uitgebracht als onderdeel van Core Components 2.0.64. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | — |
| v1 | Compatibel met<br>[release 2.0.64](/help/adaptive-forms/version.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.

## Technische details {#technical-details}

Ga voor de meest recente informatie over de Adaptive Forms Switch Core Component naar de technische documentatie op [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/switch/v1/switch). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

U kunt uw ervaring van de component van de Schakelaar voor bezoekers gemakkelijk aanpassen met Configure Dialoog. U kunt de opties voor de component Switch eenvoudig definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard

![Het tabblad Basis](/help/adaptive-forms/assets/switch-basic.png)

- **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. De titel wordt standaard naast de component weergegeven. Als u geen titel toevoegt, wordt de component niet weergegeven.
<!-- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png)-->

- **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.

- **Statuswaarde voor uitschakelen behouden** - Als u deze optie selecteert, kunt u de waarde opgeven die moet worden geretourneerd wanneer de schakelcomponent niet is geselecteerd.
- **Opties** - Geef de gegevenswaarde en de weergavetekst voor elke optie op.
   - **Gegevenswaarde** - Geef de waarde op die moet worden verzonden wanneer de switch in een adaptieve vorm is ingeschakeld.
   - **Tekst weergeven** - Geef de tekst op die als label moet worden weergegeven wanneer de schakelaar is ingeschakeld in een adaptief formulier.
   - **Uit-gegevenswaarde** - Geef de waarde op die moet worden verzonden wanneer de switch niet in een adaptieve vorm is ingeschakeld. Deze optie is alleen zichtbaar als de **Statuswaarde voor uitschakelen behouden** switch is ingeschakeld.
   - **Niet-weergegeven tekst** - Geef de tekst op die als label moet worden weergegeven wanneer de switch niet is ingeschakeld in een adaptief formulier. Deze optie is alleen zichtbaar als de **Statuswaarde voor uitschakelen behouden** switch is ingeschakeld.

<!-- You can also format the options for switch using **Allow Rich Text for Options**. 
  
     ![Rich text support for options](/help/adaptive-forms/assets/switch-optipn-rich-text.png)

    Once you select the checkbox for **Allow Rich Text for options** formatting options become visible to style the component's options. To access all available formatting options, you can click on the `Fullscreen` ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
    
    ![Rich text support for options](/help/adaptive-forms/assets/switch-richtext-for-display.png) -->

- **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u met AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.
- **Markeren als niet-gebonden formulierelement**: Selecteer de optie om een formulierveld te configureren dat niet is gekoppeld aan een schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.

- **Gegevenstype van verzonden waarde**: Met deze optie geeft u het gegevenstype op van de waarde die wordt verzonden wanneer een optie is geselecteerd. Als de **gegevenstype van verzonden waarde** is ingesteld op `Number` en u voegt tekenreeksgegevens toe aan **Gegevenswaarde** &#x200B; &#x200B; op de **Opties** tabblad geeft het scherm een `Value type mismatch` foutbericht.
- **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

- **Component uitschakelen** - Selecteer de optie om de component uit te schakelen of te vergrendelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

- **Standaardwaarde**: Met deze optie kunt u een standaardwaarde toevoegen aan een formulierveld. Indien **Uitgeschakelde component** of **Component (alleen-lezen)** is geselecteerd, wordt de standaardwaarde op het scherm weergegeven. Als geen waarde wordt ingevoerd door de gebruiker in het formulierveld, wordt deze waarde verzonden op het moment dat het formulier wordt verzonden.

### Tabblad Validatie {#validation-tab}

![Tabblad Validatie](/help/adaptive-forms/assets/switch-validation.png)

- **Vereist** - Selecteer deze optie als u de component wilt weergeven in een adaptief formulier. Nadat u de optie hebt geselecteerd, moet u een selectie maken voordat u een formulier kunt verzenden. U kunt de **Component verbergen** of **Component uitschakelen**  in de **Basis** als deze optie is geselecteerd.

- **Foutbericht** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de optie **Vereist** wordt ingeschakeld en wordt het formulierveld leeg gelaten.

- **Bericht voor scriptvalidatie** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de scriptvalidatie mislukt.

### Het tabblad Help-inhoud {#helpcontent-tab}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/switch-help.png)

- **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de achtergrondafbeelding onder de component weer te geven.

- **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

- **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/switch-accessibility.png)

**Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

### Tabblad Stijlen {#styles-tab}

![Het tabblad Stijlen](/help/adaptive-forms/assets/switch-styles.png)

- **Labels verbergen** - Selecteer deze optie om de labels van de schakelcomponent te verbergen.

- **Labels tonen** - Selecteer deze optie om de etiketten van de schakelaarcomponent te tonen.

## Ontwerpdialoogvenster {#design-dialog}

Het Dialoogvenster van het ontwerp wordt gebruikt om CSS stijlen voor de component van de Schakelaar te bepalen en te beheren.

### Tabblad Stijlen {#styles-design-tab}

De Adaptive Forms Switch Core-component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Ontwerpdialoogvenster](/help/adaptive-forms/assets/checkbox-style.png)

- **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Switch Group Core-component.

- **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![Dialoogvenster Aangepaste eigenschappen](/help/adaptive-forms/assets/checkbox-customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Groepsnaam**: U kunt een naam opgeven om de groep met aangepaste eigenschappen te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **Belangrijke paren**: U kunt meerdere aangepaste eigenschapnamen en aangepaste eigenschapswaarden toevoegen door op de knop **Toevoegen** knop voor elke aangepaste groep eigenschappen.

   - **Verwijderen**: Tik of klik om de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te verwijderen.

   - **Opnieuw rangschikken**: Tik of klik en sleep om de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap opnieuw te rangschikken.

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
