---
title: Tekstcomponent (v1)
description: De component Text is een component voor tekstbewerking en -compositie met tekstopmaak die op locatie kan worden bewerkt.
index: n
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1662'
ht-degree: 1%

---


# Tekstcomponent (v1) {#text-component-v}

De component Text is een component voor tekstbewerking en -compositie met tekstopmaak die op locatie kan worden bewerkt.

## Gebruik {#usage}

De component Text biedt een robuuste teksteditor met tekstopmaak die het mogelijk maakt tekst eenvoudig te bewerken in een vereenvoudigde, inline editor en in een volledige schermopmaak.

Het [bewerkingsdialoogvenster](#edit-dialog) bevat inline bewerking met beperkte opties met volledige functionaliteit beschikbaar in het dialoogvenster Volledig scherm bewerken. Met behulp van het [ontwerpdialoogvenster](#design-dialog) kunnen opties voor tekstopmaak, zoals koppen, speciale tekens en alineastijlen, worden geconfigureerd voor de sjabloon voor de auteur van de inhoud.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de tekstcomponent beschreven, die oorspronkelijk is geïntroduceerd met versie 1.0.0 van de kerncomponenten met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van v1 van de tekstcomponent weergegeven.

| AEM | Tekstcomponent v1 |
|--- |--- |
| 6,3 | Compatibel |
| 6,4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de tekstcomponent beschreven.
>
>Zie het document [Tekstcomponent](/help/components/text.md) voor meer informatie over de huidige versie van de tekstcomponent.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende voorbeeld wordt genomen uit [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](/help/assets/chlimage_1-27.png)

### HTML {#html}

```
<div class="cmp cmp-text aem-GridColumn aem-GridColumn--default--12">
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer porttitor ante a tortor volutpat maximus. Donec eu porta eros. Aenean sit amet eleifend arcu, eu vestibulum magna. Fusce eget nisi tincidunt, tristique felis quis, tincidunt est. Aliquam consequat aliquam quam non eleifend. Phasellus ut magna luctus, aliquam risus eget, fermentum augue. Aliquam lobortis accumsan magna, quis efficitur enim dictum eu. Pellentesque iaculis felis eget felis commodo, non euismod dolor euismod. Quisque nec arcu rutrum, mollis tortor non, sollicitudin odio. Sed dictum nulla mauris, eu pretium dui vulputate a. Maecenas lacus massa, egestas vitae tincidunt eu, interdum et magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eleifend ex lacus, in consectetur nunc interdum et. Donec interdum mi vitae dolor pretium mattis. In quis arcu sapien. Phasellus at metus vitae nisi tincidunt varius.<br />
</p>
</div>
```

### JSON {#json}

```
"text": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "text": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer porttitor ante a tortor volutpat maximus. Donec eu porta eros. Aenean sit amet eleifend arcu, eu vestibulum magna. Fusce eget nisi tincidunt, tristique felis quis, tincidunt est. Aliquam consequat aliquam quam non eleifend. Phasellus ut magna luctus, aliquam risus eget, fermentum augue. Aliquam lobortis accumsan magna, quis efficitur enim dictum eu. Pellentesque iaculis felis eget felis commodo, non euismod dolor euismod. Quisque nec arcu rutrum, mollis tortor non, sollicitudin odio. Sed dictum nulla mauris, eu pretium dui vulputate a. Maecenas lacus massa, egestas vitae tincidunt eu, interdum et magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eleifend ex lacus, in consectetur nunc interdum et. Donec interdum mi vitae dolor pretium mattis. In quis arcu sapien. Phasellus at metus vitae nisi tincidunt varius.</p>\n",
              "richText": true,
              ":type": "weretail/components/content/text"
            }
```

>[!NOTE]
>
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Zie [compatibiliteitsinformatie voor Core Components v1](/help/versions.md) voor meer informatie.

## Dialoogvenster {#edit-dialog} bewerken

Het dialoogvenster Bewerken bevat de standaardgereedschappen voor tekstopmaak die de gebruiker zou verwachten bij het samenstellen van tekst.

![](/help/assets/chlimage_1-52.png)

* Vet

   ![](/help/assets/chlimage_1-53.png)

   Wordt gebruikt om vette opmaak toe te passen op geselecteerde tekst of opgemaakte tekst die na de cursor wordt ingevoerd.

   **Ctrl+** Bcan wordt gebruikt als een sneltoets.

* Cursief

   ![](/help/assets/chlimage_1-54.png)

   Wordt gebruikt om cursieve opmaak toe te passen op geselecteerde tekst of om tekst die na de cursor wordt ingevoerd, cursief te maken.

   **Ctrl+** Ican be used as a keyboard shortcut.

* Onderstrepen

   ![](/help/assets/chlimage_1-55.png)

   Wordt gebruikt om onderstreepte opmaak toe te passen op geselecteerde tekst of onderstreepte tekst die na de cursor wordt ingevoerd.

   **Ctrl+** Ucan be used as a keyboard shortcut.

* Subscript

   ![](/help/assets/chlimage_1-56.png)

   Wordt gebruikt om geselecteerde tekst of tekst die na de cursor is ingevoerd, op te maken als een subscript.

* Superscript

   ![](/help/assets/chlimage_1-57.png)

   Wordt gebruikt om geselecteerde tekst of tekst die na de cursor is ingevoerd, op te maken als superscript.

* Plakken als tekst

   ![](/help/assets/chlimage_1-58.png)

   Hiermee plakt u alle gekopieerde tekst als onbewerkte tekst zonder opmaak.

   Wanneer u deze optie selecteert, wordt een venster geopend waarin de tekst als onbewerkte tekst zonder opmaak kan worden geplakt als een voorvertoning voordat deze in de tekst wordt ingevoegd. Accepteren door te tikken of op het vinkje te klikken, annuleren door te tikken of op de x te klikken.

   ![](/help/assets/chlimage_1-59.png)

* Plakken vanuit Word

   ![](/help/assets/chlimage_1-60.png)

   Wanneer u deze optie selecteert, wordt een venster geopend waarin de tekst kan worden geplakt met behoud van de opmaak als voorvertoning voordat deze in de tekst wordt ingevoegd. Accepteren door te tikken of op het vinkje te klikken, annuleren door te tikken of op de x te klikken.

   ![](/help/assets/chlimage_1-61.png)

* Hyperlink

   ![](/help/assets/chlimage_1-62.png)

   Met deze optie kunt u de geselecteerde tekst omzetten in een hyperlink of een reeds gedefinieerde koppeling wijzigen. Deze optie is alleen actief als er al tekst is geselecteerd en er een venster wordt geopend met aanvullende opties voor het instellen van de koppeling.

   ![](/help/assets/chlimage_1-63.png)

   * Voer de locatie in

      * Kies in het dialoogvenster Selectie openen een pad in AEM
      * Als de koppeling zich niet binnen AEM bevindt, voert u de absolute URL in (niet-absolute paden worden geïnterpreteerd als relatief ten opzichte van AEM)
   * Alternatieve beschrijvende tekst voor de koppeling invoeren
   * Koppelingsgedrag selecteren

      * Doel
      * Zelfde tabblad
      * Nieuw tabblad
      * Bovenliggend frame
      * Bovenste frame

   Tik of klik op het vinkje om de koppeling toe te passen of klik op de x om te annuleren.

* Ontkoppelen

   ![](/help/assets/chlimage_1-64.png)

   Gebruik deze optie om een koppeling te verwijderen die al op de geselecteerde tekst is toegepast. Deze optie is alleen actief als er al een koppeling is geselecteerd.

* Zoeken

   ![](/help/assets/chlimage_1-65.png)

   Gebruik deze optie om de tekst te zoeken op instanties van een opgegeven tekstreeks. Als u deze optie selecteert, wordt een venster geopend waarin u de zoekopties kunt opgeven.

   ![](/help/assets/chlimage_1-66.png)

   Voer de tekst in waarvoor u wilt zoeken en tikken of klik op **Zoeken** om de zoekopdracht te starten. Tik of klik op de x om te annuleren.

   Als u een nauwkeurige gelijke volgens het geval wilt doen, selecteer de optie **Kwestie** alvorens het onderzoek te beginnen.

   Als een overeenkomst wordt gevonden, wordt deze gemarkeerd en wordt het zoekdialoogvenster gedimd weergegeven. Tik of klik nogmaals op de knop **Zoeken** in het grijze dialoogvenster om naar de volgende instantie te zoeken.

   ![](/help/assets/chlimage_1-67.png)

   Als er geen andere exemplaren worden gevonden, wordt een bericht weergegeven en wordt de zoekopdracht opnieuw gestart vanaf het begin van de tekst.

   ![](/help/assets/chlimage_1-68.png)

* Replace

   ![](/help/assets/chlimage_1-69.png)

   Gebruik deze optie om de tekst te zoeken op instanties van een opgegeven tekenreeks en de overeenkomsten te vervangen door een andere tekenreeks. Als u deze optie selecteert, wordt een venster geopend waarin u de opties voor zoeken en vervangen kunt opgeven.

   ![](/help/assets/chlimage_1-70.png)

   Voer de tekst in waarnaar u wilt zoeken en de tekst waarmee u deze wilt vervangen.

   Tik of klik op **Zoeken** om te beginnen met zoeken. Klik of tik op de x om te annuleren.

   Als u een nauwkeurige gelijke volgens het geval wilt doen, selecteer de optie **Kwestie** alvorens het onderzoek te beginnen.

   Als een overeenkomst wordt gevonden, wordt deze gemarkeerd en wordt het zoekdialoogvenster gedimd weergegeven. Klik nogmaals op de knop **Zoeken** in het grijze dialoogvenster om naar de volgende instantie te zoeken of selecteer de knop **Vervangen** om de gemarkeerde, overeenkomende tekst te vervangen. De knop **Vervangen** is alleen actief als er een overeenkomst is gemaakt.

   Selecteer **Alles vervangen** om alle instanties van de tekst tegelijk te vervangen.

* Tekst links uitlijnen

   ![](/help/assets/chlimage_1-71.png)

   Wordt gebruikt om de tekst uit te lijnen met de linkermarge.

* Tekst centreren

   ![](/help/assets/chlimage_1-72.png)

   Wordt gebruikt om de tekst te centreren.

* Tekst rechts uitlijnen

   ![](/help/assets/chlimage_1-73.png)

   Wordt gebruikt om de tekst uit te lijnen met de rechtermarge.

* Opsommingsteken

   ![](/help/assets/chlimage_1-74.png)

   Wordt gebruikt om de geselecteerde tekst op te maken als een lijst met opsommingstekens of om te beginnen met het invoegen van een lijst met opsommingstekens na de cursor.

   Tik of klik nogmaals op de knop **Opsommingsteken** of voer twee regeleinden in om een lijst met opsommingstekens te beëindigen.

* Genummerd

   ![](/help/assets/chlimage_1-75.png)

   Hiermee maakt u de geselecteerde tekst op als een genummerde lijst of begint u met het invoegen van een genummerde lijst na de cursor.

   Tik of klik nogmaals op de knop **Genummerd** of voer twee regeleinden in om een genummerde lijst te beëindigen.

* Uitspringen

   ![](/help/assets/chlimage_1-76.png)

   Wordt gebruikt om het inspringingsniveau te verlagen van de geselecteerde tekst of tekst die na de cursor wordt ingevoerd.

   Alleen actief als de geselecteerde tekst of positie van de cursor al is ingesprongen.

* Inspringen

   ![](/help/assets/chlimage_1-77.png)

   Wordt gebruikt om het inspringingsniveau te verhogen van de geselecteerde tekst of tekst die na de cursor wordt ingevoerd.

* Tabel

   ![](/help/assets/chlimage_1-78.png)

   Wordt gebruikt om een tabel in de tekst in te voegen. Als u deze optie selecteert, wordt een venster geopend waarin u de details van de tabel kunt opgeven.

   ![](/help/assets/chlimage_1-79.png)

   * **Kolommen**  - Het aantal kolommen van de tabel (vereist)
   * **Rijen**  - Het aantal rijen van de tabel (vereist)
   * **Breedte**  - De breedte van de tabel
   * **Hoogte**  - De hoogte van de tabel
   * **Celopvulling**- De ruimte rondom de celinhoud
   * **Celafstand** : de ruimte tussen cellen
   * **Rand**  - Het gewicht van de randlijnen van de tabel
   * Indien voor de koptekst van de tabel:

      * De eerste rij moet worden gebruikt
      * De eerste kolom moet worden gebruikt
      * De eerste rij en de eerste kolom moeten worden gebruikt
      * Of er moet geen header worden gebruikt.
   * **Bijschrift**  - Het bijschrift van de tabel


* Spellingcontrole

   ![](/help/assets/chlimage_1-80.png)

   Wordt gebruikt om de spelling van de tekstinhoud te controleren. Mogelijke spelfouten worden onderstreept met gebroken, rode lijnen.

* Speciale tekens

   ![](/help/assets/chlimage_1-81.png)

   Wordt gebruikt om speciale tekens in te voegen in de tekst. Als u deze optie selecteert, wordt een venster geopend waarin de beschikbare tekens worden weergegeven.

   ![](/help/assets/chlimage_1-82.png)

   Tik op het gewenste teken of klik op het gewenste teken om het na de cursor in de tekst in te voegen. U kunt meerdere tekens invoegen. Tik of klik op de x om het selectievenster te sluiten.

* Bron bewerken

   ![](/help/assets/chlimage_1-83.png)

   Wordt gebruikt om de HTML-bron van de tekst weer te geven en te wijzigen.

   Tik of klik op het pictogram **Bron bewerken** om de inhoud van de tekst vanuit de opgemaakte weergave te wijzigen en de onbewerkte HTML weer te geven. In deze modus zijn alle andere opmaakopties uitgeschakeld. Tik of klik nogmaals op het pictogram **Bron bewerken** om terug te keren naar de opgemaakte weergave.

   >[!CAUTION]
   >
   >Zoals altijd het geval met toegang tot ruwe HTML, moet de voorzichtigheid worden uitgeoefend wanneer het gebruiken van **Bron geeft** optie uit!
   >
   >
   >HTML die is ingevoerd via **Source Edit** wordt gescand op XSS-risico&#39;s en alle scripts die worden ingevoegd, worden verwijderd en worden niet weergegeven op de resulterende pagina. Maar misvormde HTML die is ingevoerd in **Source Edit** kan de sjabloon voor de pagina onderbreken, wat resulteert in onverwachte opmaak of het onbruikbaar maken van de resulterende pagina.

* Alineaopmaak

   ![](/help/assets/chlimage_1-84.png)

   Wordt gebruikt om alineaopmaak toe te passen op de geselecteerde tekst of op tekst die na de cursor wordt ingevoegd. Als u deze optie selecteert, wordt een vervolgkeuzelijst geopend waarin de alineaopmaak wordt geselecteerd.

   ![](/help/assets/chlimage_1-85.png)

De tekstcomponent kan ook in regels worden bewerkt, maar vanwege ruimtebeperkingen zijn niet alle opmaakopties in regels beschikbaar. Schakel over naar de modus Volledig scherm om alle opties weer te geven.

![](/help/assets/chlimage_1-86.png)

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren welke tekstopmaakopties beschikbaar zijn voor de auteurs van de inhoud.

### Functies {#features}

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
* Als u een stijltik wilt verwijderen of op de knop **Delete** wilt klikken.
* Tik of klik op de handgrepen om de volgorde van de indelingen te wijzigen.

### Speciale tekens {#special-characters}

![](/help/assets/chlimage_1-31.png)

De optie voor het invoegen van speciale tekens kan voor de component worden geactiveerd of gedeactiveerd. Als deze optie is geactiveerd, kunnen de toegestane tekens worden gedefinieerd.

* Tik of klik op de knop **Toevoegen** om een nieuw teken in te voegen.
* Voer de HTML-code in van het teken en een beschrijving die wordt weergegeven in het dialoogvenster Bewerken.
* Als u een tikteken wilt verwijderen of op de knop **Verwijderen** wilt klikken.
* Als u de volgorde van de tekens wilt wijzigen, tikt u of klikt u en sleept u de handgrepen.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Tekst [kan op GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v1/text) worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).
