---
title: Component Form Container
description: Met de Core Component Form Container Component kunnen eenvoudige verzendformulieren worden gemaakt.
translation-type: tm+mt
source-git-commit: 499047a8c15a6423a56b370f41fd020740481f80
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 0%

---


# Component Form Container {#form-container-component}

Met de Core Component Form Container Component kunnen eenvoudige verzendformulieren worden gemaakt.

## Gebruik {#usage}

Met de component Form Container kunt u formulieren en functies voor eenvoudige informatieverzending maken door eenvoudige WCM-formulieren te ondersteunen en door een geneste structuur te gebruiken om extra formuliercomponenten toe te staan.

Door het dialoogvenster [](#configure-dialog) configureren te gebruiken, kan de inhoudseditor de actie definiëren die wordt geactiveerd door het verzenden van formulieren, de URL die de verzending moet verwerken en of een workflow moet worden geactiveerd. De sjabloonauteur kan het [ontwerpdialoogvenster](#design-dialog) gebruiken om de toegestane componenten en de bijbehorende toewijzingen te definiëren, net als in het ontwerpdialoogvenster voor de [standaardlay-outcontainer in de sjablooneditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>De kerncomponenten Form Container Component ondersteunen alleen het gebruik van basiscomponenten van componenten (knop, tekst, verborgen enz.). Het gebruik van [basiscomponenten](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) van formuliercomponenten in de basiscomponenten van de formuliercontainer (en andersom) wordt niet ondersteund.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Form Container Component is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatibel | Compatibel | Compatibel |
| [v1](/help/components/v1/form-container-v1.md) | Compatibel | Compatibel | - |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_form_container)voor meer informatie over de component Form Container en voorbeelden van de bijbehorende configuratieopties en over HTML- en JSON-uitvoer.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Container van de Vorm [kan op GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud definiëren welke handelingen worden uitgevoerd wanneer de component wordt verzonden.

Afhankelijk van het geselecteerde **handelingstype** veranderen de beschikbare opties in de container. De beschikbare actietypen zijn:

* [Formuliergegevens verzenden](#post-data)
* [Mail](#mail)
* [Winkelinhoud](#store-content)

Ongeacht het type zijn er [algemene instellingen](#general-settings) die van toepassing zijn op elke actie.

### Formuliergegevens verzenden {#post-data}

Wanneer het formulier wordt verzonden, worden de ingediende gegevens door het actietype voor postformuliergegevens doorgegeven aan een derde als JSON voor verwerking.

![Opties voor gegevens na formulier in het bewerkingsdialoogvenster van de component Form Container](/help/assets/form-container-edit-post.png)

* **Eindpunt** - de volledig - gekwalificeerde dienst HTTPS die de gegevens zal verwerken
* **Foutbericht** - Bericht om weer te geven als de verzending niet is gelukt

>[!TIP]
>Er zijn extra time-outopties die een systeembeheerder kan aanpassen om de verwerking van doorgestuurde formuliergegevens af te handelen. [Zie de technische documentatie op GitHub voor meer informatie.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/actions/rpc)

### Mail {#mail}

Wanneer het formulier wordt verzonden, verzendt het type e-mailactie een e-mail naar aangewezen ontvangers.

![E-mailopties in het bewerkingsdialoogvenster van de component Form Container](/help/assets/form-container-edit-mail.png)

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

![Opties voor het opslaan van inhoud in het dialoogvenster Bewerken van de formuliercontainer](/help/assets/form-container-edit-store.png)

* **Inhoudspad** - Pad naar opslagplaats voor inhoud waar verzonden inhoud wordt opgeslagen
* **Gegevens** weergeven - Tik of klik om opgeslagen verzonden gegevens weer te geven als JSON
* **Workflow** starten - Configureren om een workflow met de opgeslagen inhoud te starten als lading bij het verzenden van het formulier

>[!NOTE]
>
>Om het beheer van gebruikersgegevens eenvoudiger te maken en scheiding van zorgen af te dwingen, wordt het over het algemeen niet aanbevolen door gebruikers gegenereerde inhoud in de opslagplaats op te slaan.
>
>Gebruik in plaats daarvan het actietype [Formuliergegevens](#post-data) verzenden om gebruikersinhoud door te geven aan een specifieke serviceprovider.

### Algemene instellingen {#general-settings}

Ongeacht het geselecteerde handelingstype, kan een pagina van dank u altijd worden bepaald.

![Algemene opties in het dialoogvenster Bewerken van component Form Container](/help/assets/form-container-edit-general.png)

* **Hartelijk dank, pagina** - De gebruiker wordt na het verzenden van het formulier omgeleid naar de opgegeven pagina.
   * Gebruik het dialoogvenster Selectie om een bron binnen AEM te selecteren.
   * Geef de absolute URL op als de pagina voor bedankt niet in AEM is. Niet-absolute URL&#39;s worden ten opzichte van AEM geïnterpreteerd.
   * Laat leeg om het formulier na verzending opnieuw weer te geven.
* **ID** - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de toegestane componenten en de bijbehorende toewijzingen voor de container definiëren, vergelijkbaar met het dialoogvenster voor het ontwerp van de [standaardlay-outcontainer in de sjablooneditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

### Tabblad Stijlen {#styles-tab}

De component Form Container ondersteunt het [Stijlsysteem](/help/get-started/authoring.md#component-styling)AEM.
