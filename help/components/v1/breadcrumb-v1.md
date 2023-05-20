---
title: Breadcrumb-component (v1)
description: De component van de Breadcrumb van de Component van de Kern is een navigatiecomponent die een broodkruimel van verbindingen bouwt die op de plaats van de pagina in de inhoudshiërarchie wordt gebaseerd.
index: n
role: Architect, Developer, Admin, User
exl-id: 4845e649-033a-43a8-b5ee-892a3f2a8b98
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%

---

# Breadcrumb-component (v1) {#breadcrumb-component-v}

De component van de Breadcrumb van de Component van de Kern is een navigatiecomponent die een broodkruimel van verbindingen bouwt die op de plaats van de pagina in de inhoudshiërarchie wordt gebaseerd.

## Gebruik {#usage}

De component Breadcrumb geeft de positie van de huidige pagina binnen de sitehiërarchie weer, zodat bezoekers van de pagina vanuit hun huidige locatie kunnen navigeren in de paginahiërarchie. Deze functie is vaak geïntegreerd in kop- en voetteksten van pagina&#39;s.

Beschikbare opties, zoals het standaardnavigatieniveau en de mogelijkheid om de huidige pagina of verborgen pagina&#39;s weer te geven, kunnen door de sjabloonauteur in het dialoogvenster [ontwerpdialoogvenster](#design-dialog). De inhoudeditor kan dan kiezen of verborgen pagina&#39;s wel of niet moeten worden weergegeven en het daadwerkelijke navigatieniveau voor de component in het dialoogvenster [dialoogvenster bewerken](#edit-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Breadcrumb Component beschreven, die oorspronkelijk is geïntroduceerd met versie 1.0.0 van de Core Components met AEM 6.3.

In de volgende tabel wordt de compatibiliteit van v1 van de component Breadcrumb weergegeven.

| AEM | Breadcrumb-component v1 |
|--- |--- |
| 6.3 | Compatibel |
| 6.4 | Compatibel |

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Breadcrumb beschreven.
>Voor meer informatie over de huidige versie van de component Breadcrumb raadpleegt u de [Broodkruimelcomponent](/help/components/breadcrumb.md) document.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Het volgende monster wordt genomen uit [Wij.Detailhandel](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>Voor JSON-export van de Core Components is release 1.1.0 van de Core Components vereist. Zie de [compatibiliteitsinformatie voor Core Components v1](/help/versions.md) voor meer informatie .

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud verborgen en actieve pagina&#39;s in de broodkruimels onderdrukken, evenals de diepte in de hiërarchie die moet worden weergegeven.

![](/help/assets/chlimage_1-34.png)

* **Navigatieniveau om te starten** - Waar in de hiërarchie de breadcrumb-component naar beneden moet lopen naar de huidige pagina. Bijvoorbeeld in We.Retail:

   * 1 begint bij `/content/we-retail`
   * 2 begint bij `/content/we-retail/<country>`

* **Verborgen tonen** - Pagina&#39;s tonen die zijn gemarkeerd als verborgen in de broodkruimel (deze worden standaard niet weergegeven)
* **Huidige verbergen**- Onderdruk de huidige pagina in de broodkruimel (door gebrek zal het worden getoond)

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren wat de standaardwaarden zijn voor de opties voor het onderdrukken van verborgen en actieve pagina&#39;s in de broodkruimels en de diepte in de hiërarchie die moet worden weergegeven.

![](/help/assets/chlimage_1-35.png)

* **Navigatieniveau om te starten** - Definieert de standaardwaarde voor de plaats in de hiërarchie waar de component breadcrumb omlaag moet gaan naar de huidige pagina wanneer de component breadcrumb aan een pagina wordt toegevoegd.
* **Verborgen tonen** - Definieert de standaardwaarde van de **Verborgen tonen** als de component breadcrumb aan een pagina wordt toegevoegd.

   * Hiermee wordt de optie voor de auteur niet in- of uitgeschakeld. Hiermee wordt alleen de standaardwaarde ingesteld.

* **Huidige verbergen** - Definieert de standaardwaarde van de **Huidige verbergen** als de component breadcrumb aan een pagina wordt toegevoegd.

   * Hiermee wordt de optie voor de auteur niet in- of uitgeschakeld. Hiermee wordt alleen de standaardwaarde ingesteld.

## Technische details {#technical-details}

De meest recente technische documentatie over de Breadcrumb-component [kan op GitHub worden gevonden](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v1/breadcrumb).

Het volledige kerncomponentenproject kan van GitHub worden gedownload.

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).
