---
title: Kerncomponenten aanpassen
description: De componenten van de Kern voeren verscheidene patronen uit die gemakkelijke aanpassing, van eenvoudig het stileren aan geavanceerd functionaliteit hergebruik toestaan.
translation-type: tm+mt
source-git-commit: fe8a121520000ffd56ae3347469590e89121eaf0

---


# Kerncomponenten aanpassen{#customizing-core-components}

De [kerncomponenten](overview.md) implementeren verschillende patronen die u eenvoudig kunt aanpassen, van eenvoudige opmaak tot geavanceerd hergebruik van functionaliteit.

## Flexibele architectuur {#flexible-architecture}

De Core Components zijn vanaf het begin ontworpen om flexibel en uitbreidbaar te zijn. Een overzicht van hun architectuur onthult waar de aanpassingen kunnen worden gemaakt.

![Architectuur van kerncomponenten](/help/assets/screen_shot_2018-12-07at093742.png)

* [In het dialoogvenster](/help/get-started/authoring.md#edit-and-design-dialogs) Ontwerpen wordt gedefinieerd wat auteurs wel of niet kunnen doen in het dialoogvenster Bewerken.
* [In het dialoogvenster](/help/get-started/authoring.md#edit-and-design-dialogs) Bewerken worden alleen de opties weergegeven die de auteurs mogen gebruiken.
* [Het Sling-model](#customizing-the-logic-of-a-core-component) verifieert de inhoud en bereidt deze voor op de weergave (sjabloon).
* [Het resultaat van het het Sling model](#customizing-the-logic-of-a-core-component) kan aan JSON voor gebruik-gevallen van het KUUROORD worden in series vervaardigd.
* [Het HTML-bestand geeft de HTML](#customizing-the-markup) -server weer voor traditionele rendering op de server.
* [De HTML-uitvoer](#customizing-the-markup) is semantisch, toegankelijk, met zoekprogramma&#39;s geoptimaliseerd en eenvoudig op te maken.

En alle kerncomponenten voeren het Systeem [van de](#styling-the-components)Stijl uit.

## AEM-projectarchetype {#aem-project-archetype}

[Het AEM Project Archetype](/help/developing/archetype/overview.md) leidt tot een minimaal project van de Manager van de Ervaring van Adobe als uitgangspunt voor uw eigen projecten, met inbegrip van een voorbeeld van douaneHTML component met SlingModels voor de logica en juiste implementatie van de Componenten van de Kern met het geadviseerde volmachtspatroon.

## Aanpassingspatronen {#customization-patterns}

### Dialoogvensters aanpassen {#customizing-dialogs}

Het kan wenselijk zijn om de configuratieopties aan te passen beschikbaar in een kerncomponentendialoog, of het de Dialoog van het [Ontwerp of de Edit Dialoog](/help/get-started/authoring.md).

Elk dialoogvenster heeft een consistente knooppuntstructuur. Het wordt aanbevolen deze structuur te repliceren in een overnemende component, zodat [Sling Resource Merger](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) en [Hide Conditions](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/hide-conditions.html) kunnen worden gebruikt om secties van het oorspronkelijke dialoogvenster te verbergen, te vervangen of opnieuw te ordenen. De structuur die moet worden gerepliceerd, wordt gedefinieerd als alles tot het niveau van de tabitemnode.

Om volledig compatibel te zijn met eventuele wijzigingen die zijn aangebracht in een dialoog over de huidige versie, is het van groot belang dat structuren onder het tabitemniveau niet worden gewijzigd (verborgen, toegevoegd, vervangen, opnieuw gerangschikt, enz.). In plaats daarvan, zou een lusjepunt van de ouder via het `sling:hideResource` bezit (zie de Eigenschappen [van de Fusie van het Middel van de](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/sling-resource-merger.html)Verspreiding) moeten worden verborgen, en de nieuwe lusjepunten die de maats configuratievelden bevatten. `sling:orderBefore` U kunt tabitems desgewenst opnieuw ordenen.

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

De component titelkern gebruikt bijvoorbeeld de `jcr:title` eigenschap van de gevraagde bron om de titeltekst op te geven. Als er geen `jcr:title` eigenschap is gedefinieerd, wordt een fallback naar de huidige paginatitel geïmplementeerd. We willen het gedrag wijzigen zodat de titel van de huidige pagina altijd wordt weergegeven.

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

Voor meer details over het delegatiepatroon zie het artikel van de [Delegatie van de Partner van de Kern GitHub van het Wiki Patroon voor het Verdelen Modellen](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models).

### De opmaak aanpassen {#customizing-the-markup}

Soms is voor geavanceerde opmaak een andere markeringsstructuur van de component vereist.

Dit kan gemakkelijk worden gedaan door de HTML- dossiers te kopiëren die van de Component van de Kern in de volmachtscomponent moeten worden gewijzigd.

Als u het voorbeeld van de Core Breadcrumb-component nogmaals gebruikt en de markeringsuitvoer ervan wilt aanpassen, moet het `breadcrumb.html` bestand worden gekopieerd naar de sitespecifieke component die een code heeft `sling:resourceSuperTypes` die naar de Core Breadcrumb-component verwijst.

### De componenten opmaken {#styling-the-components}

De eerste vorm van aanpassing is het toepassen van CSS-stijlen.

Om dit gemakkelijk te maken, geven de Componenten van de Kern semantische prijsverhoging terug en volgen een gestandaardiseerde noemende overeenkomst die door [Bootstrap](https://getbootstrap.com/)wordt geïnspireerd. Om de stijlen voor de afzonderlijke componenten gemakkelijk te kunnen bepalen en naammaken, wordt elke Core-component in een DIV-element verpakt met de klassen &quot; `cmp`&quot; en &quot; `cmp-<name>`&quot;.

Bekijk bijvoorbeeld het HTML-bestand van de v1 Core Breadcrumb-component: [breadcrumb.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html), wij zien dat de hiërarchie van elementenoutput is `ol.breadcrumb > li.breadcrumb-item > a`. Om ervoor te zorgen dat een CSS-regel alleen van invloed is op de klasse breadcrumb van die component, moeten alle regels een naamruimte krijgen, zoals hieronder wordt weergegeven:

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

Daarnaast maakt elk van de Core Components gebruik van de AEM [Style System-functie](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html) waarmee sjabloonauteurs extra CSS-klassenamen kunnen definiëren die door de auteurs van de pagina op de component kunnen worden toegepast. Op deze manier kunt u voor elke sjabloon een lijst met toegestane componentstijlen definiëren en aangeven of een van deze stijlen standaard moet worden toegepast op alle componenten van dat type.

## Compatibiliteit van aanpassingen upgraden {#upgrade-compatibility-of-customizations}

Er zijn drie verschillende soorten upgrades mogelijk:

* de versie van AEM bijwerken
* de Core Components upgraden naar een nieuwe secundaire versie
* de Core Components upgraden naar een belangrijke versie

Over het algemeen heeft de upgrade van AEM naar een nieuwe versie geen invloed op de uitgevoerde kerncomponenten of aanpassingen, op voorwaarde dat de versies van de componenten ook de nieuwe AEM-versie ondersteunen waarnaar wordt gemigreerd en dat aanpassingen geen API&#39;s gebruiken die zijn [vervangen of verwijderd](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html).

Als u de kerncomponenten upgradet zonder over te schakelen op een nieuwere hoofdversie, heeft dit geen invloed op aanpassingen, zolang de aanpassingspatronen die op deze pagina worden beschreven, worden gebruikt.

Het schakelen naar een nieuwere belangrijkste versie van de Componenten van de Kern is compatibel slechts voor de inhoudsstructuur, maar de aanpassingen kunnen moeten worden gerefactored. De duidelijke veranderingslogboeken zullen voor elke componentenversie worden gepubliceerd om de veranderingen te benadrukken die het soort aanpassingen zouden beïnvloeden die op deze pagina worden beschreven.

## Ondersteuning voor aanpassingen {#support-of-customizations}

Zoals voor om het even welke component AEM, zijn er een aantal dingen om zich van betreffende aanpassingen bewust te zijn:

1. **Wijzig nooit rechtstreeks de code van de Componenten van de Kern.**

   Dit zou hen volledig ongesteund maken, en van toekomstige updates van de componenten een pijnlijk proces maken. Gebruik in plaats daarvan de aanpassingsmethoden die op deze pagina worden beschreven.

1. **Eigen code is uw eigen verantwoordelijkheid.**

   Ons supportprogramma heeft geen betrekking op aangepaste code. Problemen die niet kunnen worden gereproduceerd met vanilla Core Components die worden [gebruikt als gedocumenteerd](/help/get-started/using.md) , komen niet in aanmerking.

1. **Functionaliteit is vervangen en verwijderd.**

   Zorg ervoor dat elke nieuwe AEM-versie waarnaar wordt geüpgraded, actueel blijft door de pagina [Vervangen en Verwijderde functies](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html) in het oog te houden.

Zie ook de sectie [Core Component Support](overview.md#core-component-support) .

**Volgende lezen:**

* [Het gebruiken van de Componenten](/help/get-started/using.md) van de Kern - begin en loopt met de Componenten van de Kern in uw eigen project.
* [Componentrichtlijnen](guidelines.md) - voor het leren van de implementatiepatronen van de Core Components.