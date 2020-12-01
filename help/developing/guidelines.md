---
title: Componentrichtlijnen
description: De componenten van de Kern volgen moderne implementatiepatronen die vrij verschillend van de stichtingscomponenten zijn.
translation-type: tm+mt
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: tm+mt
source-wordcount: '1259'
ht-degree: 1%

---


# Componentrichtlijnen {#component-guidelines}

De [Kerncomponenten](overview.md) volgen moderne implementatiepatronen die heel anders zijn dan de basiscomponenten.

Deze pagina verklaart deze patronen, en wanneer om hen te gebruiken om uw eigen authorable componenten te bouwen. De eerste sectie [Algemene componentpatronen](#general-component-patterns) is van toepassing op elk type component, terwijl de tweede sectie [Herbruikbare componentpatronen](#reusable-component-patterns) van toepassing is op componenten die bedoeld zijn om hergebruikt te worden op sites of projecten, zoals de Componenten van de Kern bijvoorbeeld.

## Algemene componentpatronen {#general-component-patterns}

De richtlijnen in deze sectie worden geadviseerd voor om het even welk soort component, ongeacht of de component voor één enkel project specifiek is, of of de component bedoeld om over plaatsen of projecten wijd te worden hergebruikt.

### Configureerbare componenten {#configurable-components}

Componenten kunnen dialoogvensters met diverse opties hebben. Dit zou moeten worden leveraged om componenten flexibel en configureerbaar te maken, en het uitvoeren van veelvoudige componenten te vermijden die hoofdzakelijk variaties van elkaar zijn.

Als een draadframe of ontwerp variaties van vergelijkbare elementen bevat, moeten deze variaties gewoonlijk niet als verschillende componenten worden geïmplementeerd, maar als één component met opties om te kiezen tussen de variaties.

Om dit een stap verder te zetten, als de componenten over plaatsen of projecten worden opnieuw gebruikt, zie [pre-Configurable Capabilities](#pre-configurable-capabilities) sectie.

### Scheiding van bezorgdheid {#separation-of-concerns}

Het is doorgaans een goede gewoonte om de logica (of het model) van een component los te houden van de opmaaksjabloon (of weergave). Er zijn verscheidene manieren om dat te bereiken, nochtans adviseert men [Sling Models](https://sling.apache.org/documentation/bundles/models.html) voor de logica en [Taal van het Malplaatje van HTML](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) (HTL) voor de prijsverhoging te gebruiken, zoals de Componenten van de Kern ook doen.

Sling Models is een reeks aantekeningen van Java om tot noodzakelijke variabelen van POJOs gemakkelijk toegang te hebben, en daarom een eenvoudige, krachtige, en efficiënte manier te bieden om Java logica voor componenten uit te voeren.

HTML is ontworpen als een veilige en eenvoudige sjabloontaal die is toegesneden op AEM. Het kan vele vormen van logica noemen, die het zeer flexibel maakt.

## Herbruikbare componentpatronen {#reusable-component-patterns}

De richtlijnen in deze sectie kunnen ook voor om het even welk soort component worden gebruikt, maar zij zijn het meest logisch voor componenten die bedoeld zijn om over plaatsen of projecten, zoals de Componenten van de Kern worden opnieuw gebruikt. Deze richtlijnen kunnen daarom worden genegeerd voor componenten die slechts op één enkele plaats of project worden gebruikt.

### Vooraf configureerbare mogelijkheden {#pre-configurable-capabilities}

Naast het dialoogvenster Bewerken dat wordt gebruikt door auteurs van pagina&#39;s, kunnen componenten ook een ontwerpdialoogvenster hebben waarin sjabloonauteurs ze vooraf kunnen configureren. Met de [Sjablooneditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) kunt u al deze voorconfiguraties instellen. Deze worden &#39;Beleid&#39; genoemd.

Om componenten zo herbruikbaar mogelijk te maken, zouden zij van zinvolle opties moeten worden voorzien om vooraf te vormen. Hierdoor kunnen functies van de componenten worden in- of uitgeschakeld, zodat deze voldoen aan de specifieke behoeften van verschillende sites.

### Patroon proxycomponent {#proxy-component-pattern}

Aangezien elk inhoudsmiddel een `sling:resourceType` bezit heeft dat verwijzingen de component om het terug te geven, is het gewoonlijk goede praktijk om deze eigenschappen te hebben die aan plaats-specifieke componenten richten, in plaats van het richten aan componenten die door veelvoudige plaatsen worden gedeeld. Dit zal meer flexibiliteit aanbieden en inhoud het refactoring vermijden als één plaats een verschillend gedrag voor een component nodig heeft, omdat deze aanpassing dan op de plaats-specifieke component kan worden bereikt en niet de andere plaatsen zal beïnvloeden.

Nochtans, voor de project-specifieke componenten om het even welke code niet te dupliceren, zouden zij elk naar de gedeelde oudercomponent met het `sling:resourceSuperType` bezit moeten verwijzen. Deze project-specifieke componenten die het meest enkel naar oudercomponenten verwijzen worden genoemd &quot;volmachtscomponenten&quot;. Proxycomponenten kunnen volledig leeg zijn als ze de functionaliteit volledig overnemen of als ze bepaalde aspecten van de component opnieuw kunnen definiëren.

### Componentversie {#component-versioning}

Componenten moeten in de loop der tijd volledig compatibel blijven, maar soms zijn wijzigingen die niet compatibel kunnen worden gehouden noodzakelijk. Één oplossing aan deze tegengestelde behoeften is component het versioning door een aantal in hun middel typepad toe te voegen, en in volledig - gekwalificeerde de klassennamen van Java van hun implementaties te introduceren. Dit versienummer vertegenwoordigt een belangrijke versie zoals die door [semantische versiesrichtlijnen](https://semver.org/) wordt bepaald, die slechts voor veranderingen wordt verhoogd die niet achterwaarts-compatibel zijn.

Niet-compatibele wijzigingen in de volgende aspecten van componenten resulteren in een nieuwe versie ervan:

* Sling Models (volgens semantische versierichtlijnen)
* HTML-scripts en -sjablonen
* HTML-markeringen en CSS-kiezers
* JSON-vertegenwoordiging
* Dialoogvensters

Voor verdere details, zie [Versioning Beleid](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) document in GitHub.

Componentversioning creëert een vorm van contract die belangrijk is voor upgrades omdat het duidelijk maakt wanneer iets moet worden vernieuwd. Zie ook de sectie [Compatibiliteit van aanpassingen bijwerken](customizing.md#upgrade-compatibility-of-customizations), die verklaart welke overwegingen verschillende vormen van aanpassingen voor een verbetering vereisen.

Om pijnlijke inhoudsmigraties te vermijden, is het belangrijk om aan versioned componenten van inhoudsmiddelen nooit direct te richten. Als regel van duim, moet een `sling:resourceType` van de inhoud nooit een versieaantal in het hebben, of de verbeterende componenten zullen vereisen dat de inhoud wordt verfrist. De beste manier om dit te vermijden is het [hierboven beschreven Patroon van de Component van de Volmacht](#proxy-component-pattern) te volgen.

### Modelinterfaces {#model-interfaces}

Dit patroon gaat over de instructie `data-sly-use` van HTML om naar een Java-interface te wijzen, terwijl de implementatie van het Sling Model zich ook registreert bij het middeltype van de component.

Wanneer gecombineerd met het [hierboven beschreven Proxy Component Pattern](#proxy-component-pattern), biedt deze vorm van dubbele binding de volgende mooie uitbreidingspunten:

1. Een site kan de implementatie van een Sling-model opnieuw definiëren door het te registreren bij het type resource van de proxycomponent, zonder rekening te houden met het HTML-bestand, dat nog steeds naar de interface kan verwijzen.
1. Een site kan de HTML-opmaak van een component opnieuw definiëren, zonder rekening te houden met de implementatielogica waarnaar deze moet verwijzen.

## Alles samenvoegen {#putting-it-all-together}

Hieronder volgt een overzicht van het volledige middeltype bindingsstructuur, die het voorbeeld van de Component van de Kern van de Titel neemt. Het illustreert hoe een plaats-specifieke volmachtscomponent toestaat om componentenversioning op te lossen, om te vermijden dat het inhoudsmiddel om het even welk versieaantal bevat. Vervolgens wordt getoond hoe het bestand `title.html` [HTL](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) van de component wordt gebruikt voor de modelinterface, terwijl de implementatie zich bindt aan de specifieke versie van de component via [Sling Model](https://sling.apache.org/documentation/bundles/models.html) annotaties.

![Overzicht van binding met bronnen](/help/assets/chlimage_1-32.png)

Hieronder volgt een ander overzicht, dat niet de details van de implementatie POJO toont, maar onthult hoe de bijbehorende [sjablonen en het beleid](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html) van verwijzingen worden voorzien.

De eigenschap `cq:allowedTemplates` vertelt welke sjablonen voor een site kunnen worden gebruikt en de `cq:template` geeft voor elke pagina aan wat de bijbehorende sjabloon is. Elke sjabloon bestaat uit de volgende drie delen:

* **Structuur**  - Bevat de bronnen die op elke pagina moeten worden afgedwongen om aanwezig te zijn en die de auteur van de pagina niet kan verwijderen, zoals bijvoorbeeld de koptekst- en voettekstcomponenten van de pagina.
* **initial**  - Bevat de eerste inhoud die naar de pagina wordt gedupliceerd wanneer deze wordt gemaakt.
* **beleid**  - bevat voor elke component de afbeelding aan een beleid, dat de pre-configuratie van de component is. Deze afbeelding maakt het mogelijk dat beleid opnieuw wordt gebruikt in verschillende sjablonen en dus centraal wordt beheerd.

![Overzicht van sjablonen en beleid](/help/assets/screen_shot_2018-12-07at093102.png)

## Projectarchetype {#aem-project-archetype} AEM

[Het AEM Project ](/help/developing/archetype/overview.md) Archetypecureert een minimaal project van Adobe Experience Manager als uitgangspunt voor uw eigen projecten, met inbegrip van een voorbeeld van douaneHTML componenten met SlingModels voor de logica en juiste implementatie van de Componenten van de Kern met het geadviseerde volmachtspatroon.

**Volgende lezen:**

* [Met behulp van Core Components](/help/get-started/using.md)  kunt u snel aan de slag met Core Components in uw eigen project.
* [Kerncomponenten](customizing.md)  aanpassen - voor meer informatie over het opmaken en aanpassen van de kerncomponenten.
