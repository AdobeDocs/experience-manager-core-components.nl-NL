---
title: Component E-mailknop
description: Met de component E-mailknop kunt u een knopitem in uw inhoud configureren en weergeven.
role: Architect, Developer, Admin, User
exl-id: b144e8d1-1097-475d-b2eb-3353c176afb9
source-git-commit: 91969e4956bef1a511b8d588d5290a7999bf86ec
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---


# Component E-mailknop {#email-button-component}

Met de component E-mailknop kunt u een knopitem in uw inhoud configureren en weergeven.

## Gebruik {#usage}

Met de component E-mailknop kunt u een knop in uw inhoud opnemen, waarop door de inhoudslezer kan worden geklikt en die aan extra bronnen is gekoppeld.

* De eigenschappen van de knoop kunnen in [ worden geselecteerd vormen dialoog.](#configure-dialog)
* De stijlen voor de Component van de Knoop E-mail kunnen in de [ ontwerpdialoog worden bepaald.](#design-dialog)

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Email Button is v1, die in oktober 2022 is geïntroduceerd met release x van de Email Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel | - | - |

Voor meer informatie over de versies en de versies van de Component van de Kern, zie het document [ e-mailVersie van de Componenten van de Kern.](/help/email/versions.md)

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Knoop E-mail [ kan op GitHub worden gevonden.](https://adobe.com/go/aem_cmp_tech_email_button_v1)

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden.](/help/developing/overview.md)

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud de knop definiëren en bepalen hoe deze zich gedraagt en wordt weergegeven voor een lezer van uw inhoud.

### Tabblad Eigenschappen {#properties-tab}

![ het lusje van Eigenschappen van uitgeeft dialoog van de Component van de Knoop ](/help/email/assets/email-button-edit-properties.png)

* **Tekst** - de tekst om op de knoop te tonen
   * Klik het pictogram van de Campagne om [ Uitgezochte de Variabele van Adobe Campaign ](/help/email/campaign-variables.md) dialoog te openen om dynamische inhoud van Adobe Campaign op te nemen.
* **Verbinding** - Verbinding met een inhoudspagina binnen AEM, een extern middel, of een anker
   * Gebruik de **Dialoog van de Selectie** om een weg binnen AEM te kiezen.
   * Klik het pictogram van de Campagne om [ Uitgezochte de Variabele van Adobe Campaign ](/help/email/campaign-variables.md) dialoog te openen om dynamische inhoud van Adobe Campaign op te nemen.
* **Pictogram** - Herkenningsteken voor het tonen van een pictogram in de knoop
* **identiteitskaart** - Deze optie staat controle van het unieke herkenningsteken van de component in HTML toe.
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende inhoud te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor CSS.
* **Open verbinding in nieuw lusje** - als gecontroleerd, zal de verbinding in een nieuwe browser tabel openen.

### Tabblad Toegankelijkheid {#accessibility-tab}

![ Toegankelijkheid lusje van uitgeeft dialoog van de Component van de Knoop ](/help/email/assets/email-button-edit-accessibility.png)

Op het **lusje van de Toegankelijkheid**, kunnen de waarden voor [ de toegankelijkheidslabels van ARIA ](https://www.w3.org/WAI/standards-guidelines/aria/) voor de component worden geplaatst.

* **Etiket** - Waarde van een ARIA etiketattribuut voor de component

### Tabblad Stijlen {#styles-tab-edit}

De component van de Knoop E-mail steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [ ontwerpdialoog ](#design-dialog) worden gevormd opdat het lusje beschikbaar is.

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De E-mailComponent van de Knoop steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).
