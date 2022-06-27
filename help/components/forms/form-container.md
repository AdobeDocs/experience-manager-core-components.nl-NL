---
title: Component Form Container
description: Met de Core Component Form Container Component kunnen eenvoudige verzendformulieren worden gemaakt.
role: Architect, Developer, Admin, User
exl-id: 552f9dd5-6a3a-42d9-9969-e62a1f36e811
source-git-commit: 16930ccaa281f9d9c4ddbb890d4222e128557580
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 0%

---

# Component Form Container {#form-container-component}

Met de Core Component Form Container Component kunnen eenvoudige verzendformulieren worden gemaakt.

## Gebruik {#usage}

Met de component Form Container kunt u formulieren en functies voor eenvoudige informatieverzending maken door eenvoudige WCM-formulieren te ondersteunen en door een geneste structuur te gebruiken om extra formuliercomponenten toe te staan.

Met de [dialoogvenster configureren](#configure-dialog) De inhoudeditor kan de actie definiëren die wordt geactiveerd door het verzenden van formulieren, de URL die de verzending moet verwerken en of een workflow moet worden geactiveerd. De sjabloonauteur kan de opdracht [ontwerpdialoogvenster](#design-dialog) om de toegestane componenten en hun toewijzingen te bepalen gelijkend op de ontwerpdialoog voor [standaardlay-outcontainer in de sjablooneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>De kerncomponenten Form Container Component ondersteunen alleen het gebruik van basiscomponenten van componenten (knop, tekst, verborgen enz.). Gebruiken [stichtingscomponenten](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/siteandpage/default-components-foundation.html) formuliercomponenten binnen de kerncomponenten van de formuliercontainer (en omgekeerd) worden niet ondersteund.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Form Container Component is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel | Compatibel |
| [v1](/help/components/v1/form-container-v1.md) | Compatibel | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de component Form Container wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_form_container).

## Technische details {#technical-details}

De meest recente technische documentatie over de component Form Container [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_form_container_v2).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud definiëren welke handelingen worden uitgevoerd wanneer de component wordt verzonden.

Afhankelijk van de geselecteerde **Type handeling** De beschikbare opties in de container worden gewijzigd. De beschikbare actietypen zijn:

* [Formuliergegevens verzenden](#post-data)
* [Mail](#mail)
* [Winkelinhoud](#store-content)

Ongeacht het type zijn er [algemene instellingen](#general-settings) die van toepassing zijn op elke actie.

### Formuliergegevens verzenden {#post-data}

Wanneer het formulier wordt verzonden, worden de ingediende gegevens door het actietype voor postformuliergegevens doorgegeven aan een derde als JSON voor verwerking.

![Opties voor gegevens na formulier in het bewerkingsdialoogvenster van de component Form Container](/help/assets/form-container-edit-post.png)

* **Endpoint** - De volledig gekwalificeerde HTTPS-service die de gegevens verwerkt
* **Foutbericht** - Bericht om weer te geven als de verzending niet is gelukt

>[!TIP]
>Er zijn extra time-outopties die een systeembeheerder kan aanpassen om de verwerking van doorgestuurde formuliergegevens af te handelen. [Zie de technische documentatie op GitHub voor meer informatie.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/actions/rpc)

### Mail {#mail}

Wanneer het formulier wordt verzonden, verzendt het type e-mailactie een e-mail naar aangewezen ontvangers.

![E-mailopties in het bewerkingsdialoogvenster van de component Form Container](/help/assets/form-container-edit-mail.png)

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

![Opties voor het opslaan van inhoud in het dialoogvenster Bewerken van de formuliercontainer](/help/assets/form-container-edit-store.png)

* **Inhoudspad** - Pad van inhoudsopslagplaats waar verzonden inhoud wordt opgeslagen
* **Gegevens weergeven** - Tik of klik om opgeslagen verzonden gegevens weer te geven als JSON
* **Workflow starten** - Configureren om een workflow met de opgeslagen inhoud te starten als een payload bij het verzenden van het formulier

>[!NOTE]
>
>Om het beheer van gebruikersgegevens eenvoudiger te maken en scheiding van zorgen af te dwingen, wordt het over het algemeen niet aanbevolen door gebruikers gegenereerde inhoud in de opslagplaats op te slaan.
>
>Gebruik in plaats daarvan de [Formuliergegevens verzenden](#post-data) actietype om gebruikersinhoud door te geven aan een specifieke dienstverlener.

### Algemene instellingen {#general-settings}

Ongeacht het geselecteerde handelingstype, kan een pagina van dank u altijd worden bepaald.

![Algemene opties in het dialoogvenster Bewerken van component Form Container](/help/assets/form-container-edit-general.png)

* **Bedankt, pagina** - De gebruiker wordt na het verzenden van het formulier omgeleid naar de opgegeven pagina.
   * Gebruik het dialoogvenster Selectie om een bron binnen AEM te selecteren.
   * Geef de absolute URL op als de pagina voor bedankt niet in AEM is. Niet-absolute URL&#39;s worden ten opzichte van AEM geïnterpreteerd.
   * Laat leeg om het formulier na verzending opnieuw weer te geven.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de toegestane componenten en de bijbehorende toewijzingen voor de container definiëren, vergelijkbaar met het ontwerpdialoogvenster voor de [standaardlay-outcontainer in de sjablooneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html).

### Tabblad Stijlen {#styles-tab}

De component Form Container ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
