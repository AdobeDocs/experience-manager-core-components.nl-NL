---
title: Component Tabs
description: Met de component Tabs kunt u meerdere tabbladen maken om de inhoud op een pagina te rangschikken.
translation-type: tm+mt
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 1%

---


# Tabs-component {#tabs-component}

Met de component Core Component Tabs kunt u inhoud op meerdere tabbladen ordenen.

## Gebruik {#usage}

Met de component Tabs kan de auteur van de inhoud de pagina-inhoud op meerdere tabbladen ordenen.

Met het dialoogvenster [bewerken](#edit-dialog) kan de auteur van de inhoud meerdere tabbladen definiëren en het actieve tabblad instellen. Met behulp van het [ontwerpdialoogvenster](#design-dialog) kan de sjabloonauteur definiëren welke componenten aan tabbladen kunnen worden toegevoegd en de stijlen aanpassen.

>[!TIP]
>
>Geneste tabcomponenten (tabs binnen tabs) worden ondersteund.
>
>Eenvoudige (niet-geneste) tabcomponenten kunnen worden gevonden/geselecteerd met behulp van de [inhoudsstructuur](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html#content-tree), maar geneste tabbladen kunnen niet worden gevonden.

## Diep koppelen aan een deelvenster {#deep-linking}

De tabs en [Accordeoncomponenten](accordion.md) ondersteunen het rechtstreeks koppelen naar een deelvenster binnen de component.

Dit doet u als volgt:

1. Bekijk de pagina met de component gebruikend **[Mening als Gepubliceerd](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** optie in de paginaredacteur.
1. Inspect de inhoud van de pagina en identificeer de id van het deelvenster.
   * Bijvoorbeeld `id="accordion-86196c94d3-item-ca319dbb0b"`
1. De id wordt het anker dat u met een hash (`#`) aan de URL kunt toevoegen.
   * Bijvoorbeeld `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Wanneer u met de deelvenster-id als anker naar de URL navigeert, schuift de browser rechtstreeks naar de desbetreffende component en geeft deze het opgegeven deelvenster weer. Als het deelvenster is geconfigureerd om niet standaard te worden uitgevouwen, wordt het automatisch uitgevouwen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Tabs Component is v1, die in oktober 2018 is geïntroduceerd met release 2.2.0 van de Core Components (Basiscomponenten). Deze versie wordt in dit document beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_tabs) om de Tabs-component te ervaren en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van Lusjes [kan op GitHub](https://adobe.com/go/aem_cmp_tech_tabs_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster {#edit-dialog} bewerken

In het dialoogvenster Bewerken kan de auteur van de inhoud tabbladen maken, hernoemen en opnieuw rangschikken, en het actieve tabblad definiëren.

### Tabblad Items {#items-tab}

![Tabs Component&#39;s edit dialog items tab](/help/assets/tabs-edit-items.png)

Gebruik de **Add** knoop om de componentenselecteur te openen om te kiezen welke component om als lusje toe te voegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:

* **Pictogram**  - Het pictogram van het componenttype van de tab voor eenvoudige identificatie in de lijst. Plaats de muis boven de volledige componentnaam als knopinfo.
* **Beschrijving**  - De beschrijving die als tekst van het lusje wordt gebruikt, die aan de naam van de component in gebreke blijft die voor het lusje wordt geselecteerd.
* **Verwijderen**  - Tik of klik om de tab uit de tabcomponent te verwijderen.
* **Herschikken**  - Tik of klik en sleep om de tabvolgorde te wijzigen.

>[!TIP]
>
>Als de viewport van de pagina wordt verminderd zodat het bewerkingsdialoogvenster volledig scherm wordt, wordt de **Add** knoop verborgen. Componenten kunnen nog steeds worden toegevoegd aan de component Tabs door [te slepen vanuit de componentenbrowser en neer te zetten op de component Tabs in de pagina-editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component).

### Tabblad Eigenschappen {#properties-tab}

![Tabs Component&#39;s edit dialog properties tab](/help/assets/tabs-edit-properties.png)

* **Actief item**  - De auteur van de inhoud kan bepalen welk tabblad actief is wanneer de pagina wordt geladen.
   * Met de optie **Standaard** wordt het eerste tabblad geselecteerd.
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheidstabblad van dialoogvenster dialoogvenster voor bewerken van tabs Component](/help/assets/tabs-edit-accessibility.png)

Op het tabblad **Toegankelijkheid** kunnen waarden worden ingesteld voor [ARIA-toegankelijkheidslabels](https://www.w3.org/WAI/standards-guidelines/aria/) voor de component.

* **Label**  - waarde van een ARIA-labelkenmerk voor de component

## Deelvenster {#select-panel} selecteren

De auteur van de inhoud kan de optie **Select Panel** op de componentwerkbalk gebruiken om over te schakelen naar een ander deelvenster voor bewerking en om de tabvolgorde gemakkelijk te wijzigen.

![Pictogram van deelvenster Selecteren](/help/assets/select-panel-icon.png)

Nadat u de optie **Deelvenster selecteren** hebt geselecteerd op de componentwerkbalk, worden de geconfigureerde tabbladen weergegeven als een vervolgkeuzelijst.

* De lijst wordt geordend door de toegewezen rangschikking van de lusjes en in de nummering weerspiegeld.
* Het componenttype van de tab wordt als eerste weergegeven, gevolgd door de beschrijving van de tab in lichtere lettertypen.

![Pop-upmenu van deelvenster selecteren](/help/assets/select-panel-popover.png)

* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar dat tabblad verplaatst.
* U kunt de tabvolgorde op de juiste plaats wijzigen door de sleepgrepen te gebruiken.

>[!NOTE]
>
>Tabs kunnen niet door de auteur worden geselecteerd in de modus **Bewerken**. Gebruik de **[modus Voorvertoning](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode)** of de optie **[Weergeven als gepubliceerd](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** om te communiceren met de tabbladen als een lezer van de gepubliceerde inhoud.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren welke componenten als items aan de component tabs kunnen worden toegevoegd en welke aangepaste stijlen beschikbaar zijn voor de auteur van de inhoud.

### Tabblad Toegestane componenten {#allowed-components-tab}

Het tabblad **Toegestane componenten** wordt gebruikt om te definiëren welke componenten door de auteur van de inhoud als items aan de component tabs kunnen worden toegevoegd.

Het tabblad Toegestane componenten werkt op dezelfde manier als het tabblad met dezelfde naam wanneer [het beleid en de eigenschappen van een container voor de layout in de Sjablooneditor worden gedefinieerd.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Tabblad Stijlen {#styles-tab}

De component van Lusjes steunt het AEM [Systeem van de Stijl](/help/get-started/authoring.md#component-styling).
