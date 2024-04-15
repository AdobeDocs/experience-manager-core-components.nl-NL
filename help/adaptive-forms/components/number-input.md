---
title: Adaptive Forms Core Component - Nummerinvoer
description: De Adaptive Forms Number input Core Component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: 75604ecf-1ec5-4e97-b934-d6ed49726147
source-git-commit: 79b99d4f6b5a2b186ff3dbf570a58dc86bf24d4a
workflow-type: tm+mt
source-wordcount: '2103'
ht-degree: 0%

---

# Nummerinvoer {#number-input-adaptive-forms-core-component}

<span class="preview"> Dit artikel bevat inhoud over de **RTF-tekst voor titel toestaan** , een pre-releasefunctie. De pre-release functie is alleen toegankelijk via onze [pre-releasekanaal](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html#new-features).</span>

Een component Number Input in een adaptief formulier is een type formulierveld waarmee gebruikers numerieke waarden kunnen invoeren. De component wordt gewoonlijk vertegenwoordigd door een tekstveld met een pijl-omhoog en pijl-omlaag voor het verhogen en verlagen van het getal.

Deze kan ook worden gebruikt met kenmerken als min, max, step, value en meer. Deze kenmerken kunnen worden gebruikt om de minimale en maximale waarden in te stellen die zijn toegestaan in het veld, het stapinterval voor het verhogen of verlagen van het getal en de standaardwaarde van het veld.

Deze component kan worden gebruikt om numerieke gegevens zoals leeftijd, hoeveelheid, en meer te verzamelen. Het kan ook worden gebruikt om wiskundige bewerkingen uit te voeren, zoals optellen en aftrekken. Deze component kan ook worden gebruikt om de numerieke gegevens te valideren die de gebruiker heeft ingevoerd.

Voor toegankelijkheid is het belangrijk om &#39;label&#39; op te geven dat het doel van het invoerveld voor nummers beschrijft en welke invoer wordt verwacht.

**Voorbeeld**

![voorbeeld](/help/adaptive-forms/assets/numeric-stepper.png)

## Gebruik {#reasons-to-use-number-input-numeric-stepper}

Er zijn verschillende redenen waarom het nuttig is om een numerieke invoercomponent op te nemen in een adaptief formulier, zoals:

- **Wiskundige bewerkingen**: Met numerieke velden kunt u wiskundige bewerkingen uitvoeren, zoals optellen, aftrekken, vermenigvuldigen en delen.

- **Gegevensbereik**: numerieke velden kunnen worden gebruikt om een reeks geldige waarden in te stellen met de kenmerken min, max en step.

- **Dynamische inhoud**: De numerieke component kan worden gebruikt om dynamische gegevens weer te geven op basis van de formuliervelden.


## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.12](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Ga voor de meest recente informatie over de Adaptive Forms Number input Core Component naar de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/numberinput/v1/numberinput). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de gebruikersinvoer voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig opties voor numerieke invoer definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![Tabblad Standaard](/help/adaptive-forms/assets/numberinput_basictab.png)

- **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **RTF-tekst voor titel toestaan** - Met deze functies kunnen gebruikers gewone teksttitels opmaken en functies zoals vet, cursief, onderstreepte tekst, diverse lettertypen, tekengrootten, kleuren en extra opties opnemen om de visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Na het selecteren van het selectievakje voor **RTF-tekst voor titel toestaan** worden opmaakopties zichtbaar om de titel van de component op te maken. Als u toegang wilt tot alle beschikbare opmaakopties, klikt u op de knop ![Pictogram Volledig scherm](/help/adaptive-forms/assets/fullscreen-icon.png) tab.

  ![RTF-ondersteuning](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.
- **Plaatsaanduidingstekst** - Plaatsaanduidingstekst in een formuliercomponent verwijst naar een kort label of een korte vraag die binnen een invoerveld wordt weergegeven als een tip voor de gebruiker met betrekking tot welk type informatie naar verwachting in dat veld wordt ingevoerd. Plaatsaanduidingstekst verdwijnt wanneer de gebruiker in het veld typt en verschijnt opnieuw als het veld leeg blijft. De klasse biedt een visuele aanwijzing voor de gebruiker, maar fungeert niet als een permanent label of een permanente waarde voor het veld.
- **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u met AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.
- **Markeren als niet-gebonden formulierelement**: Selecteer de optie om een formulierveld te configureren dat niet is gekoppeld aan een schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.
- **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
- **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **Type nummer** - Met deze optie kunt u het type numerieke waarden selecteren dat &#x200B; toegestaan in het formulierveld. U kunt de typen Decimaal of Geheel getal selecteren in het keuzemenu.
- **Standaardwaarde** - Met deze optie kunt u een standaardwaarde toevoegen aan een formulierveld. Indien **Uitgeschakelde component** of **Component (alleen-lezen)** is geselecteerd, wordt de standaardwaarde op het scherm weergegeven. Als er geen waarde wordt ingevoerd door de gebruiker in het formulierveld, wordt deze waarde verzonden op het moment dat het formulier wordt verzonden

### Tabblad Validatie {#validation-tab}

![Tabblad Validatie](/help/adaptive-forms/assets/numberinput_validationtab.png)

- **Vereist** - Selecteer deze optie als u de component wilt weergeven in een adaptief formulier. Nadat u de optie hebt geselecteerd, moet u een waarde invoeren voordat u verdergaat met het verzenden van een formulier. U kunt de **Component verbergen** of **Component uitschakelen**  in de **Basis** als deze optie is geselecteerd.

- **Foutbericht** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de optie **Vereist** selectievakje is ingeschakeld en het veld blijft leeg.

- **Bericht voor scriptvalidatie** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de scriptvalidatie mislukt.

- **Laagste getal / Kleinste getal** - Gebruik deze optie om het minimaal toegestane aantal in te voeren in het formulierveld te selecteren. Als de waarde kleiner is dan het getal dat is opgegeven in **Laagste getal / Kleinste getal** wordt ingevoerd in het formulierveld, wordt het foutbericht weergegeven.

- **Minimale foutmelding** - Met deze optie kunt u een foutbericht invoeren dat wordt weergegeven wanneer de gebruiker een waarde invoert die lager is dan de waarde die is opgegeven in het dialoogvenster **Minimum aantal/minimum aantal** -optie.

- **Minimumwaarde uitsluiten** - Schakel dit selectievakje in als u niet de minimumwaarde wilt opgeven in het dialoogvenster **Laagste getal / Kleinste getal** op te nemen in het bereik van waarden die &#x200B; in het formulierveld worden ingevoerd.

- **Hoogste getal / Grootste getal** - Gebruik deze optie om het maximum toegestane aantal in te voeren in het formulierveld te selecteren. Als het getal groter is dan het getal dat is opgegeven in **Hoogste getal / Grootste getal** wordt ingevoerd in het formulierveld, wordt het foutbericht weergegeven.

- **Maximum foutbericht** - Met deze optie kunt u een foutbericht invoeren dat wordt weergegeven wanneer de gebruiker een waarde invoert die groter is dan de waarde die is opgegeven in het dialoogvenster **Hoogste getal / Grootste getal** -optie.

- **Maximumwaarde uitsluiten** - Schakel dit selectievakje in als u niet de maximumwaarde wilt opgeven in het dialoogvenster **Hoogste getal / Grootste getal** in het formulierveld in te voeren waarden.

### Het tabblad Help-inhoud {#help-content}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/numberinput_helptab.png)

- **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de achtergrondafbeelding onder de component weer te geven.

- **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

- **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/numberinput_accessibility.png)

**Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

### Tabblad Opmaak {#formats-configure-tab}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/numberinput_formattab.png)

- **Weergave-indeling** - Met deze optie kunt u opties selecteren uit verschillende numerieke indelingen voor weergave. Wanneer de gebruiker een optie selecteert in het menu **Type** vervolgkeuzemenu, **Indeling** wordt weergegeven in het deelvenster. U kunt een specifieke indeling kiezen waarin getallen worden weergegeven aan de gebruiker.

<!--   **Number of digits before the decimal separator (1234.000)** - Use this option to specify the number of digits to display before the decimal point. 

- **Number of digits after the decimal separator (1234.000)** - Use this option to specify the number of digits to display after the decimal point. -->

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de invoercomponent Number te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Number Input Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Het tabblad Stijl](/help/adaptive-forms/assets/datepicker_styletab.png)

- **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Number Input Core-component.

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

![Formattab](/help/adaptive-forms/assets/emailinput_formattab.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
