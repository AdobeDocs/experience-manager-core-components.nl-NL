---
title: Pagina-component
description: De component Pagina is een uitbreidbare paginacomponent die wordt ontworpen om met de malplaatjeredacteur te werken en paginakopbal/footer en structuurcomponenten toe te laten om met de malplaatjedacteur worden samengesteld.
role: Architect, Developer, Admin, User
exl-id: 2503e067-abed-427d-8a54-8b79e3451487
source-git-commit: 16930ccaa281f9d9c4ddbb890d4222e128557580
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 1%

---

# Pagina-component{#page-component}

De component Pagina is een uitbreidbare pagina-component die is ontworpen om te werken met de [sjablooneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) en staat toe dat paginakoptekst/voettekst en structuurcomponenten met de malplaatjeredacteur worden samengesteld.

## Gebruik {#usage}

De component Pagina vormt de basis van alle pagina&#39;s die zijn ontworpen met de kerncomponenten en bewerkbare sjablonen. Met de component Pagina kunt u kop- en voetteksten en de structuur van de pagina definiëren als een sjabloon met de andere kerncomponenten.

Met de [ontwerpdialoogvenster](#design-dialog)aangepaste clientbibliotheken kunnen voor de pagina worden gedefinieerd. In tegenstelling tot andere componenten met een bewerkingsdialoogvenster dat rechtstreeks vanuit de component toegankelijk is, is de component Pagina de pagina zelf, de component [dialoogvenster bewerken](#edit-dialog) van de component Pagina is het venster met pagina-eigenschappen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de pagina-component is v3, die in februari 2022 is geïntroduceerd met release 2.18.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|---|
| v3 | - | Compatibel | Compatibel |
| [v2](v2/page.md) | Compatibel | Compatibel | Compatibel |
| [v1](v1/page-v1.md) | Compatibel | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Progressieve ondersteuning voor webtoepassingen {#pwa-support}

Versie 2.15.0 van de Core Components introduceerde steun voor AEM ingebouwde as a Cloud Service [Progressieve functies van Web Apps (PWA).](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html) Met een eenvoudige configuratie op siteniveau verandert u uw AEM in een PWA!

### Technische details {#technical-details}

De meest recente technische documentatie over de pagina-component [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_page_v2).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

Omdat de component de gehele pagina vertegenwoordigt, worden instellingen die normaal gesproken in een bewerkingsdialoogvenster staan, gevonden in het dialoogvenster [Pagina-eigenschappen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) venster.

## Ontwerpdialoogvenster {#design-dialog}

Omdat de component de volledige pagina vertegenwoordigt, is het ontwerpdialoogvenster toegankelijk via **Paginagegevens -> Paginabeleid** bij het bewerken van de paginasjabloon.

![Paginabeleid](/help/assets/page-policy.png)

>[!NOTE]
>
>In eerdere versies van AEM **Paginabeleid** is gebeld **Paginaontwerp**.

### Tabblad Eigenschappen {#properties-tab}

Met behulp van het venster Paginaontwerp kunt u de te laden clientbibliotheken en de bibliotheek met webbronnen voor de pagina definiëren.

* **Clientbibliotheken** - Hiermee worden de categorieën van de clientbibliotheek gedefinieerd die moeten worden geladen. JavaScript wordt toegevoegd aan het hoofdgedeelte en de CSS wordt toegevoegd aan de paginakop.
* **JavaScript-paginakop voor clientbibliotheken** - Hiermee worden de JavaScript Client-bibliotheekcategorieën gedefinieerd die in de paginakop moeten worden geladen.
   * Categorieën die hier worden gedefinieerd en die ook voorkomen in het dialoogvenster **Clientbibliotheken** in het veld wordt JavaScript geladen in de paginakop in plaats van aan het tekstuele einde.
   * Geen CSS wordt geladen tenzij de categorie ook aanwezig is in de **Clientbibliotheken** veld.

* **Web Resources Client Library** - De categorie van de clientbibliotheek die wordt gebruikt voor webbronnen, zoals favicons.

* **Overslaan naar de selectie van het hoofdelement** - Wordt gebruikt als toegankelijkheidsfunctie om rechtstreeks naar de hoofdinhoud van de pagina te gaan

* **Koppelingen naar alternatieve talen renderen** - Indien ingeschakeld, worden koppelingen naar alternatieve taalversies van de pagina op dezelfde site toegevoegd aan de kop van de pagina.

![Dialoogvenster Pagina-componentontwerp](/help/assets/page-design.png)

De bibliotheken kunnen voor beide worden gevormd **Clientbibliotheken** en **JavaScript-paginakop voor clientbibliotheken** velden als volgt:

* Als u een nieuw veld wilt toevoegen, klikt u op de knop **Toevoegen** onder de velden.
* Als u een veld wilt verwijderen, klikt of tikt u op het prullenbakpictogram naast het veld dat u wilt verwijderen.
* Als u de laadvolgorde wilt wijzigen, klikt of tikt u op de greep naast het te verplaatsen veld.

Voor meer informatie over het gebruiken van cliënt-zijbibliotheken zie [Clientzijbibliotheken gebruiken](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>De mogelijkheid om clientbibliotheken voor de paginakop afzonderlijk te definiëren, is geïntroduceerd met versie 2.2.0 van de kerncomponenten.

### Tabblad Stijlen {#styles-tab}

De component Pagina ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component Pagina ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
