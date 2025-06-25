---
title: Adaptieve Forms Core-component - Keuzerondje
description: De Adaptive Forms Radio Button Core Component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: 86b5e9ec-58ac-4cd5-9c7c-4269247ec34f
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '2135'
ht-degree: 0%

---


# Component keuzerondje {#radio-button-adaptive-forms-core-component}

Een keuzerondje in een adaptief formulier is een invoerelement waarmee een gebruiker een optie kan selecteren in een groep gerelateerde opties. Deze wordt weergegeven met een kleine ronde knop die gevuld of leeg is om aan te geven of de optie is geselecteerd. Wanneer een gebruiker een keuzerondje selecteert, worden de overige keuzerondjes in de groep uitgeschakeld. Keuzerondjes worden doorgaans gebruikt wanneer er meerdere opties zijn die elkaar wederzijds uitsluiten en er slechts één optie tegelijk kan worden geselecteerd.

{{traditional-aem}}

**Voorbeeld**

![ voorbeeld ](/help/adaptive-forms/assets/radio-button.png)

**de Dialoog van Eigenschappen**

![ voorbeeld ](/help/adaptive-forms/assets/radio-button-properties.png)

In dit voorbeeld wordt het element Opties gebruikt om de keuzerondjes te groeperen. Het **tekstelement van de Vertoning** wordt gebruikt om een etiket voor een punt te verstrekken en **Waarde van Gegevens** wordt gebruikt om de waarde te specificeren die wordt verzonden naar de server wanneer de vorm wordt voorgelegd.

Elke keuzerondje heeft een unieke gegevenswaarde en een uniek kenmerk Tekst weergeven. Als een gebruiker &quot;1-10&quot;selecteert, wordt de overeenkomstige Waarde van Gegevens verzonden naar de server wanneer de vorm wordt voorgelegd. Deze gegevens kunnen vervolgens worden verwerkt door een serverscript om te bepalen welke opties door de gebruiker zijn geselecteerd en kunnen worden gebruikt om verschillende handelingen uit te voeren, zoals het bijwerken van andere velden in het formulier of het verzenden van de formuliergegevens naar een serverscript voor verdere verwerking.

Bovendien kan elk keuzerondje zo worden geconfigureerd dat het verschillende verwerkingswaarden heeft voor elke optie. Dit kan worden ingesteld met de Adaptive Forms Rule Editor

## Gebruik {#reasons-to-use-radio-button}

Er zijn verschillende redenen om keuzerondjes in een formulier te gebruiken, zoals:

- **Beperkte keuzen**: De radioknopen worden gebruikt om een lijst van vooraf bepaalde opties voor de gebruiker te verstrekken om van te kiezen, en slechts één optie kan tegelijkertijd worden geselecteerd. Dit is handig wanneer het aantal opties beperkt is en elkaar uitsluiten.

- **Duidelijke vertegenwoordiging**: De radioknopen zijn duidelijk en gemakkelijk te begrijpen, makend het voor gebruikers eenvoudig om te weten wat zij selecteren.

- **Consistentie**: Het gebruiken van radioknopen verzekert een verenigbare en gestandaardiseerde manier om opties aan gebruikers voor te stellen, die het voor hen gemakkelijker maken om met de vorm te begrijpen en in wisselwerking te staan.

- **Gemakkelijker te gebruiken**: De radioknopen zijn gemakkelijk te gebruiken, vooral voor gebruikers die niet vertrouwd met technologie zijn, of die beperkte mobiliteit hebben.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Radio Button Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 voor Cloud Service en Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM-compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/adaptive-forms/version.md) en later | Compatibel met <br>[ versie 1.1.12 ](/help/adaptive-forms/version.md) en later maar minder dan 2.0.0. |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het ](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0}.[

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Krijg de recentste informatie over de Adaptieve Component van de Kern van de RadioKnoop van Forms in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/radiobutton/v1/radiobutton). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de ervaring met keuzerondjes eenvoudig aanpassen aan bezoekers. U kunt ook eenvoudig opties voor keuzerondjes definiëren voor een naadloze gebruikerservaring.

### Het tabblad Basis

![ Basis lusje ](/help/adaptive-forms/assets/radiobutton_basictab.png)

- **Naam** - u kunt een vormcomponent gemakkelijk met zijn unieke naam zowel in de vorm als in de regelredacteur identificeren, maar de naam moet geen ruimten of speciale karakters bevatten.

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bovenop de component. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **staat RTF voor Titel** toe - Deze eigenschappen laat gebruikers toe om gewone teksttitels te formatteren, die eigenschappen zoals vette, cursieve, onderstreepte tekst, diverse doopvonten, doopvontgrootte, kleuren, en extra optie opnemen om visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Op het selecteren van checkbox voor **staat RTF-tekst voor Titel** toe, wordt het formatteren opties zichtbaar om de titel van de component te stileren. Om tot alle beschikbare het formatteren opties toegang te hebben, kunt u op het ![ pictogram Volledig scherm ](/help/adaptive-forms/assets/fullscreen-icon.png) tabel klikken.

  ](/help/adaptive-forms/assets/richtext-support-title.png) de rijke tekststeun van 0}![

- **Verberg Titel** - selecteer de optie om de Titel van de component te verbergen.

- **Opties** - u kunt gegevenswaarden en vertoningstekstparen toevoegen gebruikend **toevoegen** knoop.\
  Nadat een nieuwe optie is toegevoegd, kunnen de volgende acties worden uitgevoerd:
   - **Waarde van Gegevens** - deze optie staat toe om de inhoud in te gaan om voor te leggen wanneer een optie wordt geselecteerd.
   - **Tekst van de Vertoning** - Deze optie staat toe om de inhoud in te gaan om in een AanpassingsVorm te tonen.
   - **Schrapping** - Tik of klik om de optie van een radioknoop te schrappen.
   - **herschikt** - Tik of klik en sleep om de orde van de opties te herschikken.
U kunt de opties voor radioknoopgroep ook formatteren gebruikend **Verrijkte Tekst voor Opties** toestaan.

  ![ Rijke tekststeun voor opties ](/help/adaptive-forms/assets/richtext-for-options.png)

  Zodra u checkbox voor **selecteert sta RTF voor het formatteren van Opties** toe zichtbaar worden om de opties van de component te stileren. Om tot alle beschikbare het formatteren opties toegang te hebben, kunt u op het `Fullscreen` ![ pictogram Volledig scherm ](/help/adaptive-forms/assets/fullscreen-icon.png) tabel klikken.

  ![ Rijke tekststeun voor opties ](/help/adaptive-forms/assets/richtextoptions-support.png)

- **Bind Verwijzing** - A bindt verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

- **Teken als Niet-gebonden Element van de Vorm**: Selecteer de optie om een vormgebied te vormen niet verbonden aan om het even welk schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.

- **Type van Gegevens van voorgelegde waarde** - Deze optie specificeert het gegevenstype van de verzonden waarde wanneer om het even welke optie wordt geselecteerd. Als het **gegevenstype van voorgelegde waarde** aan `Number` wordt geplaatst en u koordgegevens aan **Waarde van Gegevens** &#x200B; &#x200B; op het **lusje van Opties** toevoegt, toont het scherm een `Value type mismatch` foutenmelding.

- **Standaard optie** - deze optie staat u toe om standaardwaarden toe te voegen die vooraf worden geselecteerd, wanneer de vorm laadt. Als het **gegevenstype van voorgelegde waarde** aan `Number` wordt geplaatst en u koordgegevens aan **Standaardopties** toevoegt, toont het scherm een `Value type mismatch` foutenmelding.

- **de opties van de Vertoning** - Deze optie wordt gebruikt om de visuele groepering van radioknopen in een Aangepaste Vorm te plaatsen. De twee ondersteunde opties zijn:
   - **Horizontaal** - wanneer deze optie wordt geselecteerd, worden de radioknopen getoond links aan recht in een AanpassingsVorm.
   - **Verticaal** - wanneer deze optie wordt geselecteerd, worden de radioknopen getoond van boven naar onder in een AanpassingsVorm.
- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **read-only** - selecteer de optie om de component niet-editable te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tabblad Validatie {#validation-tab}

![ het lusje van de Bevestiging ](/help/adaptive-forms/assets/radiobutton_validationtab.png)

- **Vereist** - selecteer deze optie, als u de component in een Aangepaste Vorm wilt tonen. Nadat u de optie hebt geselecteerd, moet u een selectie maken voordat u een formulier kunt verzenden. U kunt niet de **Component van de Verbergen** selecteren of **Component** in het **Basis** lusje onbruikbaar maken wanneer deze optie wordt geselecteerd.
- **Bericht van de Fout** - Deze optie staat u toe om een bericht in te gaan dat wordt getoond als **Vereiste** checkbox wordt gecontroleerd en het vormgebied wordt verlaten leeg.

- **Bericht van de Bevestiging van het Manuscript** - Deze optie staat u toe om een bericht in te gaan dat moet worden getoond als de manuscriptbevestiging ontbreekt.

### Het tabblad Help-inhoud {#helpcontent-tab}

![ Inhoud tabel van de Hulp ](/help/adaptive-forms/assets/radiobutton_helptab.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.

- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}

![ Toegankelijkheid tabel ](/help/adaptive-forms/assets/radiobutton_accessibilitytab.png)

- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.
   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component RadioButton te definiëren en te beheren.


### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De adaptieve component van de Kern van de RadioKnoop van Forms steunt het AEM [ Systeem van de Stijl ](/help/get-started/authoring.md#component-styling).

![ Dialoog van het Ontwerp ](/help/adaptive-forms/assets/checkbox-style.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de Adaptieve Component van de Kern van de RadioKnoop van Forms verstrekken.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![ de Dialoog van Eigenschappen van de Douane ](/help/adaptive-forms/assets/checkbox-customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de orde van de naam van het douanebezit en de waarde van het douanebezit te herschikken.

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
