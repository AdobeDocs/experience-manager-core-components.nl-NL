---
title: Adaptive Forms Core Component - Wizard
description: De Adaptive Forms Wizard Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: fd785cd2-5ed6-4efb-997f-ce9056ed113d
source-git-commit: 8388de05c86641d4887b48a9fd10901cb5a19998
workflow-type: tm+mt
source-wordcount: '2025'
ht-degree: 0%

---

# Wizard {#wizard-adaptive-forms-core-component}

Een wizardindeling in een adaptief formulier verwijst naar een formulier dat is verdeeld in meerdere stappen of pagina&#39;s, waarbij de gebruiker stap voor stap door het formulier beweegt. Deze indeling wordt een &quot;wizard&quot; genoemd omdat deze de gebruiker in een stapsgewijs proces door het formulier begeleidt.

Elke stap van de wizard bevat doorgaans een groep gerelateerde formuliervelden en een navigatiemechanisme, zoals de knoppen Volgende en Vorige, waarmee u tussen de stappen kunt navigeren. De gebruiker kan pas verdergaan naar de volgende stap nadat de huidige stap is voltooid en alle vereiste velden zijn ingevuld.

De indeling van de wizard is handig voor formulieren met veel velden of gegevens die moeten worden verzameld, omdat het formulier dan wordt opgedeeld in kleinere, beter te beheren blokken. Hiermee kunnen gebruikers zich ook op één set velden tegelijk concentreren, waardoor het invullen van het formulier minder overweldigend wordt.

Het kan echter ook de complexiteit van het formulier vergroten, omdat de gebruiker meerdere pagina&#39;s moet doorlopen om het formulier in te vullen. Het is dus noodzakelijk om de formuliervereisten en gebruikersbehoeften te evalueren voordat u besluit een wizardindeling te gebruiken.

Met de Core-component voor de wizardlay-out kunt u in een adaptief formulier de wizardlay-out maken.


**Voorbeeld**

![voorbeeld](/help/adaptive-forms/assets/wizard.png)

## Gebruik {#reasons-to-use-wizard-in-an-adaptive-form}

Er zijn verscheidene redenen waarom het nuttig kan zijn om een lay-out van de Tovenaar in een AanpassingsVorm te gebruiken:

- **Eenvoud**: Door een formulier in meerdere stappen in te delen, kunnen gebruikers het formulier eenvoudiger begrijpen en voltooien, omdat ze zich tegelijk op één set velden kunnen concentreren.

- **Organisatie**: De indeling van een wizard kan u helpen formulieren op onderwerp of doel in te delen en kan ook gerelateerde velden groeperen, waardoor het invullen van formulieren logischer en efficiënter kan verlopen.

- **Validatie**: Een wizardlay-out staat voor geleidelijke bevestiging toe, die gebruikers kan helpen fouten identificeren en verbeteren aangezien zij gaan, eerder dan het wachten tot het eind van de vorm.

- **Voortgangsindicator**: De indeling van een wizard kan de voortgang van het formulier weergeven, zodat de gebruiker kan zien hoeveel van het formulier nog moet worden ingevuld.

- **Lange formulieren**: Als het formulier veel velden bevat, kan het voor de gebruiker overweldigend zijn om ze allemaal tegelijk te zien, zodat het intimideren van het formulier in kleinere, beter te beheren brokken minder intimiderend kan zijn.

- **Afschaffing voorkomen**: Een indeling van een wizard kan ook helpen het verlaten van formulieren te verminderen, aangezien gebruikers waarschijnlijk een formulier zullen invullen als ze de voortgang kunnen zien en kunnen begrijpen hoeveel er nog moet gebeuren.

- **Mobiele ervaring**: Een wizardlay-out kan ook nuttig zijn voor formulieren die worden geopend op mobiele apparaten, omdat het formulieren toestaat voor kleinere pagina&#39;s die sneller worden geladen en waarmee u gemakkelijker kunt navigeren.

Over het algemeen kan een wizardindeling het invullen van formulieren overzichtelijker en efficiënter maken voor gebruikers, maar het is belangrijk om rekening te houden met de complexiteit van het formulier en de behoeften van de gebruiker voordat u besluit om dit type indeling te gebruiken.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Wizard Layout Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | — |
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Lees de nieuwste informatie over de Adaptive Forms Title Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/wizard/v1/wizard). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de tovenaarservaring eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig wizardopties definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![Het tabblad Basis](/help/adaptive-forms/assets/wizard-basic.png)

- **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven.

- **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.

- **Gegevens in een object laten omlopen** - Kies &quot;Gegevens laten teruglopen in een object&quot; om de veldgegevens in de wizard in een JSON-object te plaatsen. Als deze optie niet is gekozen, heeft de verzendgegevens-JSON een platte structuur voor de velden van de wizard.

- **Layout** - U kunt een vaste lay-out (Eenvoudig) of een flexibele lay-out (Responsief raster) voor uw wizard gebruiken. De eenvoudige lay-out houdt alles vast op de plaats, terwijl het Responsieve Net u toestaat om de positie van componenten aan uw behoeften aan te passen. Gebruik bijvoorbeeld Responsief raster om &quot;Voornaam&quot;, &quot;Tweede naam&quot; en &quot;Achternaam&quot; in één rij uit te lijnen in een formulier.

- **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u met AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

- **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

- **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tabblad Wizard Herhalen {#repeat-wizard-tab}

![Wizard Herhalen](/help/adaptive-forms/assets/wizard-repeat.png)

Met de opties voor herhaling kunt u de wizard en de onderliggende componenten dupliceren, een minimum- en maximumaantal herhalingen definiëren en de replicatie van vergelijkbare secties in een formulier vergemakkelijken. Wanneer het in wisselwerking staan met de component van de Tovenaar en de toegang tot van zijn montages, worden de volgende opties voorgesteld:

- **Wizard herhaalbaar maken**: Een schakelfunctie waarmee gebruikers de herhaalbaarheidsfunctionaliteit kunnen in- of uitschakelen.
- **Minimale herhalingen**: Hiermee stelt u het minimale aantal keren in dat het deelvenster Wizard kan worden herhaald. De waarde nul geeft aan dat het deelvenster Wizard niet wordt herhaald; de standaardwaarde is nul.
- **Maximale herhalingen**: Hiermee stelt u in hoe vaak het deelvenster Wizard kan worden herhaald. Deze waarde is standaard onbeperkt.

Om herhaalbare secties binnen de Tovenaar effectief te beheren, volg de stappen die in worden verstrekt [Formulieren maken met herhaalbare secties](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html) artikel.

### Tabblad Items {#items-tab}

![Tabblad Items](/help/adaptive-forms/assets/wizard_helptab.png)

Met deze optie kunt u componenten Adaptief formulier toevoegen door op de knop Toevoegen te klikken. Deze knop wordt standaard weergegeven wanneer de wizard wordt toegevoegd in de bewerkingsmodus.

### Help, tabblad {#help-tab}

![Het tabblad Help](/help/adaptive-forms/assets/wizard_helptab.png)

- **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de achtergrondafbeelding onder de component weer te geven.

- **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

- **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.


### Tabblad Toegankelijkheid {#accessibility}

![Tabblad Toegankelijkheid](/help/adaptive-forms/assets/wizard_accessibiltytab.png)

- **Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

- **HTML-rol voor schermlezer om aan te kondigen** - De rol HTML is een kenmerk dat wordt gebruikt om het doel van een element HTML aan ondersteunende hulpmiddelen, zoals schermlezers, op te geven. Het rolattribuut wordt gebruikt om extra context en semantische betekenis aan een element te verstrekken, die het voor schermlezers gemakkelijker maken om de inhoud te interpreteren en aan de gebruiker aan te kondigen. In AEM Forms heeft het label van een formulierveld bijvoorbeeld de rol &quot;label&quot; en kan het invoerveld de rol &quot;textbox&quot; hebben. Hierdoor kan de schermlezer de relatie tussen het label en het invoerveld begrijpen en deze correct aan de gebruiker meedelen.


## Ontwerpdialoogvenster {#design-dialog}

De dialoog van het Ontwerp laat malplaatjemakers controleren hoe de dingen door gebrek worden getoond. Voor de component Adaptive Forms Wizard kunt u het volgende instellen:

- De kerncomponenten die een maker van het formulier aan de wizard kan toevoegen in de Adaptive Forms-editor
- Eenvoudige namen voor stijlen (CSS-klassen) die kunnen worden toegepast in het dialoogvenster met eigenschappen van de component Wizard in de Adaptive Forms-editor.

Hierdoor wordt het maken en aanpassen van formulieren eenvoudiger en efficiënter.

### Tabblad Toegestane componenten {#allowed-components-tab}

![Tabblad Toegestane componenten](/help/adaptive-forms/assets/tabs-allowed-component.png)

De **Toegestane componenten** kunt u in de sjablooneditor de componenten instellen die als items kunnen worden toegevoegd aan de deelvensters in de wizard-component in de Adaptieve Forms-editor.

### Tabblad Stijlen {#styles-tab}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Wizard Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Het tabblad Stijlen](/help/adaptive-forms/assets/tabs-styles-tab.png)

- **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms wizard Core Component.

- **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Tabblad Aangepaste eigenschappen

![Tabblad Aangepaste eigenschappen](/help/adaptive-forms/assets/tabs-custom-properties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Groepsnaam**: U kunt een naam opgeven om de groep met aangepaste eigenschappen te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **Belangrijke paren**: U kunt meerdere aangepaste eigenschapnamen en aangepaste eigenschapswaarden toevoegen door op de knop **Toevoegen** knop voor elke aangepaste groep eigenschappen.

   - **Verwijderen**: Tik of klik om de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te verwijderen.

   - **Opnieuw rangschikken**: Tik of klik en sleep om de volgorde van de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te wijzigen.

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}