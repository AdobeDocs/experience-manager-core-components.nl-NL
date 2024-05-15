---
title: Adaptieve Forms Core-component - Bestandsbijlage
description: De Adaptive Forms-component voor bestandsbijlagen gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: 64a54fc6-db52-481f-bf5a-60c05122004d
source-git-commit: 58a0f0f2ef6d9dec3ce2436dad954a8a7aca188c
workflow-type: tm+mt
source-wordcount: '1852'
ht-degree: 0%

---

# Bestandsbijlage-component {#file-attachment-adaptive-forms-core-component}

<span class="preview"> Dit artikel bevat inhoud over de   **RTF-tekst voor titel toestaan**    , een pre-releasefunctie. De pre-release functie is alleen toegankelijk via onze [pre-releasekanaal](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html#new-features).</span>

Met een bestandsbijlage in een adaptief formulier kunnen gebruikers bestanden selecteren en uploaden vanaf hun lokale computer of apparaat. De component Bestandsbijlage kan zo worden geconfigureerd dat specifieke bestandstypen, grootten en meerdere bijlagen mogelijk zijn.

**Voorbeeld**

![voorbeeld](/help/adaptive-forms/assets/upload-image.png)


## Gebruik {#reasons-to-use-file-attachment}

Er zijn verschillende redenen waarom het nuttig is om een component voor bestandsbijlagen op te nemen in een adaptieve vorm, zoals:

- **Verzamelen van aanvullende informatie**: Met een bestandsbijlage kunnen gebruikers documenten, afbeeldingen, video&#39;s of andere bestandstypen uploaden als onderdeel van het verzenden van het formulier. Dit kan nuttig zijn om extra informatie zoals hervatting, portefeuilles, of ondersteunende documentatie te verzamelen.

- **Eenvoudig delen van grote bestanden**: Met de component Bestandsbijlage kunnen gebruikers grote bestanden eenvoudig delen, zonder dat ze hoeven te vertrouwen op externe services voor het delen van bestanden.

- **Handigheid**: Met de component Bestandsbijlage kunnen gebruikers bestanden uploaden vanaf hun lokale computer zonder dat ze van het formulier moeten navigeren of andere gereedschappen moeten gebruiken.

- **Gegevensanalyse**: Bestandsbijlage kan worden gebruikt om gegevens van verschillende bronnen te verzamelen en te analyseren, of als invoer voor verdere verwerking.

- **Gebruikerservaring**: Bestandsbijlage kan worden gebruikt om het formulier gebruiksvriendelijker te maken door gebruikers een duidelijke en intuïtieve manier te bieden om bestanden te uploaden.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.12](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Lees de nieuwste informatie over de Adaptive Forms File Attachment Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fileinput/v1/fileinput). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de ervaring met bestandsbijlagen eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig opties voor bestandsbijlagen definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![Het tabblad Basis](/help/adaptive-forms/assets/fileattachement_basictab.png)

- **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **RTF-tekst voor titel toestaan** - Met deze functies kunnen gebruikers gewone teksttitels opmaken en functies zoals vet, cursief, onderstreepte tekst, diverse lettertypen, tekengrootten, kleuren en extra opties opnemen om de visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Na het selecteren van het selectievakje voor **RTF-tekst voor titel toestaan** worden opmaakopties zichtbaar om de titel van de component op te maken. Als u toegang wilt tot alle beschikbare opmaakopties, klikt u op de knop ![Pictogram Volledig scherm](/help/adaptive-forms/assets/fullscreen-icon.png) tab.

  ![RTF-ondersteuning](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.

- **Knoptitel** - Deze optie wordt gebruikt om het label in te stellen van de knop die wordt weergegeven op een adaptief formulier.
- **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.
- **Markeren als niet-gebonden formulierelement**: Selecteer de optie om een formulierveld te configureren dat niet is gekoppeld aan een schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.
- **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
- **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **Meerdere bijlagen toestaan** - Selecteer deze optie om meerdere bijlagen te uploaden met de **Bestandsbijlage** knop.
- **Tekst slepen** - Dit is de tekst die boven aan het dialoogvenster **Koppelen** om gebruikers te vragen bestanden te koppelen of te slepen. U hebt de optie om de tekst aan te passen die boven aan het dialoogvenster **Koppelen** knop. Daarnaast kunt u de tekst opmaken met het menu Rich Text.

### Tabblad Validatie {#validation-tab}

![Tabblad Validatie](/help/adaptive-forms/assets/fileattachment_validationtab.png)

- **Vereist** - Selecteer deze optie als u de component wilt weergeven in een adaptief formulier. Nadat u de optie hebt geselecteerd, moet u bijlagen toevoegen voordat u verdergaat met het verzenden van een formulier. U kunt de **Component verbergen** of **Component uitschakelen**  in de **Basis** als deze optie is geselecteerd.
- **Foutbericht** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de optie **Vereist** selectievakje is ingeschakeld en het veld blijft leeg.

- **Bericht voor scriptvalidatie** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de scriptvalidatie mislukt.

<!--   **Minimum files error message** - This option is used to enter an error message that is displayed if you upload files lesser than the specified minimum number of files.-->

- **Maximale bestandsgrootte (MB)** - Met deze optie kunt u een maximale bestandsgrootte opgeven. Bestandsgrootten worden opgegeven in MB.
  <!--   **Maximum files error message** - This option is used to enter an error message that is displayed if you upload files greater than the specified maximum number of files.-->

- **Foutbericht voor maximale bestandsgrootte** - Deze optie wordt gebruikt om een foutbericht in te voeren dat wordt weergegeven als u bestanden uploadt die groter zijn dan de bestandsgrootte die is opgegeven in **Maximale bestandsgrootte (MB)** -optie.

- **Toegestane bestandstypen** - Verschillende bestandstypen die kunnen worden geüpload met de opdracht **Bestandsbijlage** wordt hier toegevoegd. Hiermee kunt u ook een nieuwe bestandsindeling toevoegen door op de knop **Toevoegen** knop. Ondersteunde bestandsindelingen zijn: audio, video, afbeelding, tekst of PDF. U kunt toegestane bestandstypen ook verwijderen of opnieuw rangschikken met:
   - **Verwijderen** - Tik of klik om specifieke bestandstypen te verwijderen.
   - **Opnieuw rangschikken** - Tik of klik en sleep om de volgorde van toegestane bestandstypen te wijzigen.

- **Foutbericht voor bestandstype** - Met deze optie kunt u een foutbericht invoeren dat wordt weergegeven wanneer u de andere bestandsindelingen uploadt dan die in het dialoogvenster **Toegestane bestandstypen** -optie.

### Het tabblad Help-inhoud {#help-content-tab}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

- **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de achtergrondafbeelding onder de component weer te geven.

- **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

- **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}


![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

- **Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Bestandsbijlage te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

De Adaptive Forms File Attachment Core-component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Ontwerpdialoogvenster](/help/adaptive-forms/assets/checkbox-style.png)

- **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms File Attachment Core-component.

- **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![Dialoogvenster Aangepaste eigenschappen](/help/adaptive-forms/assets/checkbox-customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Groepsnaam**: U kunt een naam opgeven om de groep met aangepaste eigenschappen te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **Belangrijke paren**: U kunt meerdere aangepaste eigenschapnamen en aangepaste eigenschapswaarden toevoegen door op de knop **Toevoegen** knop voor elke aangepaste groep eigenschappen.

   - **Verwijderen**: Tik of klik om de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te verwijderen.

   - **Opnieuw rangschikken**: Tik of klik en sleep om de volgorde van de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te wijzigen.
<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
