---
title: Component Form Container
description: Met de Core Component Form Container Component kunnen eenvoudige verzendformulieren worden gemaakt.
translation-type: tm+mt
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Component Form Container {#form-container-component}

Met de Core Component Form Container Component kunnen eenvoudige verzendformulieren worden gemaakt.

## Gebruik {#usage}

Met de component Form Container kunt u formulieren en functies voor eenvoudige informatieverzending maken door eenvoudige WCM-formulieren te ondersteunen en door een geneste structuur te gebruiken om extra formuliercomponenten toe te staan.

Door het dialoogvenster [](#configure-dialog) configureren te gebruiken, kan de inhoudseditor de actie definiëren die wordt geactiveerd door het verzenden van formulieren, waar de verzonden inhoud moet worden opgeslagen en of een workflow moet worden geactiveerd. De sjabloonauteur kan het [ontwerpdialoogvenster](#design-dialog) gebruiken om de toegestane componenten en de bijbehorende toewijzingen te definiëren, net als in het ontwerpdialoogvenster voor de [standaardlay-outcontainer in de sjablooneditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>De kerncomponenten Form Container Component ondersteunen alleen het gebruik van basiscomponenten van componenten (knop, tekst, verborgen enz.). Het gebruik van [basiscomponenten](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) van formuliercomponenten in de basiscomponenten van de formuliercontainer (en andersom) wordt niet ondersteund.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Form Container Component is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatibel | Compatibel | Compatibel | Compatibel |
| [v1](/help/components/v1/form-container-v1.md) | Compatibel | Compatibel | Compatibel | - |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_form_container)voor meer informatie over de component Form Container en voorbeelden van de bijbehorende configuratieopties en over HTML- en JSON-uitvoer.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Container van de Vorm [kan op GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud definiëren welke handelingen worden uitgevoerd wanneer de component wordt verzonden.

![](/help/assets/screen_shot_2018-01-12at122046.png)

Afhankelijk van het geselecteerde **handelingstype** veranderen de beschikbare opties in de container. De beschikbare actietypen zijn:

* [Mail](#mail)
* [Winkelinhoud](#store-content)
* [Bestelling verzenden](#submit-order)
* [Volgorde bijwerken](#update-order)

Ongeacht het type zijn er [algemene instellingen](#general-settings) die van toepassing zijn op elke actie.

### Mail {#mail}

Wanneer het formulier wordt verzonden, verzendt het type e-mailactie een e-mail naar aangewezen ontvangers.

![](/help/assets/screen_shot_2018-01-12at122554.png)

* **Betreft** Het onderwerp van de e-mail die wordt verzonden bij het verzenden van het formulier
* **Van** het e-mailadres van het e-mailadres dat wordt verzonden bij het verzenden van het formulier
* **Aan** de adressen van de ontvangers die na het verzenden van het formulier een e-mail zullen ontvangen

   * Tik of klik op de knop **Toevoegen** om extra adressen toe te voegen
   * Tik of klik op de knop **Verwijderen** om een e-mailadres te verwijderen
* **CC** De adressen van ontvangers die een koolstofkopie zullen ontvangen van het e-mailbericht dat is verzonden bij het verzenden van het formulier
   * Tik of klik op de knop **Toevoegen** om extra adressen toe te voegen
   * Tik of klik op de knop **Verwijderen** om een e-mailadres te verwijderen

### Winkelinhoud {#store-content}

Wanneer het formulier wordt verzonden, wordt de inhoud van het formulier opgeslagen in een aangewezen opslagplaats.

![](/help/assets/screen_shot_2018-01-12at122538.png)

* **Pad** naar opslagplaats voor inhoud waar verzonden inhoud is opgeslagen
* **De Tik van Gegevens** van de Mening of klik om opgeslagen voorgelegde gegevens als JSON te bekijken
* **Start Workflow** Configure (Configureren) om een workflow met de opgeslagen inhoud te starten als payload bij het verzenden van het formulier

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

In het ontwerpdialoogvenster kan de sjabloonauteur de toegestane componenten en de bijbehorende toewijzingen voor de container definiëren, vergelijkbaar met het dialoogvenster voor het ontwerp van de [standaardlay-outcontainer in de sjablooneditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).
