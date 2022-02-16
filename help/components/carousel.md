---
title: Carousel-component
description: Met de Carousel-component kan de auteur van de inhoud inhoud inhoud presenteren in een roterende carrousel.
role: Architect, Developer, Admin, User
exl-id: 3331214c-a05c-47e1-b54c-fbfd1045bd60
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '1119'
ht-degree: 0%

---

# Carousel-component{#carousel-component}

Met de Core Component Carousel Component kan de auteur van de inhoud inhoud inhoud presenteren in een navigeerbare carrousel.

## Gebruik {#usage}

Met de Carousel-component ordent de auteur van de inhoud de inhoud in een draaiende carrousel van dia&#39;s.

De [dialoogvenster bewerken](#edit-dialog) Hiermee kan de auteur van de inhoud meerdere dia&#39;s maken, benoemen en ordenen en automatische overgang met vertraging inschakelen. Met de [ontwerpdialoogvenster](#design-dialog)kan de sjabloonauteur definiëren welke componenten aan de carrousel kunnen worden toegevoegd, automatische overgangen in- of uitschakelen en de stijlen aanpassen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Carousel-component is v1, die in oktober 2018 is geïntroduceerd met versie 2.2.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de Carousel-component wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_carousel).

### Technische details {#technical-details}

De meest recente technische documentatie over de Carousel-component [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_carousel_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud dia&#39;s toevoegen, hernoemen en opnieuw rangschikken en de instellingen voor automatische overgangen definiëren.

### Tabblad Items {#items-tab}

![Tabblad Items van het dialoogvenster Bewerken van de Carousel-component](/help/assets/carousel-edit-items.png)

Gebruik de **Toevoegen** om de componentkiezer te openen en te kiezen welke component u als tab wilt toevoegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:

* **Pictogram** - Het pictogram van het componenttype van de tab voor eenvoudige identificatie in de lijst. Plaats de muis boven de volledige componentnaam als knopinfo.
* **Beschrijving** - De beschrijving die als tekst van het lusje wordt gebruikt, stellend aan de naam van de component die voor het lusje wordt geselecteerd.
* **Verwijderen** - Tik of klik om het tabblad te verwijderen uit de component Tabs.
* **Opnieuw ordenen** - Tik of klik en sleep om de tabbladen te ordenen.

>[!TIP]
>
>Als de viewport van de pagina wordt verkleind zodat het dialoogvenster Bewerken volledig scherm wordt, wordt het dialoogvenster **Toevoegen** wordt verborgen. Componenten kunnen nog steeds door [slepen vanuit de componentbrowser en neerzetten op de Carousel-component in de pagina-editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component-from-the-components-browser).

### Tabblad Eigenschappen {#properties-tab}

![Het tabblad Eigenschappen van het dialoogvenster Bewerken van de Carousel-component](/help/assets/carousel-edit-properties.png)

Op de **Eigenschappen** kan de auteur van de inhoud de dia&#39;s instellen op een automatische overgang.

* **Automatisch overgangsdia&#39;s** - Als de component actief is, gaat deze na een bepaalde vertraging automatisch naar de volgende dia.
* **Vertraging overgang** - Wanneer u de overgangsdia&#39;s Automatisch selecteert, wordt deze waarde gebruikt om de vertraging tussen overgangen (in milliseconden) te bepalen.
* **Automatisch onderbreken bij aanwijzen uitschakelen** - Wanneer **Automatisch overgangsdia&#39;s** is geselecteerd, wordt de carrouselovergang automatisch gepauzeerd wanneer de curseur over de carrousel beweegt. Selecteer deze optie om de overgang niet te pauzeren.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

>[!NOTE]
>
>De besturingselementen voor diavoorstellingen zijn niet ingeschakeld wanneer u zich in **Bewerken** in. Gebruiken [**Voorvertoning** mode](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode) of de **[Weergeven als gepubliceerd](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** de mogelijkheid om met de carrousel te communiceren als een lezer van de gepubliceerde inhoud.
>
>De functie voor automatisch vooruitgaan is niet ingeschakeld als de functie is ingeschakeld **Bewerken** in. Gebruiken **[Weergeven als gepubliceerd](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** als u de functie voor automatisch vooruitgaan wilt zien als een lezer van de gepubliceerde inhoud.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Het tabblad Toegankelijkheid van het dialoogvenster Bewerken van de Carousel-component](/help/assets/carousel-edit-accessibility.png)

Op de **Toegankelijkheid** tab, waarden kunnen worden ingesteld voor [Toegankelijkheid ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) labels voor de component.

* **Label** - Waarde van een ARIA-labelkenmerk voor de component

## Deelvenster selecteren {#select-panel}

De auteur van de inhoud kan de **Deelvenster selecteren** op de werkbalk van de component om te schakelen naar een andere dia om deze te bewerken en om de volgorde van de dia&#39;s gemakkelijk te wijzigen.

![Pictogram van deelvenster Selecteren](/help/assets/select-panel-icon.png)

Wanneer u de **Deelvenster selecteren** in de componentwerkbalk worden de geconfigureerde dia&#39;s weergegeven als een vervolgkeuzelijst.

* De lijst wordt geordend door de toegewezen rangschikking van de dia&#39;s en wordt weerspiegeld in de nummering.
* Het componenttype van de dia wordt eerst weergegeven, gevolgd door de beschrijving van de dia in een lichter lettertype.

![Deelvenster Selecteren](/help/assets/select-panel-popover.png)

* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar die dia verplaatst.
* U kunt de volgorde van de dia op de juiste plaats wijzigen door de sleepgrepen te gebruiken.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren welke componenten als dia&#39;s aan de carrouselcomponent kunnen worden toegevoegd, en welke standaardinstellingen voor automatische overgangen worden gedefinieerd en welke aangepaste stijlen beschikbaar zijn voor de auteur van de inhoud.

### Tabblad Eigenschappen {#properties-tab-1}

De **Eigenschappen** wordt gebruikt om de standaardinstellingen voor de diaovergangen te definiëren wanneer de auteur van de inhoud de carrouselcomponent aan een pagina toevoegt.

![Dialoogvenster Ontwerpen van de Carousel-component](/help/assets/carousel-design.png)

* **Automatisch overgangsdia&#39;s** - Hiermee wordt gedefinieerd of de optie om de carrousel automatisch naar de volgende dia te verplaatsen standaard is ingeschakeld wanneer de auteur van de inhoud de carrouselcomponent aan een pagina toevoegt.
* **Vertraging overgang** - Definieert de standaardwaarde van de overgangsvertraging tussen dia&#39;s (in milliseconden) wanneer de auteur van de inhoud de carrouselcomponent aan een pagina toevoegt.
* **Automatisch onderbreken bij aanwijzen uitschakelen** - Definieert of standaard de optie voor het uitschakelen van het automatische pauzeren is ingeschakeld wanneer **Automatisch overgangsdia&#39;s** is geselecteerd door de auteur van de inhoud.

### Tabblad Toegestane componenten {#allowed-components-tab}

De **Toegestane componenten** wordt gebruikt om te definiëren welke componenten door de auteur van de inhoud als dia&#39;s aan de Carousel-component kunnen worden toegevoegd.

Het tabblad Toegestane componenten werkt op dezelfde manier als het tabblad met dezelfde naam wanneer [het definiëren van het beleid en de eigenschappen van een container voor layout in de Sjablooneditor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Tabblad Stijlen {#styles-tab}

De Carousel-component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De Carousel-component ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
