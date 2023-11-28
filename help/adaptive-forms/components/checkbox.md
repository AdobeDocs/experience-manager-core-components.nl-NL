---
title: Adaptieve Forms Core-component - Selectievakje
description: De Adaptive Forms Checkbox Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: c6ca4800-bd10-4aeb-957a-fb1780cf94f3
source-git-commit: f0b450ef93a32a56000c31d82bf92394c57b55f9
workflow-type: tm+mt
source-wordcount: '1708'
ht-degree: 0%

---

# Selectievakje {#checkbox-component}

Een selectievakje is een grafisch interface-element dat vaak wordt gebruikt in softwaretoepassingen en formulieren, zodat gebruikers een binaire keuze kunnen maken tussen twee opties: ingeschakeld (geselecteerd) of uitgeschakeld (uitgeschakeld).

Een selectievakje wordt meestal weergegeven als een klein vierkant dat in- of uitgeschakeld kan worden door erop te klikken of erop te tikken. Als een selectievakje is ingeschakeld, wordt een vinkje weergegeven om aan te geven dat de bijbehorende optie of functie actief of ingeschakeld is.

**Voorbeeld**

![groep selectievakjes](/help/adaptive-forms/assets/checkbox-example.png)

## Gebruik {#reasons-to-use-checkbox}

De algemene redenen om een selectievakje in een adaptief formulier te gebruiken zijn:

- **Gebruiksgemak**: Selectievakjes zijn visueel duidelijk en bieden een eenvoudige manier om binaire keuzes te maken. Ze zijn intuïtief en gemakkelijk te begrijpen en maken ze gebruiksvriendelijk.

- **Goedkeuring en Overeenkomst**: Selectievakjes worden gebruikt om de toestemming van de gebruiker voor verschillende doeleinden te verkrijgen, bijvoorbeeld het accepteren van voorwaarden, het abonneren op nieuwsbrieven of het bevestigen van leeftijdsverificatie. Ze maken duidelijk dat de gebruiker actief met iets instemt.

- **Visuele bevestiging**: Ingeschakelde selectievakjes geven gebruikers een visuele bevestiging dat hun selectie is opgenomen. Deze feedback helpt gebruikersfouten te voorkomen en zorgt ervoor dat gebruikers weten dat hun keuzes zijn geregistreerd.

- **Foutpreventie**: Met selectievakjes wordt de kans op fouten verkleind doordat gebruikers de keuzes kunnen controleren en bevestigen voordat het formulier wordt verzonden.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Checkbox Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | --- |
| v1 | Compatibel met<br>[versie 2.0.4](/help/versions.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/versions.md) document.

## Technische details {#technical-details}

Lees de nieuwste informatie over de Adaptive Forms Checkbox Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkbox/v1/checkbox). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de ervaring in het selectievakje voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig opties voor selectievakjes definiëren voor een naadloze gebruikerservaring.

![Het tabblad Basis](/help/adaptive-forms/assets/checkbox-basic.png)

- **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. De titel wordt standaard naast de component weergegeven. Als u geen titel toevoegt, wordt de component niet weergegeven.

- **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.

- **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u met AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

- **Markeren als niet-gebonden formulierelement**: Selecteer de optie om een formulierveld te configureren dat niet is gekoppeld aan een schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.

- **Gegevenstype van verzonden waarde**: Met deze optie geeft u het gegevenstype op van de waarde die wordt verzonden wanneer een optie is geselecteerd. Als de **gegevenstype van verzonden waarde** is ingesteld op `Number` en u voegt tekenreeksgegevens toe aan **Gegevenswaarde** &#x200B; &#x200B; op de **Opties** tabblad geeft het scherm een `Value type mismatch` foutbericht.

- **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

- **Component uitschakelen** - Selecteer de optie om de component uit te schakelen of te vergrendelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **Retourwaarde bij controle** -Selecteer deze optie om op te geven welke waarde aan het selectievakje moet worden gekoppeld wanneer dit wordt ingeschakeld. Het is de actie die voorkomt wanneer u of checkbox merkt.
- **Schakel Uitschakelen in.**- Selecteer de optie om een eerder ingeschakeld selectievakje in of uit te schakelen.
   - Indien **Uitschakelen inschakelen** is ingeschakeld of ingesteld op true, betekent dit dat de gebruiker naar eigen goeddunken het selectievakje kan in- en uitschakelen. Ze kunnen het selectievakje naar wens in- en uitschakelen.

   - Indien **Uitschakelen inschakelen** is uitgeschakeld of op false is ingesteld, betekent dit dat de gebruiker het selectievakje niet mag uitschakelen als het selectievakje eenmaal is ingeschakeld.
- **Retourwaarde indien uitgeschakeld** - Met deze optie kunt u opgeven welke waarde aan het selectievakje moet worden gekoppeld wanneer het selectievakje is uitgeschakeld of uitgeschakeld.

- **Standaardwaarde**: Met deze optie kunt u een standaardwaarde toevoegen aan een formulierveld. Indien **Uitgeschakelde component** of **Component (alleen-lezen)** is geselecteerd, wordt de standaardwaarde op het scherm weergegeven. Als geen waarde wordt ingevoerd door de gebruiker in het formulierveld, wordt deze waarde verzonden op het moment dat het formulier wordt verzonden.

### Tabblad Validatie {#validation-tab}

![Tabblad Validatie](/help/adaptive-forms/assets/checkbox-validation.png)

- **Vereist** - Selecteer deze optie als u de component wilt weergeven in een adaptief formulier. Nadat u de optie hebt geselecteerd, moet u een selectie maken voordat u een formulier kunt verzenden. U kunt de **Component verbergen** of **Component uitschakelen**  in de **Basis** als deze optie is geselecteerd.

- **Foutbericht** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de optie **Vereist** wordt ingeschakeld en wordt het formulierveld leeg gelaten.

- **Bericht voor scriptvalidatie** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de scriptvalidatie mislukt.

### Het tabblad Help-inhoud {#helpcontent-tab}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/checkbox-help.png)

- **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de achtergrondafbeelding onder de component weer te geven.

- **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

- **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/checkbox-accessibility.png)

**Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Check-box te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

De Adaptive Forms Checkbox Core-component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Ontwerpdialoogvenster](/help/adaptive-forms/assets/checkbox-style.png)

- **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Checkbox Group Core-component.

- **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![Dialoogvenster Aangepaste eigenschappen](/help/adaptive-forms/assets/checkbox-customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Groepsnaam**: U kunt een naam opgeven om de groep met aangepaste eigenschappen te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **Belangrijke paren**: U kunt meerdere aangepaste eigenschapnamen en aangepaste eigenschapswaarden toevoegen door op de knop **Toevoegen** knop voor elke aangepaste groep eigenschappen.

   - **Verwijderen**: Tik of klik om de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te verwijderen.

   - **Opnieuw rangschikken**: Tik of klik en sleep om de volgorde van de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te wijzigen.

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
