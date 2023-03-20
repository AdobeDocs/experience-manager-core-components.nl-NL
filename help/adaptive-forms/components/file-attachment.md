---
title: Adaptieve Forms Core-component - Bestandsbijlage
description: De Adaptive Forms-component voor bestandsbijlagen gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: 64a54fc6-db52-481f-bf5a-60c05122004d
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '1508'
ht-degree: 0%

---

# Bestandsbijlage {#file-attachment-adaptive-forms-core-component}

Met een bestandsbijlage in een adaptief formulier kunnen gebruikers bestanden selecteren en uploaden vanaf hun lokale computer of apparaat. De component Bestandsbijlage kan zo worden geconfigureerd dat specifieke bestandstypen, grootten en meerdere bijlagen mogelijk zijn.

**Voorbeeld**

![](/help/adaptive-forms/assets/upload-image.png)


## Gebruik {#reasons-to-use-file-attachment}

Er zijn verschillende redenen waarom het nuttig is om een component voor bestandsbijlagen op te nemen in een adaptieve vorm, zoals:

* **Aanvullende informatie verzamelen**: Met een bestandsbijlage kunnen gebruikers documenten, afbeeldingen, video&#39;s of andere bestandstypen uploaden als onderdeel van het verzenden van het formulier. Dit kan nuttig zijn om extra informatie zoals hervatting, portefeuilles, of ondersteunende documentatie te verzamelen.

* **Eenvoudig delen van grote bestanden**: Met de component Bestandsbijlage kunnen gebruikers grote bestanden eenvoudig delen, zonder dat ze hoeven te vertrouwen op externe services voor het delen van bestanden.

* **Handigheid**: Met de component Bestandsbijlage kunnen gebruikers bestanden uploaden vanaf hun lokale computer zonder dat ze van het formulier moeten navigeren of andere gereedschappen moeten gebruiken.

* **Gegevensanalyse**: Bestandsbijlagen kunnen worden gebruikt om gegevens van verschillende bronnen te verzamelen en te analyseren, of om deze te gebruiken als invoer voor verdere verwerking.

* **Gebruikerservaring**: Bestandsbijlage kan worden gebruikt om het formulier gebruikersvriendelijker te maken door gebruikers een duidelijke en intuïtieve manier te bieden om bestanden te uploaden.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.12](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Core Components-versies](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Lees de nieuwste informatie over de Adaptive Forms File Attachment Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fileinput/v1/fileinput). Raadpleeg de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de ervaring met bestandsbijlagen eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig opties voor bestandsbijlagen definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![Het tabblad Basis](/help/adaptive-forms/assets/fileattachement_basictab.png)

* **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

* **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

* **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.

* **Knoptitel** - Deze optie wordt gebruikt om het label in te stellen van de knop die wordt weergegeven op een adaptief formulier.

* **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.
* **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
* **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
* **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
* **Meerdere bijlagen toestaan** - Selecteer deze optie om meerdere bijlagen te uploaden met de **Bestandsbijlage** knop.

### Tabblad Validatie {#validation-tab}

![Tabblad Validatie](/help/adaptive-forms/assets/fileattachment_validationtab.png)

* **Vereist** - Selecteer deze optie als u de component wilt weergeven in een adaptief formulier. U kunt de **Component verbergen** of **Component uitschakelen**  in de **Basis** als deze optie is geselecteerd.

* **Foutbericht** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de optie **Vereist** selectievakje is ingeschakeld en het veld blijft leeg.

* **Bericht voor scriptvalidatie** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de scriptvalidatie mislukt.

* **Foutbericht voor minimale bestanden** - Deze optie wordt gebruikt om een foutbericht in te voeren dat wordt weergegeven als u bestanden uploadt die kleiner zijn dan het opgegeven minimumaantal bestanden.

* **Foutbericht voor Maximum aantal bestanden** - Deze optie wordt gebruikt om een foutbericht in te voeren dat wordt weergegeven als u bestanden uploadt die groter zijn dan het opgegeven maximumaantal bestanden.

* **Maximale bestandsgrootte (MB)** - Met deze optie kunt u een maximale bestandsgrootte opgeven. Bestandsgrootten worden opgegeven in MB.

* **Foutbericht voor maximale bestandsgrootte** - Deze optie wordt gebruikt om een foutbericht in te voeren dat wordt weergegeven als u bestanden uploadt die groter zijn dan de bestandsgrootte die is opgegeven in **Maximale bestandsgrootte (MB)** optie.

* **Toegestane bestandstypen** - Verschillende bestandstypen die kunnen worden geüpload met de opdracht **Bestandsbijlage** wordt hier toegevoegd. Hiermee kunt u ook een nieuwe bestandsindeling toevoegen door op de knop **Toevoegen** knop. Ondersteunde bestandsindelingen zijn: audio, video, afbeelding, tekst of PDF. U kunt toegestane bestandstypen ook verwijderen of opnieuw rangschikken met:
   * **Verwijderen** - Tik of klik om specifieke bestandstypen te verwijderen.
   * **Opnieuw rangschikken** - Tik of klik en sleep om de volgorde van toegestane bestandstypen te wijzigen.

* **Foutbericht voor bestandstype** - Met deze optie kunt u een foutbericht invoeren dat wordt weergegeven wanneer u de andere bestandsindelingen uploadt dan in het dialoogvenster **Toegestane bestandstypen** optie.

### Het tabblad Help-inhoud {#help-content-tab}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

* **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de component onder de component weer te geven.

* **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

* **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}


![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

* **Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.


## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Bestandsbijlage te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

De Adaptive Forms File Attachment Core-component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Dialoogvenster Ontwerp bestandsbijlage](/help/adaptive-forms/assets/fileattachment_designdialog.png)

* **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms File Attachment Core-component.

* **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight&quot; opgeven: vet&quot;. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.
