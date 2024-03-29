---
title: Experience Fragment
description: Met de ervaringsfragmentcomponent kan de auteur van de inhoud een ervaringsfragmentvariatie aan een pagina toevoegen.
role: Architect, Developer, Admin, User
exl-id: 103f729a-084d-4b6a-a239-d8ef8902eb95
source-git-commit: 327c239b02e0aecee878784c918bfa98d960530e
workflow-type: tm+mt
source-wordcount: '893'
ht-degree: 1%

---

# Experience Fragment{#experience-fragment-component}

Met de Core Component Experience Fragment Component kan de auteur van de inhoud een ervaringsfragmentvariatie op een pagina plaatsen en een gelokaliseerde sitestructuur ondersteunen.

## Gebruik {#usage}

Met de Core Component Experience Fragment Component kan de auteur van de inhoud uit bestaande ervaringsfragmentvariaties selecteren en er een op de inhoudspagina plaatsen. De component Experience Fragment ondersteunt ook een gelokaliseerde sitestructuur.

* De eigenschappen van de component kunnen worden gedefinieerd in het dialoogvenster [dialoogvenster configureren](#configure-dialog).
* De standaardwaarden voor de component wanneer deze aan een pagina wordt toegevoegd, kunnen worden gedefinieerd in het dialoogvenster [ontwerpdialoogvenster](#design-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Experience Fragment Component is v2, die in februari 2022 werd geïntroduceerd met release 2.18.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v2 | - | Compatibel | Compatibel |
| [v1](v1/experience-fragment.md) | Compatibel | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Ondersteuning voor gelokaliseerde sitestructuur {#localized-site-structure}

De Experience Fragment Component is adaptief aan gelokaliseerde sitestructuren en geeft het juiste ervaringsfragment weer op basis van de lokalisatie van de pagina. Hiervoor moet het ervaringsfragment aan de volgende voorwaarden voldoen.

* De component Experience Fragment wordt toegevoegd aan een sjabloon.
* Die sjabloon wordt gebruikt om een nieuwe inhoudspagina te maken die deel uitmaakt van een onderstaande gelokaliseerde structuur `/content/<site>`.
* Het ervaringsfragment waarnaar op een inhoudspagina wordt verwezen, maakt deel uit van een onderstaande gelokaliseerde ervaringsfragmentstructuur `/content/experience-fragments` die dezelfde patronen volgt als de onderstaande site `/content/<site>` inclusief het gebruik van dezelfde componentnamen.

In dit geval wordt het fragment met dezelfde lokalisatie (taal, blauwdruk of live kopie) als de huidige pagina weergegeven als onderdeel van de sjabloon.

Dit gedrag is beperkt tot Geniet van fragmentcomponenten die aan sjablonen zijn toegevoegd. De Componenten van het Fragment van de ervaring die aan individuele inhoudspagina&#39;s worden toegevoegd zullen de nauwkeurige vertoningen van het ervaringsfragment teruggeven die binnen de component worden gevormd.

* Voor een voorbeeld van hoe de lokalisatiefuncties van de Component van het Fragment van de Ervaring werken, zie [het onderstaande gedeelte](#example).
* Voor een voorbeeld van hoe de lokalisatiefuncties van de Core Components samenwerken, raadpleegt u de [Localisatiefuncties van de pagina Core Components](/help/get-started/localization.md).

### Voorbeeld {#example}

Laten we zeggen dat uw inhoud er ongeveer als volgt uitziet:

```
/content
+-- experience-fragments
   \-- wknd
      +-- language-masters
      +-- us
         +-- en
            +-- footerTextXf
            \-- headerTextXf
         \-- es
            +-- footerTextXf
            \-- headerTextXf
      \-- ch
         +-- de
            +-- footerTextXf
            \-- headerTextXf
         +-- fr
            +-- footerTextXf
            \-- headerTextXf
         \-- it
            +-- footerTextXf
            \-- headerTextXf
+-- wknd
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

U ziet dat de onderstaande structuur `/content/experience-fragments/wknd` spiegelt de structuur van `/content/wknd`.

In dit geval, als de component van het Fragment van de Ervaring `/content/experience-fragments/wknd/us/en/footerTextXf` op een sjabloon wordt geplaatst, geven de gelokaliseerde pagina&#39;s die op basis van die sjabloon worden gemaakt automatisch het gelokaliseerde ervaringsfragment weer dat overeenkomt met de gelokaliseerde inhoudspagina.

Dus als u naar een inhoudspagina onder navigeert `/content/wknd/ch/de` die dezelfde sjabloon gebruiken, `/content/experience-fragments/wknd/ch/de/footerTextXf` wordt weergegeven in plaats van `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Fallback {#fallback}

De component van het Fragment van de Ervaring zal proberen om een overeenkomstige gelokaliseerde component in de volgende orde te vinden.

1. Eerst wordt geprobeerd een taalhoofdmap te vinden.
1. Als deze niet wordt gevonden, wordt geprobeerd een blauwdruk te vinden.
1. Als deze niet wordt gevonden, wordt geprobeerd een live kopie te zoeken.
1. Als deze optie niet wordt gevonden, wordt standaard het ervaringsfragment weergegeven dat in de component is geconfigureerd.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de Experience Fragment-component wilt ervaren en voorbeelden wilt zien van zijn configuratieopties en HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_xf).

## Technische details {#technical-details}

De meest recente technische documentatie over de component Experience Fragment [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_xf_v2).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud de variatie van het ervaringsfragment selecteren die op de pagina moet worden weergegeven.

![Het bewerkingsdialoogvenster van de fragmentcomponent beleven](/help/assets/experience-fragment-edit.png)

Gebruik de **Dialoogvenster Selectie openen** om de componentkiezer te openen en te kiezen welke fragmentcomponentvariatie u aan de inhoudspagina wilt toevoegen.

Als u de Component van het Fragment van de Ervaring aan een malplaatje toevoegt, merk op dat het automatisch zal worden gelokaliseerd op voorwaarde dat de Fragmenten van de Ervaring worden gelokaliseerd, zodat wat op de pagina wordt teruggegeven van de component kan variëren u uitdrukkelijk selecteert. [Zie het bovenstaande voorbeeld](#example) voor meer informatie .

U kunt ook een **ID**. Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).

* Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
* Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
* Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Stijlen {#styles-tab-edit}

![Stijlen, tabblad van het dialoogvenster Bewerken van Experience Fragment Component](/help/assets/experience-fragment-edit-styles.png)

De ervaringsfragmentcomponent ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in worden gevormd [ontwerpdialoogvenster](#design-dialog) zodat het vervolgkeuzemenu beschikbaar is.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de component Experience Fragment gebruikt en de standaardinstellingen die zijn ingesteld bij het plaatsen van de Experience Fragment-component.

### Tabblad Stijlen {#styles-tab}

De ervaringsfragmentcomponent ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
