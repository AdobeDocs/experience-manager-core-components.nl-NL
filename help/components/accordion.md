---
title: Accordion-component
description: Met de component Core Component Accordion kunt u een verzameling deelvensters maken die zijn gerangschikt in een accordeon op een pagina.
role: Architect, ontwikkelaar, beheerder, praktijkgerichte
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1072'
ht-degree: 1%

---


# Accordeoncomponent{#accordion-component}

Met de component Core Component Accordion kunt u een verzameling deelvensters maken die zijn gerangschikt in een accordeon op een pagina.

## Gebruik {#usage}

Met de component Core Component Accordion kunt u een verzameling componenten maken, die als deelvensters zijn samengesteld en in een accordeon op een pagina zijn gerangschikt, vergelijkbaar met de [Tabs Component](tabs.md), maar kunt u de deelvensters uit- en samenvouwen.

* De eigenschappen van de accordeon kunnen worden gedefinieerd in [configure dialog](#configure-dialog).
* De orde van de panelen van de accordeon kan in vormen dialoog evenals [uitgezocht paneelpopover](#select-panel-popover) worden bepaald.
* De standaardwaarden voor de component Accordion wanneer het toevoegen van het aan een pagina kunnen in [ontwerpdialoog](#design-dialog) worden bepaald.

## Diep koppelen aan een deelvenster {#deep-linking}

De componenten Accordion en [Tabs](tabs.md) ondersteunen het rechtstreeks koppelen aan een deelvenster binnen de component.

Dit doet u als volgt:

1. Bekijk de pagina met de component gebruikend **[Mening als Gepubliceerd](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** optie in de paginaredacteur.
1. Inspect de inhoud van de pagina en identificeer de id van het deelvenster.
   * Bijvoorbeeld `id="accordion-86196c94d3-item-ca319dbb0b"`
1. De id wordt het anker dat u met een hash (`#`) aan de URL kunt toevoegen.
   * Bijvoorbeeld `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Wanneer u met de deelvenster-id als anker naar de URL navigeert, schuift de browser rechtstreeks naar de desbetreffende component en geeft deze het opgegeven deelvenster weer. Als het deelvenster is geconfigureerd om niet standaard te worden uitgevouwen, wordt het automatisch uitgevouwen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Accordion Component is v1, die in juni 2019 met versie 2.5.0 van de Core Components is geïntroduceerd en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_accordion) om de component Accordion te ervaren en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Accordeon [kan op GitHub](https://adobe.com/go/aem_cmp_tech_accordion_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster {#configure-dialog} configureren

In het dialoogvenster Configureren kan de auteur van de inhoud het accordeonitem, de deelvensters definiëren en bepalen hoe het zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

### Tabblad Items {#items-tab}

![Tabblad Items van dialoogvenster Bewerken van accordeoncomponent](/help/assets/accordion-edit-items.png)

Gebruik de knop **Toevoegen** om de componentkiezer te openen en te kiezen welke component u als deelvenster wilt toevoegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:

* **Pictogram**  - Het pictogram van het componenttype van het paneel voor gemakkelijke identificatie in de lijst. Plaats de muis boven de volledige componentnaam als knopinfo.
* **Beschrijving**  - De beschrijving die wordt gebruikt als de tekst van het deelvenster, met standaard de naam van de component die voor het deelvenster is geselecteerd.
* **Verwijderen**  - Tik of klik om het deelvenster uit de accordeoncomponent te verwijderen.
* **herschikken**  - Tik of klik en sleep om de volgorde van de deelvensters te wijzigen.

>[!TIP]
>
>Als de viewport van de pagina wordt verminderd zodat het bewerkingsdialoogvenster volledig scherm wordt, wordt de **Add** knoop verborgen. Componenten kunnen nog steeds worden toegevoegd aan de Accordion-component door [te slepen vanuit de componentenbrowser en neer te zetten op de Accordion-component in de pagina-editor](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent).

### Tabblad Eigenschappen {#properties-tab}

![Het tabblad Eigenschappen van het dialoogvenster Bewerken van de accordeoncomponent](/help/assets/accordion-edit-properties.png)

* **Eén item uitbreiden**  - Als deze optie is geselecteerd, wordt één accordeonitem tegelijkertijd uitgebreid. Als u één item uitvouwt, worden alle andere items samengevouwen.
* **Uitgebreide items**  - Met deze optie worden de items gedefinieerd die standaard worden uitgevouwen wanneer de pagina wordt geladen.
   * Als **Enkel item vergroten** is geselecteerd, moet er één deelvenster zijn geselecteerd. Standaard is het eerste deelvenster geselecteerd.
   * Wanneer **Uitbreiding van één item** niet is geselecteerd, is deze optie een meervoudige selectie en is deze optie optioneel.
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Pop-over {#select-panel-popover} in deelvenster selecteren

De auteur van de inhoud kan de optie **Select Panel** op de componentwerkbalk gebruiken om over te schakelen naar een ander deelvenster om te bewerken en om de volgorde van de deelvensters in de accordeon eenvoudig te wijzigen.

![Pictogram van deelvenster Selecteren](/help/assets/select-panel-icon.png)

Nadat u de optie **Deelvenster selecteren** hebt geselecteerd op de componentwerkbalk, worden de geconfigureerde accordeondeelvensters weergegeven als een vervolgkeuzelijst.

![Pop-upmenu van deelvenster selecteren](/help/assets/select-panel-popover.png)

* De lijst wordt geordend door de toegewezen rangschikking van de deelvensters en wordt weergegeven in de nummering.
* Het componenttype van het deelvenster wordt eerst weergegeven, gevolgd door de beschrijving van het deelvenster in lichtere lettertypen.
* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar dat deelvenster verplaatst.
* U kunt de deelvensters op hun plaats verplaatsen met behulp van de sleepgrepen.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de component Accordion gebruikt en de standaardinstellingen die zijn ingesteld bij het plaatsen van de component Accordion.

### Tabblad Eigenschappen {#properties-tab-design}

![Dialoogvenster Ontwerp, tabblad](/help/assets/accordion-design-properties.png)

* **Elementen**  met toegelaten koptekst - Deze meerkeuzekeuzelijst definieert de koptekst van de accordeon-item HTML-elementen die door een auteur mogen worden geselecteerd.
* **Standaardkopelement**  - Deze vervolgkeuzelijst definieert het standaard HTML-element voor de kop van accordeonitems.

### Tabblad Toegestane componenten {#allowed-components-tab}

Het tabblad **Toegestane componenten** wordt gebruikt om te definiëren welke componenten door de auteur van de inhoud als items aan deelvensters in de component Accordion kunnen worden toegevoegd.

Het tabblad Toegestane componenten werkt op dezelfde manier als het tabblad met dezelfde naam wanneer [het beleid en de eigenschappen van een container voor de layout in de Sjablooneditor worden gedefinieerd.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-layout-template-author)

### Tabblad Stijlen {#styles-tab}

De component Accordion ondersteunt het AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Adobe-gegevenslaag client {#data-layer}

De component Accordion ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
