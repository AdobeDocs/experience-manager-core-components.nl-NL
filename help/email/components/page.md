---
title: Component E-mailpagina
description: De component E-mailpagina
role: Architect, Developer, Admin, User
exl-id: 17fd0f5e-2b85-41a1-abaf-8ad190a5341a
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 0%

---


# Component E-mailpagina {#email-page-component}

De component E-mail van de Pagina is een verlengbare paginacomponent die wordt ontworpen om met de [ malplaatjedacteur ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) te werken en staat paginakopbal/footer en structuurcomponenten toe om met de malplaatjedacteur worden geassembleerd, die voor het creëren van de inhoud van Adobe Campaign wordt gemaakt.

## Gebruik {#usage}

De component E-mailpagina vormt de basis voor alle pagina&#39;s die zijn ontworpen met de E-mailkern-componenten en bewerkbare sjablonen. Met de component E-mailpagina kunt u kop- en voetteksten en de structuur van de pagina definiëren als een sjabloon met de andere onderdelen van de e-mailkern.

* Gebruikend de [ ontwerpdialoog, ](#design-dialog) douane cliënt-zijbibliotheken kunnen voor de pagina worden bepaald.
* In tegenstelling tot andere componenten die een uitgeven dialoog hebben direct toegankelijk van de component, omdat de Component van de E-mailPagina de pagina zelf is, geeft [ dialoog uit ](#edit-dialog) van de Component van de E-mailPagina is het venster van pagina-eigenschappen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de E-mailpaginacomponent is v1, die in oktober 2022 werd geïntroduceerd met release X van de Email Core Components, en wordt in dit document beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel | - | - |

Voor meer informatie over de versies en versies van de Component van de Kern E-mailE-mail van de Component, zie het document [ Versies van de Componenten van de Kern ](/help/email/versions.md)

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Pagina [ kan op GitHub worden gevonden.](https://adobe.com/go/aem_cmp_tech_email_page_v1)

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

Omdat de component de volledige pagina vertegenwoordigt, worden de montages die normaal in zouden zijn uitgeeft dialoog gevonden in het [ venster van de Eigenschappen van de Pagina ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

### Tabblad Cloud Services {#cloud-services}

De pagina moet gekoppeld zijn aan een Adobe Campaign-configuratie zodat de e-mailCore-componenten campagnevariabelen en -gegevens kunnen ophalen.

![ E-mailEigenschappen van de Pagina ](/help/email/assets/email-page-properties.png)

Onder **de rubriek van de Configuratie van Cloud Service**, in de drop-down uitgezochte **voegt Configuratie** toe.

Onder **Adobe Campaign** rubriek, selecteer de configuratie voor uw integratie met Adobe Campaign.

Zie het document [ Gebruikend de Componenten van de Kern E-mail ](/help/email/using.md) voor meer informatie over vestiging de Componenten van de Kern E-mail.

### Tabblad E-mail {#email-tab}

Het tabblad E-mail definieert eigenschappen van e-mails die via Adobe Campaign worden verzonden op basis van de inhoud van deze pagina, zoals het onderwerp E-mail en onbewerkte tekstinhoud.

![ E-mailEigenschappen van de Pagina ](/help/email/assets/email-page-properties-email.png)

* **Onderwerp** - Het onderwerp van e-mail die door Adobe Campaign wordt verzonden die op deze pagina wordt gebaseerd
   * Klik het **Uitgezochte de Variabele van Adobe Campaign** pictogram om [ Uitgezochte de Variabele van Adobe Campaign ](/help/email/campaign-variables.md) dialoog te openen om dynamische inhoud van Adobe Campaign op te nemen.
* **pre-kopbal**
   * Klik het **Uitgezochte de Variabele van Adobe Campaign** pictogram om [ Uitgezochte de Variabele van Adobe Campaign ](/help/email/campaign-variables.md) dialoog te openen om dynamische inhoud van Adobe Campaign op te nemen.
* **Onbewerkte tekst** - de gewone tekstversie van e-mail die door Adobe Campaign wordt verzonden
   * Klik het **Uitgezochte de Variabele van Adobe Campaign** pictogram om [ Uitgezochte de Variabele van Adobe Campaign ](/help/email/campaign-variables.md) dialoog te openen om dynamische inhoud van Adobe Campaign op te nemen.
* **Verwijzing URL**

## Ontwerpdialoogvenster {#design-dialog}

Omdat de component de volledige pagina vertegenwoordigt, wordt de ontwerpdialoog betreden via **Informatie van de Pagina -> Beleid van de Pagina** wanneer het uitgeven van het paginamalplaatje.

![ Beleid van de Pagina ](/help/assets/page-policy.png)

### Tabblad Eigenschappen {#properties-tab}

Met behulp van het venster Paginaontwerp kunt u de te laden clientbibliotheken en de bibliotheek met webbronnen voor de pagina definiëren.

![ het ontwerpdialoog van de Component van de E-mail van de Pagina ](/help/email/assets/email-page-design.png)

* **Bibliotheken van de Cliënt** - dit bepaalt de categorieën van de cliëntbibliotheek aan lading. JavaScript wordt toegevoegd aan het hoofdgedeelte en de CSS wordt toegevoegd aan de paginakop.
* **de Bibliotheken van de Cliënt JavaScript Hoofd van de Pagina** - dit bepaalt de categorieën van de de cliëntbibliotheek van JavaScript in de paginakop te laden.
   * De categorieën die hier worden bepaald die ook aanwezig zijn in het **gebied van de Bibliotheken van de Cliënt** zullen JavaScript hebben die in de paginakop in plaats van bij lichaamseind wordt geladen.
   * Geen CSS zal worden geladen tenzij de categorie ook op het **gebied van de Bibliotheken van de Cliënt 0&rbrace; &lbrace;aanwezig is.**
* **de Bibliotheken van JavaScript van de Lading asynchroon** - Indien toegelaten, zullen de bibliotheken van douaneJavaScript asynchroon worden geladen.
* **Bibliotheek van de Cliënt van Middelen van het Web** - de categorie van de cliëntbibliotheek die wordt gebruikt om Webmiddelen zoals favicons te dienen.
* **Overslaan aan de selecteur van het belangrijkste inhoudselement** - Gebruikt als toegankelijkheidseigenschap om rechtstreeks aan de belangrijkste inhoud van de pagina over te slaan

De bibliotheken kunnen voor zowel de **Bibliotheken van de Cliënt** als **het Hoofd van de Pagina van JavaScript van de Bibliotheken van de Cliënt** gebieden als volgt worden gevormd:

* Om een nieuw gebied toe te voegen, klik of tik **toevoegen** knoop onder de gebieden.
* Als u een veld wilt verwijderen, klikt of tikt u op het prullenbakpictogram naast het veld dat u wilt verwijderen.
* Als u de laadvolgorde wilt wijzigen, klikt of tikt u op de greep naast het te verplaatsen veld.

Voor meer informatie over het gebruiken van cliënt-zijbibliotheken, zie [ Gebruikend de Bibliotheken van de Kant van de Cliënt.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html)

### Tabblad Stijlen {#styles-tab}

De Component van de Pagina steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).
