---
title: Kerncomponenten aanpassen
description: De componenten van de Kern voeren verscheidene patronen uit die gemakkelijke aanpassing, van eenvoudig het stileren aan geavanceerd functionaliteit hergebruik toestaan.
role: Architect, Developer, Admin
exl-id: ec4b918b-bc70-4d72-ba84-a24556aedb41
source-git-commit: bd688d422a072a9d5627c27817ac67f95829de4f
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 0%

---

# Kerncomponenten aanpassen{#customizing-core-components}

De [Kernonderdelen](overview.md) Implementeer verschillende patronen die u eenvoudig kunt aanpassen, van eenvoudige opmaak tot geavanceerde functionaliteit en hergebruik.

## Flexibele architectuur {#flexible-architecture}

De Core Components zijn vanaf het begin ontworpen om flexibel en uitbreidbaar te zijn. Een overzicht van hun architectuur onthult waar de aanpassingen kunnen worden gemaakt.

![Architectuur van kerncomponenten](/help/assets/screen_shot_2018-12-07at093742.png)

* [Het dialoogvenster Ontwerpen](/help/get-started/authoring.md#edit-and-design-dialogs) Hiermee bepaalt u wat auteurs wel of niet kunnen doen in het dialoogvenster Bewerken.
* [Het dialoogvenster Bewerken](/help/get-started/authoring.md#edit-and-design-dialogs) toont auteurs slechts de opties zij worden toegestaan te gebruiken.
* [Het verkoopmodel](#customizing-the-logic-of-a-core-component) controleert en bereidt de inhoud voor de mening (malplaatje) voor.
* [Het resultaat van het verkoopmodel](#customizing-the-logic-of-a-core-component) kan aan JSON voor SPA gebruik-gevallen in series worden vervaardigd.
* [De HTML geeft de HTML weer](#customizing-the-markup) server-kant voor traditionele rendering op de server.
* [De HTML-uitvoer](#customizing-the-markup) is semantisch, toegankelijk, zoekmachine geoptimaliseerd, en gemakkelijk aan stijl.

En alle kerncomponenten implementeren de [Stijlsysteem](#styling-the-components).

## Projectarchetype AEM {#aem-project-archetype}

[Het AEM Project Archetype](/help/developing/archetype/overview.md) leidt tot een minimaal Adobe Experience Manager project als uitgangspunt voor uw eigen projecten, met inbegrip van een voorbeeld van douaneHTML component met SlingModels voor de logica en juiste implementatie van de Componenten van de Kern met het geadviseerde volmachtspatroon.

## Aanpassingspatronen {#customization-patterns}

### Dialoogvensters aanpassen {#customizing-dialogs}

Het kan wenselijk zijn om de configuratieopties beschikbaar in een kerncomponentendialoog aan te passen, of het [Het dialoogvenster Ontwerpen of het dialoogvenster Bewerken](/help/get-started/authoring.md).

Elk dialoogvenster heeft een consistente knooppuntstructuur. Het wordt aanbevolen deze structuur te repliceren in een overnemende component, zodat [Samenvoeging van verkoopbronnen](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) en [Voorwaarden verbergen](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/hide-conditions.html) U kunt secties van het oorspronkelijke dialoogvenster verbergen, vervangen of opnieuw ordenen. De structuur die moet worden gerepliceerd, wordt gedefinieerd als alles tot het niveau van de tabitemnode.

Om volledig compatibel te zijn met eventuele wijzigingen die zijn aangebracht in een dialoog over de huidige versie, is het van groot belang dat structuren onder het tabitemniveau niet worden gewijzigd (verborgen, toegevoegd, vervangen, opnieuw gerangschikt, enz.). In plaats daarvan moet een tab-item van het bovenliggende item via het dialoogvenster `sling:hideResource` eigenschap (zie [Eigenschappen van samenvoeging van resources afspelen](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/sling-resource-merger.html)), en nieuwe toegevoegde lusjepunten die de op maat gemaakte configuratiegebieden bevatten. `sling:orderBefore` U kunt tabitems desgewenst opnieuw ordenen.

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
                        <myTab
                               jcr:primaryType="nt:unstructured"
                               jcr:title="My Tab"
                               sling:resourceType="granite/ui/components/coral/foundation/container">
                                  
                               <!-- myTab content -->
                                  
                        </myTab>
                </items>
            </tabs>
        </items>
    </content>
</jcr:root>
```

### De logica van een kerncomponent aanpassen {#customizing-the-logic-of-a-core-component}

De bedrijfslogica voor de kerncomponenten wordt uitgevoerd in Sling Models. Deze logica kan worden uitgebreid door een Sling delegatiepatroon te gebruiken.

De component title core gebruikt bijvoorbeeld de opdracht `jcr:title` eigenschap van de gevraagde bron om de titeltekst te verstrekken. Indien niet `jcr:title` -eigenschap is gedefinieerd, wordt een fallback naar de huidige paginatitel geïmplementeerd. We willen het gedrag wijzigen zodat de titel van de huidige pagina altijd wordt weergegeven.

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

Voor meer details over het delegatiepatroon zie het artikel van GitHub Wiki van de Componenten van de Kern [Delegatiepatroon voor verkoopmodellen](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models).

### De opmaak aanpassen {#customizing-the-markup}

Soms is voor geavanceerde opmaak een andere markeringsstructuur van de component vereist.

Dit kan eenvoudig door de HTML- dossiers te kopiëren die van de Component van de Kern in [proxycomponent.](guidelines.md#proxy-component-pattern)

Als u het voorbeeld van de Core Breadcrumb-component nogmaals gebruikt, kunt u de opmaakuitvoer van de component aanpassen, `breadcrumb.html` bestand moet worden gekopieerd naar de sitespecifieke component met een `sling:resourceSuperTypes` die naar de Core Breadcrumb Component wijst.

### De componenten opmaken {#styling-the-components}

De eerste vorm van aanpassing is het toepassen van CSS-stijlen.

Om dit gemakkelijk te maken, geven de Componenten van de Kern semantische prijsverhoging terug en volgen een gestandaardiseerde noemende overeenkomst die door wordt geïnspireerd [Bootstrap](https://getbootstrap.com/). Om de stijlen voor de afzonderlijke componenten gemakkelijk te kunnen bepalen en naammaken, wordt elke Core-component in een DIV-element opgenomen met de opdracht &quot; `cmp`&quot; en &quot; `cmp-<name>`&quot;.

Bekijk bijvoorbeeld het HTML-bestand van de v1 Core Breadcrumb-component: [breadcrumb.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html), zien we dat de hiërarchie van uitgevoerde elementen `ol.breadcrumb > li.breadcrumb-item > a`. Om er zeker van te zijn dat een CSS-regel alleen van invloed is op de klasse breadcrumb van die component, moeten alle regels een naamruimte krijgen, zoals hieronder wordt weergegeven:

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

Bovendien maken alle Core Components gebruik van de AEM [Stijlsysteemfunctie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/style-system.html) waarmee sjabloonauteurs extra CSS-klassenamen kunnen definiëren die door de auteurs van de pagina op de component kunnen worden toegepast. Op deze manier kunt u voor elke sjabloon een lijst met toegestane componentstijlen definiëren en aangeven of een van deze stijlen standaard moet worden toegepast op alle componenten van dat type.

## Compatibiliteit van aanpassingen upgraden {#upgrade-compatibility-of-customizations}

Er zijn drie verschillende soorten upgrades mogelijk:

* upgrade uitvoeren van AEM
* de Core Components upgraden naar een nieuwe secundaire versie
* de Core Components upgraden naar een belangrijke versie

Doorgaans heeft de upgrade van AEM naar een nieuwe versie geen invloed op de uitgevoerde Core Components of aanpassingen, op voorwaarde dat de versies van de componenten ook de nieuwe AEM versie ondersteunen waarnaar wordt gemigreerd en dat aanpassingen geen API&#39;s gebruiken die zijn [afgekeurd of verwijderd](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html).

Als u de kerncomponenten upgradet zonder over te schakelen op een nieuwere hoofdversie, heeft dit geen invloed op aanpassingen, zolang de aanpassingspatronen die op deze pagina worden beschreven, worden gebruikt.

Het schakelen naar een nieuwere belangrijkste versie van de Componenten van de Kern is compatibel slechts voor de inhoudsstructuur, maar de aanpassingen kunnen moeten worden gerefactored. De duidelijke veranderingslogboeken zullen voor elke componentenversie worden gepubliceerd om de veranderingen te benadrukken die het soort aanpassingen zouden beïnvloeden die op deze pagina worden beschreven.

## Ondersteuning voor aanpassingen {#support-of-customizations}

Zoals voor om het even welke AEM component, zijn er een aantal dingen om zich van betreffende aanpassingen bewust te zijn:

1. **Wijzig nooit rechtstreeks de code van de Componenten van de Kern.**

   Dit zou hen volledig ongesteund maken, en van toekomstige updates van de componenten een pijnlijk proces maken. Gebruik in plaats daarvan de aanpassingsmethoden die op deze pagina worden beschreven.

1. **Eigen code is uw eigen verantwoordelijkheid.**

   Ons ondersteuningsprogramma heeft geen betrekking op aangepaste code en heeft problemen gemeld die niet kunnen worden gereproduceerd met vanilla Core Components die [gebruikt als gedocumenteerd](/help/get-started/using.md) komt niet in aanmerking.

1. **Functionaliteit is vervangen en verwijderd.**

   Wanneer elke nieuwe AEM wordt bijgewerkt naar, moet u ervoor zorgen dat alle gebruikte API actueel blijven door de [Verouderde en verwijderde functies](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html) pagina.

Zie ook de [Ondersteuning van kerncomponenten](overview.md#core-component-support) sectie.

**Volgende lezen:**

* [Basiscomponenten gebruiken](/help/get-started/using.md) - Ga aan de slag met Core Components in uw eigen project.
* [Componentrichtlijnen](guidelines.md) - om de implementatiepatronen van de Core Components te leren.
