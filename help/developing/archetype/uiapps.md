---
title: ui.apps Module van het Archetype van het AEM Project
description: ui.apps Module van het Archetype van het AEM Project
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: fc63a19a-3253-44ee-96e2-bb5544c2235b
source-git-commit: 19bceb1d8ba07c70798f2e7203db957d3e8b3d03
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---

# ui.apps Module van het Archetype van het AEM Project {#uiapps-module}

De module ui.apps gemaakt (`<src-directory>/<project>/ui.apps`) bevat alle renderingcode die nodig is voor de onderliggende site `/apps`. Dit omvat CSS/JS die in een AEM genoemd formaat zal worden opgeslagen [clientlibs.](uifrontend.md#clientlibs) Dit omvat ook HTML-scripts voor het renderen van dynamische HTML. U kunt de module ui.apps zien als een kaart aan de structuur in JCR maar in een formaat dat op een dossiersysteem kan worden opgeslagen en aan broncontrole wordt geëngageerd.

Met de Apache Jackrabbit FileVault Package-insteekmodule wordt de inhoud van de module ui.apps gecompileerd naar een AEM pakket dat kan worden geïmplementeerd op AEM. De algemene configuraties voor de plug-in worden gedefinieerd in de bovenliggende pom.xml.

## Bovenliggende POM {#parent-pom}

[De bovenliggende POM](/help/developing/archetype/using.md#parent-pom) (`<src>/<project>/pom.xml`) include `<plugin>` secties die diverse configuraties voor de plugins bepalen die in het project worden gebruikt. Dit omvat een configuratie voor `filterSource` voor de Jackrabbit FileVault Package Plugin. De `filterSource` wijst naar de locatie van de `filter.xml` bestand dat wordt gebruikt voor het definiëren van de jcr-paden die in het pakket worden opgenomen.

Naast de Jackrabbit FileVault Package Plugin is een definitie van de Content Package Plugin die wordt gebruikt om het pakket vervolgens in AEM te duwen. Variabelen voor `aem.host`, `aem.port`, `vault.user`, en `vault.password` worden gebruikt die overeenkomen met de algemene eigenschappen die in dezelfde bovenliggende POM zijn gedefinieerd.

## ui.apps/pom.xml {#uiapps-pom}

Merk op dat de pakketten core.wcm.components.all en core.wcm.components.examples als subpakket worden omvat. Hierdoor wordt het pakket Core Components samen met de WKND-code telkens geïmplementeerd.

core.wcm.components.all en core.wcm.components.examples zijn inbegrepen als gebiedsdelen in de gebiedsdeellijst. Nochtans als beste praktijken, worden de versies voor gebiedsdelen weggelaten hier en beheerd in [bovenliggend pomabestand](/help/developing/archetype/using.md#core-components).

## filter.xml {#filter}

De `filter.xml` bestand voor de module ui.apps is te vinden op `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml` en bevat de paden die bij het pakket ui.apps worden opgenomen en geïnstalleerd.
