---
title: Pagina-component
description: De component Pagina is een uitbreidbare paginacomponent die wordt ontworpen om met de malplaatjeredacteur te werken en paginakopbal/footer en structuurcomponenten toe te laten om met de malplaatjedacteur worden samengesteld.
role: Architect, Developer, Admin, User
exl-id: 2503e067-abed-427d-8a54-8b79e3451487
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---


# Pagina-component{#page-component}

De Component van de Pagina is een verlengbare paginacomponent die wordt ontworpen om met de [ malplaatjedacteur ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) te werken en staat paginakopbal/footer en structuurcomponenten toe om met de malplaatjedacteur worden samengesteld.

{{traditional-aem}}

## Gebruik {#usage}

De component Pagina vormt de basis van alle pagina&#39;s die zijn ontworpen met de kerncomponenten en bewerkbare sjablonen. Met de component Pagina kunt u kop- en voetteksten en de structuur van de pagina definiëren als een sjabloon met de andere kerncomponenten.

Gebruikend de [ ontwerpdialoog ](#design-dialog), kunnen de douane cliënt-zijbibliotheken voor de pagina worden bepaald. In tegenstelling tot andere componenten die een uitgeven dialoog hebben die direct van de component toegankelijk is, omdat de Component van de Pagina de pagina zelf is, [ uitgeeft dialoog ](#edit-dialog) van de Component van de Pagina is het venster van pagina-eigenschappen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de pagina-component is v3, die in februari 2022 is geïntroduceerd met release 2.18.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v3 | - | Compatibel | Compatibel | Compatibel |
| [ v2 ](v2/page.md) | Compatibel | Compatibel | - | Compatibel |
| [ v1 ](v1/page-v1.md) | Compatibel | Compatibel | - | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Progressieve ondersteuning voor webtoepassingen {#pwa-support}

Versie 2.15.0 van de Componenten van de Kern introduceerde steun voor ingebouwde [ Progressieve eigenschappen van het Web van AEM as a Cloud Service (PWA).](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html) Met een eenvoudige configuratie op site-niveau kunt u uw AEM-ervaring veranderen in een PWA!

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Pagina [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_page_v3) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

Omdat de component de volledige pagina vertegenwoordigt, worden de montages die normaal in zouden zijn uitgeeft dialoog gevonden in het [ venster van de Eigenschappen van de Pagina ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Ontwerpdialoogvenster {#design-dialog}

Omdat de component de volledige pagina vertegenwoordigt, wordt de ontwerpdialoog betreden via **Informatie van de Pagina -> Beleid van de Pagina** wanneer het uitgeven van het paginamalplaatje.

![ Beleid van de Pagina ](/help/assets/page-policy.png)

>[!NOTE]
>
>In vorige versies van AEM, **het Beleid van de Pagina** werd genoemd **het Ontwerp van de Pagina**.

### Tabblad Eigenschappen {#properties-tab}

Met behulp van het venster Paginaontwerp kunt u de te laden clientbibliotheken en de bibliotheek met webbronnen voor de pagina definiëren.

* **Bibliotheken van de Cliënt** - dit bepaalt de categorieën van de cliëntbibliotheek aan lading. JavaScript wordt toegevoegd aan het hoofdgedeelte en de CSS wordt toegevoegd aan de paginakop.
* **de Bibliotheken van de Cliënt JavaScript Hoofd van de Pagina** - dit bepaalt de de bibliotheekcategorieën van de Cliënt van JavaScript in het paginakop te laden.
   * De categorieën die hier worden bepaald die ook aanwezig zijn in het **gebied van de Bibliotheken van de Cliënt** zullen JavaScript hebben die in de paginakop in plaats van bij lichaamseind wordt geladen.
   * Geen CSS zal worden geladen tenzij de categorie ook op het **gebied van de Bibliotheken van de Cliënt 0&rbrace; &lbrace;aanwezig is.**

* **Bibliotheek van de Cliënt van Middelen van het Web** - de categorie van de cliëntbibliotheek die wordt gebruikt om Webmiddelen zoals favicons te dienen.

* **Overslaan aan de selecteur van het belangrijkste inhoudselement** - Gebruikt als toegankelijkheidseigenschap om rechtstreeks aan de belangrijkste inhoud van de pagina over te slaan

* **geef alternatieve taalverbindingen** terug - indien toegelaten, zullen de verbindingen met afwisselende taalversies van de pagina in de zelfde plaats aan het hoofd van de pagina worden toegevoegd.

![ de ontwerpdialoog van de Component van de Pagina ](/help/assets/page-design.png)

De bibliotheken kunnen voor zowel de **Bibliotheken van de Cliënt** als **het Hoofd van de Pagina van JavaScript van de Bibliotheken van de Cliënt** gebieden als volgt worden gevormd:

* Om een nieuw gebied toe te voegen klik of tik **toevoegen** knoop onder de gebieden.
* Als u een veld wilt verwijderen, klikt of tikt u op het prullenbakpictogram naast het veld dat u wilt verwijderen.
* Als u de laadvolgorde wilt wijzigen, klikt of tikt u op de greep naast het te verplaatsen veld.

Voor meer informatie over het gebruiken van cliënt-zijbibliotheken zie [ Gebruikend de Bibliotheken van de Kant van de Cliënt ](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>De mogelijkheid om clientbibliotheken voor de paginakop afzonderlijk te definiëren, is geïntroduceerd met versie 2.2.0 van de kerncomponenten.

### Tabblad Stijlen {#styles-tab}

De Component van de Pagina steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De Component van de Pagina steunt de [ Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
