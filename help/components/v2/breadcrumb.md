---
title: Breadcrumb-component (v2)
description: De component van de Breadcrumb van de Component van de Kern is een navigatiecomponent die een broodkruimel van verbindingen bouwt die op de plaats van de pagina in de inhoudshiërarchie wordt gebaseerd.
role: Architect, Developer, Admin, User
source-git-commit: f8aa86d58ba71ede3c3cd867c45aafff06923325
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---


# Breadcrumb-component (v2) {#breadcrumb-component}

De component van de Breadcrumb van de Component van de Kern is een navigatiecomponent die een broodkruimel van verbindingen bouwt die op de plaats van de pagina in de inhoudshiërarchie wordt gebaseerd.

## Gebruik {#usage}

De component Breadcrumb geeft de positie van de huidige pagina binnen de sitehiërarchie weer, zodat bezoekers van de pagina vanuit hun huidige locatie kunnen navigeren in de paginahiërarchie. Deze functie is vaak geïntegreerd in kop- en voetteksten van pagina&#39;s.

Beschikbare opties, zoals het standaardnavigatieniveau en de mogelijkheid om de huidige pagina of verborgen pagina&#39;s weer te geven, kunnen door de sjabloonauteur in het dialoogvenster [ontwerpdialoogvenster](#design-dialog). De inhoudeditor kan dan kiezen of verborgen pagina&#39;s wel of niet moeten worden weergegeven en het daadwerkelijke navigatieniveau voor de component in het dialoogvenster [dialoogvenster bewerken](#edit-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 2 van de Breadcrumb Component beschreven, die in januari 2018 is geïntroduceerd met release 2.0.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 2 van de component Breadcrumb beschreven.
>
>Voor meer informatie over de huidige versie van de component Breadcrumb raadpleegt u de [Broodkruimelcomponent](/help/components/breadcrumb.md) document.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de component Breadcrumb wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_breadcrumb).

>[!NOTE]
>
>Vanaf versie 2.1.0 van Core Components biedt de component Breadcrumb ondersteuning voor [schema.org-microgegevens](https://schema.org/BreadcrumbList).

## Technische details {#technical-details}

De meest recente technische documentatie over de Breadcrumb-component [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud verborgen en actieve pagina&#39;s in de broodkruimels onderdrukken, evenals de diepte in de hiërarchie die moet worden weergegeven.

![Dialoogvenster voor bewerken van component Breadcrumb](/help/assets/breadcrumb-edit.png)

* **Beginniveau navigatie** - Waar in de hiërarchie de breadcrumb-component naar beneden moet lopen naar de huidige pagina. Bijvoorbeeld:

   * 0 begint bij `/content`
   * 1 begint bij `/content/<yourSite>`
   * 2 begint bij `/content/<yourSite>/<country>`

* **Verborgen navigatie-items tonen** - Pagina&#39;s tonen die zijn gemarkeerd als verborgen in de broodkruimel (deze worden standaard niet weergegeven)
* **Huidige pagina verbergen** - Onderdruk de huidige pagina in de broodkruimel (door gebrek zal het worden getoond)
* **Schaduwen uitschakelen** - Als de pagina in de hiërarchie een omleiding is, wordt de naam van de omleidingspagina weergegeven in plaats van het doel. Zie de [Ondersteuning voor schaduwsitestructuur](../v1/navigation.md#shadow-structure) van de navigatiecomponent voor meer informatie.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren wat de standaardwaarden zijn voor de opties voor het onderdrukken van verborgen en actieve pagina&#39;s in de broodkruimels en de diepte in de hiërarchie die moet worden weergegeven.

### Hoofdtabblad {#main-tab}

![](/help/assets/breadcrumb-design.png)

* **Beginniveau navigatie** - Definieert de standaardwaarde voor de plaats in de hiërarchie waar de component breadcrumb omlaag moet gaan naar de huidige pagina wanneer de component breadcrumb aan een pagina wordt toegevoegd.
* **Verborgen navigatie-items tonen** - Definieert de standaardwaarde van de **Verborgen navigatie-items tonen** als de component breadcrumb aan een pagina wordt toegevoegd.

   * Hiermee wordt de optie voor de auteur niet in- of uitgeschakeld. Hiermee wordt alleen de standaardwaarde ingesteld.

* **Huidige pagina verbergen**- Definieert de standaardwaarde van de **Huidige pagina verbergen** als de component breadcrumb aan een pagina wordt toegevoegd.

   * Hiermee wordt de optie voor de auteur niet in- of uitgeschakeld. Hiermee wordt alleen de standaardwaarde ingesteld.

* **Schaduwen uitschakelen** - Definieert de standaardwaarde van de **Schaduwen uitschakelen** als de component breadcrumb aan een pagina wordt toegevoegd.

### Tabblad Stijlen {#styles-tab}

De component Breadcrumb ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component Breadcrumb ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
