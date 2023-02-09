---
title: Adaptive Forms Core Component - Button
description: De Adaptive Forms-kerncomponent voor knoppen gebruiken of aanpassen.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1491'
ht-degree: 0%

---


# Component Button {#button-component-adaptive-forms-core-component}

Een knop in een adaptief formulier is een interface-element waarmee gebruikers een handeling kunnen starten wanneer ze erop klikken. Het knopelement kan worden gebruikt om een formulier te verzenden, een formulier opnieuw in te stellen of andere handelingen uit te voeren, zoals naar een andere pagina navigeren of aangepaste code activeren. De knop kan worden gemaakt met de component Button Core.

Met de Adaptive Forms Rule Editor kunnen gebruikers verschillende handelingen instellen voor de knopcomponent. Tot deze acties behoren het openen van een website, het tonen of verbergen van formuliercomponenten, het toevoegen van een exemplaar van een deelvenster of component, het verzenden of opnieuw instellen van een formulier, enzovoort.

Adaptief Forms biedt ook aparte knopcomponenten voor het verzenden of opnieuw instellen van een formulier, maar de knopcomponent kan ook zo nodig worden geconfigureerd voor het uitvoeren van deze handelingen.

Gebruikers kunnen de volledige lijst met ondersteunde acties voor de knopcomponent openen met de Adaptive Forms Rule Editor. Met de regeleditor kunnen gebruikers regels maken die door verschillende gebeurtenissen worden geactiveerd, zoals wanneer op een knop wordt geklikt, wanneer een formulier wordt geladen of wanneer een veldwaarde verandert. Deze regels kunnen vervolgens worden gebruikt om verschillende handelingen uit te voeren, zoals het weergeven of verbergen van componenten, het instellen van veldwaarden of het verzenden van het formulier.

## Gebruik {#reasons-to-use-button}

Er zijn verschillende redenen waarom het nuttig is om een knop in een adaptieve vorm op te nemen, zoals:

* **Formulierverzending**: Een knop wordt doorgaans gebruikt om een formulier te verzenden, zodat gebruikers de ingevoerde gegevens naar de server kunnen verzenden voor verwerking.

* **Opnieuw instellen van formulier**: U kunt ook knoppen gebruiken om een formulier opnieuw in te stellen, zodat alle gegevens die de gebruiker heeft ingevoerd, worden gewist.

* **Navigatie**: Met knoppen kunt u navigeren tussen verschillende secties van een formulier of verschillende pagina&#39;s op een website.

* **Gebeurtenisafhandeling**: Met knoppen kunt u verschillende gebeurtenissen activeren, zoals het openen van een website, het tonen/verbergen van componenten en het toevoegen van een instantie van een deelvenster of component aan de knop.

* **Interactiviteit**: Met knoppen kunt u interactieve formulieren maken. U kunt bijvoorbeeld een knop gebruiken om een modaal dialoogvenster te openen of om een sectie van het formulier in of uit te schakelen.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Button Core Component v1 is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | --- |
| v1 | Compatibel met<br>[versie 2.0.4](/help/versions.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Core Components-versies](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Ga voor de meest recente informatie over de Adaptive Forms Button Core Component naar de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button). Raadpleeg de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de knopervaring voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig knopeigenschappen definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![Tabblad Standaard](/help/adaptive-forms/assets/button_basictab.png)

* **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

* **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

* **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

* **Document met bindingsverwijzing record** - Met deze optie kunt u een veld Adaptief formulier koppelen aan het veld Document of Record. Wanneer een gebruiker een waarde invoert in een gekoppeld veld van een adaptief formulier, wordt die waarde ook weergegeven in het gekoppelde veld van het corresponderende document met records. Zo kunt u bijvoorbeeld een bindingsverwijzing naar Document of Record gebruiken om de naam en het adres van een klant weer te geven in een Document of Record, op basis van de id die de klant in het formulier heeft ingevoerd. Op deze manier kunt u met AEM Forms Document of Record genereren en beschikt u over een naadloze gebruikerservaring voor het verzamelen en beheren van gegevens.

* **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
* **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
* **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Het tabblad Help-inhoud {#help-content}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/button_helptab.png)

* **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de component onder de component weer te geven.

* **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

* **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Toegankelijkheid {#accessibility}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/button_accessibilitytab.png)


Op de **Toegankelijkheid** tab, waarden worden ingesteld voor [Toegankelijkheid ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) labels voor de component. Er zijn verschillende opties beschikbaar voor het gebruik van de tekst voor schermlezers:

* **Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.


   * **Aangepaste tekst**: Selecteer deze optie als u de aangepaste tekst voor toegankelijkheidslabels van ARIA wilt gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   * **Beschrijving**: Selecteer deze optie als u de beschrijving voor toegankelijkheidslabels van ARIA wilt gebruiken.
   * **Titel**: Selecteer deze optie als u de titel voor toegankelijkheidslabels van ARIA wilt gebruiken.
   * **Naam**: Selecteer deze optie als u de naam voor toegankelijkheidslabels van ARIA wilt gebruiken.
   * **Geen**: Selecteer deze optie als u geen toegankelijkheidslabels voor ARIA wilt toevoegen.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de knopcomponent te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

De Adaptive Forms Button Core-component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

**Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Button Core-component.

**Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight&quot; opgeven: vet&quot;. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

