---
title: Kerncomponenten aanpassen
description: De componenten van de Kern voeren verscheidene patronen uit die gemakkelijke aanpassing, van eenvoudig het stileren aan geavanceerd functionaliteit hergebruik toestaan.
role: Architect, Developer, Administrator
exl-id: ec4b918b-bc70-4d72-ba84-a24556aedb41
translation-type: tm+mt
source-git-commit: b5b77f21cbeaa46622cef85f3bbaa549f17f1a06
workflow-type: tm+mt
source-wordcount: '1106'
ht-degree: 1%

---

# Kerncomponenten aanpassen{#customizing-core-components}

Met de [Core Components](overview.md) kunt u verschillende patronen implementeren die u eenvoudig kunt aanpassen, van eenvoudige opmaak tot geavanceerd hergebruik van functionaliteit.

## Flexibele architectuur {#flexible-architecture}

De Core Components zijn vanaf het begin ontworpen om flexibel en uitbreidbaar te zijn. Een overzicht van hun architectuur onthult waar de aanpassingen kunnen worden gemaakt.

![Architectuur van kerncomponenten](/help/assets/screen_shot_2018-12-07at093742.png)

* [In het ](/help/get-started/authoring.md#edit-and-design-dialogs) dialoogvenster Ontwerpen wordt gedefinieerd wat auteurs wel of niet kunnen doen in het dialoogvenster Bewerken.
* [In het ](/help/get-started/authoring.md#edit-and-design-dialogs) dialoogvenster Bewerken worden alleen de opties weergegeven die de auteurs mogen gebruiken.
* [In het Sling-](#customizing-the-logic-of-a-core-component) model wordt de inhoud voor de weergave (sjabloon) gecontroleerd en voorbereid.
* [Het resultaat van het Sling-](#customizing-the-logic-of-a-core-component) model kan aan JSON voor SPA gebruiksgevallen in series worden vervaardigd.
* [De HTML rendert de ](#customizing-the-markup) HTML-server voor traditionele rendering op de server.
* [De HTML-](#customizing-the-markup) uitvoer is semantisch, toegankelijk, met zoekprogramma&#39;s geoptimaliseerd en eenvoudig op te maken.

En alle kerncomponenten voeren [Stijlsysteem](#styling-the-components) uit.

## Projectarchetype {#aem-project-archetype} AEM

[Het AEM Project ](/help/developing/archetype/overview.md) Archetypecureert een minimaal project van Adobe Experience Manager als uitgangspunt voor uw eigen projecten, met inbegrip van een voorbeeld van douaneHTML component met SlingModels voor de logica en juiste implementatie van de Componenten van de Kern met het geadviseerde volmachtspatroon.

## Aanpassingspatronen {#customization-patterns}

### Dialoogvensters {#customizing-dialogs} aanpassen

Het kan wenselijk zijn om de configuratieopties aan te passen beschikbaar in een kerncomponentendialoog, of het [Dialoogvenster van het Ontwerp of Edit Dialog](/help/get-started/authoring.md).

Elk dialoogvenster heeft een consistente knooppuntstructuur. Aanbevolen wordt dat deze structuur wordt gerepliceerd in een overnemende component, zodat [Sling Resource Merger](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) en [Hide Conditions](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/hide-conditions.html) kunnen worden gebruikt om secties van het oorspronkelijke dialoogvenster te verbergen, te vervangen of opnieuw te ordenen. De structuur die moet worden gerepliceerd, wordt gedefinieerd als alles tot het niveau van de tabitemnode.

Om volledig compatibel te zijn met eventuele wijzigingen die zijn aangebracht in een dialoog over de huidige versie, is het van groot belang dat structuren onder het tabitemniveau niet worden gewijzigd (verborgen, toegevoegd, vervangen, opnieuw gerangschikt, enz.). In plaats daarvan, zou een lusjepunt van de ouder via het `sling:hideResource` bezit (zie [het Verspreiden Eigenschappen van de Fusie van het Middel](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/sling-resource-merger.html)) moeten worden verborgen, en de nieuwe lusjepunten die de op maat gemaakte configuratiegebieden bevatten. `sling:orderBefore` U kunt tabitems desgewenst opnieuw ordenen.

In het onderstaande dialoogvenster ziet u de aanbevolen dialoogstructuur en hoe u een overgeërfd tabblad zoals hierboven beschreven, kunt verbergen en vervangen:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<jcr:root xmlns:sling="https://sling.apache.org/jcr/sling/1.0"
          xmlns:jcr="https://www.jcp.org/jcr/1.0"
          xmlns:nt="https://www.jcp.org/jcr/nt/1.0"
          xmlns:granite="https://www.adobe.com/jcr/granite/1.0"
          jcr:primaryType="nt:unstructured">
    <content jcr:primaryType="nt:unstructured">
        <items jcr:primaryType="nt:unstructured">
            <tabs jcr:primaryType="nt:unstructured">
                <items jcr:primaryType="nt:unstructured">
                        <originalTab
                                jcr:primaryType="nt:unstructured"
                                sling:hideResource="true"/>
                        </originalTab>
                        <myTab
                               jcr:primaryType="nt:unstructured"
                               jcr:title="My Tab"
                               sling:resourceType="granite/ui/components/coral/foundation/container"/>
                               <!-- myTab content -->
                        </myTab>
                </items>
            </basic>
        </items>
    </content>
</jcr:root>
```

### De logica van een kerncomponent aanpassen {#customizing-the-logic-of-a-core-component}

De bedrijfslogica voor de kerncomponenten wordt uitgevoerd in Sling Models. Deze logica kan worden uitgebreid door een Sling delegatiepatroon te gebruiken.

De component titelkern gebruikt bijvoorbeeld de eigenschap `jcr:title` van de gevraagde bron om de titeltekst op te geven. Als er geen `jcr:title`-eigenschap is gedefinieerd, wordt een fallback naar de huidige paginatitel geïmplementeerd. We willen het gedrag wijzigen zodat de titel van de huidige pagina altijd wordt weergegeven.

Omdat de modellen van de Componenten van de Kern privé zijn, moeten zij met een delegatiepatroon worden uitgebreid.

```java
@Model(adaptables = SlingHttpServletRequest.class,
       adapters = Title.class,
       resourceType = "myproject/components/pageHeadline")
public class PageHeadline implements Title {
    @ScriptVariable private Page currentPage;
    @Self @Via(type = ResourceSuperType.class)
    private Title title;
    @Override public String getText() {
        return currentPage.getTitle();
    }
    @Override public String getType() {
        return title.getType();
    }
}
```

Voor verdere details over het delegatiepatroon zie het artikel van GitHub Wiki van de Componenten van de Kern [Het Patroon van de Delegatie voor het Verdelen Modellen](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models).

### De markering {#customizing-the-markup} aanpassen

Soms is voor geavanceerde opmaak een andere markeringsstructuur van de component vereist.

Dit kan gemakkelijk worden gedaan door de HTML- dossiers te kopiëren die van de Component van de Kern in [volmachtscomponent moeten worden gewijzigd.](guidelines.md#proxy-component-pattern)

Als u het voorbeeld van de Core Breadcrumb-component nogmaals gebruikt en de markeringsuitvoer ervan wilt aanpassen, moet het `breadcrumb.html`-bestand worden gekopieerd naar de sitespecifieke component met een `sling:resourceSuperTypes` die naar de Core Breadcrumb-component wijst.

### De componenten opmaken {#styling-the-components}

De eerste vorm van aanpassing is het toepassen van CSS-stijlen.

Om dit gemakkelijk te maken, geven de Componenten van de Kern semantische prijsverhoging terug en volgen een gestandaardiseerde noemende overeenkomst die door [Bootstrap wordt geïnspireerd. ](https://getbootstrap.com/) Om de stijlen voor de afzonderlijke componenten eenvoudig te kunnen toewijzen en naammaken, wordt elke Core-component in een DIV-element opgenomen met de klassen &quot; `cmp`&quot; en &quot; `cmp-<name>`&quot;.

Bekijk bijvoorbeeld het HTML-bestand van de v1 Core Breadcrumb-component: [breadcrumb.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html), wij zien dat de hiërarchie van elementenoutput `ol.breadcrumb > li.breadcrumb-item > a` is. Om er zeker van te zijn dat een CSS-regel alleen van invloed is op de klasse breadcrumb van die component, moeten alle regels een naamruimte krijgen, zoals hieronder wordt weergegeven:

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

Bovendien maakt elk van de Componenten van de Kern hefboomwerking AEM [de eigenschap van het Systeem van de Stijl](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html) die malplaatjeauteurs toestaat om extra CSS klassennamen te bepalen die op de component door de paginaauteurs kunnen worden toegepast. Op deze manier kunt u voor elke sjabloon een lijst met toegestane componentstijlen definiëren en aangeven of een van deze stijlen standaard moet worden toegepast op alle componenten van dat type.

## Compatibiliteit van aanpassingen upgraden {#upgrade-compatibility-of-customizations}

Er zijn drie verschillende soorten upgrades mogelijk:

* upgrade uitvoeren van de versie van AEM
* de Core Components upgraden naar een nieuwe secundaire versie
* de Core Components upgraden naar een belangrijke versie

Doorgaans heeft de upgrade van AEM naar een nieuwe versie geen invloed op de uitgevoerde Core Components of aanpassingen, op voorwaarde dat de versies van de componenten ook de nieuwe AEM versie ondersteunen waarnaar wordt gemigreerd en dat aanpassingen geen API&#39;s gebruiken die [verouderd of verwijderd](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html) zijn.

Als u de kerncomponenten upgradet zonder over te schakelen op een nieuwere hoofdversie, heeft dit geen invloed op aanpassingen, zolang de aanpassingspatronen die op deze pagina worden beschreven, worden gebruikt.

Het schakelen naar een nieuwere belangrijkste versie van de Componenten van de Kern is compatibel slechts voor de inhoudsstructuur, maar de aanpassingen kunnen moeten worden gerefactored. De duidelijke veranderingslogboeken zullen voor elke componentenversie worden gepubliceerd om de veranderingen te benadrukken die het soort aanpassingen zouden beïnvloeden die op deze pagina worden beschreven.

## Ondersteuning voor aanpassingen {#support-of-customizations}

Zoals voor om het even welke AEM component, zijn er een aantal dingen om zich van betreffende aanpassingen bewust te zijn:

1. **Wijzig nooit rechtstreeks de code van de Componenten van de Kern.**

   Dit zou hen volledig ongesteund maken, en van toekomstige updates van de componenten een pijnlijk proces maken. Gebruik in plaats daarvan de aanpassingsmethoden die op deze pagina worden beschreven.

1. **Eigen code is uw eigen verantwoordelijkheid.**

   Ons supportprogramma heeft geen betrekking op aangepaste code. Problemen die niet kunnen worden gereproduceerd met vanilla Core Components die [worden gebruikt als gedocumenteerd](/help/get-started/using.md), komen niet in aanmerking.

1. **Functionaliteit is vervangen en verwijderd.**

   Zorg ervoor dat elke nieuwe AEM die wordt bijgewerkt, actueel blijft door de pagina [Vervangen en Verwijderde functies](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html) in het oog te houden.

Zie ook de [Kerncomponentondersteuning](overview.md#core-component-support) sectie.

**Volgende lezen:**

* [Met behulp van Core Components](/help/get-started/using.md)  kunt u snel aan de slag met Core Components in uw eigen project.
* [Componentrichtlijnen](guidelines.md)  - om de implementatiepatronen van de kerncomponenten te leren.
