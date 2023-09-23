---
title: Adaptive Forms Core Component - Vervolgkeuzelijst
description: De Adaptive Forms Drop-down Core Component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: 9d59d0d2-d38f-4ed5-8b43-984c45f26f27
source-git-commit: ad3e3bca5cb46f14e864e4704c90ac3b62779794
workflow-type: tm+mt
source-wordcount: '1767'
ht-degree: 0%

---

# Vervolgkeuzelijst {#drop-down-list-adaptive-forms-core-component}

Met een vervolgkeuzelijst in een adaptief formulier kunnen gebruikers een of meer opties selecteren in een lijst met vooraf gedefinieerde opties. De opties kunnen van het type String, Number of Boolean zijn. Bovendien, kan de drop-down lijstcomponent worden gevormd om verschillende bevestiging en standaardwaarden te hebben.

**Voorbeeld**
![](/help/adaptive-forms/assets/drop-down-list.png)

## Gebruik {#reasons-to-use-drop-down-list}

Er zijn verschillende redenen waarom het nuttig is om een vervolgkeuzelijst op te nemen in een adaptief formulier, zoals:

* **Lange lijst met opties**: Vervolgkeuzelijsten zijn handig voor situaties waarin een veld een lange lijst met opties bevat. Ze nemen minder ruimte in het formulier in beslag dan een lijst met keuzerondjes of selectievakjes. De gebruikers hebben dit minder nodig.

* **Consistentie**: Vervolgkeuzelijsten bieden consistentie in het ontwerp en de indeling van het formulier, waardoor het intuïtiever wordt en gebruikers gemakkelijker door het formulier kunnen navigeren.

* **Helderheid**: Met vervolgkeuzelijsten kunt u het formulier duidelijker en begrijpelijker maken door een duidelijke en beknopte lijst met opties te bieden.

* **Gebruikerservaring**: Met vervolgkeuzelijsten kunt u het formulier gebruiksvriendelijker maken door gebruikers een duidelijke en intuïtieve manier te bieden om opties te selecteren.

* **Gegevensanalyse**: Vervolgkeuzelijsten kunnen worden gebruikt om gegevens van verschillende bronnen te verzamelen en te analyseren, of om deze als invoer voor verdere verwerking te gebruiken.


**Dialoogvenster Eigenschappen**

![](/help/adaptive-forms/assets/drop-down-list-properties.png)

In dit voorbeeld wordt het element Opties gebruikt om de lijstitems te definiëren. De **Tekst weergeven** element wordt gebruikt om een label voor lijstitems te verstrekken en **Gegevenswaarde** wordt gebruikt om de waarde op te geven die naar de server wordt verzonden wanneer het formulier wordt verzonden.

Elke vervolgkeuzelijst heeft een unieke waarde voor Gegevens en een uniek kenmerk voor Tekst weergeven. Als een gebruiker de optie &quot;Rood&quot; selecteert, wordt de bijbehorende waarde van Gegevens verzonden naar de server wanneer het formulier wordt verzonden. Deze gegevens kunnen vervolgens worden verwerkt door een serverscript om te bepalen welke opties door de gebruiker zijn geselecteerd en kunnen worden gebruikt om verschillende handelingen uit te voeren, zoals het bijwerken van andere velden in het formulier of het verzenden van de formuliergegevens naar een serverscript voor verdere verwerking.

Bovendien, kan de drop-down lijst worden gevormd om verschillende verwerkingswaarden voor elke optie te hebben, en dit kan worden geplaatst door de Adaptieve Redacteur van de Regel van Forms te gebruiken.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.12](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Lees de nieuwste informatie over de Adaptive Forms vervolgkeuzelijst Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/dropdown/v1/dropdown). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u uw ervaring in de vervolgkeuzelijst eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig opties voor vervolgkeuzelijsten definiëren voor een naadloze gebruikerservaring.

![Het tabblad Basis](/help/adaptive-forms/assets/dropdown_basictab.png)

* **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

* **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

* **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.

* **Meerdere selecties toestaan** - Selecteer deze optie als u meerdere opties in een vervolgkeuzelijst wilt selecteren.

* **Waarde opslaan als** - Met deze optie geeft u het gegevenstype op van de waarde die wordt verzonden wanneer een optie is geselecteerd. Als de **Waarde opslaan als** is ingesteld op `Number` en u voegt tekenreeksgegevens toe aan **Gegevenswaarde** &#x200B; &#x200B; op de **Opties** tabblad geeft het scherm een `Value type mismatch` foutbericht.

  In de **Opties** kunt u gegevenswaarden toevoegen en tekstparen weergeven met de opdracht **Toevoegen** knop. Nadat een nieuwe optie is toegevoegd, worden de volgende handelingen uitgevoerd:

   * **Gegevenswaarde** - Met deze optie kunt u de inhoud invoeren die u wilt verzenden wanneer een optie is geselecteerd.
   * **Tekst weergeven** - Met deze optie kunt u de inhoud invoeren die u wilt weergeven in een adaptief formulier.
   * **Verwijderen** - Tik of klik om de optie van een vervolgkeuzemenu te verwijderen.
   * **Opnieuw rangschikken** - Tik of klik en sleep om de volgorde voor de optie van een vervolgkeuzemenu te wijzigen.

* **Standaardopties** - U kunt nu standaardwaarden toevoegen. Gebruik het verwijderpictogram om de toegevoegde optie te verwijderen. Als de **Waarde opslaan als** is ingesteld op `Number` en u voegt tekenreeksgegevens toe aan **Standaardopties**, wordt een `Value type mismatch` foutbericht.

* **Plaatsaanduidingstekst** - Plaatsaanduidingstekst in een formuliercomponent verwijst naar een kort label of een korte vraag die binnen een invoerveld wordt weergegeven als een tip voor de gebruiker met betrekking tot welk type informatie naar verwachting in dat veld wordt ingevoerd. Plaatsaanduidingstekst verdwijnt wanneer de gebruiker in het veld typt en verschijnt opnieuw als het veld leeg blijft. De klasse biedt een visuele aanwijzing voor de gebruiker, maar fungeert niet als een permanent label of een permanente waarde voor het veld.

* **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

* **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
* **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
* **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tabblad Validatie {#validation-tab}

![Tabblad Validatie](/help/adaptive-forms/assets/dropdown_validationtab.png)

* **Vereist** - Selecteer deze optie als u de component wilt weergeven in een adaptief formulier. U kunt de **Component verbergen** of **Component uitschakelen**  in de **Basis** als deze optie is geselecteerd.

* **Foutbericht** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de optie **Vereist** wordt ingeschakeld en wordt het formulierveld leeg gelaten.

* **Bericht voor scriptvalidatie** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de scriptvalidatie mislukt.

### Het tabblad Help-inhoud {#help-content-tab}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/dropdown_helptab.png)

* **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de achtergrondafbeelding onder de component weer te geven.

* **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

* **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/dropdown_accessibilitytab.png)


**Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.


## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de vervolgkeuzelijstcomponent te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms vervolgkeuzelijst Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Vervolgkeuzelijst](/help/adaptive-forms/assets/dropdown_designdialog.png)

* **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms vervolgkeuzelijst Core Component.

* **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

## Verwante artikelen {#related-article}

* [Een adaptief formulier maken in AEM Sites Page of Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

* [Een zelfstandig adaptief formulier maken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)


## Zie ook {#see-also}

* [Accordeon](/help/adaptive-forms/components/accordion.md)
* [Knop](/help/adaptive-forms/components/button.md)
* [Selectievakjesgroep](/help/adaptive-forms/components/checkbox-group.md)
* [Datumkiezer](/help/adaptive-forms/components/date-picker.md)
* [E-mailinvoer](/help/adaptive-forms/components/email-input.md)
* [Formuliercontainer](/help/adaptive-forms/components/form-container.md)
* [Bestandsbijlage](/help/adaptive-forms/components/file-attachment.md)
* [Voettekst](/help/adaptive-forms/components/footer.md)
* [Koptekst](/help/adaptive-forms/components/header.md)
* [Horizontale tabs](/help/adaptive-forms/components/horizontal-tabs.md)
* [Afbeelding](/help/adaptive-forms/components/image.md)
* [Nummerinvoer](/help/adaptive-forms/components/number-input.md)
* [Deelvenstercontainer](/help/adaptive-forms/components/panel-container.md)
* [Keuzerondje](/help/adaptive-forms/components/radio-button.md)
* [Knop Opnieuw instellen](/help/adaptive-forms/components/reset-button.md)
* [Verzendknop](/help/adaptive-forms/components/submit-button.md)
* [Telefooninvoer](/help/adaptive-forms/components/telephone-input.md)
* [Tekstinvoer](/help/adaptive-forms/components/text-input.md)
* [Tekst](/help/adaptive-forms/components/text.md)
* [Titel](/help/adaptive-forms/components/title.md)
* [Wizard](/help/adaptive-forms/components/wizard.md)