---
title: Adaptive Forms Core Component - Datumkiezer
description: De Adaptive Forms Date Picker Core Component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: aa9402de-ca57-4c19-8d36-2dd0a78d6806
source-git-commit: daeabccaff39e255c111c6af2540ca4d5be0c709
workflow-type: tm+mt
source-wordcount: '2298'
ht-degree: 0%

---


# component Datumkiezer{#date-picker-adaptive-forms-core-component}

Een component voor de datumkiezer in een adaptief formulier is een interface-element waarmee gebruikers een datum in een kalender kunnen selecteren of een datum handmatig in een specifieke notatie kunnen invoeren. De component van de datumkiezer kan worden gevormd om verschillende het formatteren, bevestiging, en standaardwaarden te hebben.

**Voorbeeld**

![&#x200B; voorbeeld &#x200B;](/help/adaptive-forms/assets/date-picker.png)

## Gebruik {#reasons-to-use-drop-date-picker}

Er zijn verschillende redenen waarom het nuttig is een datumkiezer op te nemen in een adaptief formulier, zoals:

- **Handigheid**: Een component van de datumkiezer staat gebruikers toe om een datum van een kalender gemakkelijk te selecteren zonder het moeten de datum op een tekstgebied manueel ingaan. Dit kan tijd besparen en fouten verminderen.

- **Ervaring van de Gebruiker**: De component van de plukker van de datum kan worden gebruikt om de vorm gebruikersvriendelijker te maken door een duidelijke en intuïtieve manier voor gebruikers te verstrekken om datum te selecteren.

- **analyse van Gegevens**: De component van de plukker van de datum kan worden gebruikt om gegevens uit diverse bronnen te verzamelen en het te analyseren, of het als input voor verdere verwerking te gebruiken.

- **Gebeurtenisbeheer**: De component van de plukker van de datum kan in gebeurtenisbeheerwebsites worden gebruikt om de gebeurtenisdatum te selecteren.

- **Boek en reserve**: De component van de plukker van de datum kan in boekings en reserveringswebsites worden gebruikt om de controle-binnen en controledata te selecteren.

- **formaat van de Datum**: De component van de plukker van de Datum kan worden gebruikt om het formaat te bevestigen waarin de datum wordt getoond en ingegaan. Zorg ervoor dat de datumnotatie in het formulier consistent is, zodat de gebruiker er altijd last van heeft.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Date picker Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 voor Cloud Service en Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM-compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel systeem met <br>[&#x200B; versie 2.0.4 &#x200B;](/help/adaptive-forms/version.md) en later | Compatibel met <br>[&#x200B; versie 1.1.12 &#x200B;](/help/adaptive-forms/version.md) en later maar minder dan 2.0.0. |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het [&#x200B; document van de Versies van de Componenten van de Kern 0&rbrace;.](/help/adaptive-forms/version.md)

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Krijg de recentste informatie over de AanpassingsComponent van de Kern van de Plukker van de Datum van Forms in de technische documentatie op [&#x200B; GitHub &#x200B;](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [&#x200B; de ontwikkelaarsdocumentatie van de Componenten van de Kern &#x200B;](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de datumkiezer-ervaring voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig opties voor datumkiezers definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![&#x200B; Basis lusje &#x200B;](/help/adaptive-forms/assets/datepicker_basictab.png)

- **Naam** - de naam identificeert uniek de component in de regelredacteur. Speciale tekens en spaties zijn niet toegestaan in de naamtekenreeksen.

- **Titel** - de Titel is een koord dat bij de bovenkant van een component in een Aangepaste Vorm verschijnt. De titel geeft de component in de boomstructuur van een adaptief formulier op unieke wijze aan. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **staat RTF voor Titel** toe - Deze eigenschappen laat gebruikers toe om gewone teksttitels te formatteren, die eigenschappen zoals vette, cursieve, onderstreepte tekst, diverse doopvonten, doopvontgrootte, kleuren, en extra optie opnemen om visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Op het selecteren van checkbox voor **staat RTF-tekst voor Titel** toe, wordt het formatteren opties zichtbaar om de titel van de component te stileren. Om tot alle beschikbare het formatteren opties toegang te hebben, kunt u op het ![&#x200B; pictogram Volledig scherm &#x200B;](/help/adaptive-forms/assets/fullscreen-icon.png) tabel klikken.

  ![&#x200B; de rijke tekststeun van 0&rbrace;](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel van de Huid** - selecteer deze optie om titel van het componenttype in een Aangepaste Vorm te verbergen.

- **Plaatsaanduidingstekst** - De placeholder tekst in een vormcomponent verwijst naar een kort etiket of een herinnering die binnen een inputgebied als wenk aan de gebruiker verschijnt op welk type van informatie naar verwachting op dat gebied zal zijn ingegaan. Plaatsaanduidingstekst verdwijnt wanneer de gebruiker in het veld typt en verschijnt opnieuw als het veld leeg blijft. De klasse biedt een visuele aanwijzing voor de gebruiker, maar fungeert niet als een permanent label of een permanente waarde voor het veld.
- **Bind Verwijzing** - A bindt verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u met AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

- **Teken als Niet-gebonden Element van de Vorm**: Selecteer de optie om een vormgebied te vormen niet verbonden aan om het even welk schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.

- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **read-only** - selecteer de optie om de component niet-editable te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **StandaardDatum** - deze optie staat u toe om een datum aan het vormgebied toe te voegen. De ingevoerde datum wordt standaard weergegeven op de plaats van de component. Als de gebruiker geen datum invoert, wordt deze waarde verzonden op het moment dat het formulier wordt verzonden. In het geval **Gehandicapte Component** of **read-only Component** wordt geselecteerd, wordt de standaarddatum getoond op het scherm en voorgelegd op het tijdstip van vormvoorlegging.


### Tabblad Validatie {#validation-tab}

![&#x200B; het lusje van de Bevestiging &#x200B;](/help/adaptive-forms/assets/datepicker_validation.png)

- **Vereist** - selecteer deze optie, als u de component in een Aangepaste Vorm wilt tonen. Nadat u de optie hebt geselecteerd, moet u een selectie maken voordat u een formulier kunt verzenden. U kunt niet de **Component van de Verbergen** selecteren of **Component** in het **Basis** lusje onbruikbaar maken wanneer deze optie wordt geselecteerd.

- **Bericht van de Fout** - Deze optie staat u toe om een bericht in te gaan dat wordt getoond als **Vereiste** checkbox wordt gecontroleerd en het vormgebied wordt verlaten leeg.

- **Bericht van de Bevestiging van het Manuscript** - Deze optie staat u toe om een bericht in te gaan dat moet worden getoond als de manuscriptbevestiging ontbreekt.

- **Minimale Datum** - deze optie staat u toe om de minimaal vereiste datum in te gaan. Als u een datum vóór de in Minimumdatum opgegeven datum invoert, verschijnt er een foutbericht op het scherm. Het **Minimale de dialoogvakje van het Bericht van de Fout** staat u toe om een bericht van de douanefout toe te voegen.

- **Minimale Bericht van de Fout** - het **Minimale de dialoogvakje van het Bericht van de Fout** staat u toe om een te tonen douanefoutenmelding toe te voegen, als u een datum vroeger dan de datum ingaat die in de **Minimale optie van de Datum** wordt gespecificeerd.
- **sluit minimumdatum** uit - deze optie staat toe om de minimumdatum in een bepaalde waaier of een reeks data weg te laten.

- **Maximale Datum** - deze optie staat u toe om de maximum vereiste datum in te gaan. Als u een datum later dan de datum ingaat die in MaximumDatum wordt gespecificeerd, verschijnt een foutenmelding op het scherm. Het **Maximale de dialoogvakje van het Bericht van de Fout** staat u toe om een bericht van de douanefout toe te voegen.

- **MaximumBericht van de Fout** - het **Maximale de dialoogvakje van het Bericht van de Fout** staat u toe om een te tonen douanefoutenmelding toe te voegen, als u een datum later dan de datum ingaat die in de **MaximumDatum** optie wordt gespecificeerd.

- **sluit maximumdatum** uit - deze optie staat toe om de maximumdatum in een bepaalde waaier of een reeks data weg te laten.

### Het tabblad Help-inhoud {#help-content-tab}

![&#x200B; Inhoud tabel van de Hulp &#x200B;](/help/adaptive-forms/assets/datepicker_helptab.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.

- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.


### Tabblad Toegankelijkheid {#accessibility-tab}

![&#x200B; Toegankelijkheid tabel &#x200B;](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.
   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.

### Tabblad Opmaak {#format-tab}

![&#x200B; Formaten tabel &#x200B;](/help/adaptive-forms/assets/datepicker_formattab.png)

- **Formaat van de Vertoning** - het vertegenwoordigt het datumformaat dat aan de gebruiker wordt getoond. De **optie van het Type** staat de gebruiker toe om het datumformaat te selecteren. U kunt het datumformaat ook aanpassen gebruikend de **optie van de Douane** in het **Type** dropdown menu.

- **geeft Formaat** uit - het vertegenwoordigt een datumformaat waarin de gebruiker de datum kan uitgeven. De **optie van het Type** staat de gebruiker toe om het datumformaat te selecteren. U kunt het datumformaat ook aanpassen gebruikend de **optie van de Douane** in het **Type** dropdown menu.
- **de foutenmelding van het Formaat** - Deze optie staat u toe om het bericht in te gaan dat op het scherm wordt getoond wanneer de ingegaan datum niet in het correcte formaat is.
- **Taal** - deze eigenschap wordt gebruikt voor het formatteren van het specifieke gebied. Wanneer een gebruiker om het even welke taaloptie van het **Type** drop-down menu selecteert, verschijnt de **IETF BCP 47 taalmarkering** optie in het paneel. U kunt de taal voor veldopmaak kiezen wanneer u een adaptief formulier in een specifieke taal vertaalt.

De reeks talen is niet zichtbaar door gebrek, maar de gebruikers kunnen een douane **IETF BCP 47 taalmarkering** invoeren door het malplaatjebeleid bij te werken:

1. Open de bijbehorende sjabloon die aan een adaptief formulier is gekoppeld in de sjablooneditor.
2. Selecteer het bestaande beleid als `datepicker-default-policy` in de keuzelijst.

   ![&#x200B; het malplaatjebeleid van de Plukker van de Datum &#x200B;](/help/adaptive-forms/assets/date-picker-template-policy.png)

3. Klik **Gedaan**.

   >[!NOTE]
   >
   > Voor verdere informatie over hoe te om een AanpassingsVorm aan een specifieke scène te vertalen, [&#x200B; klik hier &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components).

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Date-Picker te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De adaptieve de datum-plukkerComponent van de Kern van Forms steunt het systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

![&#x200B; lusje van de Stijl &#x200B;](/help/adaptive-forms/assets/datepicker_styletab.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de AanpassingsForms Datum-plukker Component van de Kern verstrekken.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![&#x200B; de Dialoog van Eigenschappen van de Douane &#x200B;](/help/adaptive-forms/assets/datepicker_customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de orde van de naam van het douanebezit en de waarde van het douanebezit te herschikken.

### Tabblad Opmaak {#formats-tab}

Op het tabblad Indelingen kunt u standaard- en aangepaste datumnotaties opgeven.

![&#x200B; Formattab &#x200B;](/help/adaptive-forms/assets/datepicker_formatpolicy.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=nl-NL)

-->

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}


