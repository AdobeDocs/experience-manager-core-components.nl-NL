---
title: ui.apps Module van het Archetype van het AEM Project
description: ui.apps Module van het Archetype van het AEM Project
feature: Core Components, AEM Project Archetype
role: Architect, ontwikkelaar, beheerder
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---


# ui.apps Module van het Archetype van het AEM Project {#uiapps-module}

De module ui.apps maven (`<src-directory>/<project>/ui.apps`) bevat alle renderingcode die nodig is voor de site onder `/apps`. Dit omvat CSS/JS die in een AEM formaat genoemd [clientlibs zal worden opgeslagen.](uifrontend.md#clientlibs) Dit omvat ook HTML-scripts voor het renderen van dynamische HTML. U kunt de module ui.apps zien als een kaart aan de structuur in JCR maar in een formaat dat op een dossiersysteem kan worden opgeslagen en aan broncontrole wordt geëngageerd.

Met de Apache Jackrabbit FileVault Package-insteekmodule wordt de inhoud van de module ui.apps gecompileerd naar een AEM pakket dat kan worden geïmplementeerd op AEM. De algemene configuraties voor de plug-in worden gedefinieerd in de bovenliggende pom.xml.

## Bovenliggende POM {#parent-pom}

[De bovenliggende POM](/help/developing/archetype/using.md#parent-pom) (`<src>/<project>/pom.xml`) bevat  `<plugin>` secties die verschillende configuraties definiëren voor de plug-ins die in het project worden gebruikt. Dit omvat een configuratie voor `filterSource` voor de Insteekmodule van het Pakket van het Pakket Jackrabbit FileVault. `filterSource` wijst naar de locatie van het `filter.xml`-bestand dat wordt gebruikt om de JCr-paden te definiëren die in het pakket zijn opgenomen.

Naast de Jackrabbit FileVault Package Plugin is een definitie van de Content Package Plugin die wordt gebruikt om het pakket vervolgens in AEM te duwen. Merk op dat de variabelen voor `aem.host`, `aem.port`, `vault.user`, en `vault.password` worden gebruikt die aan de globale eigenschappen beantwoorden die in zelfde ouderPOM worden bepaald.

## ui.apps/pom.xml {#uiapps-pom}

De pom ui.apps (`<src>/<project>/ui.apps/pom.xml`) verstrekt `embedded` markeringen voor `filevault-package-maven-plugin`. De `embedded`-tags bevatten de gecompileerde kernbundel als onderdeel van het pakket ui.apps en waar deze wordt geïnstalleerd.

Merk op dat de pakketten core.wcm.components.all en core.wcm.components.examples als subpakket worden omvat. Hierdoor wordt het pakket Core Components samen met de WKND-code telkens geïmplementeerd.

core.wcm.components.all en core.wcm.components.examples zijn inbegrepen als gebiedsdelen in de gebiedsdeellijst. Nochtans als beste praktijken, worden de versies voor gebiedsdelen hier weggelaten en in het [ouderpomadossier](/help/developing/archetype/using.md#core-components) beheerd.

## filter.xml {#filter}

Het `filter.xml`-bestand voor de module ui.apps bevindt zich op `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml` en bevat de paden die worden opgenomen en geïnstalleerd met het pakket ui.apps.
