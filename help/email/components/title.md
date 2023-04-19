---
title: Component E-mailtitel
description: De component E-mailtitel is een onderdeel voor sectiekoppen van uw e-mailberichten waarin bewerkingen op locatie worden uitgevoerd.
role: Architect, Developer, Admin, User
exl-id: f65b6973-bb36-406f-bbea-f85a23f5340b
source-git-commit: 3abc29e0c186a84f079d5938b8b716f4c7378d65
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 1%

---


# Component E-mailtitel {#email-title-component}

De component E-mailtitel is een onderdeel voor sectiekoppen van uw e-mailberichten waarin bewerkingen op locatie worden uitgevoerd.

## Gebruik {#usage}

De component E-mailtitel is bedoeld om te worden gebruikt als de titel of koptekst van een sectie van een e-mailbericht.

* De beschikbare kopniveaus kunnen door de sjabloonauteur in het dialoogvenster [ontwerpdialoogvenster.](#design-dialog)
* De auteur van de inhoud kan een keuze maken uit de beschikbare koptekstniveaus in het dialoogvenster [dialoogvenster bewerken.](#edit-dialog)

Voor meer gemak is het ook mogelijk de koptekst eenvoudig op locatie te bewerken.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component E-mailtitel is v1, die in oktober 2022 is geïntroduceerd met release x van de Email Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatibel | - |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Email Components Versies](/help/versions.md).

### Technische details {#technical-details}

De meest recente technische documentatie over de component Title [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_email_title_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de titeltekst definiëren en het kopniveau selecteren.

* **Titel** - Als de paginatitel leeg is, wordt deze gebruikt
   * Klik op het pictogram Campagne om het dialoogvenster [Adobe Campaign-variabele selecteren](/help/email/campaign-variables.md) om dynamische inhoud uit Adobe Campaign in te voegen.
* **Tekst/grootte** - Definieert het kopniveau van de titel
* **Koppeling** - Hiermee definieert u de inhoud waaraan de titel wordt gekoppeld. Dit kan een pad zijn naar een inhoudspagina, een externe URL of een pagina-anker.
   * Klik op het pictogram Campagne om het dialoogvenster [Adobe Campaign-variabele selecteren](/help/email/campaign-variables.md) om dynamische inhoud uit Adobe Campaign in te voegen.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML bepalen.
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor CSS.

![Dialoogvenster voor bewerken van component E-mailtitel](/help/email/assets/email-title-edit.png)

U kunt de editor op zijn plaats ook gebruiken om de tekst van de titelcomponent te bewerken.

![Lokaal bewerken van component E-mailtitel](/help/email/assets/email-title-edit-inline.png)

### Tabblad Stijlen {#styles-tab-edit}

De component E-mailtitel ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling)

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in worden gevormd [ontwerpdialoogvenster](#design-dialog) zodat het vervolgkeuzemenu beschikbaar is.

![Het tabblad Stijlen van het dialoogvenster Titel-component bewerken](/help/email/assets/email-title-edit-styles.png)

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur het standaardkopniveau definiëren dat titelcomponenten hebben wanneer ze door de auteurs van de inhoud worden gemaakt.

### Tabblad Grootte {#sizes-tab}

![Ontwerpdialoogvenster van component Title](/help/email/assets/email-title-design.png)

* **Toegestane typen/grootten voor auteurs** - Keuzetypen in- of uitschakelen die beschikbaar zijn voor auteurs van inhoud wanneer ze de component E-mailtitel gebruiken.
* **Standaardtype/grootte** - Definieer het koptype dat automatisch wordt toegewezen wanneer een auteur van de inhoud de component E-mailtitel aan een pagina toevoegt.
* **Koppeling uitschakelen** - Schakel ondersteuning voor koppelingen in de component E-mailtitel uit om te voorkomen dat auteurs van inhoud koppelingen naar titels maken.

### Tabblad Stijlen {#styles-tab}

De component E-mailtitel ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
