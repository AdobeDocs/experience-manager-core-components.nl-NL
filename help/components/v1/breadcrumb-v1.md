---
title: Breadcrumb-component (v1)
description: De component van de Breadcrumb van de Component van de Kern is een navigatiecomponent die een broodkruimel van verbindingen bouwt die op de plaats van de pagina in de inhoudshiërarchie wordt gebaseerd.
index: n
role: Architect, Developer, Admin, User
exl-id: 4845e649-033a-43a8-b5ee-892a3f2a8b98
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---


# Breadcrumb-component (v1) {#breadcrumb-component-v}

De component van de Breadcrumb van de Component van de Kern is een navigatiecomponent die een broodkruimel van verbindingen bouwt die op de plaats van de pagina in de inhoudshiërarchie wordt gebaseerd.

## Gebruik {#usage}

De component Breadcrumb geeft de positie van de huidige pagina binnen de sitehiërarchie weer, zodat bezoekers van de pagina vanuit hun huidige locatie kunnen navigeren in de paginahiërarchie. Deze functie is vaak geïntegreerd in kop- en voetteksten van pagina&#39;s.

De beschikbare opties zoals het standaardnavigatieniveau en de capaciteit om de huidige pagina of verborgen pagina&#39;s te tonen kunnen door de malplaatjeauteur in de [ ontwerpdialoog ](#design-dialog) worden bepaald. De inhoudsredacteur kan dan kiezen als de verborgen pagina&#39;s al dan niet zouden moeten worden getoond en het daadwerkelijke navigatieniveau voor de component in [ uitgeeft dialoog ](#edit-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Breadcrumb Component beschreven, die oorspronkelijk is geïntroduceerd met versie 1.0.0 van de Core Components with AEM 6.3.

In de volgende tabel wordt de compatibiliteit van v1 van de component Breadcrumb weergegeven.

| AEM-versie | Breadcrumb-component v1 |
|--- |--- |
| 6,3 | Compatibel |
| 6,4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Breadcrumb beschreven.
>&#x200B;>Voor details van de huidige versie van de Component Breadcrumb, zie het [&#128279;](/help/components/breadcrumb.md) document van de Component 0&rbrace; Breadcrumb.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende wordt steekproef genomen van [ We.Retail ](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Schermafbeelding {#screenshot}

![](/help/assets/chlimage_1-33.png)

### HTML {#html}

```
<div class="cmp cmp-breadcrumb aem-GridColumn aem-GridColumn--default--12">

<ol class="breadcrumb">
    <li class="breadcrumb-item ">
        <a href="/content/we-retail/us.html">
            United States
        </a>
    </li>

    <li class="breadcrumb-item ">
        <a href="/content/we-retail/us/en.html">
            English
        </a>
    </li>

    <li class="breadcrumb-item active">
        
            Experience
        
    </li>
</ol>
 
</div>
```

### JSON {#json}

```
"breadcrumb": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/breadcrumb"
            }
```

>[!NOTE]
>
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Gelieve te zien de [ verenigbaarheidsinformatie voor de Componenten van de Kern v1 ](/help/versions.md) voor meer informatie.

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud verborgen en actieve pagina&#39;s in de broodkruimels onderdrukken, evenals de diepte in de hiërarchie die moet worden weergegeven.

![](/help/assets/chlimage_1-34.png)

* **navigatie-Niveau om** te beginnen - waar in de hiërarchie de breadcrumb component zou moeten beginnen neer naar de huidige pagina te lopen. Bijvoorbeeld in We.Retail:

   * 1 begint bij `/content/we-retail`
   * 2 begint bij `/content/we-retail/<country>`

* **toon Verborgen** - toon pagina&#39;s duidelijk zoals verborgen in breadcrumb (door gebrek zullen zij niet worden getoond)
* **Verberg Huidige** - onderdruk de huidige pagina in breadcrumb (door gebrek zal het worden getoond)

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren wat de standaardwaarden zijn voor de opties voor het onderdrukken van verborgen en actieve pagina&#39;s in de broodkruimels en de diepte in de hiërarchie die moet worden weergegeven.

![](/help/assets/chlimage_1-35.png)

* **navigatie-Niveau om** te beginnen - bepaalt de standaardwaarde voor waar in de hiërarchie de breadcrumb component zou moeten beginnen neer naar de huidige pagina te lopen wanneer de breadcrumb component aan een pagina wordt toegevoegd.
* **toon Verborgen** - bepaalt de standaardwaarde van **toont Verborgen** optie wanneer de breadcrumb component aan een pagina wordt toegevoegd.

   * Hiermee wordt de optie voor de auteur niet in- of uitgeschakeld. Hiermee wordt alleen de standaardwaarde ingesteld.

* **Verberg Huidige** - bepaalt de standaardwaarde van de **Huidige** optie van de Verbergen wanneer de breadcrumb component aan een pagina wordt toegevoegd.

   * Hiermee wordt de optie voor de auteur niet in- of uitgeschakeld. Hiermee wordt alleen de standaardwaarde ingesteld.

## Technische details {#technical-details}

De recentste technische documentatie over de Component Breadcrumb [ kan op GitHub ](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v1/breadcrumb) worden gevonden.

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).
