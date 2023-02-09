---
title: Adaptive Forms Core Component - Datumkiezer
description: De Adaptive Forms Date Picker Core Component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1760'
ht-degree: 0%

---


# Datumkiezer {#date-picker-adaptive-forms-core-component}

Een component voor de datumkiezer in een adaptief formulier is een interface-element waarmee gebruikers een datum in een kalender kunnen selecteren of een datum handmatig in een specifieke notatie kunnen invoeren. De component van de datumkiezer kan worden gevormd om verschillende het formatteren, bevestiging, en standaardwaarden te hebben.

**Voorbeeld**

![](/help/adaptive-forms/assets/date-picker.png)

## Gebruik {#reasons-to-use-drop-date-picker}

Er zijn verschillende redenen waarom het nuttig is een datumkiezer op te nemen in een adaptief formulier, zoals:

* **Handigheid**: Met een component voor een datumkiezer kunnen gebruikers eenvoudig een datum in een kalender selecteren zonder de datum handmatig in te voeren in een tekstveld. Dit kan tijd besparen en fouten verminderen.

* **Gebruikerservaring**: De component van de plukker van de datum kan worden gebruikt om het formulier gebruikersvriendelijker te maken door een duidelijke en intuïtieve manier voor gebruikers te verstrekken om datum te selecteren.

* **Gegevensanalyse**: De component van de plukker van de datum kan worden gebruikt om gegevens uit diverse bronnen te verzamelen en het te analyseren, of het te gebruiken als input voor verdere verwerking.

* **Gebeurtenisbeheer**: De component Date Picker kan in gebeurtenisbeheerwebsites worden gebruikt om de gebeurtenisdatum te selecteren.

* **Boekhouding en reservering**: De component van de plukker van de datum kan in boekings en reserveringswebsites worden gebruikt om de controle en controledata te selecteren.

* **Datumnotatie**: De component van de plukker van de datum kan worden gebruikt om het formaat te bevestigen waarin de datum wordt getoond en ingegaan. Zorg ervoor dat de datumnotatie in het formulier consistent is, zodat de gebruiker er altijd last van heeft.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Date picker Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | --- |
| v1 | Compatibel met<br>[versie 2.0.4](/help/versions.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Core Components-versies](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technische details {#technical-details}

Lees de nieuwste informatie over de Adaptive Forms Date Picker Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker). Raadpleeg de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de datumkiezer-ervaring voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig opties voor datumkiezers definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![Het tabblad Basis](/help/adaptive-forms/assets/datepicker_basictab.png)

* **Naam** - De naam identificeert uniek de component in de regelredacteur. Speciale tekens en spaties zijn niet toegestaan in de naamtekenreeksen.

* **Titel** - Titel is een tekenreeks die boven aan een component in een adaptief formulier wordt weergegeven. De titel geeft de component in de boomstructuur van een adaptief formulier op unieke wijze aan. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

* **Titel verbergen** - Selecteer deze optie om de titel van het componenttype in een adaptief formulier te verbergen.

* **Plaatsaanduidingstekst** - Plaatsaanduidingstekst in een formuliercomponent verwijst naar een kort label of een korte vraag die binnen een invoerveld wordt weergegeven als een tip voor de gebruiker met betrekking tot welk type informatie naar verwachting in dat veld wordt ingevoerd. Plaatsaanduidingstekst verdwijnt wanneer de gebruiker in het veld typt en verschijnt opnieuw als het veld leeg blijft. De klasse biedt een visuele aanwijzing voor de gebruiker, maar fungeert niet als een permanent label of een permanente waarde voor het veld.

* **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
* **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
* **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
* **Standaarddatum** - Met deze optie kunt u een datum toevoegen aan het formulierveld. De ingevoerde datum wordt standaard weergegeven op de plaats van de component. Als de gebruiker geen datum invoert, wordt deze waarde verzonden op het moment dat het formulier wordt verzonden. In geval van **Uitgeschakelde component** of **Component (alleen-lezen)** is geselecteerd, wordt de standaarddatum weergegeven op het scherm en verzonden op het moment dat het formulier wordt verzonden.


### Tabblad Validatie {#validation-tab}

![Tabblad Validatie](/help/adaptive-forms/assets/datepicker_validation.png)

* **Vereist** - Selecteer deze optie als u de component wilt weergeven in een adaptief formulier. U kunt de **Component verbergen** of **Component uitschakelen** in de **Basis** als deze optie is geselecteerd.

* **Foutbericht** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de optie **Vereist** wordt ingeschakeld en wordt het formulierveld leeg gelaten.

* **Bericht voor scriptvalidatie** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de scriptvalidatie mislukt.

* **Minimumdatum** - Met deze optie kunt u de minimaal vereiste datum invoeren. Als u een datum vóór de in Minimumdatum opgegeven datum invoert, verschijnt er een foutbericht op het scherm. De **Minimale foutmelding** kunt u een aangepast foutbericht toevoegen.

* **Minimale foutmelding** - de **Minimale foutmelding** kunt u een aangepast foutbericht toevoegen dat moet worden weergegeven als u een eerdere datum invoert dan de datum die is opgegeven in het dialoogvenster **Minimumdatum** optie.

* **Maximumdatum** - Met deze optie kunt u de maximaal vereiste datum invoeren. Als u een datum later dan de datum ingaat die in MaximumDatum wordt gespecificeerd, verschijnt een foutenmelding op het scherm. De **Maximum foutbericht** kunt u een aangepast foutbericht toevoegen.

* **Maximum foutbericht** - de **Maximum foutbericht** kunt u een aangepast foutbericht toevoegen dat wordt weergegeven als u een datum later dan de datum invoert die in het dialoogvenster **Maximumdatum** optie.


### Het tabblad Help-inhoud {#help-content-tab}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/datepicker_helptab.png)

* **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de component onder de component weer te geven.

* **Altijd korte beschrijving tonen**- Schakel de optie in om de korte beschrijving onder de component weer te geven.

* **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.


### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

Op de **Toegankelijkheid** tab, waarden worden ingesteld voor [Toegankelijkheid ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) labels voor de component. Er zijn verschillende opties beschikbaar voor het gebruik van de tekst voor schermlezers:

* **Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.


   * **Aangepaste tekst**: Selecteer deze optie als u de aangepaste tekst voor toegankelijkheidslabels van ARIA wilt gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   * **Beschrijving**: Selecteer deze optie als u de beschrijving voor toegankelijkheidslabels van ARIA wilt gebruiken.
   * **Titel**: Selecteer deze optie als u de titel voor toegankelijkheidslabels van ARIA wilt gebruiken.
   * **Naam**: Selecteer deze optie als u de naam voor toegankelijkheidslabels van ARIA wilt gebruiken.
   * **Geen**: Selecteer deze optie als u geen toegankelijkheidslabels voor ARIA wilt toevoegen.



### Tabblad Opmaak {#format-tab}

![Tabblad Indelingen](/help/adaptive-forms/assets/datepicker_formattab.png)

* **Weergave-indeling** - Het staat voor de datumnotatie die aan de gebruiker wordt weergegeven. De **Type** kan de gebruiker de datumnotatie selecteren. U kunt de datumnotatie ook aanpassen met de opdracht **Aangepast** in de **Type** vervolgkeuzemenu.

* **Opmaak bewerken** - Dit is een datumnotatie waarin de gebruiker de datum kan bewerken. De **Type** kan de gebruiker de datumnotatie selecteren. U kunt de datumnotatie ook aanpassen met de opdracht **Aangepast** in de **Type** vervolgkeuzemenu.

* **Weergave-indeling** - Het staat voor de datumnotatie die aan de gebruiker wordt weergegeven. Met de optie Type kan de gebruiker de datumnotatie selecteren. U kunt de datumnotatie ook aanpassen met de opdracht **Aangepast** in de **Type** vervolgkeuzemenu.

* **Opmaak bewerken** - Het staat voor een datumnotatie waarin de gebruiker de datum bewerkt. Met de optie Type kan de gebruiker de datumnotatie selecteren. U kunt de datumnotatie ook aanpassen met de opdracht **Aangepast** in de **Type** vervolgkeuzemenu.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Date-Picker te definiëren en te beheren.


### Tabblad Stijlen {#styles-tab}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Date-Picker Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

**Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Date-picker Core Component.

**Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight&quot; opgeven: vet&quot;. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Tabblad Opmaak {#formats-tab}

Op het tabblad Indelingen kunt u standaard- en aangepaste datumnotaties opgeven.
