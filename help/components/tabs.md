---
title: Component Tabs
description: Met de component Tabs kunt u meerdere tabbladen maken om de inhoud op een pagina te rangschikken.
role: Architect, Developer, Admin, User
exl-id: 0031c5f3-447c-4932-898f-2f453801e492
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 1%

---

# Component Tabs {#tabs-component}

Met de component Core Component Tabs kunt u inhoud op meerdere tabbladen ordenen.

## Gebruik {#usage}

Met de component Tabs kan de auteur van de inhoud de pagina-inhoud op meerdere tabbladen ordenen.

De [dialoogvenster bewerken](#edit-dialog) Hiermee kan de auteur van de inhoud meerdere tabbladen definiëren en het actieve tabblad instellen. Met de [ontwerpdialoogvenster](#design-dialog)kan de sjabloonauteur definiëren welke componenten aan tabbladen kunnen worden toegevoegd en de stijlen aanpassen.

>[!TIP]
>
>Geneste tabcomponenten (tabs binnen tabs) worden ondersteund.
>
>U kunt eenvoudige (niet-geneste) tabonderdelen vinden of selecteren met de opdracht [inhoudsstructuur](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html#content-tree)geneste tabbladen kunnen echter niet worden gebruikt.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Tabs Component is v1, die in oktober 2018 is geïntroduceerd met release 2.2.0 van de Core Components (Basiscomponenten). Deze versie wordt in dit document beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de component Tabs wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_tabs).

### Technische details {#technical-details}

De meest recente technische documentatie over de Tabs-component [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_tabs_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Diep koppelen aan een deelvenster {#deep-linking}

De tabs en [Accordeoncomponenten](accordion.md) ondersteuning voor koppelingen rechtstreeks naar een deelvenster binnen de component.

Dit doet u als volgt:

1. De pagina met de component weergeven met de **[Weergeven als gepubliceerd](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** in de pagina-editor.
1. Inspect de inhoud van de pagina en identificeer de id van het deelvenster.
   * Bijvoorbeeld `id="accordion-86196c94d3-item-ca319dbb0b"`
1. De id wordt het anker dat u met een hash aan de URL kunt toevoegen (`#`).
   * Bijvoorbeeld `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

Wanneer u met de deelvenster-id als anker naar de URL navigeert, schuift de browser rechtstreeks naar de desbetreffende component en geeft deze het opgegeven deelvenster weer. Als het deelvenster is geconfigureerd om niet standaard te worden uitgevouwen, wordt het automatisch uitgevouwen.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud tabbladen maken, hernoemen en opnieuw rangschikken, en het actieve tabblad definiëren.

### Tabblad Items {#items-tab}

![Tabs Component&#39;s edit dialog items tab](/help/assets/tabs-edit-items.png)

Gebruik de **Toevoegen** om de componentkiezer te openen en te kiezen welke component u als tab wilt toevoegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:

* **Pictogram** - Het pictogram van het componenttype van de tab voor eenvoudige identificatie in de lijst. Plaats de muis boven de volledige componentnaam als knopinfo.
* **Beschrijving** - De beschrijving die als tekst van het lusje wordt gebruikt, stellend aan de naam van de component die voor het lusje wordt geselecteerd.
* **Verwijderen** - Tik of klik om de tab uit de tabcomponent te verwijderen.
* **Opnieuw rangschikken** - Tik of klik en sleep om de tabvolgorde te wijzigen.

>[!TIP]
>
>Als de viewport van de pagina wordt verkleind zodat het dialoogvenster Bewerken volledig scherm wordt, wordt het dialoogvenster **Toevoegen** wordt verborgen. Componenten kunnen nog steeds door [slepen vanuit de componentenbrowser en neerzetten op de component Tabs in de paginaeditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component).

### Tabblad Eigenschappen {#properties-tab}

![Tabs Component&#39;s edit dialog properties tab](/help/assets/tabs-edit-properties.png)

* **Actief item** - De auteur van de inhoud kan bepalen welk tabblad actief is wanneer de pagina wordt geladen.
   * Met de **Standaard** wordt de eerste tab geselecteerd.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheidstabblad van dialoogvenster dialoogvenster voor bewerken van tabs Component](/help/assets/tabs-edit-accessibility.png)

Op de **Toegankelijkheid** tab, waarden kunnen worden ingesteld voor [Toegankelijkheid ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) labels voor de component.

* **Label** - Waarde van een ARIA-labelkenmerk voor de component

## Deelvenster selecteren {#select-panel}

De auteur van de inhoud kan de **Deelvenster selecteren** op de werkbalk van de component om te schakelen naar een ander deelvenster voor bewerking en om de tabvolgorde gemakkelijk te wijzigen.

![Pictogram van deelvenster Selecteren](/help/assets/select-panel-icon.png)

Wanneer u de **Deelvenster selecteren** in de componentwerkbalk worden de geconfigureerde tabbladen weergegeven als een vervolgkeuzelijst.

* De lijst wordt geordend door de toegewezen rangschikking van de lusjes en in de nummering weerspiegeld.
* Het componenttype van de tab wordt als eerste weergegeven, gevolgd door de beschrijving van de tab in lichtere lettertypen.

![Pop-upmenu van deelvenster selecteren](/help/assets/select-panel-popover.png)

* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar dat tabblad verplaatst.
* U kunt de tabvolgorde op de juiste plaats wijzigen door de sleepgrepen te gebruiken.

>[!NOTE]
>
>Tabs kunnen niet door de auteur worden geselecteerd wanneer deze zich aanmeldt **Bewerken** in. Gebruiken **[Voorvertoning](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode)** of de **[Weergeven als gepubliceerd](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** gebruiken om te communiceren met de tabbladen, zoals een lezer van de gepubliceerde inhoud zou doen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren welke componenten als items aan de component tabs kunnen worden toegevoegd en welke aangepaste stijlen beschikbaar zijn voor de auteur van de inhoud.

### Tabblad Toegestane componenten {#allowed-components-tab}

De **Toegestane componenten** wordt gebruikt om te definiëren welke componenten door de auteur van de inhoud als items aan de component tabs kunnen worden toegevoegd.

Het tabblad Toegestane componenten werkt op dezelfde manier als het tabblad met dezelfde naam wanneer [het definiëren van het beleid en de eigenschappen van een container voor layout in de Sjablooneditor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Tabblad Stijlen {#styles-tab}

De component Tabs ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component Tabs ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
