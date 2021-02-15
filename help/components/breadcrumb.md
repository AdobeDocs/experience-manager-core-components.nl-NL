---
title: Broodkruimelcomponent
description: De component van de Breadcrumb van de Component van de Kern is een navigatiecomponent die een broodkruimel van verbindingen bouwt die op de plaats van de pagina in de inhoudshiërarchie wordt gebaseerd.
translation-type: tm+mt
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 1%

---


# Broodkruimelcomponent{#breadcrumb-component}

De component van de Breadcrumb van de Component van de Kern is een navigatiecomponent die een broodkruimel van verbindingen bouwt die op de plaats van de pagina in de inhoudshiërarchie wordt gebaseerd.

## Gebruik {#usage}

De component Breadcrumb geeft de positie van de huidige pagina binnen de sitehiërarchie weer, zodat bezoekers van de pagina vanuit hun huidige locatie kunnen navigeren in de paginahiërarchie. Deze functie is vaak geïntegreerd in kop- en voetteksten van pagina&#39;s.

Beschikbare opties, zoals het standaardnavigatieniveau en de mogelijkheid om de huidige pagina of verborgen pagina&#39;s weer te geven, kunnen worden gedefinieerd door de sjabloonauteur in het dialoogvenster [ontwerp](#design-dialog). De inhoudeditor kan dan kiezen of verborgen pagina&#39;s wel of niet moeten worden weergegeven en het daadwerkelijke navigatieniveau voor de component in het dialoogvenster [bewerken.](#edit-dialog)

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Breadcrumb Component is v2, die in januari 2018 is geïntroduceerd met release 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- | --- |--- |---|
| v2 | Compatibel | Compatibel | Compatibel |
| [v1](v1/breadcrumb-v1.md) | Compatibel | Compatibel | - |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_breadcrumb) om de component Breadcrumb te bekijken en voorbeelden van de configuratieopties en de HTML- en JSON-uitvoer te bekijken.

>[!NOTE]
>
>Vanaf versie 2.1.0 van de Componenten van de Kern, steunt de Component Breadcrumb [schema.org microdata](https://schema.org/BreadcrumbList).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van Breadcrumb [kan op GitHub](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster {#edit-dialog} bewerken

In het dialoogvenster Bewerken kan de auteur van de inhoud verborgen en actieve pagina&#39;s in de broodkruimels onderdrukken, evenals de diepte in de hiërarchie die moet worden weergegeven.

![Dialoogvenster voor bewerken van component Breadcrumb](/help/assets/breadcrumb-edit.png)

* **Beginniveau**  navigatie - Waar in de hiërarchie moet de component breadcrumb omlaag gaan naar de huidige pagina. Bijvoorbeeld:

   * 0 begint bij `/content`
   * 1 begint bij `/content/<yourSite>`
   * 2 begint bij `/content/<yourSite>/<country>`

* **Verborgen navigatie-items**  tonen - Pagina&#39;s tonen die zijn gemarkeerd als verborgen in de broodkruimel (deze worden standaard niet weergegeven)
* **Huidige pagina**  verbergen - De huidige pagina in de broodkruimel onderdrukken (standaard wordt deze weergegeven)
* **Schaduwen**  uitschakelen - Als de pagina in de hiërarchie een omleiding is, wordt de naam van de omleidingspagina weergegeven in plaats van het doel. Zie [Ondersteuning voor schaduwsitestructuur](navigation.md#shadow-structure) van de navigatiecomponent voor meer informatie.
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren wat de standaardwaarden zijn voor de opties voor het onderdrukken van verborgen en actieve pagina&#39;s in de broodkruimels en de diepte in de hiërarchie die moet worden weergegeven.

### Hoofdtabblad {#main-tab}

![](/help/assets/breadcrumb-design.png)

* **Beginniveau**  navigatie - Hiermee wordt de standaardwaarde gedefinieerd waarvoor de component breadcrumb in de hiërarchie naar de huidige pagina moet gaan wanneer de component breadcrumb aan een pagina wordt toegevoegd.
* **Verborgen navigatie-items**  tonen - Hiermee definieert u de standaardwaarde van de optie Verborgen navigatiepunten  **tonen** wanneer de component breadcrumb aan een pagina wordt toegevoegd.

   * Hiermee wordt de optie voor de auteur niet in- of uitgeschakeld. Hiermee wordt alleen de standaardwaarde ingesteld.

* **Huidige pagina** verbergen - Definieert de standaardwaarde van de optie Huidige pagina  **verbergen** wanneer de component breadcrumb aan een pagina wordt toegevoegd.

   * Hiermee wordt de optie voor de auteur niet in- of uitgeschakeld. Hiermee wordt alleen de standaardwaarde ingesteld.

* **Schaduwen**  uitschakelen - Hiermee definieert u de standaardwaarde van de optie  **Schaduwen** uitschakelen wanneer de component breadcrumb aan een pagina wordt toegevoegd.

### Tabblad Stijlen {#styles-tab}

De component Breadcrumb ondersteunt het AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Adobe-gegevenslaag client {#data-layer}

De component Breadcrumb ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
