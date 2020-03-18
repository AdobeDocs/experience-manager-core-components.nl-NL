---
title: Formuliercontainercomponent (v1)
description: Met de Core Component Form Container Component kunnen eenvoudige verzendformulieren worden gemaakt.
index: n
translation-type: tm+mt
source-git-commit: 68472ab548fb6ebb443a06c12e7b37797a0c1302

---


# Formuliercontainercomponent (v1) {#form-container-component-v1}

Met de Core Component Form Container Component kunnen eenvoudige verzendformulieren worden gemaakt.

## Gebruik {#usage}

Met de component Form Container konden eenvoudige formulieren en functies voor het verzenden van informatie worden gemaakt door eenvoudige WCM-formulieren te ondersteunen en door een geneste structuur te gebruiken om extra formuliercomponenten toe te staan.

Door het dialoogvenster [](#settings-dialog) Instelling te gebruiken, kan de inhoudseditor definiëren welk type actie door het verzenden van een formulier wordt geactiveerd, waar de verzonden inhoud moet worden opgeslagen en of een workflow moet worden geactiveerd. De sjabloonauteur kan het [ontwerpdialoogvenster](#design-dialog) gebruiken om de toegestane componenten en de bijbehorende toewijzingen te definiëren, net als het ontwerpdialoogvenster voor de [standaardlay-outcontainer in de sjablooneditor](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Form Container Component beschreven, die oorspronkelijk werd geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van versie 1 van de component Form Container weergegeven.

| AEM-versie | Formuliercontainercomponent v1 |
|--- |--- |
| 6.3 | Compatibel |
| 6.4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Form Container beschreven.
>
>Zie het document [Form Container Component](/help/components/forms/form-container.md) voor meer informatie over de huidige versie van Form Container Component.

## Dialoogvenster Instellingen {#settings-dialog}

In het dialoogvenster met instellingen kan de auteur van de inhoud definiëren welke handelingen worden uitgevoerd wanneer de component wordt verzonden.

![](/help/assets/chlimage_1.png)

Afhankelijk van het geselecteerde **handelingstype** veranderen de beschikbare opties in de container. De beschikbare actietypen zijn:

* [Mail](#mail)
* [Winkelinhoud](#store-content)
* [Bestelling verzenden](#submit-order)
* [Volgorde bijwerken](#update-order)

Ongeacht het type zijn er [algemene instellingen](#general-settings) die van toepassing zijn op elke actie.

### Mail {#mail}

Wanneer het formulier wordt verzonden, verzendt het type e-mailactie een e-mail naar aangewezen ontvangers.

![](/help/assets/chlimage_1-1.png)

* **Betreft** : Het onderwerp van de e-mail die wordt verzonden bij het verzenden van het formulier
* **Van** - Het e-mailadres van het e-mailadres dat wordt verzonden bij het verzenden van het formulier
* **Aan** - De adressen van de ontvangers die na het verzenden van het formulier een e-mail zullen ontvangen
   * Tik of klik op de knop **Toevoegen** om extra adressen toe te voegen
   * Tik of klik op de knop **Verwijderen** om een e-mailadres te verwijderen
* **CC** - De adressen van ontvangers die een koolstofkopie ontvangen van het e-mailbericht dat wordt verzonden bij het verzenden van het formulier
   * Tik of klik op de knop **Toevoegen** om extra adressen toe te voegen
   * Tik of klik op de knop **Verwijderen** om een e-mailadres te verwijderen

### Winkelinhoud {#store-content}

Wanneer het formulier wordt verzonden, wordt de inhoud van het formulier opgeslagen in een aangewezen opslagplaats.

![](/help/assets/chlimage_1-2.png)

* **Inhoudspad** - Pad naar opslagplaats voor inhoud waar verzonden inhoud wordt opgeslagen
* **Gegevens** weergeven - Tik of klik om opgeslagen verzonden gegevens weer te geven als JSON
* **Workflow** starten - Configureren om een workflow met de opgeslagen inhoud te starten als lading bij het verzenden van het formulier

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
* Geef de absolute URL op als de pagina Hartelijk dank zich niet in AEM bevindt. Niet-absolute URL&#39;s worden geïnterpreteerd ten opzichte van AEM.
* Laat leeg om het formulier na verzending opnieuw weer te geven.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de toegestane componenten en de bijbehorende toewijzingen voor de container definiëren, vergelijkbaar met het dialoogvenster voor het ontwerp van de [standaardlay-outcontainer in de sjablooneditor](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Container van de Vorm [kan op GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container)worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.
