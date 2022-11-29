---
title: Component E-mailpagina
description: De component E-mailpagina
role: Architect, Developer, Admin, User
exl-id: 17fd0f5e-2b85-41a1-abaf-8ad190a5341a
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---


# Component E-mailpagina {#email-page-component}

De component E-mailpagina is een uitbreidbare pagina-component die is ontworpen voor gebruik met de [sjablooneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) en staat toe dat paginakoptekst/voettekst en structuurcomponenten worden samengevoegd met de sjablooneditor, op maat gemaakt voor het maken van Adobe Campaign-inhoud.

## Gebruik {#usage}

De component E-mailpagina vormt de basis voor alle pagina&#39;s die zijn ontworpen met de E-mailkern-componenten en bewerkbare sjablonen. Met de component E-mailpagina kunt u kop- en voetteksten en de structuur van de pagina definiëren als een sjabloon met de andere onderdelen van de e-mailkern.

* Met de [dialoogvenster voor ontwerp,](#design-dialog) aangepaste clientbibliotheken kunnen voor de pagina worden gedefinieerd.
* In tegenstelling tot andere componenten met een bewerkingsdialoogvenster dat rechtstreeks vanuit de component toegankelijk is, is de component E-mailpagina de pagina zelf, de component [dialoogvenster bewerken](#edit-dialog) van de component E-mailpagina is het venster met pagina-eigenschappen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de E-mailpaginacomponent is v1, die in oktober 2022 werd geïntroduceerd met release X van de Email Core Components, en wordt in dit document beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van e-mail Core Component [Core Components-versies e-mailen](/help/email/versions.md)

### Technische details {#technical-details}

De meest recente technische documentatie over de pagina-component [kan op GitHub worden gevonden.](https://adobe.com/go/aem_cmp_tech_email_page_v1)

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

Omdat de component de gehele pagina vertegenwoordigt, worden instellingen die normaal gesproken in een bewerkingsdialoogvenster staan, gevonden in het dialoogvenster [Pagina-eigenschappen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) venster.

### Tabblad Cloud Services {#cloud-services}

De pagina moet gekoppeld zijn aan een Adobe Campaign-configuratie zodat de e-mailCore-componenten campagnevariabelen en -gegevens kunnen ophalen.

![Eigenschappen van e-mailpagina](/help/email/assets/email-page-properties.png)

Onder **Configuratie Cloud Service** kop, in de vervolgkeuzelijst selecteert u **Configuratie toevoegen**.

Onder **Adobe Campaign** Selecteer de configuratie voor uw integratie met Adobe Campaign.

Zie het document [E-mailkerncomponenten gebruiken](/help/email/using.md) voor meer informatie over het instellen van de E-mailkern-componenten.

### E-mailtabblad {#email-tab}

Het tabblad E-mail definieert eigenschappen van e-mails die via Adobe Campaign worden verzonden op basis van de inhoud van deze pagina, zoals het onderwerp E-mail en onbewerkte tekstinhoud.

![Eigenschappen van e-mailpagina](/help/email/assets/email-page-properties-email.png)

* **Onderwerp** - Het onderwerp van de e-mail die Adobe Campaign op deze pagina heeft verzonden
   * Klik op de knop **Adobe Campaign-variabele selecteren** pictogram om het [Adobe Campaign-variabele selecteren](/help/email/campaign-variables.md) om dynamische inhoud uit Adobe Campaign in te voegen.
* **Pre-header**
   * Klik op de knop **Adobe Campaign-variabele selecteren** pictogram om het [Adobe Campaign-variabele selecteren](/help/email/campaign-variables.md) om dynamische inhoud uit Adobe Campaign in te voegen.
* **Onbewerkte tekst** - De onbewerkte tekstversie van het e-mailbericht dat door Adobe Campaign is verzonden
   * Klik op de knop **Adobe Campaign-variabele selecteren** pictogram om het [Adobe Campaign-variabele selecteren](/help/email/campaign-variables.md) om dynamische inhoud uit Adobe Campaign in te voegen.
* **Referentie-URL**

## Ontwerpdialoogvenster {#design-dialog}

Omdat de component de volledige pagina vertegenwoordigt, is het ontwerpdialoogvenster toegankelijk via **Paginagegevens -> Paginabeleid** bij het bewerken van de paginasjabloon.

![Paginabeleid](/help/assets/page-policy.png)

### Tabblad Eigenschappen {#properties-tab}

Met behulp van het venster Paginaontwerp kunt u de te laden clientbibliotheken en de bibliotheek met webbronnen voor de pagina definiëren.

![Dialoogvenster Ontwerp van e-mailcomponent](/help/email/assets/email-page-design.png)

* **Clientbibliotheken** - Hiermee worden de categorieën van de clientbibliotheek gedefinieerd die moeten worden geladen. JavaScript wordt toegevoegd aan het hoofdgedeelte en de CSS wordt toegevoegd aan de paginakop.
* **JavaScript-paginakop voor clientbibliotheken** - Hiermee worden de JavaScript-clientbibliotheekcategorieën gedefinieerd die in de paginakop moeten worden geladen.
   * Categorieën die hier worden gedefinieerd en die ook voorkomen in het dialoogvenster **Clientbibliotheken** in het veld wordt JavaScript geladen in de paginakop in plaats van aan het tekstuele einde.
   * Geen CSS wordt geladen tenzij de categorie ook aanwezig is in de **Clientbibliotheken** veld.
* **JavaScript-bibliotheken asynchroon laden** - Als deze optie is ingeschakeld, worden de aangepaste JavaScript-bibliotheken asynchroon geladen.
* **Web Resources Client Library** - De categorie van de clientbibliotheek die wordt gebruikt voor webbronnen, zoals favicons.
* **Overslaan naar de selectie van het hoofdelement** - Wordt gebruikt als toegankelijkheidsfunctie om rechtstreeks naar de hoofdinhoud van de pagina te gaan

De bibliotheken kunnen voor beide worden gevormd **Clientbibliotheken** en **JavaScript-paginakop voor clientbibliotheken** velden als volgt:

* Als u een nieuw veld wilt toevoegen, klikt of tikt u op de knop **Toevoegen** onder de velden.
* Als u een veld wilt verwijderen, klikt of tikt u op het prullenbakpictogram naast het veld dat u wilt verwijderen.
* Als u de laadvolgorde wilt wijzigen, klikt of tikt u op de greep naast het te verplaatsen veld.

Voor meer informatie over het gebruiken van cliënt-zijbibliotheken, zie [Clientzijbibliotheken gebruiken.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html)

### Tabblad Stijlen {#styles-tab}

De component Pagina ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
