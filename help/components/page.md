---
title: Pagina-component
description: De component Pagina is een uitbreidbare paginacomponent die wordt ontworpen om met de malplaatjeredacteur te werken en paginakopbal/footer en structuurcomponenten toe te laten om met de malplaatjedacteur worden samengesteld.
role: Architect, Developer, Admin, User
exl-id: 2503e067-abed-427d-8a54-8b79e3451487
source-git-commit: d435e82d5950336c66997399829e3baf23f170c0
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 1%

---

# Pagina-component{#page-component}

De component van de Pagina is een verlengbare paginacomponent die wordt ontworpen om met [malplaatjeredacteur ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) te werken en paginakopbal/footer en structuurcomponenten toe te laten om met de malplaatjedacteur worden samengesteld.

## Gebruik {#usage}

De component Pagina vormt de basis van alle pagina&#39;s die zijn ontworpen met de kerncomponenten en bewerkbare sjablonen. Met de component Pagina kunt u kop- en voetteksten en de structuur van de pagina definiëren als een sjabloon met de andere kerncomponenten.

Met behulp van het [ontwerpdialoogvenster](#design-dialog) kunnen aangepaste client-side bibliotheken worden gedefinieerd voor de pagina. In tegenstelling tot andere componenten die een bewerkingsdialoogvenster hebben dat rechtstreeks toegankelijk is vanuit de component, omdat de component Pagina de pagina zelf is, is het [bewerkingsdialoogvenster](#edit-dialog) van de component Pagina het venster met pagina-eigenschappen.

## Progressieve ondersteuning voor webtoepassingen {#pwa-support}

Versie 2.15.0 van de Componenten van de Kern introduceerde steun voor AEM als ingebouwde [Progressieve eigenschappen van de Web Apps (PWA) van de Cloud Service.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html) Met een eenvoudige configuratie op siteniveau verandert u uw AEM in een PWA!

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de paginacomponent is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de kerncomponenten en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | Compatibel | Compatibel | Compatibel |
| [v1](v1/page-v1.md) | Compatibel | Compatibel | - |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Pagina [kan op GitHub](https://adobe.com/go/aem_cmp_tech_page_v2) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

Aangezien de component de gehele pagina vertegenwoordigt, worden instellingen die normaal gesproken in een bewerkingsdialoogvenster staan, gevonden in het venster [Pagina-eigenschappen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html).

## Ontwerpdialoogvenster {#design-dialog}

Omdat de component de volledige pagina vertegenwoordigt, is het ontwerpdialoogvenster toegankelijk via **Pagina-informatie -> Paginabeleid** bij het bewerken van de paginasjabloon.

![Paginabeleid](/help/assets/page-policy.png)

>[!NOTE]
>
>In vorige versies van AEM werd **Paginabeleid** **Paginaontwerp** genoemd.

### Tabblad Eigenschappen {#properties-tab}

Met behulp van het venster Paginaontwerp kunt u de te laden clientbibliotheken en de bibliotheek met webbronnen voor de pagina definiëren.

* **Clientbibliotheken**  - Hiermee worden de categorieën in de clientbibliotheek gedefinieerd die moeten worden geladen. JavaScript wordt toegevoegd aan het hoofdgedeelte en de CSS wordt toegevoegd aan de paginakop.
* **JavaScript-paginakop**  Client-bibliotheken - Hiermee worden de JavaScript-clientbibliotheekcategorieën gedefinieerd die in de paginakop moeten worden geladen.
   * Voor categorieën die hier worden gedefinieerd en die ook voorkomen in het veld **Client Libraries**, wordt JavaScript geladen in de paginakop in plaats van aan het body-einde.
   * CSS wordt alleen geladen als de categorie ook aanwezig is in het veld **Clientbibliotheken**.

* **De Bibliotheek**  van de Cliënt van Middelen van het Web - de categorie van de cliëntbibliotheek die wordt gebruikt om Webmiddelen zoals favicons te dienen.

* **Selector**  van hoofdelement overslaan naar hoofdinhoud - Wordt gebruikt als toegankelijkheidsfunctie om rechtstreeks naar de hoofdinhoud van de pagina over te slaan

![Dialoogvenster Pagina-componentontwerp](/help/assets/page-design.png)

Bibliotheken kunnen als volgt worden geconfigureerd voor zowel de velden **Client Libraries** als **Client Libraries JavaScript Page Head**:

* Als u een nieuw veld wilt toevoegen, klikt u op de knop **Toevoegen** onder de velden.
* Als u een veld wilt verwijderen, klikt of tikt u op het prullenbakpictogram naast het veld dat u wilt verwijderen.
* Als u de laadvolgorde wilt wijzigen, klikt of tikt u op de greep naast het te verplaatsen veld.

Zie [Client Side Libraries gebruiken](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html) voor meer informatie over het gebruik van client-side bibliotheken.

>[!CAUTION]
>
>De mogelijkheid om clientbibliotheken voor de paginakop afzonderlijk te definiëren, is geïntroduceerd met versie 2.2.0 van de kerncomponenten.

### Tabblad Stijlen {#styles-tab}

De component van de Pagina steunt het AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component van de Pagina steunt [Adobe de Laag van de Gegevens van de Cliënt.](/help/developing/data-layer/overview.md)
