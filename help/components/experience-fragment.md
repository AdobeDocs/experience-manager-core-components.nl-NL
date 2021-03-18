---
title: Experience Fragment
description: Met de ervaringsfragmentcomponent kan de auteur van de inhoud een ervaringsfragmentvariatie aan een pagina toevoegen.
role: Architect, ontwikkelaar, beheerder, praktijkgerichte
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---


# De Component van het Fragment van de ervaring{#experience-fragment-component}

Met de Core Component Experience Fragment Component kan de auteur van de inhoud een ervaringsfragmentvariatie op een pagina plaatsen en een gelokaliseerde sitestructuur ondersteunen.

## Gebruik {#usage}

Met de Core Component Experience Fragment Component kan de auteur van de inhoud uit bestaande ervaringsfragmentvariaties selecteren en er een op de inhoudspagina plaatsen. De component Experience Fragment ondersteunt ook een gelokaliseerde sitestructuur.

* De eigenschappen van de component kunnen worden bepaald in [vorm dialoog](#configure-dialog).
* De standaardwaarden voor de component wanneer het toevoegen van het aan een pagina kunnen in [ontwerpdialoog](#design-dialog) worden bepaald.

## Ondersteuning voor gelokaliseerde sitestructuur {#localized-site-structure}

De Experience Fragment Component is adaptief aan gelokaliseerde sitestructuren en geeft het juiste ervaringsfragment weer op basis van de lokalisatie van de pagina. Hiervoor moet het ervaringsfragment aan de volgende voorwaarden voldoen.

* De component Experience Fragment wordt toegevoegd aan een sjabloon.
* Die sjabloon wordt gebruikt om een nieuwe inhoudspagina te maken die deel uitmaakt van een gelokaliseerde structuur onder `/content/<site>`.
* Het ervaringsfragment waarnaar op een inhoudspagina wordt verwezen, maakt deel uit van een gelokaliseerde ervaringsfragmentstructuur onder `/content/experience-fragments` die dezelfde patronen volgt als de site onder `/content/<site>` inclusief het gebruik van dezelfde componentnamen.

In dit geval wordt het fragment met dezelfde lokalisatie (taal, blauwdruk of live kopie) als de huidige pagina weergegeven als onderdeel van de sjabloon.

Dit gedrag is beperkt tot Geniet van fragmentcomponenten die aan sjablonen zijn toegevoegd. De Componenten van het Fragment van de ervaring die aan individuele inhoudspagina&#39;s worden toegevoegd zullen de nauwkeurige vertoningen van het ervaringsfragment teruggeven die binnen de component worden gevormd.

* Zie [de sectie hieronder](#example) voor een voorbeeld van de werking van de lokalisatiefuncties van de Experience Fragment Component.
* Voor een voorbeeld van hoe de localisatiefuncties van de Componenten van de Kern samenwerken, zie [Localisatiefuncties van de pagina van de Componenten van de Kern](/help/get-started/localization.md).

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

De structuur hieronder `/content/experience-fragments/wknd` spiegelt de structuur van `/content/wknd`.

In dit geval, als de component van het Fragment van de Ervaring `/content/experience-fragments/wknd/us/en/footerTextXf` op een malplaatje wordt geplaatst, zullen de gelokaliseerde pagina&#39;s die op dat malplaatje worden gecreeerd automatisch het gelokaliseerde ervaringsfragment teruggeven dat aan de gelokaliseerde inhoudspagina beantwoordt.

Als u dus naar een inhoudspagina navigeert onder `/content/wknd/ch/de` die dezelfde sjabloon gebruikt, wordt `/content/experience-fragments/wknd/ch/de/footerTextXf` weergegeven in plaats van `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Terugvalfunctie {#fallback}

De component van het Fragment van de Ervaring zal proberen om een overeenkomstige gelokaliseerde component in de volgende orde te vinden.

1. Eerst wordt geprobeerd een taalhoofdmap te vinden.
1. Als deze niet wordt gevonden, wordt geprobeerd een blauwdruk te vinden.
1. Als deze niet wordt gevonden, wordt geprobeerd een live kopie te zoeken.
1. Als deze optie niet wordt gevonden, wordt standaard het ervaringsfragment weergegeven dat in de component is geconfigureerd.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Experience Fragment Component is v1, die in september 2019 is geïntroduceerd met release 2.6.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_xf) om de Experience Fragment Component te bekijken en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van het Fragment van de Ervaring [kan op GitHub](https://adobe.com/go/aem_cmp_tech_xf_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster {#configure-dialog} configureren

In het dialoogvenster Configureren kan de auteur van de inhoud de variatie van het ervaringsfragment selecteren die op de pagina moet worden weergegeven.

![Het bewerkingsdialoogvenster van de fragmentcomponent beleven](/help/assets/experience-fragment-edit.png)

Met de knop **Dialoogvenster Selectie openen** opent u de componentkiezer en kiest u welke ervaring met de fragmentcomponentvariatie u wilt toevoegen aan de inhoudspagina.

Als u de Component van het Fragment van de Ervaring aan een malplaatje toevoegt, merk op dat het automatisch zal worden gelokaliseerd op voorwaarde dat de Fragmenten van de Ervaring worden gelokaliseerd, zodat wat op de pagina wordt teruggegeven van de component kan variëren u uitdrukkelijk selecteert. [Zie het voorbeeld ](#example) hierboven voor meer informatie.

U kunt ook een **ID** definiëren. Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).

* Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
* Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
* Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de component Experience Fragment gebruikt en de standaardinstellingen die zijn ingesteld bij het plaatsen van de Experience Fragment-component.

### Tabblad Stijlen {#styles-tab}

De component van het Fragment van de Ervaring steunt het AEM [Systeem van de Stijl](/help/get-started/authoring.md#component-styling).
