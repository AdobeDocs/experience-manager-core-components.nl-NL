---
title: Adaptief formulierfragment
description: Gebruik formulierfragmenten om formuliersegmenten of -groepen te maken en deze te hergebruiken in Adaptive Forms om de efficiëntie en herbruikbaarheid te verbeteren.
role: Architect, Developer, Admin, User
exl-id: bde4a416-1d6b-4e9e-ac74-70fccef473cb
source-git-commit: 4c510b8fe59f4be6e1b329ee4257ab1b780fbf22
workflow-type: tm+mt
source-wordcount: '1954'
ht-degree: 0%

---

# Aangepast formulierfragmentonderdeel {#form-fragment-component-adaptive-forms-core-component}

Adaptief Forms biedt een handige manier om formuliersegmenten te maken, zoals deelvensters of groepen velden, zodat deze opnieuw kunnen worden gebruikt in verschillende Adaptief Forms. Deze herbruikbare en standalone segmenten worden bedoeld als [Adaptieve formulierfragmenten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html).

U kunt [een fragment meerdere keren toevoegen aan een document](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html#insert-a-fragment-in-an-adaptive-form) en gebruik eigenschappen voor gegevensbinding van zijn componenten om deze aan verschillende gegevensbronnen of schema te koppelen. U kunt bijvoorbeeld hetzelfde adresfragment gebruiken voor een vast adres, communicatie en factureringsadres en dit koppelen aan verschillende velden van een gegevensbron of schema.

![voorbeeld](/help/adaptive-forms/assets/using-multiple-fragment-af.gif)


U kunt ook de opdracht [herhaalbaarheid, optie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html) Als u een formulierfragmentcomponent en de onderliggende componenten wilt dupliceren, definieert u een minimum- en maximumaantal herhalingen en vereenvoudigt u de replicatie van vergelijkbare secties in een formulier.

>[!NOTE]
>
> U kunt [Een adaptief formulierfragment maken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html#create-a-fragment) geheel nieuw zijn of een deelvenster opslaan in een bestaand adaptief formulier als fragment.

## Gebruik {#usage}

- **Herbruikbaarheid**: De mogelijkheid om formulierfragmenten te hergebruiken in meerdere Adaptieve Forms is het belangrijkste voordeel van het gebruik van formulierfragmenten. Het draagt bij aan het behoud van consistentie in ontwerp en functionaliteit, aangezien de veranderingen die aan een fragment worden aangebracht in alle gevallen worden weerspiegeld waar het wordt gebruikt.

- **Consistente gebruikerservaring**: Het gebruik van formulierfragmenten voor gemeenschappelijke elementen, zoals kop- en voetteksten, zorgt voor een consistente en samenhangende gebruikerservaring.

- **Eenvoudig onderhoud**: De wijzigingen of wijzigingen die zijn aangebracht in een formulierfragment worden weerspiegeld in alle gevallen waarin het wordt gebruikt. Het vereenvoudigt onderhoud en verkleint de kans op fouten.

- **Efficiëntie**: Ontwerpers en ontwikkelaars besparen tijd door formulierfragmenten slechts eenmaal te maken en te testen. De formulierfragmenten kunnen dan eenvoudig worden opgenomen in meerdere Adaptieve Forms zonder dat er overbodig werk nodig is.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Fragment Core Component is uitgebracht als onderdeel van Core Components 2.0.50 for Cloud Service and Core Components 1.1.26 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[versie 2.0.50](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.26](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.

## Technische details {#technical-details}

Lees de nieuwste informatie over de Adaptive Forms Fragment Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fragment). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de fragmentervaring voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig fragmenteigenschappen definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![Tabblad Standaard](/help/adaptive-forms/assets/fragment-basictab.png)

- **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **RTF-tekst voor titel toestaan** - Met deze functies kunnen gebruikers gewone teksttitels opmaken en functies zoals vet, cursief, onderstreepte tekst, diverse lettertypen, tekengrootten, kleuren en extra opties opnemen om de visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Na het selecteren van het selectievakje voor **RTF-tekst voor titel toestaan** worden opmaakopties zichtbaar om de titel van de component op te maken. Als u toegang wilt tot alle beschikbare opmaakopties, klikt u op de knop ![Pictogram Volledig scherm](/help/adaptive-forms/assets/fullscreen-icon.png) tab.

  ![RTF-ondersteuning](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.
- **Gegevens van onderliggende componenten groeperen over het verzenden van formulieren (gegevens laten teruglopen in object)** - Wanneer de optie is geselecteerd, worden de gegevens van de onderliggende componenten genest in het JSON-object van de bovenliggende component. Als de optie echter niet is geselecteerd, hebben de verzonden JSON-gegevens een platte structuur, zonder object voor de bovenliggende component. Bijvoorbeeld:

   - Wanneer de optie is geselecteerd, worden de gegevens van de onderliggende componenten (bijvoorbeeld Straat, Plaats en Postcode) genest binnen de bovenliggende component (Adres) als een JSON-object. Dit leidt tot een hiërarchische structuur, en de gegevens worden georganiseerd onder de oudercomponent.

     Structuur van de ingediende gegevens:

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - Wanneer de optie niet is geselecteerd, hebben de verzonden JSON-gegevens een platte structuur zonder object voor de bovenliggende component (Adres). Alle gegevens bevinden zich op hetzelfde niveau, zonder hiërarchische organisatie.


     Structuur van de ingediende gegevens:

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

- **Fragmentverwijzing** - Een fragmentverwijzing is een verwijzing naar een formulierfragment dat is opgeslagen in een externe gegevensbron en wordt gebruikt in een formulier. Met de fragmentverwijzing kunt u het formulierfragment dynamisch aan een formulier binden.

- **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u met AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

- **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
- **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
- **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tabblad Fragment herhalen {#repeat-tab}

![Tabblad Fragment herhalen](/help/adaptive-forms/assets/fragment-repeattab.png)

- **Fragment herhaalbaar maken**: Een schakelfunctie waarmee gebruikers de herhaalbaarheidsfunctionaliteit kunnen in- of uitschakelen.
- **Minimale herhalingen**: Hiermee stelt u in hoe vaak de fragmentcomponent minimaal kan worden herhaald. De waarde nul geeft aan dat de fragmentcomponent niet wordt herhaald; de standaardwaarde is nul.
- **Maximale herhalingen**: Hiermee stelt u in hoe vaak de fragmentcomponent maximaal kan worden herhaald. Deze waarde is standaard onbeperkt.

### Het tabblad Help-inhoud {#help-content}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/fragment-helptab.png)

- **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de achtergrondafbeelding onder de component weer te geven.

- **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

- **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Toegankelijkheid {#accessibility}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/fragment-accessibilitytab.png)

- **Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.
   - **Aangepaste tekst**: Selecteer deze optie als u de aangepaste tekst voor toegankelijkheidslabels in ARIA wilt gebruiken. Als u deze optie selecteert, wordt het dialoogvenster Aangepaste tekst weergegeven. U kunt relevante informatie toevoegen in het dialoogvenster Aangepaste tekst.
   - **Beschrijving**: Selecteer deze optie als u de beschrijving voor toegankelijkheidslabels van ARIA wilt gebruiken.
   - **Titel**: Selecteer deze optie als u de titel voor toegankelijkheidslabels in ARIA wilt gebruiken.
   - **Naam**: Selecteer deze optie als u de naam voor toegankelijkheidslabels van ARIA wilt gebruiken.
   - **Geen**: Selecteer deze optie als u geen toegankelijkheidslabels voor ARIA wilt toevoegen.

- **HTML-rol voor schermlezer om aan te kondigen** - De rol HTML is een kenmerk dat wordt gebruikt om het doel van een element HTML aan ondersteunende hulpmiddelen, zoals schermlezers, op te geven. Het rolattribuut wordt gebruikt om extra context en semantische betekenis aan een element te verstrekken, die het voor schermlezers gemakkelijker maken om de inhoud te interpreteren en aan de gebruiker aan te kondigen. In AEM Forms heeft het label van een formulierveld bijvoorbeeld de rol &quot;label&quot; en kan het invoerveld de rol &quot;textbox&quot; hebben. Hierdoor kan de schermlezer de relatie tussen het label en het invoerveld begrijpen en deze correct aan de gebruiker meedelen.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt voor het definiëren en beheren van CSS-stijlen voor de formulierfragmentcomponent.

### Tabblad Stijlen {#styles-tab}

De kerncomponent Adaptief formulierfragment ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Ontwerpdialoogvenster](/help/adaptive-forms/assets/checkbox-style.png)

- **Standaard CSS-klassen**: U kunt een standaard-CSS-klasse opgeven voor de kerncomponent Adaptief formulierfragment.

- **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![Dialoogvenster Aangepaste eigenschappen](/help/adaptive-forms/assets/checkbox-customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Groepsnaam**: U kunt een naam opgeven om de groep met aangepaste eigenschappen te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **Belangrijke paren**: U kunt meerdere aangepaste eigenschapnamen en aangepaste eigenschapswaarden toevoegen door op de knop **Toevoegen** knop voor elke aangepaste groep eigenschappen.

   - **Verwijderen**: Tik of klik om de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te verwijderen.

   - **Opnieuw rangschikken**: Tik of klik en sleep om de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap opnieuw te rangschikken.


## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
