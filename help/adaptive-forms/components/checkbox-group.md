---
title: Adaptieve Forms Core-component - Checkbox-groep
description: De Adaptive Forms Checkbox Group Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: 2ced0223-e664-470b-a400-b6865d3a67c9
source-git-commit: 7888cfa0f1358ce8018fc1e3cc3b19eb66a82b9d
workflow-type: tm+mt
source-wordcount: '1664'
ht-degree: 0%

---

# Groep selectievakjes {#button-component-adaptive-forms-core-component}

Een groep selectievakjes in een adaptief formulier is een set verwante selectievakjes waarmee gebruikers een of meer opties in een lijst kunnen selecteren. Elk selectievakje wordt vertegenwoordigd door een gegevenswaarde (waarde die wordt gebruikt om items van een selectievakje te verwerken) en een weergavewaarde (label voor elk selectievakje dat het doel beschrijft)

**Voorbeeld**

![](/help/adaptive-forms/assets/checkbox-group.png)

**Dialoogvenster Eigenschappen**

![](/help/adaptive-forms/assets/checkbox-group-properties.png)

In dit voorbeeld wordt het element Opties gebruikt om de selectievakjes samen te groeperen. De **Tekst weergeven** -element wordt gebruikt om een label voor een item op te geven en **Gegevenswaarde** wordt gebruikt om de waarde op te geven die naar de server wordt verzonden wanneer het formulier wordt verzonden.

Elke optie/elk item in het selectievakje heeft een unieke waarde voor Gegevens en een uniek kenmerk voor Tekst weergeven. Als een gebruiker de selectievakjes &quot;Son&quot; en &quot;Daughter&quot; selecteert, wordt de bijbehorende gegevenswaarde verzonden naar de server wanneer het formulier wordt verzonden. Deze gegevens kunnen vervolgens worden verwerkt door een serverscript om te bepalen welke opties door de gebruiker zijn geselecteerd en kunnen worden gebruikt om verschillende handelingen uit te voeren, zoals het bijwerken van andere velden in het formulier of het verzenden van de formuliergegevens naar een serverscript voor verdere verwerking.

Bovendien, kan de checkbox groep worden gevormd om verschillende verwerkingswaarden voor elke optie te hebben, en dit kan worden geplaatst door de Adaptieve Redacteur van de Regel van Forms te gebruiken.

## Gebruik {#reasons-to-use-check-box-group}

Er zijn verschillende redenen waarom het nuttig is om een groep selectievakjes op te nemen in een adaptief formulier, zoals:

* **Meerdere selecties**: Met een groep selectievakjes kunnen gebruikers meerdere opties in een lijst selecteren. Dit kan handig zijn in situaties waarin meerdere selecties zijn toegestaan of vereist.

* **Gebruikerservaring**: U kunt de selectievakjesgroep gebruiken om het formulier gebruiksvriendelijker te maken door gebruikers een duidelijke en intuïtieve manier te bieden om meerdere opties te selecteren.

* **Gegevensanalyse**: U kunt de selectievakjesgroep gebruiken om gegevens van verschillende bronnen te verzamelen en te analyseren, of om deze groep te gebruiken als invoer voor verdere verwerking.

* **Enquêtes**: U kunt in enquêtes de groep Selectievakjes gebruiken om meerdere opties voor een vraag te selecteren.

* **Gebruikersvoorkeuren**: U kunt de groep selectievakjes gebruiken om gebruikersvoorkeuren voor verschillende opties te verzamelen.

* **Gegevenswaarde**: U kunt ook een groep selectievakjes gebruiken om items van een groep selectievakjes te verwerken.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.12](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Core Components-versies](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Lees de nieuwste informatie over de Adaptive Forms Checkbox Group Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/checkboxgroup/v1/checkboxgroup). Raadpleeg de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de ervaring van het selectievakje voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig opties voor selectievakjes definiëren voor een naadloze gebruikerservaring.


### Tabblad Standaard {#basic-tab}

![Het tabblad Basis](/help/adaptive-forms/assets/checkbox_basictab.png)

* **Naam** - De naam identificeert uniek de component in de regelredacteur.De speciale karakters en de ruimten worden niet toegestaan in de naamkoorden.

* **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

* **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.

* **Opties** - U kunt gegevenswaarden toevoegen en tekstparen weergeven met de opdracht **Toevoegen** knop. Nadat een nieuwe optie is toegevoegd, kunnen de volgende handelingen worden uitgevoerd:

   * **Gegevenswaarde** - Met deze optie kunt u de inhoud invoeren die u wilt verzenden wanneer een optie is geselecteerd.
   * **Tekst weergeven** - Met deze optie kunt u de inhoud invoeren die u wilt weergeven in een adaptief formulier.
   * **Verwijderen** - Tik of klik om de optie van een selectievakje te verwijderen.
   * **Opnieuw rangschikken** - Tik of klik en sleep om de volgorde van de deelvensters te wijzigen.

* **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.

* **Gegevenstype van verzonden waarde** - Met deze optie geeft u het gegevenstype op van de waarde die wordt verzonden wanneer een optie is geselecteerd. Als de **gegevenstype van verzonden waarde** is ingesteld op `Number` en u voegt tekenreeksgegevens toe aan **Gegevenswaarde** &#x200B; &#x200B; **Opties** tabblad geeft het scherm een `Value type mismatch` foutbericht.

* **Weergaveopties** - Deze optie wordt gebruikt om de visuele uitlijning van selectievakjes in een adaptief formulier in te stellen. De twee ondersteunde opties zijn:
   * **Horizontaal** - Als deze optie is geselecteerd, worden selectievakjes van links naar rechts weergegeven in een adaptief formulier.
   * **Verticaal** - Als deze optie is geselecteerd, worden de selectievakjes van boven naar beneden weergegeven in een adaptief formulier.

* **Standaardopties** - Met deze optie kunt u vooraf geselecteerde standaardwaarden toevoegen wanneer het formulier wordt geladen. Gebruik het verwijderpictogram om de toegevoegde opties te verwijderen. Als de **gegevenstype van verzonden waarde** is ingesteld op `Number` en u voegt tekenreeksgegevens toe aan **Standaardopties**, wordt een `Value type mismatch` foutbericht.
* **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
* **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.
* **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tabblad Validatie {#validation-tab}

![Tabblad Validatie](/help/adaptive-forms/assets/checkbox_validationtab.png)

* **Vereist** - Selecteer deze optie als u de component wilt weergeven in een adaptief formulier. U kunt de **Component verbergen** of **Component uitschakelen**  in de **Basis** als deze optie is geselecteerd.

* **Foutbericht** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de optie **Vereist** wordt ingeschakeld en wordt het formulierveld leeg gelaten.

* **Bericht voor scriptvalidatie** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de scriptvalidatie mislukt.

### Het tabblad Help-inhoud {#helpcontent-tab}

![Help-inhoud, tabblad](/help/adaptive-forms/assets/checkbox_helptab.png)

* **Korte beschrijving** - Een korte beschrijving is een korte tekstuitleg met aanvullende informatie of verduidelijking over het doel van een specifiek formulierveld. Het helpt de gebruiker begrijpen welk type gegevens in het gebied moeten worden ingegaan en kan richtlijnen of voorbeelden verstrekken helpen ervoor zorgen dat de ingevoerde informatie geldig is en aan de gewenste criteria voldoet. Korte beschrijvingen blijven standaard verborgen. De optie **Altijd korte beschrijving tonen** gebruiken om de component onder de component weer te geven.

* **Altijd korte beschrijving tonen** - Schakel de optie in om de korte beschrijving onder de component weer te geven.

* **Help-tekst** - De Help-tekst verwijst naar aanvullende informatie of aanwijzingen die de gebruiker krijgt om deze te helpen bij het correct invullen van een formulierveld. Deze wordt weergegeven wanneer de gebruiker op het Help-pictogram (i) naast de component klikt. De Help-tekst biedt gedetailleerdere informatie dan de label- of plaatsaanduidingstekst van een formulierveld en is ontworpen om de gebruiker te helpen de vereisten of beperkingen van het veld te begrijpen. Het kan ook suggesties of voorbeelden bevatten om het invullen van het formulier eenvoudiger en nauwkeuriger te maken.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheid, tabblad](/help/adaptive-forms/assets/checkbox_accessibility.png)

**Tekst voor schermlezers** - Tekst voor schermlezers verwijst naar extra tekst die specifiek is bedoeld om te worden gelezen door ondersteunende hulpmiddelen, zoals schermlezers, die door visueel gehandicapten worden gebruikt. Deze tekst bevat een audiobeschrijving van het doel van het formulierveld en kan informatie bevatten over de titel, beschrijving, naam en relevante berichten (aangepaste tekst) van het veld. Met de schermlezertekst kunt u ervoor zorgen dat het formulier toegankelijk is voor alle gebruikers, inclusief gebruikers met een visuele handicap, en krijgt deze een volledig inzicht in het formulierveld en de vereisten ervan.

    ##-ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Groep van het selectievakje te definiëren en te beheren.

### Tabblad Stijlen {#styles-tab}

De Adaptive Forms Checkbox Group Core-component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Ontwerpdialoogvenster](/help/adaptive-forms/assets/checkbox_designdialog.png)

* **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Checkbox Group Core-component.

* **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight&quot; opgeven: vet&quot;. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

## Verwante artikelen {#related-article}

* [Een adaptief formulier maken in AEM Sites Page of Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

* [Een zelfstandig adaptief formulier maken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

