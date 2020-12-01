---
title: Carousel-component
description: Met de Carousel-component kan de auteur van de inhoud inhoud inhoud presenteren in een roterende carrousel.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '1112'
ht-degree: 0%

---


# Carousel-component{#carousel-component}

Met de Core Component Carousel Component kan de auteur van de inhoud inhoud inhoud presenteren in een navigeerbare carrousel.

## Gebruik {#usage}

Met de Carousel-component ordent de auteur van de inhoud de inhoud in een draaiende carrousel van dia&#39;s.

Met het dialoogvenster [Bewerken](#edit-dialog) kan de auteur van de inhoud meerdere dia&#39;s maken, benoemen en ordenen en kan de automatische overgang met vertraging worden ingeschakeld. Met behulp van het [ontwerpdialoogvenster](#design-dialog) kan de sjabloonauteur definiëren welke componenten aan de carrousel kunnen worden toegevoegd, automatische overgangen in- of uitschakelen en de stijlen aanpassen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Carousel-component is v1, die in oktober 2018 is geïntroduceerd met versie 2.2.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_carousel) om de Carousel-component te ervaren en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van Carousel [kan op GitHub](https://adobe.com/go/aem_cmp_tech_carousel_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster {#edit-dialog} bewerken

In het dialoogvenster Bewerken kan de auteur van de inhoud dia&#39;s toevoegen, hernoemen en opnieuw rangschikken en de instellingen voor automatische overgangen definiëren.

### Tabblad Items {#items-tab}

![Tabblad Items van het dialoogvenster Bewerken van de Carousel-component](/help/assets/carousel-edit-items.png)

Gebruik de **Add** knoop om de componentenselecteur te openen om te kiezen welke component om als lusje toe te voegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:

* **Pictogram**  - Het pictogram van het componenttype van de tab voor eenvoudige identificatie in de lijst. Plaats de muis boven de volledige componentnaam als knopinfo.
* **Beschrijving**  - De beschrijving die als tekst van het lusje wordt gebruikt, die aan de naam van de component in gebreke blijft die voor het lusje wordt geselecteerd.
* **Verwijderen**  - Tik of klik om de tab uit de tabbladcomponent te verwijderen.
* **Opnieuw ordenen**  - Tik of klik en sleep om de tabbladen te ordenen.

>[!TIP]
>
>Als de viewport van de pagina wordt verminderd zodat het bewerkingsdialoogvenster volledig scherm wordt, wordt de **Add** knoop verborgen. Componenten kunnen nog steeds aan de Carousel-component worden toegevoegd door [vanuit de componentbrowser te slepen en neer te zetten op de Carousel-component in de pagina-editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component-from-the-components-browser).

### Tabblad Eigenschappen {#properties-tab}

![Het tabblad Eigenschappen van het dialoogvenster Bewerken van de Carousel-component](/help/assets/carousel-edit-properties.png)

Op het tabblad **Eigenschappen** kan de auteur van de inhoud de dia&#39;s instellen op automatische overgang.

* **Dia&#39;s**  automatisch overschakelen - Als de component actief is, gaat deze na een opgegeven vertraging automatisch naar de volgende dia.
* **Vertraging**  overgang - Wanneer de optie voor automatische overgang is ingeschakeld, wordt deze waarde gebruikt om de vertraging tussen overgangen (in milliseconden) te definiëren.
* **Automatisch pauzeren uitschakelen bij aanwijzen**  - Als  **Automatische** overgang is ingeschakeld, wordt de carrouselovergang automatisch gepauzeerd wanneer de cursor boven de carrousel wordt geplaatst. Selecteer deze optie om de overgang niet te pauzeren.
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

>[!NOTE]
>
>De besturingselementen voor diavoorstellingen worden niet ingeschakeld in de modus **Bewerken**. Gebruik [**Voorvertoning** modus](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode) of de optie **[Weergeven als gepubliceerd](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** om te communiceren met de carrousel als een lezer van de gepubliceerde inhoud.
>
>De functie voor automatisch vooruitgaan is niet ingeschakeld in de modus **Bewerken**. Gebruik **[Weergeven als gepubliceerd](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** optie om de functie voor automatisch vooruitgaan te zien als een lezer van de gepubliceerde inhoud.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Het tabblad Toegankelijkheid van het dialoogvenster Bewerken van de Carousel-component](/help/assets/carousel-edit-accessibility.png)

Op het tabblad **Toegankelijkheid** kunnen waarden worden ingesteld voor [ARIA-toegankelijkheidslabels](https://www.w3.org/WAI/standards-guidelines/aria/) voor de component.

* **Label**  - waarde van een ARIA-labelkenmerk voor de component

## Deelvenster {#select-panel} selecteren

De auteur van de inhoud kan de optie **Select Panel** op de componentwerkbalk gebruiken om over te schakelen naar een andere dia voor bewerking en om de volgorde van de dia&#39;s gemakkelijk te wijzigen.

![Pictogram van deelvenster Selecteren](/help/assets/select-panel-icon.png)

Nadat u de optie **Deelvenster selecteren** hebt geselecteerd op de componentwerkbalk, worden de geconfigureerde dia&#39;s weergegeven als een vervolgkeuzelijst.

* De lijst wordt geordend door de toegewezen rangschikking van de dia&#39;s en wordt weerspiegeld in de nummering.
* Het componenttype van de dia wordt eerst weergegeven, gevolgd door de beschrijving van de dia in een lichter lettertype.

![Deelvenster Selecteren](/help/assets/select-panel-popover.png)

* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar die dia verplaatst.
* U kunt de volgorde van de dia op de juiste plaats wijzigen door de sleepgrepen te gebruiken.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren welke componenten als dia&#39;s aan de carrouselcomponent kunnen worden toegevoegd, en welke standaardinstellingen voor automatische overgangen worden gedefinieerd en welke aangepaste stijlen beschikbaar zijn voor de auteur van de inhoud.

### Tabblad Eigenschappen {#properties-tab-1}

Het tabblad **Eigenschappen** wordt gebruikt om de standaardinstellingen voor de diaovergangen te definiëren wanneer de auteur van de inhoud de carrouselcomponent aan een pagina toevoegt.

![Dialoogvenster Ontwerpen van de Carousel-component](/help/assets/carousel-design.png)

* **Automatische overgangsdia** &#39;s - Hiermee wordt gedefinieerd of de optie om de carrousel automatisch naar de volgende dia te verplaatsen standaard is ingeschakeld wanneer de auteur van de inhoud de carrouselcomponent aan een pagina toevoegt.
* **Vertraging**  overgang - Hiermee wordt de standaardwaarde van de overgangsvertraging tussen dia&#39;s (in milliseconden) gedefinieerd wanneer de auteur van de inhoud de carrouselcomponent aan een pagina toevoegt.
* **Automatisch pauzeren uitschakelen bij aanwijzen**  - Hiermee wordt de optie voor het automatisch pauzeren van dia standaard uitgeschakeld als de optie voor het  **automatisch pauzeren van dia&#39;s automatisch** wordt geselecteerd door de auteur van de inhoud.

### Tabblad Toegestane componenten {#allowed-components-tab}

Het tabblad **Toegestane componenten** wordt gebruikt om te definiëren welke componenten door de auteur van de inhoud als dia&#39;s aan de Carousel-component kunnen worden toegevoegd.

Het tabblad Toegestane componenten werkt op dezelfde manier als het tabblad met dezelfde naam wanneer [het beleid en de eigenschappen van een container voor de layout in de Sjablooneditor worden gedefinieerd.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Tabblad Stijlen {#styles-tab}

De Carousel-component ondersteunt het AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
