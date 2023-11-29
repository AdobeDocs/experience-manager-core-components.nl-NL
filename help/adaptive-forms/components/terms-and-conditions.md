---
title: Adaptive Forms Core Component - Voorwaarden en bepalingen
description: De kerncomponent Adaptive Forms Terms and Conditions gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: c607d554-ad2d-4434-856d-91e174ef3149
source-git-commit: a567b5ad937d426abe16c34e039e19cd0b1af5b0
workflow-type: tm+mt
source-wordcount: '2639'
ht-degree: 0%

---

# Component Voorwaarden en bepalingen

A **Voorwaarden en bepalingen** verwijst naar een sectie binnen een formulier waarin de voorwaarden, regels en bepalingen worden beschreven die gebruikers moeten accepteren of naleven wanneer ze een service gebruiken of inhoud openen.

De **Voorwaarden en bepalingen** is een samengestelde component die bestaat uit componenten Text, Checkbox en Link. De tekstcomponent bevat een titel samen met een kort overzicht van het doel en het bereik van de voorwaarden. Het omvat ook een checkbox die wordt gebruikt om expliciete toestemming van de gebruiker te verkrijgen. U kunt een tekst met toestemming ook vervangen door koppelingen.

**Voorbeeld**

![voorwaarden](/help/adaptive-forms/assets/terms-and-conditions.png)

Zie [Subcomponenten van de component Voorwaarden en Voorwaarden](#sub-component) voor meer informatie over de verschillende componenten van de component Voorwaarden.

## Gebruik {#reasons-to-use-termsandconditions}

- **Gebruikersovereenkomst**: De component dient als een overeenkomst tussen de dienstverlener en de gebruiker. Gebruikers moeten de voorwaarden bevestigen en ermee akkoord gaan voordat ze de service of inhoud kunnen openen.

- **Juridische compatibiliteit**: Het garandeert de wettelijke naleving en bescherming van de dienstverlener door de rechten, verantwoordelijkheden en verplichtingen van beide partijen te beschrijven.

- **Registratieproces**: De registratie- of aanmeldingsformulieren bevatten de **Voorwaarden en bepalingen** , waarbij gebruikers expliciet moeten instemmen met de voorwaarden voordat ze een account maken of een service gebruiken.

- **E-commercetransacties**: Online websites bevatten de **Voorwaarden en bepalingen** zodat gebruikers worden gevraagd akkoord te gaan met de voorwaarden als onderdeel van het afrekenproces voordat ze online aankopen doen.

- **Veiligheids- en privacyovereenkomsten**: De **Voorwaarden en bepalingen** bevat details over hoe de gebruikersgegevens worden verzameld, opgeslagen en gebruikt, vaak aangevuld met een afzonderlijk privacybeleid

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.62 for Cloud Service and Core Components 1.1.28 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[release 2.0.62](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.28](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.

## Technische details {#technical-details}

Ga voor de meest recente informatie over de Adaptive Forms Checkbox Group Core Component naar de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de ervaring van de component bepalingen en voorwaarden eenvoudig aanpassen voor bezoekers. U kunt de voorwaarden en bepalingen eenvoudig definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard

![Het tabblad Basis](/help/adaptive-forms/assets/terms-and-conditions-basic-tab.png)

- **Naam** - De naam identificeert uniek de component in de regelredacteur. Speciale tekens en spaties zijn niet toegestaan in de naamtekenreeksen.

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

- **Goedkeuringsoptie tonen** - Selecteer de optie om het selectievakje voor toestemming weer te geven dat wordt gebruikt om expliciete toestemming van de gebruiker te verkrijgen.

- **Weergeven als pop-up** - Selecteer de optie om de component terms and conditions weer te geven in een pop-upvenster.

- **Tekst met toestemming vervangen door weblink(s)**: Selecteer de optie om een tekst voor toestemming te vervangen door een webkoppeling.  Als de optie is uitgeschakeld, wordt standaard de tekst voor de toestemming weergegeven.

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

### Het tabblad Help-inhoud {#help-content-tab}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/terms-and-conditions-help-tab.png)

- **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de achtergrondafbeelding onder de component weer te geven.

- **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

- **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/terms-and-conditions-accessibility-tab.png)

**Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Voorwaarden te definiëren en te beheren.


### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Terms and Conditions Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

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

## Subcomponenten van de component Voorwaarden en Voorwaarden {#sub-component}

**Voorwaarden en bepalingen** onderdeel is een samengesteld onderdeel dat de volgende subcomponenten omvat:
- [Component Koppelen](#link)
- [Tekstcomponent](#text)
- [Component CheckBox](#checkbox)

### Component Koppelen{#link}

Deze component vervangt een of meer toestemmingsteksten door een of meer webkoppelingen. Het wordt gebruikt in een scenario, waar de gebruiker verwijzingen naar bepaalde secties, extra informatie, of externe documenten probeert aan te bieden. U kunt de **Koppeling** voor bezoekers afzonderlijk met het dialoogvenster Configureren.

#### Tabblad Standaard

![Het tabblad Basis](/help/adaptive-forms/assets/link-basic-tab.png)

- **Naam** - De naam identificeert uniek de component in de regelredacteur. Speciale tekens en spaties zijn niet toegestaan in de naamtekenreeksen.

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

- **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.

- **Koppelingen** - Geef de koppeling en de bijbehorende weergavetekst op die wordt gebruikt in plaats van de tekst voor toestemming. U kunt meerdere koppelingen toevoegen door op de knop **Toevoegen** knop.

- **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u met AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

- **Markeren als niet-gebonden formulierelement**: Selecteer de optie om een formulierveld te configureren dat niet is gekoppeld aan een schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.

- **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

- **Component uitschakelen** - Selecteer de optie om de component uit te schakelen of te vergrendelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

#### Tabblad Validatie

![Tabblad Validatie](/help/adaptive-forms/assets/link-validation-tab.png)

- **Vereist** - Selecteer deze optie als u de component wilt weergeven in een adaptief formulier. Nadat u de optie hebt geselecteerd, moet u een selectie maken voordat u een formulier kunt verzenden. U kunt de **Component verbergen** of **Component uitschakelen**  in de **Basis** als deze optie is geselecteerd.

- **Foutbericht** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de optie **Vereist** wordt ingeschakeld en wordt het formulierveld leeg gelaten.

- **Bericht voor scriptvalidatie** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de scriptvalidatie mislukt.

### Het tabblad Help-inhoud {#helpcontent-tab}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/link-help-tab.png)

- **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de achtergrondafbeelding onder de component weer te geven.

- **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

- **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/link-accessibilty-tab.png)

**Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

### Tekstcomponent {#text}

**Tekst** geeft de tekstinhoud weer die informatie verschaft aan gebruikers. Deze component omvat de feitelijke voorwaarden, de juridische taal of andere relevante tekstinformatie.

U kunt de [Tekstcomponent](/help/adaptive-forms/components/text.md) afzonderlijk voor bezoekers met het dialoogvenster Configureren. Als u eenvoudig tekstopties wilt definiëren voor een naadloze gebruikerservaring, kunt u de opdracht [configureren, dialoogvenster van tekstcomponent](/help/adaptive-forms/components/text.md#configure-dialog).


### Component CheckBox {#checkbox}

Een checkbox wordt gebruikt om gebruikerstoestemming of erkenning te verkrijgen. Het dient als visuele indicator die de gebruiker heeft gelezen en met de vermelde termijnen akkoord gegaan. Het is verplicht het selectievakje in te schakelen om de toestemming van de gebruiker aan te geven.

U kunt de [Component CheckBox](/help/adaptive-forms/components/checkbox.md) afzonderlijk voor bezoekers met het dialoogvenster Configureren. Als u de eigenschappen van het selectievakje voor een naadloze gebruikerservaring wilt definiëren, gebruikt u de optie [dialoogvenster configureren van component selectievakje](/help/adaptive-forms/components/checkbox.md#configure-dialog).


## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
