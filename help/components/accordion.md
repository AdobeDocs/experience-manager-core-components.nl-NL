---
title: Accordeoncomponent
description: Met de component Core Component Accordion kunt u een verzameling deelvensters maken die zijn gerangschikt in een accordeon op een pagina.
role: Architect, Developer, Admin, User
exl-id: 1deb570a-3d8d-409e-805f-8460c49cf9bb
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 0%

---


# Accordeoncomponent{#accordion-component}

Met de component Core Component Accordion kunt u een verzameling deelvensters maken die zijn gerangschikt in een accordeon op een pagina.

## Gebruik {#usage}

De component van de Accordeon van de Component van de Kern staat voor de verwezenlijking van een inzameling van componenten toe, die als panelen worden samengesteld, en in een accordeon op een pagina worden geschikt, gelijkend op de [ Component van Lusjes ](tabs.md), maar staat voor het uitbreiden en het doen ineenstorten van de panelen toe.

* De eigenschappen van de accordeon kunnen in [ worden bepaald vormen dialoog ](#configure-dialog).
* De orde van de panelen van de accordeon kan in vormen dialoog evenals [ worden bepaald uitgezocht paneelpopover ](#select-panel-popover).
* De gebreken voor de Component van de Accordeon wanneer het toevoegen van het aan een pagina kunnen in de [ ontwerpdialoog ](#design-dialog) worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Accordion Component is v1, die in juni 2019 met versie 2.5.0 van de Core Components is geïntroduceerd en in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.17.4 ](/help/versions.md) en vroeger | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Accordeon te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_accordion).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Accordeon [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_accordion_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Diep koppelen aan een deelvenster {#deep-linking}

De accordeon, [ Carousel, ](carousel.md) en [ de steun van Componenten van Lusjes ](tabs.md) die rechtstreeks met een paneel binnen de component verbinden.

Dit doet u als volgt:

1. Bekijk de pagina met de component gebruikend de **[Mening zoals Gepubliceerde ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** optie in de paginaredacteur.
1. Controleer de inhoud van de pagina en identificeer de id van het deelvenster.
   * Bijvoorbeeld `id="accordion-86196c94d3-item-ca319dbb0b"`
1. De id wordt het anker dat u met een hash (`#`) aan de URL kunt toevoegen.
   * Bijvoorbeeld `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Wanneer u met de deelvenster-id als anker naar de URL navigeert, schuift de browser rechtstreeks naar de desbetreffende component en geeft deze het opgegeven deelvenster weer. Als het deelvenster is geconfigureerd om niet standaard te worden uitgevouwen, wordt het automatisch uitgevouwen.

## Accordeon en responsief ontwerp {#responsive-design}

Alle Core Components zijn ontworpen om volledig te reageren, zodat u over alle apparaten probleemloos kunt genieten.

Sommige geavanceerde componenten, zoals de component Accordion, moeten mogelijk in het kader van het uitvoeringsproject specifieke aandacht krijgen om de reactiesnelheid in alle omstandigheden te behouden. Gelieve te zien het document [ Responsieve Ontwerp van de Componenten van de Kern ](/help/responsive.md) voor meer informatie.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het accordeonitem, de deelvensters definiëren en bepalen hoe het zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

### Tabblad Items {#items-tab}

![ Punten lusje van uitgeeft dialoog van de Component van de Accordeon ](/help/assets/accordion-edit-items.png)

Gebruik **voeg** knoop toe om de componentenselecteur te openen om te kiezen welke component om als paneel toe te voegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:

* **Pictogram** - het pictogram van het componenttype van het paneel voor gemakkelijke identificatie in de lijst. Plaats de muisaanwijzer boven de volledige componentnaam om deze weer te geven als knopinfo.
* **Beschrijving** - de beschrijving die als tekst van het paneel wordt gebruikt, die aan de naam van de component in gebreke blijft die voor het paneel wordt geselecteerd.
* **Schrapping** - Tik of klik om het paneel van de accordeoncomponent te schrappen.
* **herschikt** - Tik of klik en sleep om de orde van de panelen te herschikken.

>[!TIP]
>
>Als viewport van de pagina wordt verminderd zodat uitgeeft dialoog volledig scherm wordt, **voegt** knoop toe zal worden verborgen. De componenten kunnen nog aan de Component van de Accordeon worden toegevoegd door [ van componenten te slepen browser en op de Component van de Accordeon in de paginaredacteur ](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent) te vallen.

### Tabblad Eigenschappen {#properties-tab}

![ het lusje van Eigenschappen van uitgeeft dialoog van de Component van de Accordeon ](/help/assets/accordion-edit-properties.png)

* **Enige puntenuitbreiding** - wanneer geselecteerd, dwingt deze optie één enkel accordeonpunt om tegelijkertijd worden uitgebreid. Als u één item uitbreidt, worden alle andere items samengevouwen.
* **Uitgebreide punten** - deze optie bepaalt de punten die door gebrek worden uitgebreid wanneer de pagina wordt geladen.
   * Wanneer **Enige puntuitbreiding** wordt geselecteerd, moet één paneel worden geselecteerd. Standaard is het eerste deelvenster geselecteerd.
   * Wanneer **Enige puntuitbreiding** niet wordt geselecteerd, is deze optie multi-select en facultatief.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Pop-upmenu van deelvenster selecteren {#select-panel-popover}

De inhoudauteur kan de **Uitgezochte 1&rbrace; optie van het Comité op de componententoolbar gebruiken om in een verschillend paneel te veranderen voor het uitgeven evenals de orde van de panelen binnen de accordeon gemakkelijk te herschikken.**

![ Uitgezochte paneelpictogram ](/help/assets/select-panel-icon.png)

Zodra het selecteren van de **Uitgezochte optie van het Comité** in de componententoolbar, worden de gevormde accordeonpanelen getoond als drop-down.

![ Uitgezochte paneel popover ](/help/assets/select-panel-popover.png)

* De lijst wordt geordend door de toegewezen rangschikking van de deelvensters en wordt weergegeven in de nummering.
* Het componenttype van het deelvenster wordt eerst weergegeven, gevolgd door de beschrijving van het deelvenster in lichtere lettertypen.
* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar dat deelvenster verplaatst.
* U kunt de deelvensters op hun plaats verplaatsen met behulp van de sleepgrepen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de inhoudauteur die de accordeoncomponent gebruikt en de standaardinstellingen die zijn ingesteld bij het plaatsen van de accordeoncomponent.

### Tabblad Eigenschappen {#properties-tab-design}

![ de dialoogeigenschappen tabel van het Ontwerp ](/help/assets/accordion-design-properties.png)

* **Toegestane Elementen van de Kop** - Dit multi-uitgezochte drop-down bepaalt de kopelementen van het accordeonpunt van HTML die door een auteur mogen worden geselecteerd.
* **Standaard het Element van de Kop** - Deze drop-down bepaalt het standaard kopelement van het accordeonpunt van HTML.

### Tabblad Toegestane componenten {#allowed-components-tab}

Het **Toegestane lusje van Componenten** wordt gebruikt om te bepalen welke componenten als punten aan panelen in de Component van de Accordeon door de inhoudauteur kunnen worden toegevoegd.

De toegelaten Componenten lusjefuncties op de zelfde manier zoals het lusje van de zelfde naam wanneer [ het bepalen van het beleid en de eigenschappen van een Container van de Lay-out in de Redacteur van het Malplaatje.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-layout-template-author)

### Tabblad Stijlen {#styles-tab}

De Component van de Accordeon steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De Component van de Accordeon steunt de [ Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
