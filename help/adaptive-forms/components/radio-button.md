---
title: Adaptieve Forms Core-component - Keuzerondje
description: De Adaptive Forms Radio Button Core Component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1645'
ht-degree: 0%

---


# Keuzerondje {#radio-button-adaptive-forms-core-component}

Een keuzerondje in een adaptief formulier is een invoerelement waarmee een gebruiker een optie kan selecteren in een groep gerelateerde opties. Deze wordt weergegeven met een kleine ronde knop die gevuld of leeg is om aan te geven of de optie is geselecteerd. Wanneer een gebruiker een keuzerondje selecteert, worden de overige keuzerondjes in de groep uitgeschakeld. Keuzerondjes worden doorgaans gebruikt wanneer er meerdere opties zijn die elkaar wederzijds uitsluiten en er slechts één optie tegelijk kan worden geselecteerd.

**Voorbeeld**

![](/help/adaptive-forms/assets/radio-button.png)

**Dialoogvenster Eigenschappen**

![](/help/adaptive-forms/assets/radio-button-properties.png)

In dit voorbeeld wordt het element Opties gebruikt om de keuzerondjes te groeperen. De **Tekst weergeven** -element wordt gebruikt om een label voor een item op te geven en **Gegevenswaarde** wordt gebruikt om de waarde op te geven die naar de server wordt verzonden wanneer het formulier wordt verzonden.

Elke keuzerondje heeft een unieke gegevenswaarde en een uniek kenmerk Tekst weergeven. Als een gebruiker &quot;1-10&quot;selecteert, wordt de overeenkomstige Waarde van Gegevens verzonden naar de server wanneer de vorm wordt voorgelegd. Deze gegevens kunnen vervolgens worden verwerkt door een serverscript om te bepalen welke opties door de gebruiker zijn geselecteerd en kunnen worden gebruikt om verschillende handelingen uit te voeren, zoals het bijwerken van andere velden in het formulier of het verzenden van de formuliergegevens naar een serverscript voor verdere verwerking.

Bovendien kan elk keuzerondje zo worden geconfigureerd dat het verschillende verwerkingswaarden heeft voor elke optie. Dit kan worden ingesteld met de Adaptive Forms Rule Editor

## Gebruik {#reasons-to-use-radio-button}

Er zijn verschillende redenen om keuzerondjes in een formulier te gebruiken, zoals:

* **Beperkte keuzen**: Keuzerondjes worden gebruikt om een lijst met vooraf gedefinieerde opties weer te geven waaruit de gebruiker kan kiezen en er kan slechts één optie tegelijk worden geselecteerd. Dit is handig wanneer het aantal opties beperkt is en elkaar uitsluiten.

* **Weergave wissen**: Keuzerondjes zijn duidelijk en gemakkelijk te begrijpen, zodat gebruikers eenvoudig kunnen zien wat ze selecteren.

* **Consistentie**: Met keuzerondjes krijgt u een consistente en gestandaardiseerde manier om gebruikers opties voor te stellen, zodat ze het formulier eenvoudiger kunnen begrijpen en ermee kunnen werken.

* **Eenvoudiger te gebruiken**: Keuzerondjes zijn gebruiksvriendelijk, vooral voor gebruikers die niet vertrouwd zijn met technologie of die slechts over beperkte mobiliteit beschikken.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Radio Button Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | --- |
| v1 | Compatibel met<br>[versie 2.0.4](/help/versions.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Core Components-versies](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Ga voor de meest recente informatie over de Adaptive Forms Radio Button Core Component naar de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/radiobutton/v1/radiobutton). Raadpleeg de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de ervaring met keuzerondjes eenvoudig aanpassen aan bezoekers. U kunt ook eenvoudig opties voor keuzerondjes definiëren voor een naadloze gebruikerservaring.

![Het tabblad Basis](/help/adaptive-forms/assets/radiobutton_basictab.png)

* **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

* **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

* **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.

   In de **Opties** kunt u gegevenswaarden toevoegen en tekstparen weergeven met de **Toevoegen** knop. Nadat een nieuwe optie is toegevoegd, kunnen de volgende handelingen worden uitgevoerd:

   * **Gegevenswaarde** - Met deze optie kunt u de inhoud invoeren die u wilt verzenden wanneer een optie is geselecteerd.
   * **Tekst weergeven** - Met deze optie kunt u de inhoud invoeren die u wilt weergeven in een adaptief formulier.
   * **Verwijderen** - Tik of klik om de optie van een keuzerondje te verwijderen.
   * **Opnieuw rangschikken** - Tik of klik en sleep om de volgorde van de opties te wijzigen.

* **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

* **Gegevenstype van verzonden waarde** - Met deze optie geeft u het gegevenstype op van de waarde die wordt verzonden wanneer een optie is geselecteerd. Als de **gegevenstype van verzonden waarde** is ingesteld op `Number` en u voegt tekenreeksgegevens toe aan **Gegevenswaarde** &#x200B; &#x200B; **Opties** tabblad geeft het scherm een `Value type mismatch` foutbericht.

* **Standaardopties** - Met deze optie kunt u standaardwaarden toevoegen die vooraf zijn geselecteerd wanneer het formulier wordt geladen. Als de **gegevenstype van verzonden waarde** is ingesteld op `Number` en u voegt tekenreeksgegevens toe aan **Standaardopties**, wordt een `Value type mismatch` foutbericht.

* **Weergaveopties** - Deze optie wordt gebruikt om de visuele uitlijning van keuzerondjes in een adaptief formulier in te stellen. De twee ondersteunde opties zijn:
   * **Horizontaal** - Als deze optie is geselecteerd, worden keuzerondjes van links naar rechts weergegeven in een adaptief formulier.
   * **Verticaal** - Als deze optie is geselecteerd, worden de keuzerondjes van boven naar beneden weergegeven in een adaptief formulier.
* **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
* **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
* **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tabblad Validatie {#validation-tab}

![Tabblad Validatie](/help/adaptive-forms/assets/radiobutton_validationtab.png)

* **Vereist** - Selecteer deze optie als u de component wilt weergeven in een adaptief formulier. U kunt de **Component verbergen** of **Component uitschakelen**  in de **Basis** als deze optie is geselecteerd.

* **Foutbericht** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de optie **Vereist** wordt ingeschakeld en wordt het formulierveld leeg gelaten.

* **Bericht voor scriptvalidatie** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de scriptvalidatie mislukt.

### Het tabblad Help-inhoud {#helpcontent-tab}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/radiobutton_helptab.png)

* **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de component onder de component weer te geven.

* **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

* **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/radiobutton_accessibilitytab.png)

* **Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.


## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component RadioButton te definiëren en te beheren.


### Tabblad Stijlen {#styles-tab}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Radio Button Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

**Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Radio Button Core Component.

**Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight&quot; opgeven: vet&quot;. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

