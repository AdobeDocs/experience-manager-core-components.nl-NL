---
title: ui.content Module van het AEM Project Archetype
description: ui.content Module van het AEM Project Archetype
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# ui.content Module van het AEM Project Archetype {#uicontent-module}

De module ui.content maven (`<src-directory>/<project>/ui.content`) bevat basislijninhoud en configuraties onder `/content` en `/conf`. ui.content wordt gecompileerd tot een AEM-pakket, net als ui.apps. Het belangrijkste verschil is dat de knooppunten die in ui.content zijn opgeslagen, rechtstreeks op de AEM-instantie kunnen worden gewijzigd. Dit zijn pagina&#39;s, DAM-elementen en bewerkbare sjablonen. De module ui.content kan worden gebruikt om steekproefinhoud voor een schone instantie op te slaan en/of om sommige basislijnconfiguraties te creëren die in broncontrole moeten worden beheerd.

## filter.xml {#filter}

Het `filter.xml` bestand voor de module ui.content bevindt zich op `<src>/<project>/ui.content/src/main/content/META-INF/vault/filter.xml` en bevat de paden die worden opgenomen en geïnstalleerd met het pakket ui.content. Er wordt een `mode="merge"` kenmerk toegevoegd aan het pad. Dit zorgt ervoor dat de configuraties die met een codeplaatsing worden opgesteld niet automatisch inhoud of configuraties met voeten treden die direct op de instantie AEM zijn ontworpen.

## ui.content/pom.xml

De module ui.content gebruikt, net als de module ui.apps, de insteekmodule FileVault Package. Nochtans omvat de ui.content pom (`<src>/<project>/ui.content/pom.xml`) een extra configuratiebezit genoemd `acHandling`, die aan `merge_preserve`. wordt geplaatst. Dit is inbegrepen omdat de module ui.content de Lijsten van het Toegangsbeheer (ACLs) omvat die toestemmingen zijn, die bepalen wie de malplaatjes kan uitgeven. Opdat deze ACLs in AEM wordt ingevoerd is het `acHandling` bezit nodig.
