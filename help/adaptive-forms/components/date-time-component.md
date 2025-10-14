---
title: Adaptieve Forms Core-component - Datum en tijd
description: De Adaptive Forms Date & Time Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
source-git-commit: daeabccaff39e255c111c6af2540ca4d5be0c709
workflow-type: tm+mt
source-wordcount: '1898'
ht-degree: 0%

---


# Datum- en tijdcomponent

Een component van de Datum &amp; van de Tijd in een AanpassingsVorm is een gebruikersinterface element dat gebruikers toestaat om zowel **datum en tijd** te selecteren gebruikend een kalender en klokinterface, of door waarden in een specifiek formaat manueel in te gaan. Het zorgt voor nauwkeurige, gestandaardiseerde input voor gebruiksgevallen waarin zowel datum als tijd van essentieel belang zijn.

**Voorbeeld**

![&#x200B; voorbeeld &#x200B;](/help/adaptive-forms/assets/date-time-picker.png)

## Gebruik {#reasons-to-use-date-time-picker}

Er zijn verschillende redenen waarom het nuttig is een datum- en tijdkiezer op te nemen in een formulier, zoals:

- **Handigheid**: Staat gebruikers toe om zowel een datum als tijd gemakkelijk te kiezen zonder het moeten waarden manueel typen.
- **Consistentie**: Dwingt een standaardformaat voor datum en tijdinput over de vorm.
- **Verbeterde gebruikerservaring**: Verstrekt een intuïtieve UI van kalender en tijdselecteurs.
- **Gebeurtenis die** plant: Nuttig in benoeming het boeken, interviews, of vergadering het plannen vormen.
- **Reizen &amp; reserveringen**: Laat gebruikers toe om controle-binnen te selecteren/controledata en tijden.
- **de nauwkeurigheid van Gegevens**: Vermindert inputfouten vergeleken met vrije-tekstingang.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptieve Component van de Kern van de Datum en van de Tijd van Forms werd vrijgegeven in **Augustus 2025** als deel van **Componenten 2.24.6 van de Kern** voor Cloud Service en later.

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel systeem met <br>[&#x200B; versie 2.24.6 &#x200B;](/help/adaptive-forms/version.md) en later | |

Voor details op versies, zie {de Versies van de Componenten van 0} Kern [.](/help/adaptive-forms/version.md)

## Technische details {#technical-details}

Krijg de recentste technische details op de Adaptieve Component van de Kern van de Datum en van de Tijd van Forms op [&#x200B; GitHub &#x200B;](https://github.com/adobe/aem-core-forms-components). Voor meer bij het ontwikkelen van de Componenten van de Kern, zie {de ontwikkelaarsdocumentatie van de Componenten van 0} Kern [.](/help/developing/overview.md)

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kunt u de datum en tijd aanpassen.

### Tabblad Standaard {#basic-tab}

![&#x200B; Basis lusje &#x200B;](/help/adaptive-forms/assets/datetime_basictab.png)

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
- **Standaard Datum en Tijd** - deze optie staat u toe om een datum en een tijd aan het vormgebied toe te voegen. De ingevoerde datum wordt standaard weergegeven op de plaats van de component. Als de gebruiker geen datum of tijd heeft ingevoerd, wordt deze waarde verzonden op het moment dat het formulier wordt verzonden. In het geval **Gehandicapte Component** of **read-only Component** wordt geselecteerd, wordt de standaarddatum en de tijd getoond op het scherm en voorgelegd op het tijdstip van vormvoorlegging.

### Tabblad Validatie {#validation-tab}

![&#x200B; het lusje van de Bevestiging &#x200B;](/help/adaptive-forms/assets/datetime_validation.png)

- **Vereist** - selecteer deze optie, als u de component in een Aangepaste Vorm wilt tonen. Nadat u de optie hebt geselecteerd, moet u een selectie maken voordat u een formulier kunt verzenden. U kunt niet de **Component van de Verbergen** selecteren of **Component** in het **Basis** lusje onbruikbaar maken wanneer deze optie wordt geselecteerd.

- **Bericht van de Fout** - Deze optie staat u toe om een bericht in te gaan dat wordt getoond als **Vereiste** checkbox wordt gecontroleerd en het vormgebied wordt verlaten leeg.

- **Bericht van de Bevestiging van het Manuscript** - Deze optie staat u toe om een bericht in te gaan dat moet worden getoond als de manuscriptbevestiging ontbreekt.

- **Minimale Datum** - deze optie staat u toe om de minimaal vereiste datum in te gaan. Als u een datum vroeger dan de datum ingaat die in MinimumDatum en Tijd wordt gespecificeerd, verschijnt een foutenmelding op het scherm. Het **Minimale de dialoogvakje van het Bericht van de Fout** staat u toe om een bericht van de douanefout toe te voegen.

- **Minimale Bericht van de Fout** - het **Minimale de dialoogvakje van het Bericht van de Fout** staat u toe om een te tonen douanefoutenmelding toe te voegen, als u een datum of een tijd vroeger dan de datum of de tijd ingaat die in de **Minimale Datum** optie wordt gespecificeerd.

- **Maximale Datum** - deze optie staat u toe om de maximum vereiste datum en de tijd in te gaan. Als u een datum of tijd later dan de datum of tijd ingaat die in MaximumDatum wordt gespecificeerd, verschijnt een foutenmelding op het scherm. Het **Maximale de dialoogvakje van het Bericht van de Fout** staat u toe om een bericht van de douanefout toe te voegen.

- **MaximumBericht van de Fout** - het **Maximale de dialoogvakje van het Bericht van de Fout** staat u toe om een te tonen douanefoutenmelding toe te voegen, als u een datum of een tijd later dan de datum of de tijd ingaat die in de **Maximale Datum** optie wordt gespecificeerd.

### Het tabblad Help-inhoud {#help-content-tab}

![&#x200B; Inhoud tabel van de Hulp &#x200B;](/help/adaptive-forms/assets/datetime_helptab.png)

- **Korte beschrijving** - een korte beschrijving is een korte tekstverklaring die extra informatie of verduidelijking over het doel van een specifiek vormgebied verstrekt. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. Laat **toe tonen altijd korte beschrijving** optie om het onder de component te tonen.

- **toont altijd korte beschrijving** - laat de optie toe om de Korte beschrijving onder de component te tonen.

- **tekst van de Hulp** - de tekst van de Hulp verwijst naar extra informatie of begeleiding die aan de gebruiker wordt verstrekt om hen bij het correct invullen van een vormgebied bij te staan. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.


### Tabblad Toegankelijkheid {#accessibility-tab}

![&#x200B; Toegankelijkheid tabel &#x200B;](/help/adaptive-forms/assets/datetime_accessibilitytab.png)

- **Tekst voor het schermlezers** - de Tekst voor het schermlezers verwijst naar extra tekst die specifiek bedoeld is om door ondersteunende technologieën, zoals het schermlezers te worden gelezen, die door visueel gehandicapte individuen wordt gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.
   - **Tekst van de Douane**: Selecteer deze optie om de douanetekst voor de toegankelijkheidslabels van ARIA te gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie om de beschrijving voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Titel**: Selecteer deze optie om de titel voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **Naam**: Selecteer deze optie om de naam voor de toegankelijkheidslabels van ARIA te gebruiken.
   - **niets**: Selecteer deze optie als u niet voor de toegankelijkheidslabels van ARIA wilt toevoegen.

<!--
### Formats Tab {#format-tab}

![Formats tab](/help/adaptive-forms/assets/datepicker_formattab.png)

-   **Display Format** - It represents the date format that is displayed to the user. The **Type** option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.

-   **Edit Format** - It represents a date format in which the user can edit the date. The **Type** option allows the user to select the date format. You can also customize the date format using the **Custom** option in the **Type** dropdown menu.
-  **Format error message** - This option allows you to enter the message displayed on the screen when the entered date is not in the correct format.
- **Language** - This feature is used for formatting the specific field. When a user selects any language option from the **Type** drop-down menu, the **IETF BCP 47 language tag** option appears in the panel. You can choose the language for field formatting when translating an Adaptive Form into a specific language.
  
The set of languages is not visible by default, but users can input a custom **IETF BCP 47 language tag** by updating the template policy:

  1. Open the corresponding template associated with an Adaptive Form in the template editor.
  2. Select the existing policy as `datepicker-default-policy` from the drop-down menu.
   
        ![Date Picker template Policy](/help/adaptive-forms/assets/date-picker-template-policy.png)

  3. Click **Done**.

        >[!NOTE]
        >
        > For further information on how to translate an Adaptive Form to a specific locale, [click here](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components).
-->

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Datum en tijd te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De adaptieve Component van de Kern van de Datum en van de Tijd van Forms steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

![&#x200B; lusje van de Stijl &#x200B;](/help/adaptive-forms/assets/datepicker_styletab.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de Aangepaste Component van de Kern van de Datum en van de Tijd van Forms verstrekken.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![&#x200B; de Dialoog van Eigenschappen van de Douane &#x200B;](/help/adaptive-forms/assets/datepicker_customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de orde van de naam van het douanebezit en de waarde van het douanebezit te herschikken.

<!--
### Formats Tab {#formats-tab}

The formats tab allows you to specify default and custom date formats.

![Formattab](/help/adaptive-forms/assets/datepicker_formatpolicy.png)



## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=nl-NL)

-->

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}


