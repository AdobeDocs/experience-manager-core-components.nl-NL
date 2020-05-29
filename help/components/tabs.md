---
title: Component Tabs
description: Met de component Tabs kunt u meerdere tabbladen maken om de inhoud op een pagina te rangschikken.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 1%

---


# Component Tabs {#tabs-component}

Met de component Core Component Tabs kunt u inhoud op meerdere tabbladen ordenen.

## Gebruik {#usage}

Met de component Tabs kan de auteur van de inhoud de pagina-inhoud op meerdere tabbladen ordenen.

In het dialoogvenster [](#edit-dialog) Bewerken kan de auteur van de inhoud meerdere tabbladen definiëren en het actieve tabblad instellen. Met behulp van het dialoogvenster [](#design-dialog)Ontwerp kan de sjabloonauteur definiëren welke componenten aan tabbladen kunnen worden toegevoegd en de stijlen aanpassen.

>[!TIP]
>
>Geneste tabcomponenten (tabs binnen tabs) worden ondersteund.
>
>Eenvoudige (niet-geneste) tabcomponenten kunnen worden gevonden/geselecteerd met de [inhoudsstructuur](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html#content-tree), maar geneste tabbladen kunnen niet worden gevonden.

## Diep koppelen aan een deelvenster {#deep-linking}

Met de tabbladen en [accordeoncomponenten](accordion.md) kunt u rechtstreeks koppelen aan een deelvenster binnen de component.

Dit doet u als volgt:

1. Bekijk de pagina met de component gebruikend de **[Mening als Gepubliceerde](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/authoring/editing-content.html#view-as-published)**optie in de paginaredacteur.
1. Controleer de inhoud van de pagina en identificeer de id van het deelvenster.
   * Bijvoorbeeld `id="accordion-86196c94d3-item-ca319dbb0b"`
1. De id wordt het anker dat u met een hash (`#`) aan de URL kunt toevoegen.
   * Bijvoorbeeld `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Wanneer u met de deelvenster-id als anker naar de URL navigeert, schuift de browser rechtstreeks naar de desbetreffende component en geeft deze het opgegeven deelvenster weer. Als het deelvenster is geconfigureerd om niet standaard te worden uitgevouwen, wordt het automatisch uitgevouwen.

## Versie en compatibiliteit {#version-and-compatibility}

The current version of the Tabs Component is v1, which was introduced with release 2.2.0 of the Core Components in October 2018, and is described in this document.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel | Compatibel | Compatibel |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

To experience the Tabs Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_tabs).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van Lusjes [kan op GitHub](https://adobe.com/go/aem_cmp_tech_tabs_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster Bewerken {#edit-dialog}

The edit dialog allows the content author to create, rename, and rearrange tabs as well as define the active tab.

### Items Tab {#items-tab}

![Tabs Component&#39;s edit dialog items tab](/help/assets/tabs-edit-items.png)

Gebruik de knop **Toevoegen** om de componentkiezer te openen en te kiezen welke component u als tab wilt toevoegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:

* **Pictogram** - Het pictogram van het componenttype van de tab voor eenvoudige identificatie in de lijst. Plaats de muis boven de volledige componentnaam als knopinfo.
* **Beschrijving** - De beschrijving die als tekst van het lusje wordt gebruikt, die aan de naam van de component in gebreke blijft die voor het lusje wordt geselecteerd.
* **Verwijderen** - Tik of klik om de tab uit de tabcomponent te verwijderen.
* **Herschik** - Tik of klik en sleep om de tabvolgorde te wijzigen.

>[!TIP]
>
>Als de viewport van de pagina wordt verminderd zodat het bewerkingsdialoogvenster volledig scherm wordt, wordt de knop **Toevoegen** verborgen. Componenten kunnen nog steeds worden toegevoegd aan de component Tabs door de [component te slepen vanuit de browser Component en neer te zetten op de component Tabs in de pagina-editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component).

### Tabblad Eigenschappen {#properties-tab}

![Tabs Component&#39;s edit dialog properties tab](/help/assets/tabs-edit-properties.png)

* **Actief item** - De auteur van de inhoud kan bepalen welk tabblad actief is wanneer de pagina wordt geladen.
   * Met de optie **Standaard** wordt het eerste tabblad geselecteerd.
* **ID** - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Tabs Component&#39;s edit dialog accessibility tab](/help/assets/tabs-edit-accessibility.png)

Op het tabblad **Toegankelijkheid** kunnen waarden worden ingesteld voor [ARIA-toegankelijkheidslabels](https://www.w3.org/WAI/standards-guidelines/aria/) voor de component.

* **Label** - waarde van een ARIA-labelkenmerk voor de component

## Deelvenster selecteren {#select-panel}

De auteur van de inhoud kan de optie Deelvenster **** selecteren op de werkbalk van de component gebruiken om de volgorde van de tabbladen te wijzigen en deze te bewerken.

![Pictogram van deelvenster Selecteren](/help/assets/select-panel-icon.png)

Nadat u de optie Deelvenster **** selecteren op de werkbalk van de component hebt geselecteerd, worden de geconfigureerde tabbladen weergegeven als een vervolgkeuzelijst.

* De lijst wordt geordend door de toegewezen rangschikking van de lusjes en in de nummering weerspiegeld.
* Het componenttype van de tab wordt als eerste weergegeven, gevolgd door de beschrijving van de tab in lichtere lettertypen.

![Pop-upmenu van deelvenster selecteren](/help/assets/select-panel-popover.png)

* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar dat tabblad verplaatst.
* U kunt de tabvolgorde op de juiste plaats wijzigen door de sleepgrepen te gebruiken.

>[!NOTE]
>
>Tabs kunnen niet door de auteur worden geselecteerd in de modus **Bewerken** . Gebruik de modus **[Voorvertoning](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode)**of de optie**[Weergeven als gepubliceerd](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** om te communiceren met de tabbladen als een lezer van de gepubliceerde inhoud.

## Ontwerpdialoogvenster {#design-dialog}

The design dialog allows the template author to define which components can be added as items to the tabs component as well as define which custom styles are available to the content author.

### Tabblad Toegestane componenten {#allowed-components-tab}

Het tabblad **Toegestane componenten** wordt gebruikt om te definiëren welke componenten door de auteur van de inhoud als items aan de component tabs kunnen worden toegevoegd.

Het tabblad Toegestane componenten werkt op dezelfde manier als het tabblad met dezelfde naam wanneer u het beleid en de eigenschappen van een container voor de layout in de Sjablooneditor [definieert.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Tabblad Stijlen {#styles-tab}

De component Tabs ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).
