---
title: Carousel-component
description: Met de Carousel-component kan de auteur van de inhoud inhoud inhoud presenteren in een roterende carrousel.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Carousel-component{#carousel-component}

Met de Core Component Carousel Component kan de auteur van de inhoud inhoud inhoud presenteren in een navigeerbare carrousel.

## Gebruik {#usage}

Met de Carousel-component ordent de auteur van de inhoud de inhoud in een draaiende carrousel van dia&#39;s.

In het dialoogvenster [](#edit-dialog) Bewerken kan de auteur van de inhoud meerdere dia&#39;s maken, benoemen en ordenen en de automatische overgang met vertraging inschakelen. Met behulp van het dialoogvenster [](#design-dialog)Ontwerp kan de sjabloonauteur definiëren welke componenten aan de carrousel kunnen worden toegevoegd, automatische overgangen in- of uitschakelen en de stijlen aanpassen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Carousel-component is v1, die in oktober 2018 is geïntroduceerd met versie 2.2.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v1 | Compatibel | Compatibel | Compatibel | Compatibel |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_carousel)om de Carousel-component te ervaren en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de Component Carousel [kan op GitHub](https://adobe.com/go/aem_cmp_tech_carousel_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud dia&#39;s toevoegen, hernoemen en opnieuw rangschikken en de instellingen voor automatische overgangen definiëren.

### Tabblad Items {#items-tab}

![](/help/assets/screen-shot-2019-08-29-12.01.39.png)

Gebruik de knop **Toevoegen** om de componentkiezer te openen en te kiezen welke component u als tab wilt toevoegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:

* **Pictogram** - Het pictogram van het componenttype van de tab voor eenvoudige identificatie in de lijst. Plaats de muis boven de volledige componentnaam als knopinfo.
* **Beschrijving** - De beschrijving die als tekst van het lusje wordt gebruikt, die aan de naam van de component in gebreke blijft die voor het lusje wordt geselecteerd.
* **Verwijderen** - Tik of klik om de tab uit de component tabs te verwijderen.
* **Opnieuw ordenen** - Tik of klik en sleep om de tabbladen te ordenen.

>[!TIP]
>
>Als de viewport van de pagina wordt verminderd zodat het bewerkingsdialoogvenster volledig scherm wordt, wordt de knop **Toevoegen** verborgen. Componenten kunnen nog steeds aan de Carousel-component worden toegevoegd door [te slepen vanuit de componentbrowser en neer te zetten op de Carousel-component in de pagina-editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component-from-the-components-browser).

### Tabblad Eigenschappen {#properties-tab}

![](/help/assets/screen-shot-2019-08-29-12.01.57.png)

Op het tabblad **Eigenschappen** kan de auteur van de inhoud de dia&#39;s instellen op een automatische overgang.

* **Dia&#39;s** automatisch overschakelen - Als deze actief zijn, gaat de component na een opgegeven vertraging automatisch naar de volgende dia.
* **Vertraging** overgang - Wanneer de dia&#39;s voor automatische overgang zijn geselecteerd, wordt deze waarde gebruikt om de vertraging tussen overgangen (in milliseconden) te bepalen.
* **Automatisch pauzeren uitschakelen bij aanwijzen** - Als **Automatisch overgangsdia** is geselecteerd, wordt de carrouselovergang automatisch gepauzeerd wanneer de cursor boven de carrousel wordt geplaatst. Selecteer deze optie om de overgang niet te pauzeren.

>[!NOTE]
>
>De besturingselementen voor diavoorstellingen zijn niet ingeschakeld in de modus **Bewerken** . Gebruik de modus [**Voorvertoning **of de optie](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode)Weergeven als gepubliceerd **[](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)**om te communiceren met de carrousel als een lezer van de gepubliceerde inhoud.
>
>De functie voor automatisch vooruitgaan is niet ingeschakeld in de modus **Bewerken** . Met de optie **[Weergeven als gepubliceerd](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)**kunt u de functie voor automatisch vooruitgaan bekijken als een lezer van de gepubliceerde inhoud.

### Tabblad Toegankelijkheid {#accessibility-tab}

![](/help/assets/screen-shot-2019-08-29-12.02.22.png)

Op het tabblad **Toegankelijkheid** kunnen waarden worden ingesteld voor [ARIA-toegankelijkheidslabels](https://www.w3.org/WAI/standards-guidelines/aria/) voor de component.

* **Label** - waarde van een ARIA-labelkenmerk voor de component

## Deelvenster selecteren {#select-panel}

De auteur van de inhoud kan de optie Deelvenster **** selecteren op de componentwerkbalk gebruiken om over te schakelen op een andere dia die u kunt bewerken en om de volgorde van de dia&#39;s gemakkelijk te wijzigen.

![](/help/assets/screenshot_2018-10-11at165417.png)

Nadat u de optie Deelvenster **** selecteren op de componentwerkbalk hebt geselecteerd, worden de geconfigureerde dia&#39;s weergegeven als een vervolgkeuzelijst.

* De lijst wordt geordend door de toegewezen rangschikking van de dia&#39;s en wordt weerspiegeld in de nummering.
* Het componenttype van de dia wordt eerst weergegeven, gevolgd door de beschrijving van de dia in een lichter lettertype.

![](/help/assets/opera_snapshot_2018-11-28141537localhost.png)

* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar die dia verplaatst.
* U kunt de volgorde van de dia op de juiste plaats wijzigen door de sleepgrepen te gebruiken.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren welke componenten als dia&#39;s aan de carrouselcomponent kunnen worden toegevoegd, en welke standaardinstellingen voor automatische overgangen worden gedefinieerd en welke aangepaste stijlen beschikbaar zijn voor de auteur van de inhoud.

### Tabblad Eigenschappen {#properties-tab-1}

Het tabblad **Eigenschappen** wordt gebruikt om de standaardinstellingen voor de diaovergangen te definiëren wanneer de auteur van de inhoud de carrouselcomponent aan een pagina toevoegt.

![](/help/assets/screenshot_2018-11-28at141824.png)

* **Automatische overgangsdia** &#39;s - Hiermee wordt gedefinieerd of de optie om de carrousel automatisch naar de volgende dia te verplaatsen standaard is ingeschakeld wanneer de auteur van de inhoud de carrouselcomponent aan een pagina toevoegt.
* **Vertraging** overgang - Definieert de standaardwaarde van de overgangsvertraging tussen dia&#39;s (in milliseconden) wanneer de auteur van de inhoud de carrouselcomponent aan een pagina toevoegt.
* **Automatisch pauzeren bij aanwijzen** uitschakelen - Definieert of de optie voor het automatisch pauzeren van dia&#39;s standaard is ingeschakeld wanneer de **overgangsdia** &#39;s automatisch worden geselecteerd door de auteur van de inhoud.

### Tabblad Toegestane componenten {#allowed-components-tab}

Het tabblad **Toegestane componenten** wordt gebruikt om te definiëren welke componenten door de auteur van de inhoud als dia&#39;s aan de Carousel-component kunnen worden toegevoegd.

Het tabblad Toegestane componenten werkt op dezelfde manier als het tabblad met dezelfde naam wanneer u het beleid en de eigenschappen van een container voor de layout in de Sjablooneditor [definieert.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Tabblad Stijlen {#styles-tab}

De Carousel-component ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).
