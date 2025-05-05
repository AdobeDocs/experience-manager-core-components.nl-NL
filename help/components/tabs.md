---
title: Component Tabs
description: Met de component Tabs kunt u meerdere tabbladen maken om de inhoud op een pagina te rangschikken.
role: Architect, Developer, Admin, User
exl-id: 0031c5f3-447c-4932-898f-2f453801e492
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '1038'
ht-degree: 0%

---


# Component Tabs {#tabs-component}

Met de component Core Component Tabs kunt u de inhoud op meerdere tabbladen ordenen.

## Gebruik {#usage}

Met de component Tabs kan de auteur van de inhoud de pagina-inhoud op meerdere tabbladen ordenen.

Het [ geeft dialoog uit ](#edit-dialog) staat de inhoudauteur toe om veelvoudige lusjes te bepalen evenals het actieve lusje te plaatsen. Gebruikend de [ ontwerpdialoog ](#design-dialog), kan de malplaatjeauteur bepalen welke componenten aan lusjes kunnen worden toegevoegd en de stijlen aanpassen.

>[!TIP]
>
>Geneste tabcomponenten (tabs binnen tabs) worden ondersteund.
>
>De eenvoudige (niet-genestelde) lusjecomponenten kunnen worden gevestigd/worden geselecteerd gebruikend de [ inhoudsboom ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html#content-tree), nochtans kunnen de genestelde lusjes niet worden gevestigd.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Tabs Component is v1, die in oktober 2018 is geïntroduceerd met release 2.2.0 van de Core Components (Basiscomponenten). Deze versie wordt in dit document beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v1 | Compatibel systeem met <br>[ versie 2.17.4 ](/help/versions.md) en vroeger | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van Lusjes te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_tabs).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van Lusjes [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_tabs_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Diep koppelen aan een deelvenster {#deep-linking}

De Lusjes, [ Carrousel, ](carousel.md) en [ de steun van Componenten van de Accordeon ](accordion.md) die rechtstreeks met een paneel binnen de component verbinden.

Dit doet u als volgt:

1. Bekijk de pagina met de component gebruikend de **[Mening zoals Gepubliceerde ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** optie in de paginaredacteur.
1. Controleer de inhoud van de pagina en identificeer de id van het deelvenster.
   * Bijvoorbeeld `id="accordion-86196c94d3-item-ca319dbb0b"`
1. De id wordt het anker dat u met een hash (`#`) aan de URL kunt toevoegen.
   * Bijvoorbeeld `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Wanneer u met de deelvenster-id als anker naar de URL navigeert, schuift de browser rechtstreeks naar de desbetreffende component en geeft deze het opgegeven deelvenster weer. Als het deelvenster is geconfigureerd om niet standaard te worden uitgevouwen, wordt het automatisch uitgevouwen.

## Tab en responsief ontwerp {#responsive-design}

Alle Core Components zijn ontworpen om volledig te reageren, zodat u over alle apparaten probleemloos kunt genieten.

Sommige geavanceerde componenten zoals de component van het Lusje kunnen specifieke overweging binnen het kader van het het uitvoeren project vereisen om ontvankelijkheid in alle omstandigheden te handhaven. Gelieve te zien het document [ Responsieve Ontwerp van de Componenten van de Kern ](/help/responsive.md) voor meer informatie.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud tabbladen maken, hernoemen en opnieuw rangschikken, en het actieve tabblad definiëren.

### Tabblad Items {#items-tab}

![ de Edit de dialoogpunten van de Component van Tabs tabel ](/help/assets/tabs-edit-items.png)

Gebruik **voeg** knoop toe om de componentenselecteur te openen om te kiezen welke component om als tabel toe te voegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:

* **Pictogram** - het pictogram van het componententype van het lusje voor gemakkelijke identificatie in de lijst. Plaats de muisaanwijzer boven de volledige componentnaam om deze weer te geven als knopinfo.
* **Beschrijving** - de beschrijving die als tekst van het lusje wordt gebruikt, die aan de naam van de component in gebreke blijft die voor het lusje wordt geselecteerd.
* **Schrapping** - Tik of klik om het lusje van de lusjecomponent te schrappen.
* **herschikt** - Tik of klik en sleep om de orde van de lusjes te herschikken.

>[!TIP]
>
>Als viewport van de pagina wordt verminderd zodat uitgeeft dialoog volledig scherm wordt, **voegt** knoop toe zal worden verborgen. De componenten kunnen nog aan de Component van Lusjes worden toegevoegd door [ te slepen van componenten browser en het vallen op de Component van Lusjes in de paginaredacteur ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component).

### Tabblad Eigenschappen {#properties-tab}

![ geeft de componenten van de Component van Tabs uit dialoogeigenschappen tabel ](/help/assets/tabs-edit-properties.png)

* **Actief Punt** - de inhoudauteur kan bepalen welk lusje actief is wanneer de pagina wordt geladen.
   * Met de **Standaard** optie, zal het eerste lusje worden geselecteerd.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Toegankelijkheid {#accessibility-tab}

![ de bewerkingsdialoog van de Component van Lusjes van Lusjes lusje ](/help/assets/tabs-edit-accessibility.png)

Op het **lusje van de Toegankelijkheid**, kunnen de waarden voor [ de toegankelijkheidslabels van ARIA ](https://www.w3.org/WAI/standards-guidelines/aria/) voor de component worden geplaatst.

* **Etiket** - Waarde van een ARIA etiketattribuut voor de component

## Deelvenster selecteren {#select-panel}

De inhoudauteur kan de **Uitgezochte 1&rbrace; optie van het Comité op de componententoolbar gebruiken om in een verschillend paneel te veranderen voor het uitgeven evenals de orde van de lusjes gemakkelijk te herschikken.**

![ Uitgezochte paneelpictogram ](/help/assets/select-panel-icon.png)

Zodra het selecteren van de **Uitgezochte optie van het Comité** in de componententoolbar, worden de gevormde lusjes getoond als drop-down.

* De lijst wordt geordend door de toegewezen rangschikking van de lusjes en in de nummering weerspiegeld.
* Het componenttype van de tab wordt als eerste weergegeven, gevolgd door de beschrijving van de tab in lichtere lettertypen.

![ Uitgezochte paneel popover ](/help/assets/select-panel-popover.png)

* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar dat tabblad verplaatst.
* U kunt de tabvolgorde op de juiste plaats wijzigen door de sleepgrepen te gebruiken.

>[!NOTE]
>
>De lusjes zijn niet selecteerbaar door de auteur wanneer op **&#x200B;**&#x200B;wijze uitgeeft. De wijze van de Voorproef van het gebruik [&#128279;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode) **of de**&#x200B;[ Mening zoals Gepubliceerde ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published) **optie om met de lusjes als lezer van de gepubliceerde inhoud in wisselwerking te staan.**

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren welke componenten als items aan de component tabs kunnen worden toegevoegd en welke aangepaste stijlen beschikbaar zijn voor de auteur van de inhoud.

### Tabblad Toegestane componenten {#allowed-components-tab}

Het **Toegestane lusje van Componenten** wordt gebruikt om te bepalen welke componenten als punten aan de component van lusjes door de inhoudauteur kunnen worden toegevoegd.

De toegelaten Componenten lusjefuncties op de zelfde manier zoals het lusje van de zelfde naam wanneer [ het bepalen van het beleid en de eigenschappen van een Container van de Lay-out in de Redacteur van het Malplaatje.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Tabblad Stijlen {#styles-tab}

De component van Lusjes steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De component van Lusjes steunt de [ Laag van de Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
