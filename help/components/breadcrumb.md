---
title: Broodkruimelcomponent
description: De component van de Breadcrumb van de Component van de Kern is een navigatiecomponent die een broodkruimel van verbindingen bouwt die op de plaats van de pagina in de inhoudshiërarchie wordt gebaseerd.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Broodkruimelcomponent{#breadcrumb-component}

De component van de Breadcrumb van de Component van de Kern is een navigatiecomponent die een broodkruimel van verbindingen bouwt die op de plaats van de pagina in de inhoudshiërarchie wordt gebaseerd.

## Gebruik {#usage}

De component Breadcrumb geeft de positie van de huidige pagina binnen de sitehiërarchie weer, zodat bezoekers van de pagina vanuit hun huidige locatie kunnen navigeren in de paginahiërarchie. Deze functie is vaak geïntegreerd in kop- en voetteksten van pagina&#39;s.

Beschikbare opties, zoals het standaardnavigatieniveau en de mogelijkheid om de huidige pagina of verborgen pagina&#39;s weer te geven, kunnen door de sjabloonauteur in het [ontwerpdialoogvenster](#design-dialog)worden gedefinieerd. De inhoudseditor kan dan kiezen of verborgen pagina&#39;s wel of niet moeten worden weergegeven en het daadwerkelijke navigatieniveau voor de component in het dialoogvenster [](#edit-dialog)Bewerken.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Breadcrumb Component is v2, die in januari 2018 is geïntroduceerd met release 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatibel | Compatibel | Compatibel | Compatibel |
| [v1](v1/breadcrumb-v1.md) | Compatibel | Compatibel | Compatibel | - |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_breadcrumb)om de component Breadcrumb te ervaren en voorbeelden van de bijbehorende configuratieopties en de HTML- en JSON-uitvoer te zien.

>[!NOTE]
>
>Vanaf versie 2.1.0 van de Componenten van de Kern, steunt de Component Breadcrumb [schema.org microdata](https://schema.org/BreadcrumbList).

## Technische details {#technical-details}

De recentste technische documentatie over de Component Breadcrumb [kan op GitHub](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud verborgen en actieve pagina&#39;s in de broodkruimels onderdrukken, evenals de diepte in de hiërarchie die moet worden weergegeven.

![](/help/assets/screen_shot_2018-01-12at124250.png)

* **Beginniveau** navigatie - Waar in de hiërarchie moet de component breadcrumb omlaag gaan naar de huidige pagina. Bijvoorbeeld in We.Retail:

   * 0 begint bij `/content`
   * 1 begint bij `/content/we-retail`
   * 2 begint bij `/content/we-retail/<country>`

* **Verborgen navigatie-items** tonen - Pagina&#39;s tonen die zijn gemarkeerd als verborgen in de broodkruimel (deze worden standaard niet weergegeven)
* **Huidige pagina** verbergen - De huidige pagina in de broodkruimel onderdrukken (standaard wordt deze weergegeven)

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren wat de standaardwaarden zijn voor de opties voor het onderdrukken van verborgen en actieve pagina&#39;s in de broodkruimels en de diepte in de hiërarchie die moet worden weergegeven.

### Hoofdtabblad {#main-tab}

![](/help/assets/screen_shot_2018-01-12at124437.png)

* **Beginniveau** van navigatie - Definieert de standaardwaarde voor de positie in de hiërarchie waar de component breadcrumb naar beneden moet lopen naar de huidige pagina wanneer de component breadcrumb aan een pagina wordt toegevoegd.
* **Verborgen navigatie-items** tonen - Hiermee definieert u de standaardwaarde van de optie Verborgen navigatie-items **** weergeven wanneer de component breadcrumb aan een pagina wordt toegevoegd.

   * Hiermee wordt de optie voor de auteur niet in- of uitgeschakeld. Hiermee wordt alleen de standaardwaarde ingesteld.

* **Huidige pagina** verbergen - Hiermee wordt de standaardwaarde van de optie Huidige pagina **** verbergen gedefinieerd wanneer de component breadcrumb aan een pagina wordt toegevoegd.

   * Hiermee wordt de optie voor de auteur niet in- of uitgeschakeld. Hiermee wordt alleen de standaardwaarde ingesteld.

### Tabblad Stijlen {#styles-tab}

De component Breadcrumb ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).
