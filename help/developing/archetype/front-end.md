---
title: Front-end ontwikkeling met het AEM Project Archetype
description: Meer informatie over het optionele, toegewijde front-end constructiemechanisme van de AEM Project Archetype op basis van Webpack.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
source-git-commit: bd92a5d1884056ca7b44ea28e5817d8bde10a4d9
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---


# Front-end ontwikkeling met het AEM Project Archetype {#front-end}

Het AEM Project Archetype omvat een facultatief, specifiek front-end bouwstijlmechanisme dat op Webpack wordt gebaseerd. De module ui.frontend wordt dus de centrale locatie voor alle front-end bronnen van het project, waaronder JavaScript- en CSS-bestanden. Om volledig gebruik te maken van deze nuttige en flexibele functie, is het belangrijk om te begrijpen hoe front-end ontwikkeling past in een AEM project.

Dit document richt zich op algemene gebruikspatronen van de front-end bouwstijlmodule en wat het voor u doet. Voor gedetailleerde bouwstijlopties en technische instructies, te zien gelieve de documentatie in de bewaarplaats GitHub van archetype.

>[!TIP]
>
>Het recentste AEM Archetype van het Project en bijbehorende technische documentatie [ kunnen op GitHub worden gevonden.](https://github.com/adobe/aem-project-archetype)

## AEM front-end en back-end ontwikkeling {#front-end-back-end}

In sterk vereenvoudigde termen kunnen AEM projecten worden beschouwd als bestaande uit twee afzonderlijke maar verwante delen:

* De ontwikkeling van het achterste deel die de logica van AEM drijft en Java bibliotheken, de diensten OSGi, enz. produceert
* Front-end ontwikkeling die de presentatie en het gedrag van de resulterende website drijft en JavaScript en CSS bibliotheken produceert

Omdat deze twee ontwikkelingsprocessen zich richten op verschillende delen van het project, kan de achterkant en front-end ontwikkeling parallel plaatsvinden.

![ front-end werkschemadiagram ](/help/assets/front-end-flow.png)

Voor elk project moet echter gebruik worden gemaakt van de resultaten van beide ontwikkelingsinspanningen, d.w.z. zowel back-end als front-end.

## De markering bepalen {#determining-markup}

Welke ontwikkelworkflow op de voorgrond u ook wilt implementeren voor uw project, de back-end ontwikkelaars en front-end ontwikkelaars moeten het eerst eens worden over de markering. AEM definieert doorgaans de markering, die wordt geleverd door de kerncomponenten. [ Nochtans kan dit indien nodig worden aangepast.](/help/developing/customizing.md#customizing-the-markup)

## Mogelijke front-end ontwikkelingsworkflows {#possible-workflows}

De bouwstijlmodule aan de voorzijde is een nuttig en zeer flexibel instrument, maar stelt geen specifieke mening over hoe deze moet worden gebruikt. Het volgende is twee voorbeelden van *mogelijk* gebruik, maar uw individuele projectbehoeften kunnen andere gebruiksmodellen dicteren.

### Statische ontwikkelingsserver van Webpack gebruiken {#using-webpack}

Met Webpack kunt u stijl en ontwikkeling toepassen op basis van de statische uitvoer van AEM webpagina&#39;s in de module ui.frontend.

1. Pagina voorvertonen in AEM met de modus Voorvertoning van pagina of doorgeven in `wcmmode=disabled` in de URL
1. De paginabron van de mening en sparen als statische HTML binnen de module ui.frontend
1. [ Webpack van het Begin ](#webpack-dev-server) en begin het stileren en het produceren van noodzakelijke JavaScript en CSS
1. Voer `npm run dev` uit om de clientlibs te genereren

In deze stroom, kan een AEM ontwikkelaar stappen één en twee uitvoeren en statische HTML van de tot de front-end ontwikkelaar overgaan die zich op de output van AEM HTML baseert.

>[!TIP]
>
>Één kon ook hefboomwerking de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library) om steekproeven van de prijsverhogingsoutput van elke component te vangen om op het componentenniveau eerder dan het paginaniveau te werken.

### Winybook gebruiken {#using-storybook}

Gebruikend [ Storybook ](https://storybook.js.org) kunt u meer atomische front-end ontwikkeling uitvoeren. Hoewel Storybook niet is opgenomen in het AEM Project Archetype, kunt u het installeren en uw objecten uit het Storybook opslaan in de module ui.frontend. Als ze klaar zijn om te worden getest binnen AEM, kunnen ze worden geïmplementeerd als clientlibs door `npm run dev` uit te voeren.

>[!NOTE]
>
>[ Storybook ](https://storybook.js.org) is niet inbegrepen in het AEM Archetype van het Project. Als u ervoor kiest om het te gebruiken, moet u het afzonderlijk installeren.

## Clientlibs-overzicht {#clientlibs}

De frontend module wordt ter beschikking gesteld gebruikend [AEM clientlib.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html). Wanneer het NPM-constructiescript wordt uitgevoerd, wordt de app gemaakt en wordt het `aem-clientlib-generator` -pakket de resulterende samengestelde uitvoer verwerkt en in een dergelijke client getransformeerd.

Een clientlib bestaat uit de volgende bestanden en mappen:

* `css/`: CSS-bestanden die kunnen worden opgevraagd in de HTML
* `css.txt`: hiermee AEM u de volgorde en namen van bestanden in `css/` zodat ze kunnen worden samengevoegd
* `js/`: JavaScript-bestanden die kunnen worden opgevraagd in de HTML
* `js.txt` Hiermee worden de volgorde en namen van bestanden in `js/` AEM zodat ze kunnen worden samengevoegd
* `resources/`: Source maps, non-entrypoint code chunks (resulterend uit code splitting), statische elementen (bijvoorbeeld pictogrammen), enz.

>[!TIP]
>
>Leer meer over hoe AEM clientlibs in de [ AEM ontwikkelingsdocumentatie ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html) hoe te om hen in de [ documentatie van de Componenten van de Kern te omvatten.](/help/developing/including-clientlibs.md)
