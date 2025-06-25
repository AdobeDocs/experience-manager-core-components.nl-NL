---
title: Carousel-component
description: Met de Carousel-component kan de auteur van de inhoud inhoud inhoud presenteren in een roterende carrousel.
role: Architect, Developer, Admin, User
exl-id: 3331214c-a05c-47e1-b54c-fbfd1045bd60
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '1317'
ht-degree: 0%

---


# Carousel-component{#carousel-component}

Met de Core Component Carousel Component kan de auteur van de inhoud inhoud inhoud presenteren in een navigeerbare carrousel.

{{traditional-aem}}

## Gebruik {#usage}

Met de Carousel-component ordent de auteur van de inhoud de inhoud in een draaiende carrousel van dia&#39;s.

Het [ geeft dialoog uit ](#edit-dialog) staat de inhoudauteur toe om, veelvoudige dia&#39;s tot stand te brengen te noemen en te ordenen evenals auto-overgang met vertraging toe te laten. Gebruikend de [ ontwerpdialoog ](#design-dialog), kan de malplaatjeauteur bepalen welke componenten aan de carrousel kunnen worden toegevoegd, automatische overgangen toelaten of onbruikbaar maken, en de stijlen aanpassen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Carousel-component is v1, die in oktober 2018 is geïntroduceerd met versie 2.2.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v1 | Compatibel systeem met <br>[ versie 2.17.4 ](/help/versions.md) en vroeger | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van Carousel te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_carousel).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van Carousel [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_carousel_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Diep koppelen aan een deelvenster {#deep-linking}

De Carrousel, [ Lusjes, ](tabs.md) en [ de steun van Componenten van de Accordeon ](accordion.md) die rechtstreeks met een paneel binnen de component verbinden.

Dit doet u als volgt:

1. Bekijk de pagina met de component gebruikend de **[Mening zoals Gepubliceerde ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=nl-NL#view-as-published)** optie in de paginaredacteur.
1. Controleer de inhoud van de pagina en identificeer de id van het deelvenster.
   * Bijvoorbeeld `id="carousel-bfe4fa6647-item-47f1a7ca67-tabpanel"`
1. De id wordt het anker dat u met een hash (`#`) aan de URL kunt toevoegen.
   * Bijvoorbeeld `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#carousel-bfe4fa6647-item-47f1a7ca67-tabpanel`

Wanneer u met de deelvenster-id als anker naar de URL navigeert, schuift de browser rechtstreeks naar de desbetreffende component en geeft deze het opgegeven deelvenster weer. Als het deelvenster is geconfigureerd om standaard niet te worden weergegeven, wordt er automatisch naar geschoven.

## Carousel en responsief ontwerp {#responsive-design}

Alle Core Components zijn ontworpen om volledig te reageren, zodat u over alle apparaten probleemloos kunt genieten.

Sommige geavanceerde componenten, zoals de Carousel-component, vereisen wellicht specifieke aandacht in het kader van het uitvoeringsproject om de reactiesnelheid in alle omstandigheden te behouden. Gelieve te zien het document [ Responsieve Ontwerp van de Componenten van de Kern ](/help/responsive.md) voor meer informatie.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud dia&#39;s toevoegen, hernoemen en opnieuw rangschikken en de instellingen voor automatische overgangen definiëren.

### Tabblad Items {#items-tab}

![ Punten tabel van uitgeeft dialoog van de Component van Carousel ](/help/assets/carousel-edit-items.png)

Gebruik **voeg** knoop toe om de componentenselecteur te openen om te kiezen welke component om als tabel toe te voegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:

* **Pictogram** - het pictogram van het componententype van het lusje voor gemakkelijke identificatie in de lijst. Plaats de muisaanwijzer boven de volledige componentnaam om deze weer te geven als knopinfo.
* **Beschrijving** - de beschrijving die als tekst van het lusje wordt gebruikt, die aan de naam van de component in gebreke blijft die voor het lusje wordt geselecteerd.
* **Schrapping** - Tik of klik om het lusje van de component van lusjes te schrappen.
* **opnieuw rangschikt** - Tik of klik en sleep om tot de lusjes opdracht te geven.

>[!TIP]
>
>Als viewport van de pagina wordt verminderd zodat uitgeeft dialoog volledig scherm wordt, **voegt** knoop toe zal worden verborgen. De componenten kunnen nog aan de Component van de Carrousel worden toegevoegd door [ van componenten te slepen browser en op de Component van de Carrousel in de paginaredacteur ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=nl-NL#inserting-a-component-from-the-components-browser) te vallen.

### Tabblad Eigenschappen {#properties-tab}

![ het lusje van Eigenschappen van uitgeeft dialoog van de Component van Carousel ](/help/assets/carousel-edit-properties.png)

Op het **lusje van Eigenschappen**, kan de inhoudauteur de dia&#39;s aan automatisch overgang plaatsen.

* **Actief Punt** - de inhoudauteur kan bepalen welk lusje actief is wanneer de pagina wordt geladen.
* **automatisch overgangsdia&#39;s** - wanneer actief, zal de component automatisch aan de volgende dia na een gespecificeerde vertraging vooruitgaan.
* **Vertraging van de Overgang** - wanneer de automatisch overgangsdia&#39;s wordt geselecteerd, wordt deze waarde gebruikt om de vertraging tussen overgangen (in milliseconden) te bepalen.
* **maak automatische pauze op hover** onbruikbaar - wanneer **automatisch overgangsdia&#39;s** wordt geselecteerd, zal de carrouselovergang automatisch pauzeren wanneer de curseur over de carrousel beweegt. Selecteer deze optie om de overgang niet te pauzeren.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

>[!NOTE]
>
>De controles van de diaversie worden niet toegelaten wanneer op **&#x200B;**&#x200B;wijze uitgeeft. De wijze van de Voorproef van het gebruik **[&#128279;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=nl-NL#preview-mode) of de**&#x200B;[ Mening zoals Gepubliceerde ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=nl-NL#view-as-published) **optie om met de carrousel in wisselwerking te staan aangezien een lezer van de gepubliceerde inhoud.**
>
>De auto-vooruitgangseigenschap wordt niet toegelaten wanneer in **&#x200B;**&#x200B;wijze uitgeeft. De Mening van het gebruik **[zoals Gepubliceerde ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=nl-NL#view-as-published)** optie om de auto-vooruitgangseigenschap als lezer van de gepubliceerde inhoud te zien.

### Tabblad Toegankelijkheid {#accessibility-tab}

![ het lusje van de Toegankelijkheid van uitgeeft dialoog van de Component van Carousel ](/help/assets/carousel-edit-accessibility.png)

Op het **lusje van de Toegankelijkheid**, kunnen de waarden voor [ de toegankelijkheidslabels van ARIA ](https://www.w3.org/WAI/standards-guidelines/aria/) voor de component worden geplaatst.

* **Etiket** - Waarde van een aria-etiket attribuut voor de carrousel, die de inhoud van de carrousel beschrijft
* **Vorige** - Waarde van een aria-etiket attribuut voor het vorige knoopetiket van de carrouselnavigatie
* **Volgende** - Waarde van een aria-etiket attribuut voor het volgende de knoopetiket van de carrouselnavigatie
* **Spel** - Waarde van een aria-etiket attribuut voor het de spelknoopetiket van de carrouselnavigatie
* **Pauze** - Waarde van een aria-etiket attribuut voor het de pauzeknoelabel van de carrouselnavigatie
* **Lijst** - Waarde van een aria-etiket attribuut voor de lijst van punten van de carrouselnavigatie etiket
* **plaats het etiket van de aria van het punt aan zijn titel** - als gecontroleerd, plaatst deze optie automatisch de carrouselpunttitel aan zijn aria-label beschrijving.

## Deelvenster selecteren {#select-panel}

De inhoudauteur kan de **Uitgezochte 1&rbrace; optie van het Comité op de componententoolbar gebruiken om in een verschillende dia te veranderen voor het uitgeven evenals de orde van de dia&#39;s gemakkelijk te herschikken.**

![ Uitgezochte paneelpictogram ](/help/assets/select-panel-icon.png)

Zodra het selecteren van de **Uitgezochte optie van het Comité** in de componententoolbar, worden de gevormde dia&#39;s getoond als drop-down.

* De lijst wordt geordend door de toegewezen rangschikking van de dia&#39;s en wordt weerspiegeld in de nummering.
* Het componenttype van de dia wordt eerst weergegeven, gevolgd door de beschrijving van de dia in een lichter lettertype.

![ Uitgezochte paneel ](/help/assets/select-panel-popover.png)

* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar die dia verplaatst.
* U kunt de volgorde van de dia op de juiste plaats wijzigen door de sleepgrepen te gebruiken.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren welke componenten als dia&#39;s aan de carrouselcomponent kunnen worden toegevoegd, en welke standaardinstellingen voor automatische overgangen worden gedefinieerd en welke aangepaste stijlen beschikbaar zijn voor de auteur van de inhoud.

### Tabblad Eigenschappen {#properties-tab-1}

Het **lusje van Eigenschappen** wordt gebruikt om de standaardmontages voor de diaovergangen te bepalen wanneer een inhoudsauteur de carrouselcomponent aan een pagina toevoegt.

![ dialoog van het Ontwerp van de Component van Carousel ](/help/assets/carousel-design.png)

* **automatisch overgangsdia&#39;s** - bepaalt als door gebrek de optie om de carrousel aan de volgende dia automatisch vooruit te gaan wordt toegelaten wanneer de inhoudauteur de carrouselcomponent aan een pagina toevoegt.
* **prepend controleelementen** - wanneer gecontroleerd, zullen de controleelementen vóór de carrouselpunten worden geplaatst om toegankelijkheid te verbeteren.

### Tabblad Toegestane componenten {#allowed-components-tab}

Het **Toegestane lusje van Componenten** wordt gebruikt om te bepalen welke componenten als dia&#39;s aan de Component van Carousel door de inhoudauteur kunnen worden toegevoegd.

De toegelaten Componenten lusjefuncties op de zelfde manier zoals het lusje van de zelfde naam wanneer [ het bepalen van het beleid en de eigenschappen van een Container van de Lay-out in de Redacteur van het Malplaatje.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=nl-NL)

### Tabblad Stijlen {#styles-tab}

De component Carousel steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De Component van Carousel steunt de [ Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
