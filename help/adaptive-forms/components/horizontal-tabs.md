---
title: Adaptive Forms Core Component - Horizontale tabbladen
description: De Adaptive Forms Horizontal tabs Core Component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: fbdf330b-3b85-4f94-9dab-eea8465fba67
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1609'
ht-degree: 0%

---

# Horizontale tabbladen {#horizontal-tabs-adaptive-forms-core-component}

Horizontale tabbladen in een adaptief formulier verwijzen naar een ontwerppatroon waarbij meerdere secties van een formulier zijn gegroepeerd en worden weergegeven als afzonderlijke tabbladen, die horizontaal zijn uitgelijnd. De gebruiker kan schakelen tussen de tabbladen om toegang te krijgen tot verschillende secties van het formulier. Elk tabblad fungeert als trigger voor het weergeven en verbergen van de gerelateerde formulierinhoud. Met de horizontale tabbladen kunt u lange formulieren ordenen in hanteerbare gedeelten en de gebruikerservaring verbeteren. Tabs kunnen ertoe bijdragen dat een formulier toegankelijker wordt voor gebruikers met een handicap, aangezien ze met behulp van toetsenbordnavigatie tussen secties kunnen schakelen.

De tabbladen worden meestal gemaakt als een reeks koppelingen of knoppen, waarbij elke koppeling of knop overeenkomt met een sectie van het formulier. Wanneer een gebruiker op een tabblad klikt, wordt de formulierinhoud dynamisch bijgewerkt om de corresponderende sectie weer te geven.

## Gebruik {#reasons-to-use-horizontal-tabs}

De algemene redenen voor het gebruik van horizontale tabbladen in een adaptieve vorm zijn:

* **Verbeterde bruikbaarheid**: Met horizontale tabbladen kunnen gebruikers gemakkelijker door het formulier navigeren, vooral als het formulier meerdere secties of een groot aantal velden bevat.

* **Ruimtebeheer**: Met horizontale tabbladen bespaart u de schermruimte door gerelateerde formuliersecties in tabbladen te groeperen en slechts één sectie tegelijk weer te geven.

* **Betere organisatie**: Tabs bieden een duidelijke en georganiseerde structuur voor een formulier, zodat gebruikers het formulier eenvoudiger kunnen begrijpen en invullen.

* **Grotere betrokkenheid van gebruikers**: Met horizontale tabbladen kan een formulier visueel aantrekkelijker en aantrekkelijker worden voor gebruikers, wat de voltooiingssnelheid van het formulier kan verbeteren.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.12](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Core Components-versies](/help/adaptive-forms/version.md) document.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technische details {#technical-details}

Lees de nieuwste informatie over de Adaptive Forms Horizontal tabs Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageHorizontal tabs/v1/pageHorizontal tabs). Raadpleeg de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de ervaring van horizontale tabbladen eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig opties voor horizontale tabbladen definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![Het tabblad Basis](/help/adaptive-forms/assets/tabsontop_basictab.png)

* **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

* **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

* **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.

* **Gegevens in object laten teruglopen** - Kies &quot;Gegevens laten teruglopen in een object&quot; om de veldgegevens in de wizard in een JSON-object te plaatsen. Als deze optie niet is gekozen, heeft de verzendgegevens-JSON een platte structuur voor de velden van de wizard.

* **Layout** - U kunt een vaste lay-out (Eenvoudig) of een flexibele lay-out (Responsief raster) voor uw wizard gebruiken. De eenvoudige lay-out houdt alles vast op de plaats, terwijl het Responsieve Net u toestaat om de positie van componenten aan uw behoeften aan te passen. Gebruik bijvoorbeeld Responsief raster om &quot;Voornaam&quot;, &quot;Tweede naam&quot; en &quot;Achternaam&quot; in één rij uit te lijnen in een formulier.

* **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.
* **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
* **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tabblad Items {#items-tab}

![Tabblad Items](/help/adaptive-forms/assets/tabsontop_itemstab.png)

De **Toevoegen** kunt u een component selecteren om als deelvenster toe te voegen vanuit het selectievenster van de component. Nadat u de component hebt toegevoegd, kunt u de volgende opties zien:

* **Pictogram** - Het pictogram geeft de component van het deelvenster in de lijst aan. U kunt de muisaanwijzer boven het pictogram plaatsen om de volledige naam van de component als knopinfo weer te geven.
* **Beschrijving** - De beschrijving die wordt gebruikt als de tekst van het deelvenster. Standaard is dit de naam van de component die voor het deelvenster is geselecteerd.
* **Verwijderen** - Tik of klik om het deelvenster uit de horizontale tabcomponent te verwijderen.
* **Opnieuw rangschikken** - Tik of klik en sleep om de volgorde van de deelvensters te wijzigen.

### Het tabblad Help-inhoud {#help-content}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/tabsontop_helptab.png)

* **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de component onder de component weer te geven.

* **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

* **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/tabsontop_accessibilitytab.png)

* **Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

* **HTML-rol voor schermlezer om aan te kondigen** - De rol HTML is een kenmerk dat wordt gebruikt om het doel van een element HTML aan ondersteunende hulpmiddelen, zoals schermlezers, op te geven. Het rolattribuut wordt gebruikt om extra context en semantische betekenis aan een element te verstrekken, die het voor schermlezers gemakkelijker maken om de inhoud te interpreteren en aan de gebruiker aan te kondigen. In AEM Forms heeft het label van een formulierveld bijvoorbeeld de rol &quot;label&quot; en kan het invoerveld de rol &quot;textbox&quot; hebben. Hierdoor kan de schermlezer de relatie tussen het label en het invoerveld begrijpen en deze correct aan de gebruiker meedelen.

## Ontwerpdialoogvenster {#design-dialog}

De dialoog van het Ontwerp laat malplaatjemakers controleren hoe de dingen door gebrek worden getoond. Voor de Adaptieve Forms-component kunt u het volgende instellen:

* De kerncomponenten die een maker van een formulier kan toevoegen aan de horizontale tabbladen in de Adaptive Forms Editor
* Eenvoudige namen voor stijlen (CSS-klassen) die kunnen worden toegepast in het dialoogvenster met eigenschappen van de component met horizontale tabbladen in de Adaptieve Forms-editor.

Hierdoor wordt het maken en aanpassen van formulieren eenvoudiger en efficiënter.

### Tabblad Toegestane componenten {#allowed-components-tab}

De **Toegestane componenten** kunt u in de sjablooneditor de componenten instellen die als items kunnen worden toegevoegd aan de deelvensters in de component Horizontale tabbladen in de Adaptieve Forms-editor.

![Horizontale tabbladen](/help/adaptive-forms/assets/horizontaltabs_designdilog.png)

### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Horizontal tabs Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Het tabblad Stijl](/help/adaptive-forms/assets/horizontaltabs_designstyletab.png)

* **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Horizontal tabs Core Component.

* **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight&quot; opgeven: vet&quot;. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.
