---
title: Adaptive Forms Core Component - Telefonische invoer
description: De Adaptive Forms Telephone Input Core Component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
source-git-commit: 0e4fb8454b7ef84eb5b1b73b01c982a2f9c12381
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 0%

---


# Telefooninvoer {#telephone-input-adaptive-forms-core-component}

Met de Adaptive Form Phone Input Core Component kunnen gebruikers een telefoonnummer invoeren. In het veld voor telefooninvoer worden toetsenborden weergegeven op mobiele apparaten die relevant zijn voor telefoonnummers. Deze kan worden aangepast met extra kenmerken, zoals &quot;patroon&quot; en &quot;plaatsaanduiding&quot;, om de notatie en beschrijving van het telefoonnummer op te geven.

Het veld voor telefooninvoer wordt vaak gebruikt in contactformulieren, registratieformulieren en andere formulieren, waarbij een telefoonnummer als contactmiddel vereist is. Het veld voor telefooninvoer kan ook worden gebruikt om ervoor te zorgen dat de gebruiker een geldig telefoonnummer invoert, omdat de browser bepaalde beperkingen kan opleggen, zoals de lengte en de indeling van het telefoonnummer, op basis van het kenmerk &quot;pattern&quot;.

## Gebruik {#reasons-to-use-telephone-input}

De algemene redenen om een veld voor telefooninvoer te gebruiken in een adaptief formulier zijn:

* **Contactgegevens**: Een veld voor telefooninvoer wordt vaak gebruikt om het telefoonnummer van een gebruiker te verzamelen als een manier om contact op te nemen.

* **Verbeterde gegevensnauwkeurigheid**: Door een veld voor telefooninvoer te gebruiken, kan het formulier bepaalde beperkingen opleggen aan de notatie van het telefoonnummer, zodat de ingevoerde gegevens correct en volledig zijn.

* **Betere gebruikerservaring**: Een veld voor telefooninvoer biedt gebruikers een duidelijke en intuïtieve manier om hun telefoonnummer in te voeren en kan de gebruikerservaring verbeteren door gebruikers in staat te stellen snel en eenvoudig hun contactgegevens in te voeren.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Telephone Input Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/versions.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Core Components-versies](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Ga voor de meest recente informatie over de Adaptive Forms Telephone Input Core Component naar de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/telephoneinput/v1/telephoneinput). Raadpleeg de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u uw telefonische invoerervaring eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig opties voor telefooninvoer definiëren voor een naadloze gebruikerservaring.

![Tabblad Standaard](/help/adaptive-forms/assets/telephoneinput_basictab.png)

* **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

* **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
* **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.

* **Plaatsaanduidingstekst** - Plaatsaanduidingstekst in een formuliercomponent verwijst naar een kort label of een korte vraag die binnen een invoerveld wordt weergegeven als een tip voor de gebruiker met betrekking tot welk type informatie naar verwachting in dat veld wordt ingevoerd. Plaatsaanduidingstekst verdwijnt wanneer de gebruiker in het veld typt en verschijnt opnieuw als het veld leeg blijft. De klasse biedt een visuele aanwijzing voor de gebruiker, maar fungeert niet als een permanent label of een permanente waarde voor het veld.
* **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.
* **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
* **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
* **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
* **Standaardwaarde** - Met deze optie kunt u een standaardwaarde toevoegen aan een formulierveld. Indien **Uitgeschakelde component** of **Component (alleen-lezen)** is geselecteerd, wordt de standaardwaarde op het scherm weergegeven. Als er geen waarde wordt ingevoerd door de gebruiker in het formulierveld, wordt deze waarde verzonden op het moment dat het formulier wordt verzonden

### Tabblad Validatie {#validation-tab}

![Tabblad Validatie](/help/adaptive-forms/assets/telephoneinput_validationtab.png)

* **Vereist** - Selecteer deze optie als u de component wilt weergeven in een adaptief formulier. U kunt de **Component verbergen** of **Component uitschakelen**  in de **Basis** als deze optie is geselecteerd.

* **Foutbericht** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de optie **Vereist** selectievakje is ingeschakeld en het veld blijft leeg.

* **Bericht voor scriptvalidatie** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de scriptvalidatie mislukt.

* **Maximum aantal tekens** - Met deze optie kunt u het maximum aantal tekens opgeven dat in de component is toegestaan. Als u tekens invoert die groter zijn dan de waarde die is opgegeven in **Maximum aantal tekens** verschijnt er een foutbericht op het scherm. De **Foutbericht voor Maximum aantal tekens** kunt u een aangepast foutbericht toevoegen.

* **Foutbericht voor Maximum aantal tekens** - de **Foutbericht voor Maximum aantal tekens** kunt u een aangepast foutbericht toevoegen als u tekens invoert die groter zijn dan de waarde die is opgegeven in **Maximum aantal tekens** optie.

* **Minimum aantal tekens** - Met deze optie kunt u het minimale aantal tekens opgeven dat in het veld is toegestaan. Als u tekens invoert die minder zijn dan de waarde die is opgegeven in **Minimum aantal tekens** verschijnt er een foutbericht op het scherm. De **Foutbericht voor minimale tekens** kunt u een aangepast foutbericht toevoegen.

* **Foutbericht voor minimale tekens** - de **Foutbericht voor minimale tekens** kunt u een aangepast foutbericht toevoegen als u tekens invoert die kleiner zijn dan de waarde die in het dialoogvenster is opgegeven **Minimum aantal tekens** optie.

De **Validatiepatroon** kunt u een patroon invoeren om het ingevoerde telefoonnummer te valideren. Het ingevoerde telefoonnummer wordt gevalideerd tegen de waarde die is ingevoerd in het dialoogvenster **Patroon** optie. Als het telefoonnummer niet valideert met de ingevoerde waarde **Patroon** verschijnt het foutbericht op het scherm.
* **Patroon** - Met deze optie kunt u de toegestane verificatiepatronen voor het telefoonnummer invoeren. Reguliere expressies zijn ook toegestaan.
* **Foutbericht** - Met deze optie kunt u een bericht invoeren dat op het scherm wordt weergegeven als het ingevoerde telefoonnummer niet wordt gevalideerd met de waarde die is ingevoerd in het dialoogvenster **Patroon** option

### Het tabblad Help-inhoud {#help-content-tab}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/telephoneinput_helptab.png)

* **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de component onder de component weer te geven.

* **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

* **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/telephoneinput_accessibilitytab.png)

* **Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.


## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de invoercomponent Telefoon te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Telephone Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

**Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Telephone Input Core Component.

**Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight&quot; opgeven: vet&quot;. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Tabblad Opmaak {#format-tab}

Op het tabblad Indelingen kunt u de standaardindelingen en de aangepaste getalnotaties opgeven.