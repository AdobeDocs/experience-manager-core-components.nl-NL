---
title: E-mailsegmenteringscomponent
description: De component E-mailsegmentatie
role: Architect, Developer, Admin, User
exl-id: 6c88b8c5-189a-40c0-ab28-04d37dc5fbac
source-git-commit: 91969e4956bef1a511b8d588d5290a7999bf86ec
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 0%

---


# E-mailsegmenteringscomponent {#email-segmentation-component}

De component E-mailsegmentatie gebruikt variabelen van Adobe Campaign om inhoud weer te geven en te verbergen op basis van de ontvanger van de inhoud.

## Gebruik {#usage}

Met de component Email Segmentation kan de auteur van de inhoud inhoud inhoud verbergen en weergeven op basis van voorwaarden waaraan wordt voldaan door variabelen over de ontvanger die door Adobe Campaign worden aangeboden. Op deze manier zien de ontvangers van de inhoud de inhoud op basis van hun segmentatie.

* De malplaatjeauteur kan de [ ontwerpdialoog ](#design-dialog) gebruiken om te bepalen welke componenten als segment kunnen worden toegevoegd.
* De inhoudauteur kan [ gebruiken vormt dialoog ](#configure-dialog) om componenten als segmenten toe te voegen en te vormen welke segmenten gebaseerd op de variabelen van Adobe Campaign worden getoond.

Als alternatief voor het gebruiken van vormen dialoog, zodra de inhoudauteur de Component van de Segmentatie E-mail aan een inhoudspagina heeft toegevoegd, kan de inhoudauteur dan extra componenten slepen en neerzetten op de Componenten van de Segmentatie E-mail om nieuwe segmenten tot stand te brengen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de E-mailsegmenteringscomponent is v1, die in oktober 2022 is geïntroduceerd met release x van de Email Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel | - | - |

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Teaser E-mail [ kan op GitHub worden gevonden.](https://adobe.com/go/aem_cmp_tech_email_segmentation_v1)

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden.](/help/developing/overview.md)

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud segmenten maken, hernoemen en opnieuw rangschikken en het actieve segment definiëren. In de Component van de Segmentatie E-mail, is een segment eenvoudig een andere component die wordt verborgen of getoond gebaseerd op voorwaarden die door de ontvanger van de inhoud worden voldaan. U kunt het met de [ Component van het Lusje van de Componenten van de Kern vergelijken, ](/help/components/tabs.md) maar in de Component van de Segmentatie, slechts de inhoud van het lusje de waarvan voorwaarden worden voldaan aan getoond.

### Tabblad Items {#items-tab}

![ Component van de Segmentatie van de E-mail vormt dialoogpunten tabel ](/help/email/assets/email-segmentation-configure-items.png)

Gebruik **voeg de knoop van het Segment** toe om de componentenselecteur te openen om welke component te kiezen om als segment toe te voegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende elementen:

* **Pictogram** - het pictogram van het componenttype van het segment voor gemakkelijke identificatie in de lijst. Plaats de muisaanwijzer boven de volledige componentnaam om deze weer te geven als knopinfo.
* **Voorwaarde** - de voorwaarde die voor dit segment moet worden voldaan om aan de ontvanger van de inhoud te worden getoond.
   * De beschikbare voorwaarden worden bepaald in de [ ontwerpdialoog.](#design-dialog)
   * **Gebrek** - bepaalt het standaardsegment om te tonen als geen andere voorwaarden worden voldaan
   * **Douane** - staat de auteur toe om een voorwaarde te bepalen
      * De voorwaarden zijn gebaseerd op Adobe Campaign-personalisatievariabelen
      * [ zie hier voor de personaliseringsmiddelen van Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?lang=nl-NL&)
      * [ zie hier voor de personaliseringsmiddelen van Adobe Campaign Classic.](https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/personalization-fields.html?lang=nl-NL)
* **Schrapping** - Tik of klik om het segment van de Component van de Segmentatie E-mail te schrappen.
* **herschikt** - Tik of klik en sleep om de segmenten opnieuw te rangschikken.

>[!TIP]
>
>Als viewport van de inhoud wordt verminderd zodat uitgeeft dialoog volledig scherm wordt, **voegt** knoop toe zal worden verborgen. De componenten kunnen nog aan de Component van de Segmentatie E-mail worden toegevoegd door [ van componenten te slepen browser en op de Component van de Segmentatie E-mail in de inhoudsredacteur te vallen.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=nl-NL#inserting-a-component)

### Tabblad Eigenschappen {#properties-tab}

![ Component van de Segmentatie van de E-mail vormt dialoogeigenschappen tabel ](/help/email/assets/email-segmentation-configure-properties.png)

* **identiteitskaart** - Deze optie staat het controleren van het unieke herkenningsteken van de component in HTML toe.
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende inhoud te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor CSS.

### Tabblad Toegankelijkheid {#accessibility-tab}

![ Component van de Segmentatie van de E-mail vormt dialoogtoegankelijkheid tabel ](/help/email/assets/email-segmentation-configure-accessibility.png)

Op het **lusje van de Toegankelijkheid**, kunnen de waarden voor [ de toegankelijkheidslabels van ARIA ](https://www.w3.org/WAI/standards-guidelines/aria/) voor de component worden geplaatst.

* **Etiket** - Waarde van een ARIA etiketattribuut voor de component

### Tabblad Stijlen {#styles-tab-edit}

De component E-mail van de Segmentatie steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling)

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [ ontwerpdialoog ](#design-dialog) worden gevormd opdat het lusje beschikbaar is.

## Deelvenster selecteren {#select-panel}

De inhoudauteur kan de **Uitgezochte 1&rbrace; optie van het Comité &lbrace;op de componententoolbar gebruiken om in een verschillend segment voor het uitgeven te veranderen evenals de segmenten gemakkelijk te herschikken.**

![ Uitgezochte paneelpictogram ](/help/email/assets/select-panel-icon.png)

Zodra het selecteren van de **Uitgezochte optie van het Comité** in de componententoolbar, worden de gevormde segmenten getoond als drop-down.

* De lijst wordt geordend door de toegewezen rangschikking van de segmenten en wordt weerspiegeld in de nummering.
* Het componenttype van het segment wordt eerst weergegeven, gevolgd door de beschrijving van het segment in lichtere lettertypen.

![ Uitgezochte paneel popover ](/help/email/assets/select-panel-popover.png)

* Als u op een item in het vervolgkeuzemenu tikt of erop klikt, wordt de weergave in de editor naar dat segment verplaatst.
* U kunt de segmenten op hun plaats opnieuw rangschikken met behulp van de sleepgrepen.

>[!NOTE]
>
>De segmenten worden teruggegeven als lusjes binnen de paginaredacteur om te tonen dat er veelvoudige opties voor de definitieve inhoud zijn. Deze tabbladen kunnen niet door de auteur worden geselecteerd in de pagina-editor. Gebruik het deelvenster Selecteren om te schakelen tussen de weergegeven segmenten.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur definiëren welke componenten als segmenten aan de E-mailsegmenteringscomponent kunnen worden toegevoegd en welke aangepaste stijlen beschikbaar zijn voor de auteur van de inhoud.

### Tabblad Toegestane componenten {#allowed-components-tab}

Het **Toegestane lusje van Componenten** wordt gebruikt om te bepalen welke componenten als segmenten aan de Component van de Segmentatie E-mail door de inhoudauteur kunnen worden toegevoegd.

**Toegestane Componenten** tabfuncties op dezelfde manier als het lusje van de zelfde naam wanneer [ het bepalen van het beleid en de eigenschappen van een Container van de Lay-out in de Redacteur van het Malplaatje.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=nl-NL)

### Tabblad Stijlen {#styles-tab}

De component E-mail van de Segmentatie steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling)

### Tabblad Gedefinieerde voorwaarden {#defined-conditions}

Gebruikend het **Gedefinieerde Voorwaarden** lusje, kan de malplaatjeredacteur bepalen welke voorwaarden aan de inhoudauteur beschikbaar zijn om te selecteren wanneer het creëren van segmenten.

![ de dialoog van het Ontwerp bepaalde het lusje van Voorwaarden ](/help/email/assets/email-segmentation-design-defined-conditions.png)

Tik of klik **voeg** knoop toe om nieuwe voorwaarden tot stand te brengen.

* **Naam van de Voorwaarde van het Segment** - een beschrijving van de voorwaarde
* **Voorwaarde van het Segment** - de daadwerkelijke voorwaarde die moet worden voldaan aan, die op de personaliseringsvariabelen van Adobe Campaign wordt gebaseerd
   * [ zie hier voor de personaliseringsmiddelen van Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?lang=nl-NL&)
   * [ zie hier voor de personaliseringsmiddelen van Adobe Campaign Classic.]&#x200B;(https://experienceleague.adobe.com/docs/?lang=nl-NL
* **verwijder** - Tik om te klikken om de voorwaarde te verwijderen
* **herschikt** - Tik of klik en sleep om de orde van de voorwaarden te herschikken
