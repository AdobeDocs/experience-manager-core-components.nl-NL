---
title: Pagina-component
description: De component Pagina is een uitbreidbare paginacomponent die wordt ontworpen om met de malplaatjeredacteur te werken en paginakopbal/footer en structuurcomponenten toe te laten om met de malplaatjedacteur worden samengesteld.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Pagina-component{#page-component}

De component Pagina is een uitbreidbare paginacomponent die wordt ontworpen om met de [malplaatjeredacteur](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) te werken en paginakopbal/footer en structuurcomponenten toe te laten om met de malplaatjedacteur worden samengesteld.

## Gebruik {#usage}

De paginacomponent vormt de basis van alle pagina&#39;s die zijn ontworpen met de kerncomponenten en bewerkbare sjablonen. Door de paginacomponent, kunnen de kopballen, footers, en de structuur van de pagina als malplaatje worden bepaald gebruikend de andere kerncomponenten.

In het [ontwerpdialoogvenster](#design-dialog)kunnen aangepaste clientbibliotheken voor de pagina worden gedefinieerd. In tegenstelling tot andere componenten met een bewerkingsdialoogvenster dat rechtstreeks vanuit de component toegankelijk is, omdat de component de pagina zelf is, is het dialoogvenster [](#edit-dialog) Bewerken van de paginacomponent het venster met pagina-eigenschappen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de paginacomponent is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de kerncomponenten en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|---|
| v2 | Compatibel | Compatibel | Compatibel | Compatibel |
| [v1](v1/page-v1.md) | Compatibel | Compatibel | Compatibel | - |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

>[!NOTE]
>
>Om omleiding op `cq:Page` niveau voor versie 2 van de paginacomponent en AEM 6.3 toe te laten, wordt de [dienstpak 2](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html) of later vereist. Een dergelijke omleiding was niet beschikbaar in eerdere releases.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Hier volgt een voorbeeld van [We.Retail](https://docs.adobe.com/content/help/en/experience-manager-65/developing/bestpractices/we-retail/we-retail.html).

### Schermafbeelding {#screenshot}

![](/help/assets/chlimage_1.png)

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Pagina [kan op GitHub](https://adobe.com/go/aem_cmp_tech_page_v2)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster Bewerken {#edit-dialog}

Omdat de component de gehele pagina vertegenwoordigt, worden instellingen die normaal gesproken in een bewerkingsdialoogvenster staan, gevonden in het venster [Pagina-eigenschappen](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) .

## Ontwerpdialoogvenster {#design-dialog}

Omdat de component de gehele pagina vertegenwoordigt, is het dialoogvenster Ontwerpen toegankelijk via **Pagina-informatie -> Paginabeleid** bij het bewerken van de paginasjabloon.

![](/help/assets/screen_shot_2018-04-03at113410.png)

>[!NOTE]
>
>In eerdere versies van AEM heette **Paginabeleid** **Paginaontwerp**.

### Tabblad Eigenschappen {#properties-tab}

Met behulp van het venster Paginaontwerp kunt u de te laden clientbibliotheken en de bibliotheek met webbronnen voor de pagina definiëren.

* **Clientbibliotheken** Hiermee worden de categorieën in de clientbibliotheek gedefinieerd die moeten worden geladen. JavaScript wordt toegevoegd aan het hoofdgedeelte en de CSS wordt toegevoegd aan de paginakop.
* **JavaScript-paginakop** van clientbibliothekenDit definieert de JavaScript-clientbibliotheekcategorieën die in de paginakop moeten worden geladen.
   * Voor de categorieën die hier worden gedefinieerd en die ook voorkomen in het veld **Clientbibliotheken** , wordt JavaScript geladen in de paginakop in plaats van aan het body-einde.
   * CSS wordt alleen geladen als de categorie ook aanwezig is in het veld **Clientbibliotheken** .

* **De Bibliotheek** van de Cliënt van Middelen van het Web de categorie van de cliëntbibliotheek die wordt gebruikt om Webmiddelen zoals favicons te dienen.

![](/help/assets/screenshot_2018-10-19at104949.png)

Bibliotheken kunnen als volgt worden geconfigureerd voor zowel de velden **Clientbibliotheken** als JavaScript-paginakoppen **van** Client-bibliotheken:

* Als u een nieuw veld wilt toevoegen, klikt u of tikt u op de knop **Toevoegen** onder de velden.
* Als u een veld wilt verwijderen, klikt of tikt u op het prullenbakpictogram naast het veld dat u wilt verwijderen.
* Als u de laadvolgorde wilt wijzigen, klikt of tikt u op de greep naast het te verplaatsen veld.

Voor meer informatie over het gebruiken van cliënt-zijbibliotheken zie het [Gebruiken van de Bibliotheken](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html)van de Kant van de Cliënt.

>[!CAUTION]
>
>De mogelijkheid om clientbibliotheken voor de paginakop afzonderlijk te definiëren, is geïntroduceerd met versie 2.2.0 van de kerncomponenten.

### Tabblad Stijlen {#styles-tab}

De component Page ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).
