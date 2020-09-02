---
title: De gegevenslaag van de Cliënt van Adobe uitbreiden
description: De de Gegevens Laag van de Cliënt van Adobe kan na sommige basispatronen worden uitgebreid
translation-type: tm+mt
source-git-commit: 896ed679ed3351cb309a34b38bf97fe81adc2cfe
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---


# De gegevenslaag van de Cliënt van Adobe uitbreiden {#extending-acdl}

U kunt de Componenten van de Kern met de opties van de douanedialoog uitbreiden die inhoudsauteurs toestaan om extra informatie met betrekking tot de Laag van Gegevens in te gaan.

Om deze gebieden in de Laag van Gegevens te omvatten die door de Componenten van de Kern wordt verstrekt, moet u het model van de component uitbreiden die zijn eigen specifieke methodes van de gegevenslaag uitvoert.

## Voorbeeld: Component Title {#example}

Een component van de Kern zoals de component [van de](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) Titel breidt [Component](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) uit die een `getData` methode heeft die door gebrek terugkeert [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` serialiseert vooraf bepaalde gebieden die uw component, als `getDataLayerLinkUrl` en `getDataLayerTitle` voor [`TitleImpl`. kan uitvoeren.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

Daarom kan uw aangepaste Sling-model een `getData` methode bevatten die een object retourneert dat zich uitbreidt `ComponentData` om meer velden te retourneren.

Als u dit doet, wordt een `data-cmp-data-layer` kenmerk toegevoegd aan het HTML-element van uw component met de JSON-code van de gegevens die worden gevuld met de gegevenslaag. Op dit punt kunt u scripts implementeren die naar deze gegevens of verwante gebeurtenissen luisteren.
