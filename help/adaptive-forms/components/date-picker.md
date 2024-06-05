---
title: Adaptive Forms Core Component - Datumkiezer
description: De Adaptive Forms Date Picker Core Component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: aa9402de-ca57-4c19-8d36-2dd0a78d6806
source-git-commit: b4a66a407e92398a98441c65ab588b9720777dfa
workflow-type: tm+mt
source-wordcount: '2299'
ht-degree: 0%

---

# component Datumkiezer{#date-picker-adaptive-forms-core-component}

Een component voor de datumkiezer in een adaptief formulier is een interface-element waarmee gebruikers een datum in een kalender kunnen selecteren of een datum handmatig in een specifieke notatie kunnen invoeren. De component van de datumkiezer kan worden gevormd om verschillende het formatteren, bevestiging, en standaardwaarden te hebben.

**Voorbeeld**

![voorbeeld](/help/adaptive-forms/assets/date-picker.png)

## Gebruik {#reasons-to-use-drop-date-picker}

Er zijn verschillende redenen waarom het nuttig is een datumkiezer op te nemen in een adaptief formulier, zoals:

- **Handigheid**: Met een component voor een datumkiezer kunnen gebruikers eenvoudig een datum in een kalender selecteren zonder de datum handmatig in te voeren in een tekstveld. Dit kan tijd besparen en fouten verminderen.

- **Gebruikerservaring**: Met de component Datumkiezer kunt u het formulier gebruiksvriendelijker maken door gebruikers een duidelijke en intuïtieve manier te bieden om de datum te selecteren.

- **Gegevensanalyse**: De component Date Picker kan worden gebruikt om gegevens van diverse bronnen te verzamelen en te analyseren, of het als input voor verdere verwerking te gebruiken.

- **Gebeurtenisbeheer**: De component Date Picker kan in gebeurtenisbeheerwebsites worden gebruikt om de gebeurtenisdatum te selecteren.

- **Boekhouding en reservering**: De component met de datumkiezer kan worden gebruikt voor het maken van boekingen en het reserveren van websites om de datum van inchecken en uitchecken te selecteren.

- **Datumnotatie**: De component van de plukker van de datum kan worden gebruikt om het formaat te bevestigen waarin de datum wordt getoond en ingegaan. Zorg ervoor dat de datumnotatie in het formulier consistent is, zodat de gebruiker er altijd last van heeft.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.12](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Ga voor de meest recente informatie over de Adaptive Forms Date Picker Core Component naar de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de datumkiezer-ervaring voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig opties voor datumkiezers definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![Het tabblad Basis](/help/adaptive-forms/assets/datepicker_basictab.png)

- **Naam** - De naam identificeert uniek de component in de regelredacteur. Speciale tekens en spaties zijn niet toegestaan in de naamtekenreeksen.

- **Titel** - Titel is een tekenreeks die boven aan een component in een adaptief formulier wordt weergegeven. De titel geeft de component in de boomstructuur van een adaptief formulier op unieke wijze aan. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **RTF-tekst voor titel toestaan** - Met deze functies kunnen gebruikers gewone teksttitels opmaken en functies zoals vet, cursief, onderstreepte tekst, diverse lettertypen, tekengrootten, kleuren en extra opties opnemen om de visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Na het selecteren van het selectievakje voor **RTF-tekst voor titel toestaan** worden opmaakopties zichtbaar om de titel van de component op te maken. Als u toegang wilt tot alle beschikbare opmaakopties, klikt u op de knop ![Pictogram Volledig scherm](/help/adaptive-forms/assets/fullscreen-icon.png) tab.

  ![RTF-ondersteuning](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel verbergen** - Selecteer deze optie om de titel van het componenttype in een adaptief formulier te verbergen.

- **Plaatsaanduidingstekst** - Plaatsaanduidingstekst in een formuliercomponent verwijst naar een kort label of een korte vraag die binnen een invoerveld wordt weergegeven als een tip voor de gebruiker met betrekking tot welk type informatie naar verwachting in dat veld wordt ingevoerd. Plaatsaanduidingstekst verdwijnt wanneer de gebruiker in het veld typt en verschijnt opnieuw als het veld leeg blijft. De klasse biedt een visuele aanwijzing voor de gebruiker, maar fungeert niet als een permanent label of een permanente waarde voor het veld.
- **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u met AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

- **Markeren als niet-gebonden formulierelement**: Selecteer de optie om een formulierveld te configureren dat niet is gekoppeld aan een schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.

- **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
- **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **Standaarddatum** - Met deze optie kunt u een datum toevoegen aan het formulierveld. De ingevoerde datum wordt standaard weergegeven op de plaats van de component. Als de gebruiker geen datum invoert, wordt deze waarde verzonden op het moment dat het formulier wordt verzonden. In geval van **Uitgeschakelde component** of **Component (alleen-lezen)** is geselecteerd, wordt de standaarddatum weergegeven op het scherm en verzonden op het moment dat het formulier wordt verzonden.


### Tabblad Validatie {#validation-tab}

![Tabblad Validatie](/help/adaptive-forms/assets/datepicker_validation.png)

- **Vereist** - Selecteer deze optie als u de component wilt weergeven in een adaptief formulier. Nadat u de optie hebt geselecteerd, moet u een selectie maken voordat u een formulier kunt verzenden. U kunt de **Component verbergen** of **Component uitschakelen** in de **Basis** als deze optie is geselecteerd.

- **Foutbericht** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de optie **Vereist** wordt ingeschakeld en wordt het formulierveld leeg gelaten.

- **Bericht voor scriptvalidatie** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de scriptvalidatie mislukt.

- **Minimumdatum** - Met deze optie kunt u de minimaal vereiste datum invoeren. Als u een datum vóór de in Minimumdatum opgegeven datum invoert, verschijnt er een foutbericht op het scherm. De **Minimale foutmelding** kunt u een aangepast foutbericht toevoegen.

- **Minimale foutmelding** - de **Minimale foutmelding** kunt u een aangepast foutbericht toevoegen dat moet worden weergegeven als u een eerdere datum invoert dan de datum die is opgegeven in het dialoogvenster **Minimumdatum** -optie.
- **Minimumdatum uitsluiten** - Met deze optie kunt u de minimumdatum weglaten in een bepaald bereik of een bepaalde set datums.

- **Maximumdatum** - Met deze optie kunt u de maximaal vereiste datum invoeren. Als u een datum later dan de datum ingaat die in MaximumDatum wordt gespecificeerd, verschijnt een foutenmelding op het scherm. De **Maximum foutbericht** kunt u een aangepast foutbericht toevoegen.

- **Maximum foutbericht** - de **Maximum foutbericht** kunt u een aangepast foutbericht toevoegen dat wordt weergegeven als u een datum later dan de datum invoert die in het dialoogvenster **Maximumdatum** -optie.

- **Maximumdatum uitsluiten** - Met deze optie kunt u de maximumdatum in een bepaald bereik of een bepaalde set datums weglaten.

### Het tabblad Help-inhoud {#help-content-tab}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/datepicker_helptab.png)

- **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de achtergrondafbeelding onder de component weer te geven.

- **Altijd korte beschrijving tonen**- Schakel de optie in om de korte beschrijving onder de component weer te geven.

- **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.


### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

- **Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.
   - **Aangepaste tekst**: Selecteer deze optie als u de aangepaste tekst voor toegankelijkheidslabels in ARIA wilt gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie als u de beschrijving voor toegankelijkheidslabels van ARIA wilt gebruiken.
   - **Titel**: Selecteer deze optie als u de titel voor toegankelijkheidslabels in ARIA wilt gebruiken.
   - **Naam**: Selecteer deze optie als u de naam voor toegankelijkheidslabels van ARIA wilt gebruiken.
   - **Geen**: Selecteer deze optie als u geen toegankelijkheidslabels voor ARIA wilt toevoegen.

### Tabblad Opmaak {#format-tab}

![Tabblad Indelingen](/help/adaptive-forms/assets/datepicker_formattab.png)

- **Weergave-indeling** - Het staat voor de datumnotatie die aan de gebruiker wordt weergegeven. De **Type** kan de gebruiker de datumnotatie selecteren. U kunt de datumnotatie ook aanpassen met de opdracht **Aangepast** in de **Type** vervolgkeuzelijst.

- **Opmaak bewerken** - Dit is een datumnotatie waarin de gebruiker de datum kan bewerken. De **Type** kan de gebruiker de datumnotatie selecteren. U kunt de datumnotatie ook aanpassen met de opdracht **Aangepast** in de **Type** vervolgkeuzelijst.
- **Foutbericht opmaken** - Met deze optie kunt u het bericht invoeren dat op het scherm wordt weergegeven wanneer de ingevoerde datum niet de juiste notatie heeft.
- **Taal** - Deze functie wordt gebruikt voor het opmaken van het specifieke veld. Wanneer een gebruiker een taaloptie selecteert in het menu **Type** vervolgkeuzemenu, **Taaltag IETF BCP 47** wordt weergegeven in het deelvenster. U kunt de taal voor veldopmaak kiezen wanneer u een adaptief formulier in een specifieke taal vertaalt.

De set talen is standaard niet zichtbaar, maar gebruikers kunnen een aangepaste set invoeren **Taaltag IETF BCP 47** door het sjabloonbeleid bij te werken:

1. Open de bijbehorende sjabloon die aan een adaptief formulier is gekoppeld in de sjablooneditor.
2. Het bestaande beleid selecteren als `datepicker-default-policy` in het keuzemenu.

   ![Sjabloonbeleid datumkiezer](/help/adaptive-forms/assets/date-picker-template-policy.png)

3. Klikken **Gereed**.

   >[!NOTE]
   >
   > Voor meer informatie over het vertalen van een adaptief formulier naar een specifieke landinstelling, [klik hier](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components).

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Date-Picker te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Date-Picker Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Het tabblad Stijl](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Date-picker Core Component.

- **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![Dialoogvenster Aangepaste eigenschappen](/help/adaptive-forms/assets/datepicker_customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Groepsnaam**: U kunt een naam opgeven om de groep met aangepaste eigenschappen te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **Belangrijke paren**: U kunt meerdere aangepaste eigenschapnamen en aangepaste eigenschapswaarden toevoegen door op de knop **Toevoegen** knop voor elke aangepaste groep eigenschappen.

   - **Verwijderen**: Tik of klik om de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te verwijderen.

   - **Opnieuw rangschikken**: Tik of klik en sleep om de volgorde van de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te wijzigen.

### Tabblad Opmaak {#formats-tab}

Op het tabblad Indelingen kunt u standaard- en aangepaste datumnotaties opgeven.

![Formattab](/help/adaptive-forms/assets/datepicker_formatpolicy.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}


