---
title: Breadcrumb-component (v2)
description: De component van de Breadcrumb van de Component van de Kern is een navigatiecomponent die een broodkruimel van verbindingen bouwt die op de plaats van de pagina in de inhoudshiërarchie wordt gebaseerd.
role: Architect, Developer, Admin, User
exl-id: 5f2e6fef-e2f6-48e2-8dac-008db3131044
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---


# Breadcrumb-component (v2) {#breadcrumb-component}

De component van de Breadcrumb van de Component van de Kern is een navigatiecomponent die een broodkruimel van verbindingen bouwt die op de plaats van de pagina in de inhoudshiërarchie wordt gebaseerd.

## Gebruik {#usage}

De component Breadcrumb geeft de positie van de huidige pagina binnen de sitehiërarchie weer, zodat bezoekers van de pagina vanuit hun huidige locatie kunnen navigeren in de paginahiërarchie. Deze functie is vaak geïntegreerd in kop- en voetteksten van pagina&#39;s.

De beschikbare opties, zoals het standaardnavigatieniveau en de capaciteit om de huidige pagina of verborgen pagina&#39;s te tonen, kunnen door de malplaatjeauteur in de [&#x200B; ontwerpdialoog &#x200B;](#design-dialog) worden bepaald. De inhoudsredacteur kan dan kiezen als de verborgen pagina&#39;s al dan niet zouden moeten worden getoond en het daadwerkelijke navigatieniveau voor de component in [&#x200B; uitgeeft dialoog &#x200B;](#edit-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 2 van de Breadcrumb Component beschreven, die in januari 2018 is geïntroduceerd met release 2.0.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 2 van de component Breadcrumb beschreven.
>
>Voor details van de huidige versie van de Component Breadcrumb, zie het [&#128279;](/help/components/breadcrumb.md) document van de Component 0&rbrace; Breadcrumb.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van Breadcrumb te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [&#x200B; Bibliotheek van de Component &#x200B;](https://adobe.com/go/aem_cmp_library_breadcrumb).

>[!NOTE]
>
>Vanaf versie 2.1.0 van de Componenten van de Kern, steunt de Component Breadcrumb [&#x200B; schema.org microdata &#x200B;](https://schema.org/BreadcrumbList).

## Technische details {#technical-details}

De recentste technische documentatie over de Component Breadcrumb [&#x200B; kan op GitHub &#x200B;](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [&#x200B; de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden &#x200B;](/help/developing/overview.md).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud verborgen en actieve pagina&#39;s in de broodkruimels onderdrukken, evenals de diepte in de hiërarchie die moet worden weergegeven.

![&#x200B; de component Breadcrumb geeft dialoog uit &#x200B;](/help/assets/breadcrumb-edit.png)

* **Niveau van het Begin van de Navigatie** - waar in de hiërarchie de breadcrumb component zou moeten beginnen neer naar de huidige pagina te lopen. Bijvoorbeeld:

   * 0 begint bij `/content`
   * 1 begint bij `/content/<yourSite>`
   * 2 begint bij `/content/<yourSite>/<country>`

* **toon verborgen navigatiepunten** - toon pagina&#39;s duidelijk zoals verborgen in breadcrumb (door gebrek zullen zij niet worden getoond)
* **Verberg huidige pagina** - onderdruk de huidige pagina in breadcrumb (door gebrek zal het worden getoond)
* **maak schaduw** onbruikbaar - als de pagina in de hiërarchie een omleiding is, zal de naam van de het omleiden pagina in plaats van het doel worden getoond. Zie de [&#x200B; Steun van de Structuur van de Plaats van de Schaduw &#x200B;](../v1/navigation.md#shadow-structure) van de Component van de Navigatie voor meer informatie.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [&#x200B; Laag van Gegevens te controleren &#x200B;](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren wat de standaardwaarden zijn voor de opties voor het onderdrukken van verborgen en actieve pagina&#39;s in de broodkruimels en de diepte in de hiërarchie die moet worden weergegeven.

### Hoofdtabblad {#main-tab}

![](/help/assets/breadcrumb-design.png)

* **het Niveau van het Begin van de Navigatie** - bepaalt de standaardwaarde voor waar in de hiërarchie de breadcrumb component zou moeten beginnen neer naar de huidige pagina te lopen wanneer de breadcrumb component aan een pagina wordt toegevoegd.
* **toon verborgen navigatiepunten** - bepaalt de standaardwaarde van **toont verborgen navigatiepunten** optie wanneer de broodkruimelcomponent aan een pagina wordt toegevoegd.

   * Hiermee wordt de optie voor de auteur niet in- of uitgeschakeld. Hiermee wordt alleen de standaardwaarde ingesteld.

* **Verberg huidige pagina** - bepaalt de standaardwaarde van de **Verberg huidige pagina** optie wanneer de breadcrumb component aan een pagina wordt toegevoegd.

   * Hiermee wordt de optie voor de auteur niet in- of uitgeschakeld. Hiermee wordt alleen de standaardwaarde ingesteld.

* **maak het schaduwen** onbruikbaar - bepaalt de standaardwaarde van **schaduwen** optie onbruikbaar wanneer de breadcrumb component aan een pagina wordt toegevoegd.

### Tabblad Stijlen {#styles-tab}

De component Breadcrumb steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De component Breadcrumb steunt de [&#x200B; Gegevens van de Cliënt van Adobe Laag.](/help/developing/data-layer/overview.md)
