---
title: Tekstcomponent
description: De component Text is een component voor tekstbewerking en -compositie met tekstopmaak die op locatie kan worden bewerkt.
translation-type: tm+mt
source-git-commit: fe8a121520000ffd56ae3347469590e89121eaf0

---


# Tekstcomponent{#text-component}

De component Core Component Text is een component voor tekstbewerking en -compositie met tekstopmaak die op locatie kan worden bewerkt.

## Gebruik {#usage}

De component Text biedt een robuuste teksteditor met tekstopmaak die het mogelijk maakt tekst eenvoudig te bewerken in een vereenvoudigde, inline editor en in een volledige schermopmaak.

Het dialoogvenster [](#edit-dialog) Bewerken bevat inline bewerkingen met beperkte opties en volledige functionaliteit in het dialoogvenster Bewerken op volledig scherm. In het dialoogvenster [](#design-dialog)Ontwerp kunt u opmaakopties voor tekst, zoals koppen, speciale tekens en alineastijlen, configureren voor de sjabloon voor de auteur van de inhoud.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Tekstcomponent is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|---|
| v2 | Compatibel | Compatibel | Compatibel | Compatibel |
| [v1](v1/text-v1.md) | Compatibel | Compatibel | Compatibel | - |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_text)om de component Text te ervaren en voorbeelden van de bijbehorende configuratieopties en de HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Tekst [kan op GitHub](https://adobe.com/go/aem_cmp_tech_text_v2)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## De component Text en de RTF-editor {#the-text-component-and-the-rich-text-editor}

De component van de Tekst van de Componenten van de Kern gebruikt de Redacteur van de Tekst van AEM Rich (RTE). RTE voorziet inhoudsauteurs van een brede waaier van functionaliteit voor het uitgeven van hun tekstinhoud. RTE is zeer flexibel in zijn configuratie en biedt een aantal opties aan. Meer details over hoe RTE kan worden gevormd kunnen in de artikelen worden gevonden [vormen de Rich Text Editor](https://docs.adobe.com/content/help/en/experience-manager-65/administering/operations/rich-text-editor.html) en [vormen de Rich Text Editor stop-ins](https://docs.adobe.com/content/help/en/experience-manager-65/administering/operations/configure-rich-text-editor-plug-ins.html).

De rest van dit artikel toont de standaardconfiguratie van de Component van de Tekst van de Componenten van de Kern met de uit-van-de-doos configuratie van RTE aan.

>[!NOTE]
>
>Alleen opties die door [UI-configuraties van de RTE](https://docs.adobe.com/content/help/en/experience-manager-65/administering/operations/configure-rich-text-editor-plug-ins.html) worden ingeschakeld, zijn beschikbaar door de component Text.

## Dialoogvenster Bewerken {#edit-dialog}

Het dialoogvenster Bewerken bevat de standaardgereedschappen voor tekstopmaak die de gebruiker zou verwachten bij het samenstellen van tekst.

![](/help/assets/screen_shot_2018-01-11at143025.png)

### Vet

![](/help/assets/screen_shot_2018-01-11at125602.png)

Wordt gebruikt om vette opmaak toe te passen op geselecteerde tekst of opgemaakte tekst die na de cursor wordt ingevoerd.

**Ctrl+B** kan worden gebruikt als een sneltoets.

### Cursief

![](/help/assets/screen_shot_2018-01-11at125609.png)

Wordt gebruikt om cursieve opmaak toe te passen op geselecteerde tekst of om tekst die na de cursor wordt ingevoerd, cursief te maken.

**Ctrl+I** kan als sneltoets worden gebruikt.

### Onderstrepen

![](/help/assets/screen_shot_2018-01-11at125615.png)

Wordt gebruikt om onderstreepte opmaak toe te passen op geselecteerde tekst of onderstreepte tekst die na de cursor wordt ingevoerd.

**Ctrl+U** kan als sneltoets worden gebruikt.

### Subscript

![](/help/assets/screen_shot_2018-01-11at125703.png)

Wordt gebruikt om geselecteerde tekst of tekst die na de cursor is ingevoerd, op te maken als een subscript.

### Superscript

![](/help/assets/screen_shot_2018-01-11at125708.png)

Wordt gebruikt om geselecteerde tekst of tekst die na de cursor is ingevoerd, op te maken als superscript.

### Plakken als tekst

![](/help/assets/screen_shot_2018-01-11at125713.png)

Hiermee plakt u alle gekopieerde tekst als onbewerkte tekst zonder opmaak.

Wanneer u deze optie selecteert, wordt een venster geopend waarin de tekst als onbewerkte tekst zonder opmaak kan worden geplakt als een voorvertoning voordat deze in de tekst wordt ingevoegd. Accepteren door te tikken of op het vinkje te klikken, annuleren door te tikken of op de x te klikken.

![](/help/assets/screen_shot_2018-01-11at143234.png)

### Plakken vanuit Word

![](/help/assets/screen_shot_2018-01-11at125717.png)

Wanneer u deze optie selecteert, wordt een venster geopend waarin de tekst kan worden geplakt met behoud van de opmaak als voorvertoning voordat deze in de tekst wordt ingevoegd. Accepteren door te tikken of op het vinkje te klikken, annuleren door te tikken of op de x te klikken.

![](/help/assets/screen_shot_2018-01-11at143250.png)

### Hyperlink

![](/help/assets/screen_shot_2018-01-11at125839.png)

Met deze optie kunt u de geselecteerde tekst omzetten in een hyperlink of een reeds gedefinieerde koppeling wijzigen. Deze optie is alleen actief als er al tekst is geselecteerd en er een venster wordt geopend met aanvullende opties voor het instellen van de koppeling.

![](/help/assets/screen_shot_2018-01-11at130003.png)

* Voer de locatie in
   * Kies een pad in AEM met het dialoogvenster Selectie openen
   * Als de koppeling zich niet binnen AEM bevindt, voert u de absolute URL in (niet-absolute paden worden geïnterpreteerd als relatief ten opzichte van AEM)
* Alternatieve beschrijvende tekst voor de koppeling invoeren
* Koppelingsgedrag selecteren
   * Doel
   * Zelfde tabblad
   * Nieuw tabblad
   * Bovenliggend frame
   * Bovenste frame
   Tik of klik op het vinkje om de koppeling toe te passen of klik op de x om te annuleren.

### Ontkoppelen

![](/help/assets/screen_shot_2018-01-11at125901.png)

Gebruik deze optie om een koppeling te verwijderen die al op de geselecteerde tekst is toegepast. Deze optie is alleen actief als er al een koppeling is geselecteerd.

### Zoeken

![](/help/assets/screen_shot_2018-01-11at125906.png)

Met deze optie kunt u de tekst doorzoeken op een opgegeven tekstreeks. Als u deze optie selecteert, wordt een venster geopend waarin u de zoekopties kunt opgeven.

![](/help/assets/screen_shot_2018-01-11at130107.png)

Voer de tekst in waarvoor u wilt zoeken en tikken of klik op **Zoeken** om de zoekopdracht te starten. Tik of klik op de x om te annuleren.
Als u een exacte overeenkomst wilt uitvoeren op basis van het hoofdlettergebruik, selecteert u de optie **Hoofdlettergebruik** afstemmen voordat u de zoekopdracht start.
Als een overeenkomst wordt gevonden, wordt deze gemarkeerd en wordt het zoekdialoogvenster gedimd weergegeven. Tik of klik nogmaals op de knop **Zoeken** in het grijze dialoogvenster om naar de volgende instantie te zoeken.

![](/help/assets/screen_shot_2018-01-11at130145.png)

Als er geen andere exemplaren worden gevonden, wordt een bericht weergegeven en wordt de zoekopdracht opnieuw gestart vanaf het begin van de tekst.

![](/help/assets/screen_shot_2018-01-11at130241.png)

### Replace

![](/help/assets/screen_shot_2018-01-11at125910.png)

Gebruik deze optie om de tekst te zoeken op instanties van een opgegeven tekenreeks en de overeenkomsten te vervangen door een andere tekenreeks. Als u deze optie selecteert, wordt een venster geopend waarin u de opties voor zoeken en vervangen kunt opgeven.

![](/help/assets/screen_shot_2018-01-11at130441.png)

Voer de tekst in waarnaar u wilt zoeken en de tekst waarmee u deze wilt vervangen.

Tik of klik op **Zoeken** om te beginnen met zoeken. Klik of tik op de x om te annuleren.

Als u een exacte overeenkomst wilt uitvoeren op basis van het hoofdlettergebruik, selecteert u de optie **Hoofdlettergebruik** afstemmen voordat u de zoekopdracht start.

Als een overeenkomst wordt gevonden, wordt deze gemarkeerd en wordt het zoekdialoogvenster gedimd weergegeven. Klik nogmaals op de knop **Zoeken** in het grijze dialoogvenster om naar de volgende instantie te zoeken of selecteer de knop **Vervangen** om de gemarkeerde, overeenkomende tekst te vervangen. De knop **Vervangen** is alleen actief nadat een overeenkomst is gemaakt.

Selecteer Alles **** vervangen om alle instanties van de tekst tegelijk te vervangen.

### Tekst links uitlijnen

![](/help/assets/screen_shot_2018-01-11at142012.png)

Wordt gebruikt om de tekst uit te lijnen met de linkermarge.

### Tekst centreren

![](/help/assets/screen_shot_2018-01-11at142017.png)

Wordt gebruikt om de tekst te centreren.

### Tekst rechts uitlijnen

![](/help/assets/screen_shot_2018-01-11at142021.png)

Wordt gebruikt om de tekst uit te lijnen met de rechtermarge.

### Opsommingsteken

![](/help/assets/screen_shot_2018-01-11at142025.png)

Wordt gebruikt om de geselecteerde tekst op te maken als een lijst met opsommingstekens of om te beginnen met het invoegen van een lijst met opsommingstekens na de cursor.

Tik of klik nogmaals op de knop **Opsommingsteken** of voer twee regeleinden in om een lijst met opsommingstekens te beëindigen.

### Genummerd

![](/help/assets/screen_shot_2018-01-11at142030.png)

Hiermee maakt u de geselecteerde tekst op als een genummerde lijst of begint u met het invoegen van een genummerde lijst na de cursor.

Tik of klik nogmaals op de knop **Genummerd** of voer twee regeleinden in om een genummerde lijst te beëindigen.

### Uitspringen

![](/help/assets/screen_shot_2018-01-11at141917.png)

Wordt gebruikt om het inspringingsniveau te verlagen van de geselecteerde tekst of tekst die na de cursor wordt ingevoerd.

Alleen actief als de geselecteerde tekst of positie van de cursor al is ingesprongen.

### Inspringen

![](/help/assets/screen_shot_2018-01-11at141922.png)

Wordt gebruikt om het inspringingsniveau te verhogen van de geselecteerde tekst of tekst die na de cursor wordt ingevoerd.

### Tabel

![](/help/assets/screen_shot_2018-01-11at141928.png)

Wordt gebruikt om een tabel in de tekst in te voegen. Als u deze optie selecteert, wordt een venster geopend waarin u de details van de tabel kunt opgeven.

![](/help/assets/screen_shot_2018-01-11at142405.png)

* **Kolommen** Het aantal kolommen van de tabel (vereist)
* **Rijen** Het aantal rijen van de tabel (vereist)
* **Breedte** De breedte van de tabel
* **Hoogte** De hoogte van de tabel
* **Celopvulling** van cellen De ruimte rondom de celinhoud
* **Celafstand** De ruimte tussen cellen
* **Rand** Het gewicht van de randlijnen van de tabel
* Indien voor de koptekst van de tabel:
   * De eerste rij moet worden gebruikt
   * De eerste kolom moet worden gebruikt
   * De eerste rij en de eerste kolom moeten worden gebruikt
   * Of er moet geen header worden gebruikt.
* **Bijschrift** Het bijschrift van de tabel

### Spellingcontrole

![](/help/assets/screen_shot_2018-01-11at141935.png)

Wordt gebruikt om de spelling van de tekstinhoud te controleren. Mogelijke spelfouten worden onderstreept met gebroken, rode lijnen.

Meer informatie over spellingcontrole en het aanpassen van de woordenboeken van de spellingcontrole kunt u in het document vinden [vormt de Rich Text Editor stop-Ins](https://docs.adobe.com/content/help/en/experience-manager-65/administering/operations/configure-rich-text-editor-plug-ins.html).

### Speciale tekens {#special-characters}

![](/help/assets/screen_shot_2018-01-11at142600.png)

Wordt gebruikt om speciale tekens in te voegen in de tekst. Als u deze optie selecteert, wordt een venster geopend waarin de beschikbare tekens worden weergegeven.

![](/help/assets/screen_shot_2018-01-11at142635.png)

Tik op het gewenste teken of klik op het gewenste teken om het teken na de cursor in te voegen in de tekst. U kunt meerdere tekens invoegen. Tik of klik op de x om het selectievenster te sluiten.

### Bron bewerken

![](/help/assets/screen_shot_2018-01-11at142746.png)

Wordt gebruikt om de HTML-bron van de tekst weer te geven en te wijzigen.

Tik of klik op het pictogram **Bron bewerken** om de inhoud van de tekst in de opgemaakte weergave te wijzigen en de onbewerkte HTML weer te geven. In deze modus zijn alle andere opmaakopties uitgeschakeld. Tik of klik nogmaals op het pictogram **Bron bewerken** om terug te keren naar de opgemaakte weergave.

>[!CAUTION]
>
>Zoals altijd het geval met toegang tot onbewerkte HTML, moet de voorzichtigheid wanneer het gebruiken van de **Bron geeft** optie uit!
>
>HTML die is ingevoerd via **Bronbewerking** , wordt gescand op XSS-risico&#39;s en alle scripts die worden ingevoegd, worden verwijderd en worden niet weergegeven op de resulterende pagina. In **Source Edit** ingevoerde misvormde HTML kan de sjabloon voor de pagina echter verbreken, wat resulteert in een onverwachte opmaak of een onbruikbare weergave van de resulterende pagina.

>[!NOTE]
>
>Omdat HTML die is ingevoerd via **Bronbewerking** wordt gescand op XSS-risico&#39;s en alle scripts en de gevonden scripts automatisch verwijdert, kan de werkelijke inhoud die wordt weergegeven afwijken van wat is ingevoerd in **Bronbewerking**. Om deze reden, om veranderingen te bewaren die gebruikend **Bron worden aangebracht geef uit**, moet u **Bron eerst weggaan uitgeven** om de tekst in de normale redacteur te bekijken alvorens op te slaan.

### Alineaopmaak

![](/help/assets/screen_shot_2018-01-11at142752.png)

Wordt gebruikt om alineaopmaak toe te passen op de geselecteerde tekst of op tekst die na de cursor wordt ingevoegd. Als u deze optie selecteert, wordt een vervolgkeuzelijst geopend waarin de alineaopmaak wordt geselecteerd.

![](/help/assets/screen_shot_2018-01-11at142828.png)

De tekstcomponent kan ook in regels worden bewerkt, maar vanwege ruimtebeperkingen zijn niet alle opmaakopties in regels beschikbaar. Schakel over naar de modus Volledig scherm om alle opties weer te geven.

![](/help/assets/screen_shot_2018-01-11at142921.png)

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren welke tekstopmaakopties beschikbaar zijn voor de auteurs van de inhoud.

### Tabblad Plugins {#plugins-tab}

Het tabblad Insteekmodules wordt gebruikt om verschillende tekstopmaakopties die beschikbaar zijn voor de auteurs van de inhoud in en uit te schakelen.

### Features {#features}

![](/help/assets/chlimage_1-28.png)

De volgende functies kunnen voor de component worden geactiveerd of gedeactiveerd.

* Onbewerkte tekst plakken
* Plakken van woord
* Zoeken en vervangen
* Spellingcontrole
* Bronbewerking

### Opmaak {#formatting}

![](/help/assets/chlimage_1-29.png)

De volgende opmaakopties kunnen voor de component worden geactiveerd of gedeactiveerd.

* Tabel
* Lijsten
* Uitlijning
* Vet, cursief, onderstrepen
* Koppelingen
* Subscript/superscript

### Alineastijlen {#paragraph-styles}

![](/help/assets/chlimage_1-30.png)

Alineastijlen kunnen voor de component worden geactiveerd of gedeactiveerd. Als deze optie is geactiveerd, kunnen de toegestane indelingen worden gedefinieerd.

* Tik of klik op de knop **Toevoegen** om een nieuwe stijl in te voegen.
* Voer de code in van de stijl en een beschrijving die worden weergegeven in het dialoogvenster Bewerken.
* Als u een stijltik wilt verwijderen of op de knop **Verwijderen** wilt klikken.
* Tik of klik op de handgrepen om de volgorde van de indelingen te wijzigen.

### Speciale tekens configureren {#configuring-special-characters}

![](/help/assets/chlimage_1-31.png)

De optie voor het invoegen van speciale tekens kan voor de component worden geactiveerd of gedeactiveerd. Als deze optie is geactiveerd, kunnen de toegestane tekens worden gedefinieerd.

* Tik of klik op de knop **Toevoegen** om een nieuw teken in te voegen.
* Voer de HTML-code in van het teken en een beschrijving die wordt weergegeven in het dialoogvenster Bewerken.
* Als u een tikteken wilt verwijderen of op de knop **Verwijderen** wilt klikken.
* Als u de volgorde van de tekens wilt wijzigen, tikt u of klikt u en sleept u de handgrepen.

## Tabblad Stijlen {#styles-tab}

De component Text ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).