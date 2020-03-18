---
title: Experience Fragment
description: Met de ervaringsfragmentcomponent kan de auteur van de inhoud een ervaringsfragmentvariatie aan een pagina toevoegen.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Experience Fragment{#experience-fragment-component}

Met de Core Component Experience Fragment Component kan de auteur van de inhoud een ervaringsfragmentvariatie op een pagina plaatsen en een gelokaliseerde sitestructuur ondersteunen.

## Gebruik {#usage}

Met de Core Component Experience Fragment Component kan de auteur van de inhoud uit bestaande ervaringsfragmentvariaties selecteren en er een op de inhoudspagina plaatsen. De component Experience Fragment ondersteunt ook een gelokaliseerde sitestructuur.

* De eigenschappen van de component kunnen in [vormen dialoog](#configure-dialog)worden bepaald.
* De standaardwaarden voor de component wanneer het toevoegen van het aan een pagina kunnen in de [ontwerpdialoog](#design-dialog)worden bepaald.

## Ondersteuning voor gelokaliseerde sitestructuur {#localized-site-structure}

De Experience Fragment Component is adaptief aan gelokaliseerde sitestructuren en geeft het juiste ervaringsfragment weer op basis van de lokalisatie van de pagina. Hiervoor moet het ervaringsfragment aan de volgende voorwaarden voldoen.

* De component Experience Fragment wordt toegevoegd aan een sjabloon.
* Die sjabloon wordt gebruikt om een nieuwe inhoudspagina te maken die deel uitmaakt van een onderstaande gelokaliseerde structuur `/content/<site>`.
* Het ervaringsfragment waarnaar op een inhoudspagina wordt verwezen, maakt deel uit van een onderstaande gelokaliseerde ervaringsfragmentstructuur `/content/experience-fragments` die dezelfde patronen volgt als de onderstaande site, `/content/<site>` inclusief het gebruik van dezelfde componentnamen.

In dit geval wordt het fragment met dezelfde lokalisatie (taal, blauwdruk of live kopie) als de huidige pagina weergegeven als onderdeel van de sjabloon.

Dit gedrag is beperkt tot Geniet van fragmentcomponenten die aan sjablonen zijn toegevoegd. De Componenten van het Fragment van de ervaring die aan individuele inhoudspagina&#39;s worden toegevoegd zullen de nauwkeurige vertoningen van het ervaringsfragment teruggeven die binnen de component worden gevormd.

* Zie [de onderstaande](#example)sectie voor een voorbeeld van de werking van de lokalisatiefuncties van de Experience Fragment Component.
* Zie de [lokalisatiefuncties van de pagina](/help/get-started/localization.md)Core Components voor een voorbeeld van hoe de lokalisatiefuncties van de Core Components samenwerken.

### Voorbeeld {#example}

Laten we zeggen dat uw inhoud er ongeveer als volgt uitziet:

```
/content
+-- experience-fragments
   \-- we-retail
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
+-- we-retail
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

De structuur hieronder `/content/experience-fragments/we-retail` spiegelt de structuur van `/content/we-retail`.

In dit geval, als de component van het Fragment van de Ervaring op een malplaatje `/content/experience-fragments/we-retail/us/en/footerTextXf` wordt geplaatst, zullen de gelokaliseerde pagina&#39;s die op dat malplaatje worden gecreeerd automatisch het gelokaliseerde ervaringsfragment teruggeven dat aan de gelokaliseerde inhoudspagina beantwoordt.

Als u dus naar een inhoudspagina navigeert onder `/content/we-retail/ch/de` die dezelfde sjabloon gebruikt, `/content/experience-fragments/we-retail/ch/de/footerTextXf` wordt deze weergegeven in plaats van `/content/experience-fragments/we-retail/us/en/footerTextXf`.

### Fallback {#fallback}

De component van het Fragment van de Ervaring zal proberen om een overeenkomstige gelokaliseerde component in de volgende orde te vinden.

1. Eerst wordt geprobeerd een taalhoofdmap te vinden.
1. Als deze niet wordt gevonden, wordt geprobeerd een blauwdruk te vinden.
1. Als deze niet wordt gevonden, wordt geprobeerd een live kopie te zoeken.
1. Als deze optie niet wordt gevonden, wordt standaard het ervaringsfragment weergegeven dat in de component is geconfigureerd.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Experience Fragment Component is v1, die in september 2019 is geïntroduceerd met release 2.6.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v1 | Compatibel | Compatibel | Compatibel | Compatibel |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_xf)om de Experience Fragment-component te bekijken en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van het Fragment van de Ervaring [kan op GitHub](https://adobe.com/go/aem_cmp_tech_xf_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud de variatie van het ervaringsfragment selecteren die op de pagina moet worden weergegeven.

![](/help/assets/screen-shot-2019-08-23-10.49.21.png)

Gebruik de knop Dialoogvenster **Selectie** openen om de componentkiezer te openen en te kiezen welke fragmentcomponentvariatie u aan de inhoudspagina wilt toevoegen.

Als u de Component van het Fragment van de Ervaring aan een malplaatje toevoegt, merk op dat het automatisch zal worden gelokaliseerd op voorwaarde dat de Fragmenten van de Ervaring worden gelokaliseerd, zodat wat op de pagina wordt teruggegeven van de component kan variëren u uitdrukkelijk selecteert. [Zie het bovenstaande](#example) voorbeeld voor meer informatie.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de component Experience Fragment gebruikt en de standaardinstellingen die zijn ingesteld bij het plaatsen van de Experience Fragment-component.

![](/help/assets/screen-shot-2019-08-23-10.48.36.png)

De component Experience Fragment ondersteunt het AEM [Style System](/help/get-started/authoring.md#component-styling).
