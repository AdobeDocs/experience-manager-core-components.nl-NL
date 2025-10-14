---
title: Kerncomponenten aanpassen
description: De componenten van de Kern voeren verscheidene patronen uit die gemakkelijke aanpassing, van eenvoudig het stileren aan geavanceerd functionaliteit hergebruik toestaan.
role: Architect, Developer, Admin
exl-id: ec4b918b-bc70-4d72-ba84-a24556aedb41
source-git-commit: 5994133947ff697f7c866fe61598c58e37e77008
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 0%

---

# Kerncomponenten aanpassen{#customizing-core-components}

De [&#x200B; Componenten van de Kern &#x200B;](overview.md) voeren verscheidene patronen uit die gemakkelijke aanpassing, van eenvoudig het stileren aan geavanceerd functionaliteit hergebruik toestaan.

{{traditional-aem}}

## Flexibele architectuur {#flexible-architecture}

De Core Components zijn vanaf het begin ontworpen om flexibel en uitbreidbaar te zijn. Een overzicht van hun architectuur onthult waar de aanpassingen kunnen worden gemaakt.

![&#128279;](/help/assets/screen_shot_2018-12-07at093742.png) Architectuur van de Componenten van 0&rbrace; Kern

* [&#x200B; de ontwerpdialoog &#x200B;](/help/get-started/authoring.md#edit-and-design-dialogs) bepaalt wat de auteurs kunnen of niet in uitgeven dialoog kunnen doen.
* [&#x200B; uitgeeft dialoog &#x200B;](/help/get-started/authoring.md#edit-and-design-dialogs) toont auteurs slechts de opties zij worden toegestaan te gebruiken.
* [&#x200B; het Verschuiven model &#x200B;](#customizing-the-logic-of-a-core-component) verifieert en bereidt de inhoud voor de mening (malplaatje) voor.
* [&#x200B; het resultaat van het het Verdelen model &#x200B;](#customizing-the-logic-of-a-core-component) kan aan JSON voor gebruik-gevallen van het KUUROORD worden in series vervaardigd.
* [&#x200B; HTML geeft HTML &#x200B;](#customizing-the-markup) server-kant voor traditionele server-kant terug teruggeeft.
* [&#x200B; de output van HTML &#x200B;](#customizing-the-markup) is semantisch, toegankelijk, onderzoek-motor geoptimaliseerd, en gemakkelijk aan stijl.

En alle kerncomponenten voeren het [&#x200B; Systeem van de Stijl &#x200B;](#styling-the-components) uit.

## AEM Project Archetype {#aem-project-archetype}

[&#x200B; het Archetype van het Project van AEM &#x200B;](/help/developing/archetype/overview.md) leidt tot een minimaal project van Adobe Experience Manager als uitgangspunt voor uw eigen projecten, met inbegrip van een voorbeeld van douaneHTML component met SlingModels voor de logica en juiste implementatie van de Componenten van de Kern met het geadviseerde volmachtspatroon.

## Aanpassingspatronen {#customization-patterns}

### Dialoogvensters aanpassen {#customizing-dialogs}

Het kan worden gewenst om de configuratieopties beschikbaar in een kerncomponentendialoog aan te passen, of het de [&#x200B; Dialoog van het Ontwerp of Edit Dialog &#x200B;](/help/get-started/authoring.md).

Elk dialoogvenster heeft een consistente knooppuntstructuur. Het wordt geadviseerd dat deze structuur in een het erven component wordt herhaald zodat [&#x200B; het Verzamelen van het Middel &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) en [&#x200B; de Voorwaarden van de Verbergen &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/developing/using/hide-conditions.html) kunnen worden gebruikt om, secties van de originele dialoog te verbergen te vervangen of te herschikken. De structuur die moet worden gerepliceerd, wordt gedefinieerd als alles tot het niveau van de tabitemnode.

Om volledig compatibel te zijn met eventuele wijzigingen die zijn aangebracht in een dialoog over de huidige versie, is het van groot belang dat structuren onder het tabitemniveau niet worden gewijzigd (verborgen, toegevoegd, vervangen, opnieuw gerangschikt, enz.). In plaats daarvan, zou een lusjepunt van de ouder via het `sling:hideResource` bezit moeten worden verborgen (zie [&#x200B; het Verspreiden Eigenschappen van de Fusie van het Middel &#x200B;](https://helpx.adobe.com/nl/experience-manager/6-5/sites/developing/using/sling-resource-merger.html)), en nieuwe toegevoegde lusjepunten die de maatbespraakte configuratiegebieden bevatten. `sling:orderBefore` kan indien nodig worden gebruikt om de tabitems opnieuw te ordenen.

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

De component title core gebruikt bijvoorbeeld de eigenschap `jcr:title` van de gevraagde bron om de titeltekst op te geven. Als er geen eigenschap `jcr:title` is gedefinieerd, wordt een fallback naar de huidige paginatitel geïmplementeerd. We willen het gedrag wijzigen zodat de titel van de huidige pagina altijd wordt weergegeven.

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

Voor verdere details over het delegatiepatroon zie het artikel van GitHub Wiki van de Componenten van de Kern [&#x200B; Patroon van de Delegatie voor het Verdelen Modellen &#x200B;](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models).

### De opmaak aanpassen {#customizing-the-markup}

Soms is voor geavanceerde opmaak een andere markeringsstructuur van de component vereist.

Dit kan gemakkelijk worden gedaan door de HTML- dossiers te kopiëren die van de Component van de Kern in de [&#x200B; volmachtscomponent moeten worden gewijzigd.](guidelines.md#proxy-component-pattern)

Als u het voorbeeld van de Core Breadcrumb-component nogmaals gebruikt en de markeringsuitvoer ervan wilt aanpassen, moet het `breadcrumb.html` -bestand worden gekopieerd naar de sitespecifieke component met een `sling:resourceSuperTypes` die naar de Core Breadcrumb-component wijst.

### De componenten opmaken {#styling-the-components}

De eerste vorm van aanpassing is het toepassen van CSS-stijlen.

Om dit gemakkelijk te maken, geven de Componenten van de Kern semantische prijsverhoging terug en volgen een gestandaardiseerde noemende overeenkomst die door [&#x200B; wordt geïnspireerd Bootstrap &#x200B;](https://getbootstrap.com/). Om de stijlen voor de afzonderlijke componenten gemakkelijk te kunnen toewijzen en naammaken, wordt elke Core-component in een DIV-element opgenomen met de klassen &quot; `cmp`&quot; en &quot; `cmp-<name>`&quot;.

Bijvoorbeeld, kijkend het HTML- dossier van de v1 Component van de Kern Breadcrumb: [&#x200B; breadcrumb.html &#x200B;](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html), zien wij dat de hiërarchie van elementenoutput `ol.breadcrumb > li.breadcrumb-item > a` is. Om er zeker van te zijn dat een CSS-regel alleen van invloed is op de klasse breadcrumb van die component, moeten alle regels een naamruimte krijgen, zoals hieronder wordt weergegeven:

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

Bovendien, elk van de hefboomwerking van de Componenten van de Kern de eigenschap van het Systeem van de Stijl van AEM [&#128279;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/style-system.html?lang=nl-NL) die malplaatjeauteurs toestaat om extra CSS klassennamen te bepalen die op de component door de paginaauteurs kunnen worden toegepast.  Op deze manier kunt u voor elke sjabloon een lijst met toegestane componentstijlen definiëren en aangeven of een van deze stijlen standaard moet worden toegepast op alle componenten van dat type.

## Compatibiliteit van aanpassingen upgraden {#upgrade-compatibility-of-customizations}

Er zijn drie verschillende soorten upgrades mogelijk:

* de versie van AEM upgraden
* de Core Components upgraden naar een nieuwe secundaire versie
* de Core Components upgraden naar een belangrijke versie

Over het algemeen, zal de bevordering van AEM aan een nieuwe versie niet de Componenten van de Kern of de aanpassingen beïnvloeden, op voorwaarde dat de versies van de componenten ook de nieuwe versie van AEM steunen die wordt gemigreerd aan, en dat de aanpassingen geen APIs gebruiken die [&#x200B; zijn afgekeurd of verwijderd &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=nl-NL).

Als u de kerncomponenten upgradet zonder over te schakelen op een nieuwere hoofdversie, heeft dit geen invloed op aanpassingen, zolang de aanpassingspatronen die op deze pagina worden beschreven, worden gebruikt.

Het schakelen naar een nieuwere belangrijkste versie van de Componenten van de Kern is compatibel slechts voor de inhoudsstructuur, maar de aanpassingen kunnen moeten worden gerefactored. De duidelijke veranderingslogboeken zullen voor elke componentenversie worden gepubliceerd om de veranderingen te benadrukken die het soort aanpassingen zouden beïnvloeden die op deze pagina worden beschreven.

## Ondersteuning voor aanpassingen {#support-of-customizations}

Net als bij elke AEM-component moet u rekening houden met een aantal aanpassingen:

1. **wijzigt nooit direct de code van de Componenten van de Kern.**

   Dit zou hen volledig ongesteund maken, en van toekomstige updates van de componenten een pijnlijk proces maken. Gebruik in plaats daarvan de aanpassingsmethoden die op deze pagina worden beschreven.

1. **de code van de Douane is uw eigen verantwoordelijkheid.**

   Ons steunprogramma behandelt douanecode niet, en rapporteerde kwesties die niet met de componenten van de Kern kunnen worden gereproduceerd vanilla die [&#x200B; worden gebruikt zoals gedocumenteerd &#x200B;](/help/get-started/using.md) niet zal kwalificeren.

1. **Controle verouderde en verwijderde functionaliteit.**

   Met elke nieuwe versie die van AEM wordt bevorderd aan, zorg ervoor dat alle gebruikte API nog actueel is door een oog op de [&#x200B; Vervangen en Verwijderde pagina van Eigenschappen &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=nl-NL) te houden.

Zie ook de [&#128279;](overview.md#core-component-support) sectie van de Steun van de Component van de 0&rbrace; Kern.

**Lees daarna:**

* [&#x200B; Gebruikend de Componenten van de Kern &#x200B;](/help/get-started/using.md) - wordt in werking gesteld met de Componenten van de Kern in uw eigen project.
* [&#x200B; Richtlijnen van de Component &#x200B;](guidelines.md) - om de implementatiepatronen van de Componenten van de Kern te leren.
