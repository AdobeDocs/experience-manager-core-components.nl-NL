---
title: Accordion-component
description: Met de component Core Component Accordion kunt u een verzameling deelvensters maken die zijn gerangschikt in een accordeon op een pagina.
role: Architect, Developer, Admin, User
exl-id: 1deb570a-3d8d-409e-805f-8460c49cf9bb
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '1067'
ht-degree: 1%

---

# Accordion-component{#accordion-component}

Met de component Core Component Accordion kunt u een verzameling deelvensters maken die zijn gerangschikt in een accordeon op een pagina.

## Gebruik {#usage}

Met de component Core Component Accordion kunt u een verzameling componenten maken, die als deelvensters zijn samengesteld en die in een accordeon op een pagina zijn gerangschikt, vergelijkbaar met de component [Component Tabs](tabs.md), maar kunt u de deelvensters uit- en samenvouwen.

* De eigenschappen van de accordeon kunnen worden gedefinieerd in het dialoogvenster [dialoogvenster configureren](#configure-dialog).
* De volgorde van de deelvensters van de accordeon kan worden gedefinieerd in het dialoogvenster Configureren en in het dialoogvenster [popup in deelvenster selecteren](#select-panel-popover).
* De standaardinstellingen voor de component Accordion wanneer deze aan een pagina wordt toegevoegd, kunnen worden gedefinieerd in het dialoogvenster [ontwerpdialoogvenster](#design-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Accordion Component is v1, die in juni 2019 met versie 2.5.0 van de Core Components is geïntroduceerd en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de accordeoncomponent wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_accordion).

## Technische details {#technical-details}

De meest recente technische documentatie over de Accordion-component [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_accordion_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Diep koppelen aan een deelvenster {#deep-linking}

De accordeon en [Componenten tabs](tabs.md) ondersteuning voor koppelingen rechtstreeks naar een deelvenster binnen de component.

Dit doet u als volgt:

1. De pagina met de component weergeven met de **[Weergeven als gepubliceerd](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** in de pagina-editor.
1. Inspect de inhoud van de pagina en identificeer de id van het deelvenster.
   * Bijvoorbeeld `id="accordion-86196c94d3-item-ca319dbb0b"`
1. De id wordt het anker dat u met een hash aan de URL kunt toevoegen (`#`).
   * Bijvoorbeeld `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Wanneer u met de deelvenster-id als anker naar de URL navigeert, schuift de browser rechtstreeks naar de desbetreffende component en geeft deze het opgegeven deelvenster weer. Als het deelvenster is geconfigureerd om niet standaard te worden uitgevouwen, wordt het automatisch uitgevouwen.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het accordeonitem, de deelvensters definiëren en bepalen hoe het zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

### Tabblad Items {#items-tab}

![Tabblad Items van dialoogvenster Bewerken van accordeoncomponent](/help/assets/accordion-edit-items.png)

Gebruik de **Toevoegen** om de componentkiezer te openen en te kiezen welke component u als deelvenster wilt toevoegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:

* **Pictogram** - Het pictogram van het componenttype van het paneel voor gemakkelijke identificatie in de lijst. Plaats de muis boven de volledige componentnaam als knopinfo.
* **Beschrijving** - De beschrijving die als tekst van het deelvenster wordt gebruikt, met standaard de naam van de component die voor het deelvenster is geselecteerd.
* **Verwijderen** - Tik of klik om het deelvenster uit de accordeoncomponent te verwijderen.
* **Opnieuw rangschikken** - Tik of klik en sleep om de volgorde van de deelvensters te wijzigen.

>[!TIP]
>
>Als de viewport van de pagina wordt verkleind zodat het dialoogvenster Bewerken volledig scherm wordt, wordt het dialoogvenster **Toevoegen** wordt verborgen. Componenten kunnen nog steeds door [slepen vanuit de componentenbrowser en neerzetten op de Component van de Accordeon in de paginaredacteur](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent).

### Tabblad Eigenschappen {#properties-tab}

![Het tabblad Eigenschappen van het dialoogvenster Bewerken van de accordeoncomponent](/help/assets/accordion-edit-properties.png)

* **Uitbreiding van één item** - Als deze optie is geselecteerd, wordt één accordeonitem tegelijkertijd uitgebreid. Als u één item uitvouwt, worden alle andere items samengevouwen.
* **Uitgebreide items** - Met deze optie worden de items gedefinieerd die standaard worden uitgevouwen wanneer de pagina wordt geladen.
   * Wanneer **Uitbreiding van één item** is geselecteerd, moet er één deelvenster zijn geselecteerd. Standaard is het eerste deelvenster geselecteerd.
   * Wanneer **Uitbreiding van één item** is niet geselecteerd, is deze optie een meerkeuzeoptie en is optioneel.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Pop-upmenu van deelvenster selecteren {#select-panel-popover}

De auteur van de inhoud kan de **Deelvenster selecteren** op de werkbalk van de component om de volgorde van de deelvensters in de accordeon te wijzigen in een ander deelvenster om te bewerken.

![Pictogram van deelvenster Selecteren](/help/assets/select-panel-icon.png)

Wanneer u de **Deelvenster selecteren** in de componentwerkbalk worden de geconfigureerde accordeondeelvensters weergegeven als een vervolgkeuzelijst.

![Pop-upmenu van deelvenster selecteren](/help/assets/select-panel-popover.png)

* De lijst wordt geordend door de toegewezen rangschikking van de deelvensters en wordt weergegeven in de nummering.
* Het componenttype van het deelvenster wordt eerst weergegeven, gevolgd door de beschrijving van het deelvenster in lichtere lettertypen.
* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar dat deelvenster verplaatst.
* U kunt de deelvensters op hun plaats verplaatsen met behulp van de sleepgrepen.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de component Accordion gebruikt en de standaardinstellingen die zijn ingesteld bij het plaatsen van de component Accordion.

### Tabblad Eigenschappen {#properties-tab-design}

![Dialoogvenster Ontwerp, tabblad](/help/assets/accordion-design-properties.png)

* **Toegestane kopelementen** - Deze meerkeuzekeuzelijst definieert de HTML-elementen van de accordeonitemkop die door een auteur mogen worden geselecteerd.
* **Standaardkopelement** - Deze vervolgkeuzelijst definieert het standaardelement HTML van de kop van het accordeonitem.

### Tabblad Toegestane componenten {#allowed-components-tab}

De **Toegestane componenten** wordt gebruikt om te definiëren welke componenten door de auteur van de inhoud als items aan deelvensters in de component Accordion kunnen worden toegevoegd.

Het tabblad Toegestane componenten werkt op dezelfde manier als het tabblad met dezelfde naam wanneer [het definiëren van het beleid en de eigenschappen van een container voor layout in de Sjablooneditor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-layout-template-author)

### Tabblad Stijlen {#styles-tab}

De component Accordion ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component Accordion ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
