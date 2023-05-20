---
title: Formuliercontainercomponent (v1)
description: Met de Core Component Form Container Component kunnen eenvoudige verzendformulieren worden gemaakt.
index: n
role: Architect, Developer, Admin, User
exl-id: 1e34219f-fa82-494e-82e2-1b4d63d37fea
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 0%

---

# Formuliercontainercomponent (v1) {#form-container-component-v1}

Met de Core Component Form Container Component kunnen eenvoudige verzendformulieren worden gemaakt.

## Gebruik {#usage}

Met de component Form Container konden eenvoudige formulieren en functies voor het verzenden van informatie worden gemaakt door eenvoudige WCM-formulieren te ondersteunen en door een geneste structuur te gebruiken om extra formuliercomponenten toe te staan.

Met de [dialoogvenster instellen](#settings-dialog) de inhoudeditor kan bepalen welk type actie door het verzenden van een formulier wordt geactiveerd, waar de verzonden inhoud moet worden opgeslagen en of een workflow moet worden geactiveerd. De sjabloonauteur kan de opdracht [ontwerpdialoogvenster](#design-dialog) om de toegestane componenten en hun toewijzingen te bepalen gelijkend op de ontwerpdialoog voor [standaardlay-outcontainer in de sjablooneditor](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Form Container Component beschreven, die oorspronkelijk werd geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van versie 1 van de component Form Container weergegeven.

| AEM | Formuliercontainercomponent v1 |
|--- |--- |
| 6.3 | Compatibel |
| 6.4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Form Container beschreven.
>
>Voor meer informatie over de huidige versie van de component Form Container raadpleegt u de [Component Form Container](/help/components/forms/form-container.md) document.

## Dialoogvenster Instellingen {#settings-dialog}

In het dialoogvenster met instellingen kan de auteur van de inhoud definiëren welke handelingen worden uitgevoerd wanneer de component wordt verzonden.

![](/help/assets/chlimage_1.png)

Afhankelijk van de geselecteerde **Type handeling** De beschikbare opties in de container worden gewijzigd. De beschikbare actietypen zijn:

* [Mail](#mail)
* [Winkelinhoud](#store-content)
* [Bestelling verzenden](#submit-order)
* [Volgorde bijwerken](#update-order)

Ongeacht het type zijn er [algemene instellingen](#general-settings) die van toepassing zijn op elke actie.

### Mail {#mail}

Wanneer het formulier wordt verzonden, verzendt het type e-mailactie een e-mail naar aangewezen ontvangers.

![](/help/assets/chlimage_1-1.png)

* **Onderwerp** - Het onderwerp van de e-mail die wordt verzonden bij het verzenden van het formulier
* **Van** - Het formulier van het e-mailadres van het e-mailbericht dat wordt verzonden bij het verzenden van het formulier
* **Naar** - De adressen van de ontvangers die een e-mail zullen ontvangen wanneer het formulier wordt verzonden
   * Tik of klik op de knop **Toevoegen** knop om extra adressen toe te voegen
   * Tik of klik op de knop **Verwijderen** knop om een e-mailadres te verwijderen
* **CC** - Het adres van ontvangers die een koolstofkopie ontvangen van de e-mail die is verzonden bij het verzenden van het formulier.
   * Tik of klik op de knop **Toevoegen** knop om extra adressen toe te voegen
   * Tik of klik op de knop **Verwijderen** knop om een e-mailadres te verwijderen

### Winkelinhoud {#store-content}

Wanneer het formulier wordt verzonden, wordt de inhoud van het formulier opgeslagen in een aangewezen opslagplaats.

![](/help/assets/chlimage_1-2.png)

* **Inhoudspad** - Pad van inhoudsopslagplaats waar verzonden inhoud wordt opgeslagen
* **Gegevens weergeven** - Tik of klik om opgeslagen verzonden gegevens weer te geven als JSON
* **Workflow starten** - Configureren om een workflow met de opgeslagen inhoud te starten als een payload bij het verzenden van het formulier

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

* Gebruik het dialoogvenster Selectie om een bron binnen AEM te selecteren.
* Geef de absolute URL op als de pagina voor bedankt niet in AEM is. Niet-absolute URL&#39;s worden ten opzichte van AEM geïnterpreteerd.
* Laat leeg om het formulier na verzending opnieuw weer te geven.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de toegestane componenten en de bijbehorende toewijzingen voor de container definiëren, vergelijkbaar met het ontwerpdialoogvenster voor de [standaardlay-outcontainer in de sjablooneditor](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843).

## Technische details {#technical-details}

De meest recente technische documentatie over de component Form Container [kan op GitHub worden gevonden](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container).

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).
