---
title: Tekstcomponent (v1)
description: De component Text is een component voor tekstbewerking en -compositie met tekstopmaak die op locatie kan worden bewerkt.
index: n
role: Architect, Developer, Admin, User
exl-id: c9fe3052-a33d-412e-9456-52c9a0cea292
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '1657'
ht-degree: 0%

---

# Tekstcomponent (v1) {#text-component-v}

De component Text is een component voor tekstbewerking en -compositie met tekstopmaak die op locatie kan worden bewerkt.

## Gebruik {#usage}

De component Text biedt een robuuste teksteditor met tekstopmaak die het mogelijk maakt tekst eenvoudig te bewerken in een vereenvoudigde, inline editor en in een volledige schermopmaak.

De [dialoogvenster bewerken](#edit-dialog) functies voor inline bewerking met beperkte opties en volledige functionaliteit beschikbaar in het dialoogvenster Volledig scherm bewerken. Met de [ontwerpdialoogvenster](#design-dialog), tekstopmaakopties zoals koppen, speciale tekens en alineastijlen kunnen worden geconfigureerd voor de sjabloon voor de auteur van de inhoud.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de tekstcomponent beschreven, die oorspronkelijk is geïntroduceerd met versie 1.0.0 van de kerncomponenten met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van v1 van de tekstcomponent weergegeven.

| AEM | Tekstcomponent v1 |
|--- |--- |
| 6.3 | Compatibel |
| 6.4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de tekstcomponent beschreven.
>
>Zie voor meer informatie over de huidige versie van de Tekstcomponent het gedeelte [Tekstcomponent](/help/components/text.md) document.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende monster wordt genomen uit [Wij.Detailhandel](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Schermafbeelding {#screenshot}

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
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Zie de [compatibiliteitsinformatie voor Core Components v1](/help/versions.md) voor meer informatie .

## Dialoogvenster Bewerken {#edit-dialog}

Het dialoogvenster Bewerken bevat de standaardgereedschappen voor tekstopmaak die de gebruiker zou verwachten bij het samenstellen van tekst.

![](/help/assets/chlimage_1-52.png)

* Vet

   ![](/help/assets/chlimage_1-53.png)

   Wordt gebruikt om vette opmaak toe te passen op geselecteerde tekst of opgemaakte tekst die na de cursor wordt ingevoerd.

   **Ctrl+B** kan als toetsenbordkortere weg worden gebruikt.

* Cursief

   ![](/help/assets/chlimage_1-54.png)

   Wordt gebruikt om cursieve opmaak toe te passen op geselecteerde tekst of om tekst die na de cursor wordt ingevoerd, cursief te maken.

   **Ctrl+I** kan als toetsenbordkortere weg worden gebruikt.

* Onderstrepen

   ![](/help/assets/chlimage_1-55.png)

   Wordt gebruikt om onderstreepte opmaak toe te passen op geselecteerde tekst of onderstreepte tekst die na de cursor wordt ingevoerd.

   **Ctrl+U** kan als toetsenbordkortere weg worden gebruikt.

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

   Voer de tekst in die u wilt doorzoeken en tikken of waarop u wilt klikken **Zoeken** om de zoekopdracht te starten. Tik of klik op de x om te annuleren.

   Selecteer de optie als u een exacte overeenkomst wilt uitvoeren op basis van het hoofdlettergebruik **Hoofdlettergebruik afstemmen** voordat u de zoekopdracht start.

   Als een overeenkomst wordt gevonden, wordt deze gemarkeerd en wordt het zoekdialoogvenster gedimd weergegeven. Tik of klik op de knop **Zoeken** weer in het grijze dialoogvenster om naar de volgende instantie te zoeken.

   ![](/help/assets/chlimage_1-67.png)

   Als er geen andere exemplaren worden gevonden, wordt een bericht weergegeven en wordt de zoekopdracht opnieuw gestart vanaf het begin van de tekst.

   ![](/help/assets/chlimage_1-68.png)

* Vervangen

   ![](/help/assets/chlimage_1-69.png)

   Gebruik deze optie om de tekst te zoeken op instanties van een opgegeven tekenreeks en de overeenkomsten te vervangen door een andere tekenreeks. Als u deze optie selecteert, wordt een venster geopend waarin u de opties voor zoeken en vervangen kunt opgeven.

   ![](/help/assets/chlimage_1-70.png)

   Voer de tekst in waarnaar u wilt zoeken en de tekst waarmee u deze wilt vervangen.

   Tik of klik op **Zoeken** om de zoekopdracht te starten. Klik of tik op de x om te annuleren.

   Selecteer de optie als u een exacte overeenkomst wilt uitvoeren op basis van het hoofdlettergebruik **Hoofdlettergebruik afstemmen** voordat u de zoekopdracht start.

   Als een overeenkomst wordt gevonden, wordt deze gemarkeerd en wordt het zoekdialoogvenster gedimd weergegeven. Klik op de knop **Zoeken** opnieuw in het gedimde dialoogvenster om naar de volgende instantie te zoeken of selecteer de knop **Vervangen** om de gemarkeerde, overeenkomende tekst te vervangen. De **Vervangen** de knop is alleen actief als er een overeenkomst is bereikt.

   Selecteren **Alles vervangen** om alle instanties van de tekst tegelijk te vervangen.

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

   Tik of klik op de knop **Opsommingsteken** nogmaals of twee Enter-tekens invoeren.

* Genummerd

   ![](/help/assets/chlimage_1-75.png)

   Hiermee maakt u de geselecteerde tekst op als een genummerde lijst of begint u met het invoegen van een genummerde lijst na de cursor.

   Tik op een genummerde lijst of klik op de knop **Genummerd** nogmaals of twee Enter-tekens invoeren.

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

   * **Kolommen** - Het aantal kolommen in de tabel (verplicht)
   * **Rijen** - Het aantal rijen van de tabel (vereist)
   * **Breedte** - De breedte van de tabel
   * **Hoogte** - De hoogte van de tabel
   * **Celopvulling** g - De ruimte rondom de celinhoud
   * **Celafstand** - De ruimte tussen cellen
   * **Rand** - Het gewicht van de randlijnen van de tabel
   * Indien voor de koptekst van de tabel:

      * De eerste rij moet worden gebruikt
      * De eerste kolom moet worden gebruikt
      * De eerste rij en de eerste kolom moeten worden gebruikt
      * Of er moet geen header worden gebruikt.
   * **Bijschrift** - Het bijschrift van de tabel


* Spellingcontrole

   ![](/help/assets/chlimage_1-80.png)

   Wordt gebruikt om de spelling van de tekstinhoud te controleren. Mogelijke spelfouten worden onderstreept met gebroken, rode lijnen.

* Speciale tekens

   ![](/help/assets/chlimage_1-81.png)

   Wordt gebruikt om speciale tekens in te voegen in de tekst. Als u deze optie selecteert, wordt een venster geopend waarin de beschikbare tekens worden weergegeven.

   ![](/help/assets/chlimage_1-82.png)

   Tik op het gewenste teken of klik op het gewenste teken om het teken na de cursor in te voegen in de tekst. U kunt meerdere tekens invoegen. Tik of klik op de x om het selectievenster te sluiten.

* Bron bewerken

   ![](/help/assets/chlimage_1-83.png)

   Wordt gebruikt om de HTML-bron van de tekst weer te geven en te wijzigen.

   Tik of klik op de knop **Bron bewerken** om de inhoud van de tekst vanuit de opgemaakte weergave te wijzigen en de onbewerkte HTML weer te geven. In deze modus zijn alle andere opmaakopties uitgeschakeld. Tik of klik op de knop **Bron bewerken** opnieuw om naar de opgemaakte weergave terug te gaan.

   >[!CAUTION]
   >
   >Zoals altijd het geval is bij de toegang tot ruwe HTML, moet voorzichtigheid worden betracht bij het gebruik van de **Bron bewerken** optie!
   >
   >
   >HTML ingevoerd via **Bron bewerken** wordt gescand op XSS-risico&#39;s en alle scripts die worden ingevoegd, worden verwijderd en niet weergegeven op de resulterende pagina. Onjuist gevormde HTML is echter ingevoerd in **Bron bewerken** kan de sjabloon voor de pagina onderbreken, wat resulteert in een onverwachte opmaak of een onbruikbare pagina.

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
* Als u een stijltik wilt verwijderen of op de knop **Verwijderen** knop.
* Tik of klik op de handgrepen om de volgorde van de indelingen te wijzigen.

### Speciale tekens {#special-characters}

![](/help/assets/chlimage_1-31.png)

De optie voor het invoegen van speciale tekens kan voor de component worden geactiveerd of gedeactiveerd. Als deze optie is geactiveerd, kunnen de toegestane tekens worden gedefinieerd.

* Tik of klik op de knop **Toevoegen** om een nieuw teken in te voegen.
* Voer de HTML-code in van het teken en een beschrijving die wordt weergegeven in het dialoogvenster Bewerken.
* Als u een tekenkraan wilt verwijderen of op de knop **Verwijderen** knop.
* Als u de volgorde van de tekens wilt wijzigen, tikt u of klikt u en sleept u de handgrepen.

## Technische details {#technical-details}

De meest recente technische documentatie over de component Text [kan op GitHub worden gevonden](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v1/text).

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).
