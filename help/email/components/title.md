---
title: Component E-mailtitel
description: De component E-mailtitel is een onderdeel voor sectiekoppen van uw e-mailberichten waarin bewerkingen op locatie worden uitgevoerd.
role: Architect, Developer, Admin, User
exl-id: f65b6973-bb36-406f-bbea-f85a23f5340b
source-git-commit: 3abc29e0c186a84f079d5938b8b716f4c7378d65
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 0%

---


# Component E-mailtitel {#email-title-component}

De component E-mailtitel is een onderdeel voor sectiekoppen van uw e-mailberichten waarin bewerkingen op locatie worden uitgevoerd.

## Gebruik {#usage}

De component E-mailtitel is bedoeld voor gebruik als titel of koptekst van een sectie van een e-mailbericht.

* De beschikbare rubriekniveaus kunnen door de malplaatjeauteur in de [ ontwerpdialoog worden bepaald.](#design-dialog)
* De inhoudauteur kan uit beschikbare kopteksten selecteren niveaus in [ uitgeven dialoog.](#edit-dialog)

Voor meer gemak is het ook mogelijk de koptekst eenvoudig op locatie te bewerken.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component E-mailtitel is v1, die in oktober 2022 is geïntroduceerd met release x van de Email Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatibel | - |

Voor meer informatie over de versies en de versies van de Component van de Kern, zie de Versies van de Componenten van de Kern van het document [ E-mail van de Kern ](/help/versions.md).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Titel [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_email_title_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de titeltekst definiëren en het kopniveau selecteren.

* **Titel** - als leeg de paginatitel zal worden gebruikt
   * Klik het pictogram van de Campagne om [ Uitgezochte de Variabele van Adobe Campaign ](/help/email/campaign-variables.md) dialoog te openen om dynamische inhoud van Adobe Campaign op te nemen.
* **Type/Grootte** - bepaalt het kopniveau van de titel
* **Verbinding** - bepaalt de inhoud waaraan de titel zal verbinden. Dit kan een pad zijn naar een inhoudspagina, een externe URL of een pagina-anker.
   * Klik het pictogram van de Campagne om [ Uitgezochte de Variabele van Adobe Campaign ](/help/email/campaign-variables.md) dialoog te openen om dynamische inhoud van Adobe Campaign op te nemen.
* **identiteitskaart** - Deze optie staat het controleren van het unieke herkenningsteken van de component in HTML toe.
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor CSS.

![ uitgeeft de Component van de Titel van de E-mail dialoog ](/help/email/assets/email-title-edit.png)

U kunt de editor op zijn plaats ook gebruiken om de tekst van de titelcomponent te bewerken.

![ In-place het uitgeven van de Component van de Titel van de E-mail ](/help/email/assets/email-title-edit-inline.png)

### Tabblad Stijlen {#styles-tab-edit}

De component van de Titel E-mail steunt het AEM [ Systeem van de Stijl.](/help/get-started/authoring.md#component-styling)

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [ ontwerpdialoog ](#design-dialog) worden gevormd opdat het drop-down menu beschikbaar is.

![ het lusje van Stijlen van uitgeeft dialoog van de Component van de Titel ](/help/email/assets/email-title-edit-styles.png)

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur het standaardkopniveau definiëren dat titelcomponenten hebben wanneer ze door de auteurs van de inhoud worden gemaakt.

### Tabblad Grootte {#sizes-tab}

![ het ontwerpdialoog van de Component van de Titel ](/help/email/assets/email-title-design.png)

* **Toegestane Types/Grootte voor Auteurs** - laat of maak rubriektypes toe onbruikbaar die voor inhoudsauteurs beschikbaar zullen zijn wanneer zij de Component van de Titel E-mail gebruiken.
* **StandaardType/Grootte** - bepaal het rubriektype dat automatisch zal worden toegewezen wanneer een inhoudsauteur de Component van de Titel E-mail aan een pagina toevoegt.
* **maak Verbinding** onbruikbaar - maak steun voor verbindingen in de Component van de Titel E-mail onbruikbaar om inhoudsauteurs van titels te verbieden te verbinden.

### Tabblad Stijlen {#styles-tab}

De component van de Titel E-mail steunt het AEM [ Systeem van de Stijl ](/help/get-started/authoring.md#component-styling).
