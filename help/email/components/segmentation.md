---
title: E-mailsegmenteringscomponent
description: De component E-mailsegmentatie
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 0%

---


# E-mailsegmenteringscomponent {#email-segmentation-component}

De component E-mailsegmentatie gebruikt variabelen van Adobe Campaign om inhoud weer te geven en te verbergen op basis van de ontvanger van de inhoud.

## Gebruik {#usage}

Met de component Email Segmentation kan de auteur van de inhoud inhoud inhoud verbergen en weergeven op basis van voorwaarden waaraan wordt voldaan door variabelen over de ontvanger die door Adobe Campaign worden aangeboden. Op deze manier zien de ontvangers van de inhoud de inhoud op basis van hun segmentatie.

* De sjabloonauteur kan de opdracht [ontwerpdialoogvenster](#design-dialog) om te bepalen welke componenten als segment kunnen worden toegevoegd.
* De auteur van de inhoud kan de [dialoogvenster configureren](#configure-dialog) om componenten als segmenten toe te voegen en te vormen welke segmenten worden getoond gebaseerd op de variabelen van Adobe Campaign.

Als alternatief voor het gebruiken van vormen dialoog, zodra de inhoudauteur de Component van de Segmentatie E-mail aan een inhoudspagina heeft toegevoegd, kan de inhoudauteur dan extra componenten slepen en neerzetten op de Componenten van de Segmentatie E-mail om nieuwe segmenten tot stand te brengen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de E-mailsegmenteringscomponent is v1, die in oktober 2022 is geïntroduceerd met release x van de Email Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatibel | Compatibel |

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de component E-mailsegmentatie wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek.](https://adobe.com/go/aem_cmp_library_email_segmentation)

### Technische details {#technical-details}

De meest recente technische documentatie over de E-maillasercomponent [kan op GitHub worden gevonden.](https://adobe.com/go/aem_cmp_tech_email_segmentation_v1)

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [De ontwikkelaarsdocumentatie van de Componenten van de kern.](/help/developing/overview.md)

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud segmenten maken, hernoemen en opnieuw rangschikken en het actieve segment definiëren. In de Component van de Segmentatie E-mail, is een segment eenvoudig een andere component die wordt verborgen of getoond gebaseerd op voorwaarden die door de ontvanger van de inhoud worden voldaan. U kunt het vergelijken met [component op het tabblad Core Components,](/help/components/tabs.md) maar in de Segmenteringscomponent wordt alleen de inhoud van het tabblad weergegeven waaraan de voorwaarden zijn voldaan.

### Tabblad Items {#items-tab}

![Het tabblad Configuratiedialoogitems van de component E-mailsegmentatie](/help/email/assets/email-segmentation-configure-items.png)

Gebruik de **Segment toevoegen** om de componentkiezer te openen en te kiezen welke component u als segment wilt toevoegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende elementen:

* **Pictogram** - Het pictogram van het componenttype van het segment voor eenvoudige identificatie in de lijst. Plaats de muis boven de volledige componentnaam als knopinfo.
* **Voorwaarde** - Aan de voorwaarde moet worden voldaan om dit segment aan de ontvanger van de inhoud te tonen.
   * De voorwaarden die beschikbaar zijn, worden gedefinieerd in de [ontwerpdialoogvenster.](#design-dialog)
   * **Standaard** - Definieert het standaardsegment om te tonen of aan geen andere voorwaarden wordt voldaan
   * **Aangepast** - Hiermee kan de auteur een voorwaarde definiëren
      * De voorwaarden zijn gebaseerd op Adobe Campaign-personalisatievariabelen
      * [Zie hier voor personalisatiebronnen van Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
      * [Zie hier voor personalisatiebronnen van Adobe Campaign Classic.](https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/personalization-fields.html)
* **Verwijderen** - Tik of klik om het segment te verwijderen uit de E-mailsegmenteringscomponent.
* **Opnieuw rangschikken** - Tik of klik en sleep om de segmenten opnieuw te rangschikken.

>[!TIP]
>
>Als de viewport van de inhoud is verkleind, zodat het dialoogvenster Bewerken volledig scherm wordt **Toevoegen** wordt verborgen. Componenten kunnen nog steeds aan de E-mailsegmenteringscomponent worden toegevoegd door [slepen vanuit de componentbrowser en neerzetten op de E-mailsegmenteringscomponent in de inhoudeditor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component)

### Tabblad Eigenschappen {#properties-tab}

![Dialoogvenster Eigenschappen van dialoogvenster E-mailsegmentatie-component configureren](/help/email/assets/email-segmentation-configure-properties.png)

* **ID** - Met deze optie kunt u de unieke id van de component in de HTML bepalen.
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende inhoud te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor CSS.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Het tabblad Toegankelijkheid van het dialoogvenster Component voor e-mailsegmentatie configureren](/help/email/assets/email-segmentation-configure-accessibility.png)

Op de **Toegankelijkheid** tab, waarden kunnen worden ingesteld voor [Toegankelijkheid ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) labels voor de component.

* **Label** - Waarde van een ARIA-labelkenmerk voor de component

### Tabblad Stijlen {#styles-tab-edit}

De component Email Segmentation ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling)

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in worden gevormd [ontwerpdialoogvenster](#design-dialog) zodat het tabblad beschikbaar is.

## Deelvenster selecteren {#select-panel}

De auteur van de inhoud kan de **Deelvenster selecteren** op de werkbalk van de component om te schakelen naar een ander segment voor bewerking en om de segmenten gemakkelijk opnieuw te rangschikken.

![Pictogram van deelvenster Selecteren](/help/email/assets/select-panel-icon.png)

Wanneer u de **Deelvenster selecteren** in de componententoolbar, worden de gevormde segmenten getoond als drop-down.

* De lijst wordt geordend door de toegewezen rangschikking van de segmenten en wordt weerspiegeld in de nummering.
* Het componenttype van het segment wordt eerst weergegeven, gevolgd door de beschrijving van het segment in lichtere lettertypen.

![Pop-upmenu van deelvenster selecteren](/help/email/assets/select-panel-popover.png)

* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar dat segment verplaatst.
* U kunt de segmenten op hun plaats opnieuw rangschikken met behulp van de sleepgrepen.

>[!NOTE]
>
>De segmenten worden teruggegeven als lusjes binnen de paginaredacteur om te tonen dat er veelvoudige opties voor de definitieve inhoud zijn. Deze tabbladen kunnen niet door de auteur worden geselecteerd in de pagina-editor. Gebruik het deelvenster Selecteren om te schakelen tussen de weergegeven segmenten.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur definiëren welke componenten als segmenten aan de E-mailsegmenteringscomponent kunnen worden toegevoegd en welke aangepaste stijlen beschikbaar zijn voor de auteur van de inhoud.

### Tabblad Toegestane componenten {#allowed-components-tab}

De **Toegestane componenten** wordt gebruikt om te bepalen welke componenten als segmenten aan de Component van de Segmentatie E-mail door de inhoudauteur kunnen worden toegevoegd.

De **Toegestane componenten** tabfuncties werken op dezelfde manier als het tabblad met dezelfde naam wanneer [het definiëren van het beleid en de eigenschappen van een container voor layout in de Sjablooneditor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Tabblad Stijlen {#styles-tab}

De component Email Segmentation ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling)

### Tabblad Gedefinieerde voorwaarden {#defined-conditions}

Met de **Gedefinieerde voorwaarden** kunt u in de sjablooneditor opgeven welke voorwaarden de auteur van de inhoud kan selecteren bij het maken van segmenten.

![Het dialoogvenster Ontwerpen, tabblad Gedefinieerde voorwaarden](/help/email/assets/email-segmentation-design-defined-conditions.png)

Tik of klik op de knop **Toevoegen** om nieuwe voorwaarden te maken.

* **Naam segmentvoorwaarde** - Een beschrijving van de voorwaarde
* **Segmentvoorwaarde** - De feitelijke voorwaarde waaraan moet worden voldaan, op basis van personalisatievariabelen van Adobe Campaign
   * [Zie hier voor personalisatiebronnen van Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
   * [Zie hier voor personalisatiebronnen van Adobe Campaign Classic.](https://experienceleague.adobe.com/docs/
* **Verwijderen** - Tik om te klikken om de voorwaarde te verwijderen
* **Opnieuw rangschikken** - Tik of klik en sleep om de volgorde van de voorwaarden te wijzigen
