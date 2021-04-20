---
title: Tekstcomponent
description: De component Text is een component voor tekstbewerking en -compositie met tekstopmaak die op locatie kan worden bewerkt.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '2218'
ht-degree: 0%

---


# Tekstcomponent{#text-component}

De component Core Component Text is een component voor tekstbewerking en -compositie met tekstopmaak die op locatie kan worden bewerkt.

## Gebruik {#usage}

De component Text biedt een robuuste teksteditor met tekstopmaak die het mogelijk maakt tekst eenvoudig te bewerken in een vereenvoudigde, inline editor en in een volledige schermopmaak.

Het [bewerkingsdialoogvenster](#edit-dialog) bevat inline bewerking met beperkte opties met volledige functionaliteit beschikbaar in het dialoogvenster Volledig scherm bewerken. Met behulp van het [ontwerpdialoogvenster](#design-dialog) kunnen opties voor tekstopmaak, zoals koppen, speciale tekens en alineastijlen, worden geconfigureerd voor de sjabloon voor de auteur van de inhoud.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Tekstcomponent is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | Compatibel | Compatibel | Compatibel |
| [v1](v1/text-v1.md) | Compatibel | Compatibel | - |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_text) om de tekstcomponent te ervaren en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Tekst [kan op GitHub](https://adobe.com/go/aem_cmp_tech_text_v2) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## De component Text en de Rich Text Editor {#the-text-component-and-the-rich-text-editor}

De component van de Tekst van de Componenten van de Kern gebruikt de AEM Rich Text Editor (RTE). RTE voorziet inhoudsauteurs van een brede waaier van functionaliteit voor het uitgeven van hun tekstinhoud. RTE is zeer flexibel in zijn configuratie en biedt een aantal opties aan. Meer details over hoe RTE kan worden gevormd kunnen in de artikelen [vormen Rich Text Editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/configuring-and-extending/rich-text-editor.html) en [vormen de Rich Text Editor stop-ins](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html) worden gevonden.

De rest van dit artikel toont de standaardconfiguratie van de Component van de Tekst van de Componenten van de Kern met de uit-van-de-doos configuratie van RTE aan.

>[!NOTE]
>
>Alleen opties die zijn ingeschakeld door [UI-configuraties van de RTE](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html) zijn beschikbaar door in de Tekstcomponent.

## Dialoogvenster {#edit-dialog} bewerken

Het dialoogvenster Bewerken bevat de standaardgereedschappen voor tekstopmaak die de gebruiker zou verwachten bij het samenstellen van tekst.

![Dialoogvenster voor bewerken van tekstcomponent](/help/assets/text-edit.png)

### Vet

![Vet pictogram](/help/assets/text-bold.png)

Wordt gebruikt om vette opmaak toe te passen op geselecteerde tekst of opgemaakte tekst die na de cursor wordt ingevoerd.

**Ctrl+** Bcan wordt gebruikt als een sneltoets.

### Cursief

![Cursief pictogram](/help/assets/text-italic.png)

Wordt gebruikt om cursieve opmaak toe te passen op geselecteerde tekst of om tekst die na de cursor wordt ingevoerd, cursief te maken.

**Ctrl+** Ican be used as a keyboard shortcut.

### Onderstrepen

![Pictogram Onderstrepen](/help/assets/text-underline.png)

Wordt gebruikt om onderstreepte opmaak toe te passen op geselecteerde tekst of onderstreepte tekst die na de cursor wordt ingevoerd.

**Ctrl+** Ucan be used as a keyboard shortcut.

### Subscript

![Subscript-pictogram](/help/assets/text-subscript.png)

Wordt gebruikt om geselecteerde tekst of tekst die na de cursor is ingevoerd, op te maken als een subscript.

### Superscript

![Pictogram Superscript](/help/assets/text-superscript.png)

Wordt gebruikt om geselecteerde tekst of tekst die na de cursor is ingevoerd, op te maken als superscript.

### Plakken als tekst

![Plakken als tekstpictogram](/help/assets/text-paste-text.png)

Hiermee plakt u alle gekopieerde tekst als onbewerkte tekst zonder opmaak.

Wanneer u deze optie selecteert, wordt een venster geopend waarin de tekst als onbewerkte tekst zonder opmaak kan worden geplakt als een voorvertoning voordat deze in de tekst wordt ingevoegd. Accepteren door te tikken of op het vinkje te klikken, annuleren door te tikken of op de x te klikken.

![Plakken als tekstvoorbeeld](/help/assets/text-paste-text-example.png)

### Plakken vanuit Word

![Plakken vanuit Word-pictogram](/help/assets/text-paste-word.png)

Wanneer u deze optie selecteert, wordt een venster geopend waarin de tekst kan worden geplakt met behoud van de opmaak als voorvertoning voordat deze in de tekst wordt ingevoegd. Accepteren door te tikken of op het vinkje te klikken, annuleren door te tikken of op de x te klikken.

![Voorbeeld van plakken in Word](/help/assets/text-paste-word-example.png)

### Hyperlink

![Pictogram Hyperlink](/help/assets/text-hyperlink.png)

Met deze optie kunt u de geselecteerde tekst omzetten in een hyperlink of een reeds gedefinieerde koppeling wijzigen. Deze optie is alleen actief als er al tekst is geselecteerd en er een venster wordt geopend met aanvullende opties voor het instellen van de koppeling.

![Voorbeeld van hyperlink](/help/assets/text-hyperlink-example.png)

* Het pad invoeren
   * Kies in het dialoogvenster Selectie openen een pad in AEM
   * Als de koppeling zich niet binnen AEM bevindt, voert u de absolute URL in
      * Niet-absolute paden worden geïnterpreteerd als relatief ten opzichte van AEM
* Alternatieve beschrijvende tekst voor de koppeling invoeren
* Koppelingsgedrag selecteren
   * Doel
   * Zelfde tabblad
   * Nieuw tabblad
   * Bovenliggend frame
   * Bovenste frame

   Tik of klik op het vinkje om de koppeling toe te passen of klik op de x om te annuleren.

### Ontkoppelen

![Pictogram Ontkoppelen](/help/assets/text-unlink.png)

Gebruik deze optie om een koppeling te verwijderen die al op de geselecteerde tekst is toegepast. Deze optie is alleen actief als er al een koppeling is geselecteerd.

### Zoeken

![Pictogram Zoeken](/help/assets/text-find.png)

Met deze optie kunt u de tekst doorzoeken op een opgegeven tekstreeks. Als u deze optie selecteert, wordt een venster geopend waarin u de zoekopties kunt opgeven.

![Voorbeeld van zoeken](/help/assets/text-find-example.png)

Voer de tekst in waarvoor u wilt zoeken en tikken of klik op **Zoeken** om de zoekopdracht te starten. Tik of klik op de x om te annuleren.
Als u een nauwkeurige gelijke volgens het geval wilt doen, selecteer de optie **Kwestie** alvorens het onderzoek te beginnen.
Als een overeenkomst wordt gevonden, wordt deze gemarkeerd en wordt het zoekdialoogvenster gedimd weergegeven. Tik of klik nogmaals op de knop **Zoeken** in het grijze dialoogvenster om naar de volgende instantie te zoeken.

![Voorbeeld van zoeken gevonden](/help/assets/text-find-example-found.png)

Als er geen andere exemplaren worden gevonden, wordt een bericht weergegeven en wordt de zoekopdracht opnieuw gestart vanaf het begin van de tekst.

![Voorbeeld niet meer zoeken](/help/assets/text-find-example-found-end.png)

### Replace

![Pictogram Vervangen](/help/assets/text-replace.png)

Gebruik deze optie om de tekst te zoeken op instanties van een opgegeven tekenreeks en de overeenkomsten te vervangen door een andere tekenreeks. Als u deze optie selecteert, wordt een venster geopend waarin u de opties voor zoeken en vervangen kunt opgeven.

![Voorbeeld vervangen](/help/assets/text-replace-example.png)

Voer de tekst in waarnaar u wilt zoeken en de tekst waarmee u deze wilt vervangen.

* Tik of klik op **Zoeken** om te beginnen met zoeken. Klik of tik op de x om te annuleren.
* Als u een nauwkeurige gelijke volgens het geval wilt doen, selecteer de optie **Kwestie** alvorens het onderzoek te beginnen.
* Selecteer **Alles vervangen** om alle instanties van de tekst tegelijk te vervangen.

Als een overeenkomst wordt gevonden, wordt deze gemarkeerd en wordt het zoekdialoogvenster gedimd weergegeven. Klik nogmaals op de knop **Zoeken** in het grijze dialoogvenster om naar de volgende instantie te zoeken of selecteer de knop **Vervangen** om de gemarkeerde, overeenkomende tekst te vervangen. De knop **Vervangen** is alleen actief als er een overeenkomst is gemaakt.

Het dialoogvenster Zoeken en vervangen wordt transparant wanneer op Zoeken wordt geklikt en wordt dekkend wanneer op Vervangen wordt geklikt. Hierdoor kan de auteur de tekst controleren die de auteur vervangt.

>[!NOTE]
>
>Wanneer u de vervangingsfunctie gebruikt, moet de te vervangen tekenreeks op hetzelfde moment worden ingevoerd als de zoektekenreeks. U kunt echter nog steeds op Zoeken klikken om de tekenreeks te zoeken voordat u deze vervangt. Als de vervangingstekenreeks wordt ingevoerd nadat op Zoeken is geklikt, wordt de zoekopdracht opnieuw ingesteld op het begin van de tekst.


### Tekst links uitlijnen

![Pictogram Links uitlijnen](/help/assets/text-left.png)

Wordt gebruikt om de tekst uit te lijnen met de linkermarge.

### Tekst centreren

![Pictogram Tekst centreren](/help/assets/text-center.png)

Wordt gebruikt om de tekst te centreren.

### Tekst rechts uitlijnen

![Pictogram rechts uitlijnen](/help/assets/text-right.png)

Wordt gebruikt om de tekst uit te lijnen met de rechtermarge.

### Opsommingsteken

![Pictogram opsommingsteken](/help/assets/text-bullet.png)

Wordt gebruikt om de geselecteerde tekst op te maken als een lijst met opsommingstekens of om te beginnen met het invoegen van een lijst met opsommingstekens na de cursor.

Tik of klik nogmaals op de knop **Opsommingsteken** of voer twee regeleinden in om een lijst met opsommingstekens te beëindigen.

### Genummerd

![Pictogram Genummerde lijst](/help/assets/text-numbered.png)

Hiermee maakt u de geselecteerde tekst op als een genummerde lijst of begint u met het invoegen van een genummerde lijst na de cursor.

Tik of klik nogmaals op de knop **Genummerd** of voer twee regeleinden in om een genummerde lijst te beëindigen.

### Uitspringen

![Pictogram Uitspringen](/help/assets/text-outdent.png)

Wordt gebruikt om het inspringingsniveau te verlagen van de geselecteerde tekst of tekst die na de cursor wordt ingevoerd.

Alleen actief als de geselecteerde tekst of positie van de cursor al is ingesprongen.

### Inspringen

![Pictogram Inspringen](/help/assets/text-outdent.png)

Wordt gebruikt om het inspringingsniveau te verhogen van de geselecteerde tekst of tekst die na de cursor wordt ingevoerd.

### Tabel

![Tabelpictogram](/help/assets/text-table.png)

Wordt gebruikt om een tabel in de tekst in te voegen. Als u deze optie selecteert, wordt een venster geopend waarin u de details van de tabel kunt opgeven.

![Tabelvoorbeeld](/help/assets/text-table-example.png)

* **Kolommen**  - Het aantal kolommen van de tabel (vereist)
* **Rijen**  - Het aantal rijen van de tabel (vereist)
* **Breedte**  - De breedte van de tabel
* **Hoogte**  - De hoogte van de tabel
* **Celopvulling** : de ruimte rondom de celinhoud
* **Celafstand** : de ruimte tussen cellen
* **Rand**  - Het gewicht van de randlijnen van de tabel
   * Indien voor de koptekst van de tabel:
      * De eerste rij moet worden gebruikt
      * De eerste kolom moet worden gebruikt
      * De eerste rij en de eerste kolom moeten worden gebruikt
      * Of er moet geen header worden gebruikt.
* **Bijschrift**  - Het bijschrift van de tabel

### Spellingcontrole

![Spellingpictogram controleren](/help/assets/text-spellcheck.png)

Wordt gebruikt om de spelling van de tekstinhoud te controleren. Mogelijke spelfouten worden onderstreept met gebroken, rode lijnen.

Meer informatie over spellingcontrole en het aanpassen van de woordenboeken van de spellingcontrole kan in het document [vormen de Rich Text Editor stop-Ins](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html) worden gevonden.

### Speciale tekens {#special-characters}

![Pictogram Speciale tekens](/help/assets/text-special-characters.png)

Wordt gebruikt om speciale tekens in te voegen in de tekst. Als u deze optie selecteert, wordt een venster geopend waarin de beschikbare tekens worden weergegeven.

![Voorbeeld van speciale tekens](/help/assets/text-special-characters-example.png)

Tik op het gewenste teken of klik op het gewenste teken om het na de cursor in de tekst in te voegen. U kunt meerdere tekens invoegen. Tik of klik op de x om het selectievenster te sluiten.

### Bron bewerken

![Pictogram Bron bewerken](/help/assets/text-source.png)

Wordt gebruikt om de HTML-bron van de tekst weer te geven en te wijzigen.

Tik of klik op het pictogram **Bron bewerken** om de inhoud van de tekst vanuit de opgemaakte weergave te wijzigen en de onbewerkte HTML weer te geven. In deze modus zijn alle andere opmaakopties uitgeschakeld. Tik of klik nogmaals op het pictogram **Bron bewerken** om terug te keren naar de opgemaakte weergave.

>[!CAUTION]
>
>Zoals altijd het geval met toegang tot ruwe HTML, moet de voorzichtigheid worden uitgeoefend wanneer het gebruiken van **Bron geeft** optie uit!
>
>HTML die is ingevoerd via **Source Edit** wordt gescand op XSS-risico&#39;s en alle scripts die worden ingevoegd, worden verwijderd en worden niet weergegeven op de resulterende pagina. Maar misvormde HTML die is ingevoerd in **Source Edit** kan de sjabloon voor de pagina onderbreken, wat resulteert in onverwachte opmaak of het onbruikbaar maken van de resulterende pagina.

>[!NOTE]
>
>Omdat HTML die is ingevoerd via **Source Edit** wordt gescand op XSS-risico&#39;s en alle scripts en de gevonden scripts automatisch worden verwijderd, kan de werkelijke inhoud die wordt weergegeven afwijken van wat is ingevoerd in **Source Edit**. Daarom moet u **Bron bewerken** eerst afsluiten om de tekst in de normale editor weer te geven voordat u de tekst opslaat. Als u de wijzigingen wilt opslaan met **Bron bewerken**, moet u Bron bewerken eerst afsluiten.

### Alineaopmaak

![Pictogram Alineaopmaak](/help/assets/text-paragraph.png)

Wordt gebruikt om alineaopmaak toe te passen op de geselecteerde tekst of op tekst die na de cursor wordt ingevoegd. Als u deze optie selecteert, wordt een vervolgkeuzelijst geopend waarin de alineaopmaak wordt geselecteerd.

![Voorbeeld van alineaopmaak](/help/assets/text-paragraph-example.png)

### In line bewerken {#in-line-editing}

De tekstcomponent kan ook in regels worden bewerkt, maar vanwege ruimtebeperkingen zijn niet alle opmaakopties in regels beschikbaar. Schakel over naar de modus Volledig scherm om alle opties weer te geven.

![Voorbeeld van inline bewerken](/help/assets/text-edit-inline-example.png)

### Instellen en id {#setting-id}

Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).

* Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
* Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
* Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren welke tekstopmaakopties beschikbaar zijn voor de auteurs van de inhoud.

### Tabblad Plugins {#plugins-tab}

Het tabblad Insteekmodules wordt gebruikt om verschillende tekstopmaakopties die beschikbaar zijn voor de auteurs van de inhoud in en uit te schakelen.

### Functies {#features}

![Dialoogvenster Ontwerpen](/help/assets/text-design-features.png)

De volgende functies kunnen voor de component worden geactiveerd of gedeactiveerd.

* Onbewerkte tekst plakken
* Plakken van woord
* Zoeken en vervangen
* Spellingcontrole
* Opties voor het wijzigen van ingevoegde afbeeldingen
* HTML-bronbewerking

### Opmaak {#formatting}

![Opmaak van dialoogvenster Ontwerp](/help/assets/text-design-formatting.png)

De volgende opmaakopties kunnen voor de component worden geactiveerd of gedeactiveerd.

* Tabel
* Lijsten (opsommingsteken, nummer, inspringing, inspringing)
* Uitlijning (links, rechts, gecentreerd)
* Vet, cursief, onderstrepen
* Koppelen (en ontkoppelen)
* Subscript/superscript

### Alineastijlen {#paragraph-styles}

![Alineastijlen in het dialoogvenster Ontwerpen](/help/assets/text-design-paragraph.png)

Alineastijlen kunnen voor de component worden geactiveerd of gedeactiveerd. Als deze optie is geactiveerd, kunnen de toegestane indelingen worden gedefinieerd.

* Tik of klik op de knop **Toevoegen** om een nieuwe stijl in te voegen.
* Voer de code in van de stijl en een beschrijving die worden weergegeven in het dialoogvenster Bewerken.
* Als u een stijltik wilt verwijderen of op de knop **Delete** wilt klikken.
* Tik of klik op de handgrepen om de volgorde van de indelingen te wijzigen.

### Speciale tekens {#configuring-special-characters}

![Speciale tekens in het dialoogvenster Ontwerpen](/help/assets/text-design-special-characters.png)

De optie voor het invoegen van speciale tekens kan voor de component worden geactiveerd of gedeactiveerd. Als deze optie is geactiveerd, kunnen de toegestane tekens worden gedefinieerd.

* Tik of klik op de knop **Toevoegen** om een nieuw teken in te voegen.
* Voer de HTML-code in van het teken en een beschrijving die wordt weergegeven in het dialoogvenster Bewerken.
* Als u een tikteken wilt verwijderen of op de knop **Verwijderen** wilt klikken.
* Als u de volgorde van de tekens wilt wijzigen, tikt u of klikt u en sleept u de handgrepen.

## Tabblad Stijlen {#styles-tab}

De component Text ondersteunt het AEM [stijlsysteem](/help/get-started/authoring.md#component-styling).

## Adobe-gegevenslaag client {#data-layer}

De component Text ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
