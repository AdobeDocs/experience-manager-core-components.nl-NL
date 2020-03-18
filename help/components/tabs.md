---
title: Component Tabs
description: Met de component Tabs kunt u meerdere tabbladen maken om de inhoud op een pagina te rangschikken.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Component Tabs

Met de component Core Component Tabs kunt u inhoud op meerdere tabbladen ordenen.

## Gebruik {#usage}

Met de component Tabs kan de auteur van de inhoud de pagina-inhoud op meerdere tabbladen ordenen.

In het dialoogvenster [](#edit-dialog) Bewerken kan de auteur van de inhoud meerdere tabbladen definiëren en het actieve tabblad instellen. Met behulp van het dialoogvenster [](#design-dialog)Ontwerp kan de sjabloonauteur definiëren welke componenten aan tabbladen kunnen worden toegevoegd en de stijlen aanpassen.

>[!NOTE]
>
>Geneste tabcomponenten (tabs binnen tabs) worden ondersteund.
>
>Eenvoudige (niet-geneste) tabcomponenten kunnen worden gevonden/geselecteerd met de [inhoudsstructuur](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html#content-tree), maar geneste tabbladen kunnen niet worden gevonden.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Tabs Component is v1, die in oktober 2018 is geïntroduceerd met release 2.2.0 van de Core Components (Basiscomponenten). Deze versie wordt in dit document beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v1 | Compatibel | Compatibel | Compatibel | Compatibel |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_tabs)om de component Tabs te bekijken en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van Lusjes [kan op GitHub](https://adobe.com/go/aem_cmp_tech_tabs_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud tabbladen maken, hernoemen en opnieuw rangschikken, en het actieve tabblad definiëren.

### Tabblad Items {#items-tab}

![](/help/assets/screen-shot-2019-08-29-12.28.16.png)

Gebruik de knop **Toevoegen** om de componentkiezer te openen en te kiezen welke component u als tab wilt toevoegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:

* **Pictogram** - Het pictogram van het componenttype van de tab voor eenvoudige identificatie in de lijst. Plaats de muis boven de volledige componentnaam als knopinfo.
* **Beschrijving** - De beschrijving die als tekst van het lusje wordt gebruikt, die aan de naam van de component in gebreke blijft die voor het lusje wordt geselecteerd.
* **Verwijderen** - Tik of klik om de tab uit de tabcomponent te verwijderen.
* **Herschik** - Tik of klik en sleep om de tabvolgorde te wijzigen.

>[!TIP]
>
>Als de viewport van de pagina wordt verminderd zodat het bewerkingsdialoogvenster volledig scherm wordt, wordt de knop **Toevoegen** verborgen. Componenten kunnen nog steeds worden toegevoegd aan de component Tabs door de [component te slepen vanuit de browser Component en neer te zetten op de component Tabs in de pagina-editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component).

### Tabblad Eigenschappen {#properties-tab}

![](/help/assets/screen-shot-2019-08-29-12.28.32.png)

Op het tabblad **Eigenschappen** kan de auteur van de inhoud definiëren welk tabblad actief is wanneer de pagina wordt geladen. Met de optie **Standaard** wordt het eerste tabblad geselecteerd.

### Tabblad Toegankelijkheid {#accessibility-tab}

![](/help/assets/screen-shot-2019-08-29-12.28.40.png)

Op het tabblad **Toegankelijkheid** kunnen waarden worden ingesteld voor [ARIA-toegankelijkheidslabels](https://www.w3.org/WAI/standards-guidelines/aria/) voor de component.

* **Label** - waarde van een ARIA-labelkenmerk voor de component

## Deelvenster selecteren {#select-panel}

De auteur van de inhoud kan de optie Deelvenster **** selecteren op de werkbalk van de component gebruiken om de volgorde van de tabbladen te wijzigen en deze te bewerken.

![](/help/assets/screenshot_2018-10-11at165417.png)

Nadat u de optie Deelvenster **** selecteren op de werkbalk van de component hebt geselecteerd, worden de geconfigureerde tabbladen weergegeven als een vervolgkeuzelijst.

* De lijst wordt geordend door de toegewezen rangschikking van de lusjes en in de nummering weerspiegeld.
* Het componenttype van de tab wordt als eerste weergegeven, gevolgd door de beschrijving van de tab in lichtere lettertypen.

![](/help/assets/screenshot_2018-10-11at165154.png)

* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar dat tabblad verplaatst.
* U kunt de tabvolgorde op de juiste plaats wijzigen door de sleepgrepen te gebruiken.

>[!NOTE]
>
>Tabs kunnen niet door de auteur worden geselecteerd in de modus **Bewerken** . Gebruik de modus **[Voorvertoning](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode)**of de optie**[ Weergeven als gepubliceerd](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** om te communiceren met de tabbladen als een lezer van de gepubliceerde inhoud.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren welke componenten als items aan de component tabs kunnen worden toegevoegd en welke aangepaste stijlen beschikbaar zijn voor de auteur van de inhoud.

### Tabblad Toegestane componenten {#allowed-components-tab}

Het tabblad **Toegestane componenten** wordt gebruikt om te definiëren welke componenten door de auteur van de inhoud als items aan de component tabs kunnen worden toegevoegd.

Het tabblad Toegestane componenten werkt op dezelfde manier als het tabblad met dezelfde naam wanneer u het beleid en de eigenschappen van een container voor de layout in de Sjablooneditor [definieert.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Tabblad Stijlen {#styles-tab}

De component Tabs ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).
