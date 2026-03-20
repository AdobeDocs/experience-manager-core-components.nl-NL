---
title: Front-end ontwikkeling met de Archetype van het Project van AEM
description: Meer informatie over het optionele, toegewijde front-end constructiemechanisme van de AEM Project Archetype op basis van Webpack.
feature: Core Components, AEM Project Archetype
role: Developer, Admin
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
source-git-commit: 7ba1374bd64686c2e7ac44398d77fb187ff60949
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---


# Front-end ontwikkeling met de Archetype van het Project van AEM {#front-end}

Het AEM Project Archetype bevat een optioneel, toegewijd mechanisme voor voorwaarts bouwen op basis van Webpack. De module ui.frontend wordt dus de centrale locatie voor alle front-end bronnen van het project, waaronder JavaScript- en CSS-bestanden. Om ten volle te kunnen profiteren van deze nuttige en flexibele functie, is het belangrijk te begrijpen hoe front-end ontwikkeling past in een AEM-project.

Dit document richt zich op algemene gebruikspatronen van de front-end bouwstijlmodule en wat het voor u doet. Voor gedetailleerde bouwstijlopties en technische instructies, te zien gelieve de documentatie in de bewaarplaats GitHub van archetype.

>[!TIP]
>
>Het recentste Archetype van het Project van AEM en bijbehorende technische documentatie [ kunnen op GitHub worden gevonden.](https://github.com/adobe/aem-project-archetype)

## AEM Front-End en Back-End Development {#front-end-back-end}

In sterk vereenvoudigde termen kunnen AEM-projecten worden beschouwd als bestaande uit twee afzonderlijke, maar verwante onderdelen:

* De ontwikkeling van het achterste deel die de logica van AEM drijft en Java bibliotheken, de diensten OSGi, enz. produceert
* Front-end ontwikkeling die de presentatie en het gedrag van de resulterende website drijft en JavaScript en CSS bibliotheken produceert

Omdat deze twee ontwikkelingsprocessen zich richten op verschillende delen van het project, kan de achterkant en front-end ontwikkeling parallel plaatsvinden.

![ front-end werkschemadiagram ](/help/assets/front-end-flow.png)

Voor elk project moet echter gebruik worden gemaakt van de resultaten van beide ontwikkelingsinspanningen, d.w.z. zowel back-end als front-end.

## De markering bepalen {#determining-markup}

Welke ontwikkelworkflow op de voorgrond u ook wilt implementeren voor uw project, de back-end ontwikkelaars en front-end ontwikkelaars moeten het eerst eens worden over de markering. AEM definieert doorgaans de opmaak, die wordt geleverd door de kerncomponenten. [Nochtans kan dit indien nodig worden aangepast.](/help/developing/customizing.md#customizing-the-markup)

## Mogelijke front-end ontwikkelingsworkflows {#possible-workflows}

De bouwstijlmodule aan de voorzijde is een nuttig en zeer flexibel instrument, maar stelt geen specifieke mening over hoe deze moet worden gebruikt. Het volgende is twee voorbeelden van *mogelijk* gebruik, maar uw individuele projectbehoeften kunnen andere gebruiksmodellen dicteren.

### Statische ontwikkelingsserver van Webpack gebruiken {#using-webpack}

Met Webpack kunt u stijl en ontwikkeling toepassen op basis van statische uitvoer van AEM-webpagina&#39;s in de module ui.frontend.

1. Voorvertoning van pagina weergeven in AEM met de modus Voorvertoning van pagina of door te geven in `wcmmode=disabled` in de URL
1. Paginabron weergeven en opslaan als statische HTML in de module ui.frontend
1. [ Webpack van het Begin ](#webpack-dev-server) en begin het stileren en het produceren van noodzakelijke JavaScript en CSS
1. Voer `npm run dev` uit om de clientlibs te genereren

In deze flow kan een AEM-ontwikkelaar stappen 1 en 2 uitvoeren en de statische HTML aan de front-end ontwikkelaar doorgeven die zich ontwikkelt op basis van de AEM HTML-uitvoer.

>[!TIP]
>
>Één kon ook hefboomwerking de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library) om steekproeven van de prijsverhogingsoutput van elke component te vangen om op het componentenniveau eerder dan het paginaniveau te werken.

### Winybook gebruiken {#using-storybook}

Gebruikend [ Storybook ](https://storybook.js.org) kunt u meer atomische front-end ontwikkeling uitvoeren. Hoewel Storybook niet is opgenomen in het AEM Project Archetype, kunt u het installeren en je Storybook-artefacten opslaan in de module ui.frontend. Als ze klaar zijn om te worden getest in AEM, kunnen ze worden geïmplementeerd als clientlibs door `npm run dev` uit te voeren.

>[!NOTE]
>
>[ Storybook ](https://storybook.js.org) is niet inbegrepen in het Archetype van het Project van AEM. Als u ervoor kiest om het te gebruiken, moet u het afzonderlijk installeren.

## Clientlibs-overzicht {#clientlibs}

De frontend module wordt ter beschikking gesteld gebruikend een [ AEM clientlib.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html). Wanneer het NPM-constructiescript wordt uitgevoerd, wordt de app gemaakt en wordt het `aem-clientlib-generator` -pakket de resulterende samengestelde uitvoer verwerkt en in een dergelijke client getransformeerd.

Een clientlib bestaat uit de volgende bestanden en mappen:

* `css/`: CSS-bestanden die kunnen worden aangevraagd in de HTML
* `css.txt`: geeft AEM de volgorde en namen van bestanden in `css/` weer, zodat ze kunnen worden samengevoegd
* `js/`: JavaScript-bestanden die kunnen worden aangevraagd in de HTML
* `js.txt` Geeft aan AEM de volgorde en namen van bestanden in `js/` zodat deze kunnen worden samengevoegd
* `resources/`: Source maps, non-entrypoint code chunks (resulterend uit code splitting), statische elementen (bijvoorbeeld pictogrammen), enz.

>[!TIP]
>
>Leer meer over hoe AEM clientlibs in de [ de ontwikkelingsdocumentatie van AEM ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html) behandelt hoe te om hen in de [ documentatie van de Componenten van de Kern te omvatten.](/help/developing/including-clientlibs.md)
