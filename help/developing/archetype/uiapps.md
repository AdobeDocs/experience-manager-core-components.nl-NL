---
title: ui.apps Module van het Archetype van het AEM Project
description: ui.apps Module van het Archetype van het AEM Project
translation-type: tm+mt
source-git-commit: a427c2ade8cca69de8e2b59fc3afb4405342909c
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---


# ui.apps Module van het Archetype van het AEM Project {#uiapps-module}

De module ui.apps (`<src-directory>/<project>/ui.apps`) bevat alle renderingcode die nodig is voor de onderliggende site `/apps`. Dit omvat CSS/JS die in een AEM formaat genoemd [clientlibs zal worden opgeslagen.](uifrontend.md#clientlibs) Dit omvat ook HTML-scripts voor het renderen van dynamische HTML. U kunt de module ui.apps zien als een kaart aan de structuur in JCR maar in een formaat dat op een dossiersysteem kan worden opgeslagen en aan broncontrole wordt geëngageerd.

Met de Apache Jackrabbit FileVault Package-insteekmodule wordt de inhoud van de module ui.apps gecompileerd naar een AEM pakket dat kan worden geïmplementeerd op AEM. De algemene configuraties voor de plug-in worden gedefinieerd in de bovenliggende pom.xml.

## Bovenliggende POM {#parent-pom}

[Het bovenliggende POM](/help/developing/archetype/using.md#parent-pom) (`<src>/<project>/pom.xml`) bevat `<plugin>` secties die verschillende configuraties definiëren voor de plug-ins die in het project worden gebruikt. Dit omvat een configuratie voor de `filterSource` voor de insteekmodule van het Pakket van het Pakket Jackrabbit FileVault. De `filterSource` punten verwijzen naar de locatie van het `filter.xml` bestand dat wordt gebruikt om de JCr-paden te definiëren die in het pakket worden opgenomen.

Naast de Jackrabbit FileVault Package Plugin is een definitie van de Content Package Plugin die wordt gebruikt om het pakket vervolgens in AEM te duwen. Merk op dat de variabelen voor `aem.host`, `aem.port`, `vault.user`en `vault.password` worden gebruikt die aan de globale eigenschappen beantwoorden die in zelfde ouderPOM worden bepaald.

## ui.apps/pom.xml {#uiapps-pom}

De pom (`<src>/<project>/ui.apps/pom.xml`) van ui.apps bevat de `embedded` tags voor de `filevault-package-maven-plugin`. De `embedded` tags bevatten de gecompileerde kernbundel als onderdeel van het pakket ui.apps en waar deze wordt geïnstalleerd.

Merk op dat de pakketten core.wcm.components.all en core.wcm.components.examples als subpakket worden omvat. Hierdoor wordt het pakket Core Components samen met de WKND-code telkens geïmplementeerd.

core.wcm.components.all en core.wcm.components.examples zijn inbegrepen als gebiedsdelen in de gebiedsdeellijst. Nochtans als beste praktijken, worden de versies voor gebiedsdelen hier weggelaten en in het [ouderpoomdossier](/help/developing/archetype/using.md#core-components)beheerd.

## filter.xml {#filter}

Het `filter.xml` bestand voor de module ui.apps bevindt zich op `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml` en bevat de paden die worden opgenomen en geïnstalleerd met het pakket ui.apps.
