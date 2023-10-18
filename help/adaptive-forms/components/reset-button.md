---
title: Adaptieve Forms Core-component - Knop Herstellen
description: De kerncomponent van de knop Adaptive Forms Reset gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: e5aa9d89-aece-491e-80a1-7fb9ea6c4b60
source-git-commit: be630c4d0a10ebaa679b77419b901fac818addb1
workflow-type: tm+mt
source-wordcount: '1230'
ht-degree: 0%

---

# Herstellen {#reset-button}

Een resetknop in een adaptief formulier is een knop waarmee gebruikers alle formuliervelden kunnen wissen of opnieuw instellen op de standaardwaarden. Wanneer op de knop Herstellen wordt geklikt, worden alle gegevens die in de formuliervelden zijn ingevoerd, verwijderd en keren de velden terug naar hun oorspronkelijke staat. De resetknop wordt meestal gebruikt als een alternatief voor de verzendknop en biedt een manier om opnieuw te beginnen als gebruikers onjuiste of ongewenste gegevens in het formulier hebben ingevoerd.


## Gebruik {#reasons-to-use-reset-button}

De redenen voor het gebruik van een resetknop in een adaptief formulier zijn:

* **Gebruikersgemak**: Met een resetknop kunnen gebruikers het formulier snel en eenvoudig wissen en opnieuw beginnen, zonder dat ze elk veld handmatig moeten verwijderen.

* **Verbeterde bruikbaarheid**: Met een resetknop kan de gebruikerservaring worden verbeterd doordat gebruikers fouten gemakkelijk kunnen corrigeren of hun invoer kunnen wijzigen.

* **Foutpreventie**: Met een resetknop kunnen gebruikers voorkomen dat per ongeluk onjuiste gegevens worden verzonden, wat tot fouten of verwerkingsproblemen kan leiden.

* **Consistentie**: Het opnemen van een resetknop in een formulier zorgt voor consistentie in de gebruikerservaring, aangezien herstellingknoppen veel voorkomen in formulieren.

* **Beter gegevensbeheer**: Met een resetknop kunnen de formuliergegevens worden ingedeeld en nauwkeurig blijven, omdat gebruikers minder kans hebben om inconsistente of onjuiste gegevens te verzenden.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 voor Cloud Service en Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.12](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Ga voor de meest recente informatie over de Adaptive Forms Reset-knop Core Component naar de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de knopervaring voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig opties voor de knop Herstellen definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![Tabblad Standaard](/help/adaptive-forms/assets/button_basictab.png)

* **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

* **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

* **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

* **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
* **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
* **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Het tabblad Help-inhoud {#help-content}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/button_helptab.png)

* **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de achtergrondafbeelding onder de component weer te geven.

* **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

* **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Toegankelijkheid {#accessibility}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/button_accessibilitytab.png)


**Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de knopcomponent Reset te definiëren en te beheren.


### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Reset-knop Core-component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Ontwerpdialoogvenster](/help/adaptive-forms/assets/reset_designdialog.png)

* **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Reset-knop Core-component.

* **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->


>[!MORELIKETHIS]
>
>* [Accordeon](/help/adaptive-forms/components/accordion.md)
>* [Knop](/help/adaptive-forms/components/button.md)
>* [Selectievakjesgroep](/help/adaptive-forms/components/checkbox-group.md)
>* [Datumkiezer](/help/adaptive-forms/components/date-picker.md)
>* [Vervolgkeuzelijst](/help/adaptive-forms/components/drop-down.md)
>* [E-mailinvoer](/help/adaptive-forms/components/email-input.md)
>* [Formuliercontainer](/help/adaptive-forms/components/form-container.md)
>* [Bestandsbijlage](/help/adaptive-forms/components/file-attachment.md)
>* [Voettekst](/help/adaptive-forms/components/footer.md)
>* [Koptekst](/help/adaptive-forms/components/header.md)
>* [Horizontale tabs](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Afbeelding](/help/adaptive-forms/components/image.md)
>* [Nummerinvoer](/help/adaptive-forms/components/number-input.md)
>* [Deelvenstercontainer](/help/adaptive-forms/components/panel-container.md)
>* [Keuzerondje](/help/adaptive-forms/components/radio-button.md)
>* [Verzendknop](/help/adaptive-forms/components/submit-button.md)
>* [Telefooninvoer](/help/adaptive-forms/components/telephone-input.md)
>* [Tekstinvoer](/help/adaptive-forms/components/text-input.md)
>* [Tekst](/help/adaptive-forms/components/text.md)
>* [Titel](/help/adaptive-forms/components/title.md)
>* [Wizard](/help/adaptive-forms/components/wizard.md)


## Zie ook {#see-also}

{{see-also}}