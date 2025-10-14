---
title: De gegevenslaag van de Cliënt van de Adobe uitbreiden
description: De gegevenslaag van de Cliënt van de Adobe kan na sommige basispatronen worden uitgebreid
feature: Core Components, Adobe Client Data Layer
role: Architect, Developer, Admin
exl-id: f3d5555b-4f08-49de-ab0f-dc0fb04aadf8
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# De gegevenslaag van de Cliënt van de Adobe uitbreiden {#extending-acdl}

U kunt de Componenten van de Kern met de opties van de douanedialoog uitbreiden die inhoudsauteurs toestaan om extra informatie met betrekking tot de Laag van Gegevens in te gaan.

Om deze gebieden in de Laag van Gegevens te omvatten die door de Componenten van de Kern wordt verstrekt, moet u het model van de component uitbreiden die zijn eigen specifieke methodes van de gegevenslaag uitvoert.

## Voorbeeld: component Title {#example}

Een Component van de Kern zoals de [&#x200B; component van de Titel &#x200B;](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) breidt [&#x200B; Component &#x200B;](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) uit die a `getData` methode heeft die door gebrek terugkeert [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serialiseert vooraf bepaalde gebieden die uw component, zoals `getDataLayerLinkUrl` en `getDataLayerTitle` voor [`TitleImpl` kan uitvoeren. &#x200B;](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Het aangepaste Sling-model kan daarom een `getData` -methode hebben die een object retourneert dat `ComponentData` uitbreidt om meer velden te retourneren.

Als u dit doet, wordt een `data-cmp-data-layer` -kenmerk toegevoegd aan het HTML-element van de component met de JSON-code van de gegevens die worden gevuld met de gegevenslaag. Op dit punt kunt u scripts implementeren die naar deze gegevens of verwante gebeurtenissen luisteren.

>[!TIP]
>
>Om de flexibiliteit van de Laag van Gegevens verder te onderzoeken, herzie over de integratieopties met inbegrip van hoe te om de Laag van Gegevens voor uw douanecomponenten toe te laten.
