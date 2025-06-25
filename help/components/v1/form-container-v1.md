---
title: Formuliercontainercomponent (v1)
description: Met de Core Component Form Container Component kunnen eenvoudige verzendformulieren worden gemaakt.
index: n
role: Architect, Developer, Admin, User
exl-id: 1e34219f-fa82-494e-82e2-1b4d63d37fea
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---


# Formuliercontainercomponent (v1) {#form-container-component-v1}

Met de Core Component Form Container Component kunnen eenvoudige verzendformulieren worden gemaakt.

## Gebruik {#usage}

Met de component Form Container konden eenvoudige formulieren en functies voor het verzenden van informatie worden gemaakt door eenvoudige WCM-formulieren te ondersteunen en door een geneste structuur te gebruiken om extra formuliercomponenten toe te staan.

Door het [ plaatsen dialoog ](#settings-dialog) te gebruiken kan de inhoudsredacteur bepalen welk type van actievorm indiensttrekkers, waar de voorgelegde inhoud zou moeten worden opgeslagen, en als een werkschema zou moeten worden teweeggebracht. De malplaatjeauteur kan de [ ontwerpdialoog ](#design-dialog) gebruiken om toe te staan componenten en hun afbeeldingen gelijkend op de ontwerpdialoog voor de [ standaardlay-outcontainer in de malplaatjedacteur ](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html) te bepalen.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Form Container Component beschreven, die oorspronkelijk werd geïntroduceerd met versie 1.0.0 van de Core Components with AEM 6.3.

In de volgende tabel wordt de compatibiliteit van versie 1 van de component Form Container weergegeven.

| AEM-versie | Formuliercontainercomponent v1 |
|--- |--- |
| 6,3 | Compatibel |
| 6,4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Form Container beschreven.
>
>Voor details van de huidige versie van de Component van de Container van de Vorm, zie het [ document van de Component van de Container van de Vorm ](/help/components/forms/form-container.md).

## Dialoogvenster Instellingen {#settings-dialog}

In het dialoogvenster met instellingen kan de auteur van de inhoud definiëren welke handelingen worden uitgevoerd wanneer de component wordt verzonden.

![](/help/assets/chlimage_1.png)

Afhankelijk van het geselecteerde **Type van Actie**, zullen de beschikbare opties binnen de container veranderen. De beschikbare actietypen zijn:

* [Mail](#mail)
* [Winkelinhoud](#store-content)
* [Bestelling verzenden](#submit-order)
* [Volgorde bijwerken](#update-order)

Ongeacht het type, zijn er [ algemene montages ](#general-settings) die op elke actie van toepassing zijn.

### Mail {#mail}

Wanneer het formulier wordt verzonden, verzendt het type e-mailactie een e-mail naar aangewezen ontvangers.

![](/help/assets/chlimage_1-1.png)

* **Onderwerp** - Het onderwerp van e-mail dat als vormvoorlegging zal worden verzonden
* **van** - de van e-mailadres van e-mail die op vormvoorlegging zal worden verzonden
* **aan** - de adressen van de ontvangers die een e-mail op vormvoorlegging zullen ontvangen
   * Tik of klik **voeg** knoop toe om extra adressen toe te voegen
   * Tik of klik de **Schrapping** knoop om een e-mailadres te verwijderen
* **CC** - de adressen van ontvangers die een koolstofkopie zullen ontvangen e-mail die op vormvoorlegging wordt verzonden
   * Tik of klik **voeg** knoop toe om extra adressen toe te voegen
   * Tik of klik de **Schrapping** knoop om een e-mailadres te verwijderen

### Winkelinhoud {#store-content}

Wanneer het formulier wordt verzonden, wordt de inhoud van het formulier opgeslagen in een aangewezen opslagplaats.

![](/help/assets/chlimage_1-2.png)

* **Weg van de Inhoud** - de weg van de bewaarplaats van de Inhoud waar de voorgelegde inhoud wordt opgeslagen
* **Gegevens van de Mening** - Tik of klik om opgeslagen voorgelegde gegevens als JSON te bekijken
* **Werkschema van het Begin** - vorm om een werkschema met de opgeslagen inhoud als nuttige lading op vormvoorlegging te beginnen

### Bestelling verzenden {#submit-order}

Wanneer het formulier wordt ingediend, wordt de bestelling verzonden.

![](/help/assets/chlimage_1-3.png)

### Volgorde bijwerken {#update-order}

Wanneer het formulier wordt verzonden, wordt de volgorde bijgewerkt.

![](/help/assets/chlimage_1-4.png)

### Algemene instellingen {#general-settings}

Ongeacht het geselecteerde handelingstype, kan een pagina van dank u altijd worden bepaald.

![](/help/assets/chlimage_1-5.png)

De gebruiker wordt na het verzenden van het formulier omgeleid naar de opgegeven pagina.

* Gebruik het dialoogvenster Selectie om een bron in AEM te selecteren.
* Geef de absolute URL op als de pagina Bedankt niet in AEM staat. Niet-absolute URL&#39;s worden geïnterpreteerd ten opzichte van AEM.
* Laat leeg om het formulier na verzending opnieuw weer te geven.

## Ontwerpdialoogvenster {#design-dialog}

De ontwerpdialoog staat de malplaatjeauteur toe om de toegestane componenten en hun afbeeldingen voor de container te bepalen gelijkend op de ontwerpdialoog voor de [ standaardlay-outcontainer in de malplaatjedacteur ](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Container van de Vorm [ kan op GitHub ](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container) worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).
