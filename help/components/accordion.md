---
title: Accordion-component
description: Met de component Core Component Accordion kunt u een verzameling deelvensters maken die zijn gerangschikt in een accordeon op een pagina.
translation-type: tm+mt
source-git-commit: fe8a121520000ffd56ae3347469590e89121eaf0

---


# Accordion-component{#accordion-component}

Met de component Core Component Accordion kunt u een verzameling deelvensters maken die zijn gerangschikt in een accordeon op een pagina.

## Gebruik {#usage}

Met de component Core Component Accordion kunt u een verzameling componenten maken, die als deelvensters zijn samengesteld en in een accordeon op een pagina zijn gerangschikt, vergelijkbaar met de component [](tabs.md)Tabs, maar kunt u de deelvensters uitvouwen en samenvouwen.

* De eigenschappen van de accordeon kunnen worden gedefinieerd in het dialoogvenster [](#configure-dialog)configureren.
* De volgorde van de deelvensters van de accordeon kan worden gedefinieerd in het dialoogvenster Configureren en in de pop-up [van het deelvenster](#select-panel-popover)Selecteren.
* De standaardinstellingen voor de component Accordion wanneer deze aan een pagina wordt toegevoegd, kunnen worden gedefinieerd in het [ontwerpdialoogvenster](#design-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Accordion Component is v1, die in juni 2019 met versie 2.5.0 van de Core Components is geïntroduceerd en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v1 | Compatibel | Compatibel | Compatibel | Compatibel |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_accordion)voor meer informatie over de component Accordion en voorbeelden van de bijbehorende configuratieopties en over HTML- en JSON-uitvoer.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Accordeon [kan op GitHub](https://adobe.com/go/aem_cmp_tech_accordion_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het accordeonitem, de deelvensters definiëren en bepalen hoe het zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

### Tabblad Items {#items-tab}

![](/help/assets/screen-shot-2019-06-21-08.26.38.png)

Gebruik de knop **Toevoegen** om de componentkiezer te openen en te kiezen welke component u als deelvenster wilt toevoegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:

* **Pictogram** - Het pictogram van het componenttype van het paneel voor gemakkelijke identificatie in de lijst. Plaats de muis boven de volledige componentnaam als knopinfo.
* **Beschrijving** - De beschrijving die wordt gebruikt als de tekst van het deelvenster, met standaard de naam van de component die voor het deelvenster is geselecteerd.
* **Verwijderen** - Tik of klik om het deelvenster uit de accordeoncomponent te verwijderen.
* **Herschikken** - Tik of klik en sleep om de volgorde van de deelvensters te wijzigen.

>[!TIP]
>
>Als de viewport van de pagina wordt verminderd zodat het bewerkingsdialoogvenster volledig scherm wordt, wordt de knop **Toevoegen** verborgen. Componenten kunnen nog steeds worden toegevoegd aan de Accordion-component door deze te [slepen vanuit de componentenbrowser en neer te zetten op de Accordion-component in de pagina-editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent).

### Tabblad Eigenschappen {#properties-tab}

![](/help/assets/screen-shot-2019-06-21-08.26.53.png)

* **Eén item uitbreiden** - Als deze optie is geselecteerd, wordt één accordeonitem tegelijkertijd uitgebreid. Als u één item uitvouwt, worden alle andere items samengevouwen.
* **Uitgebreide items** - Met deze optie worden de items gedefinieerd die standaard worden uitgevouwen wanneer de pagina wordt geladen.
   * Als **Eén item is uitgevouwen** , moet er één deelvenster zijn geselecteerd. Standaard is het eerste deelvenster geselecteerd.
   * Als **Eén item niet is uitgevouwen** , is deze optie een meervoudige selectie en optioneel.

## Pop-upmenu van deelvenster selecteren {#select-panel-popover}

De auteur van de inhoud kan de optie Deelvenster **** selecteren op de werkbalk van de component gebruiken om de volgorde van de deelvensters in de accordeon te wijzigen en deze te bewerken.

![](/help/assets/screen-shot-2019-06-21-08.49.36.png)

Nadat u de optie Deelvenster **** selecteren op de componentwerkbalk hebt geselecteerd, worden de geconfigureerde accordeondeelvensters weergegeven als een vervolgkeuzelijst.

![](/help/assets/screen-shot-2019-06-21-08.52.14.png)

* De lijst wordt geordend door de toegewezen rangschikking van de deelvensters en wordt weergegeven in de nummering.
* Het componenttype van het deelvenster wordt eerst weergegeven, gevolgd door de beschrijving van het deelvenster in lichtere lettertypen.
* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar dat deelvenster verplaatst.
* U kunt de deelvensters op hun plaats verplaatsen met behulp van de sleepgrepen.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de component Accordion gebruikt en de standaardinstellingen die zijn ingesteld bij het plaatsen van de component Accordion.

### Tabblad Eigenschappen {#properties-tab-design}

![](/help/assets/screen-shot-2019-06-21-08.58.11.png)

* **Toegestane kopelementen** - Deze meerkeuzekeuzelijst definieert de HTML-elementen van de koptekst van de accordeon-item die door een auteur mogen worden geselecteerd.
* **Standaardkopelement** - Deze vervolgkeuzelijst definieert het standaard HTML-element voor de kop van accordeonitems.

### Tabblad Toegestane componenten {#allowed-components-tab}

Het tabblad **Toegestane componenten** wordt gebruikt om te definiëren welke componenten door de auteur van de inhoud als items aan deelvensters in de component Accordion kunnen worden toegevoegd.

Het tabblad Toegestane componenten werkt op dezelfde manier als het tabblad met dezelfde naam wanneer u het beleid en de eigenschappen van een container voor de layout in de Sjablooneditor [definieert.](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/templates.html)

### Tabblad Stijlen {#styles-tab}

De component Accordion ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).
