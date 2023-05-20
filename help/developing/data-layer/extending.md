---
title: De gegevenslaag van de Cliënt van Adobe uitbreiden
description: De de Gegevens Laag van de Cliënt van Adobe kan na sommige basispatronen worden uitgebreid
feature: Core Components, Adobe Client Data Layer
role: Architect, Developer, Admin
exl-id: f3d5555b-4f08-49de-ab0f-dc0fb04aadf8
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# De gegevenslaag van de Cliënt van Adobe uitbreiden {#extending-acdl}

U kunt de Componenten van de Kern met de opties van de douanedialoog uitbreiden die inhoudsauteurs toestaan om extra informatie met betrekking tot de Laag van Gegevens in te gaan.

Om deze gebieden in de Laag van Gegevens te omvatten die door de Componenten van de Kern wordt verstrekt, moet u het model van de component uitbreiden die zijn eigen specifieke methodes van de gegevenslaag uitvoert.

## Voorbeeld: Component Title {#example}

Een kerncomponent zoals [Titelcomponent](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) extends [Component](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) die een `getData` methode die standaard wordt geretourneerd [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serialiseert vooraf bepaalde gebieden die uw component, als kan uitvoeren `getDataLayerLinkUrl` en `getDataLayerTitle` voor de [`TitleImpl`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Uw aangepaste verkoopmodel kan daarom een `getData` methode die een object retourneert dat een uitbreiding is `ComponentData` om meer velden te retourneren.

Als u dit doet, voegt u een `data-cmp-data-layer` attribuut aan het element van HTML van uw component met JSON van de gegevens die aan de gegevenslaag zullen worden bevolkt. Op dit punt kunt u scripts implementeren die naar deze gegevens of verwante gebeurtenissen luisteren.

>[!TIP]
>
>Om de flexibiliteit van de Laag van Gegevens verder te onderzoeken, herzie over de integratieopties met inbegrip van hoe te om de Laag van Gegevens voor uw douanecomponenten toe te laten.
