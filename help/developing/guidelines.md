---
title: Componentrichtlijnen
description: De componenten van de Kern volgen implementatiepatronen die vrij verschillend van de stichtingscomponenten zijn.
role: Architect, Developer, Admin
exl-id: e8c58fa5-c991-433c-8d38-575dacfc3433
source-git-commit: 5994133947ff697f7c866fe61598c58e37e77008
workflow-type: tm+mt
source-wordcount: '1225'
ht-degree: 0%

---

# Componentrichtlijnen {#component-guidelines}

De [ Componenten van de Kern ](overview.md) volgen implementatiepatronen die vrij verschillend van de stichtingscomponenten zijn.

Deze pagina verklaart deze patronen, en wanneer om hen te gebruiken om uw eigen authorable componenten te bouwen. De eerste sectie [ Algemene Patronen van de Component ](#general-component-patterns) is op om het even welk soort component van toepassing, terwijl de tweede sectie [ de Herbruikbare Patronen van de Component ](#reusable-component-patterns) op componenten van toepassing is die bedoeld zijn om over plaatsen of projecten, zoals de Componenten van de Kern bijvoorbeeld worden hergebruikt.

{{traditional-aem}}

## Algemene componentpatronen {#general-component-patterns}

De richtlijnen in deze sectie worden geadviseerd voor om het even welk soort component, ongeacht of de component voor één enkel project specifiek is, of of de component bedoeld om over plaatsen of projecten wijd te worden hergebruikt.

### Configureerbare componenten {#configurable-components}

Componenten kunnen dialoogvensters met diverse opties hebben. Dit zou moeten worden leveraged om componenten flexibel en configureerbaar te maken, en het uitvoeren van veelvoudige componenten te vermijden die hoofdzakelijk variaties van elkaar zijn.

Als een draadframe of ontwerp variaties van vergelijkbare elementen bevat, moeten deze variaties gewoonlijk niet als verschillende componenten worden geïmplementeerd, maar als één component met opties om te kiezen tussen de variaties.

Om dit een stap verder te nemen, als de componenten over plaatsen of projecten worden hergebruikt, zie de [ pre-Configureerbare sectie van Mogelijkheden ](#pre-configurable-capabilities).

### Scheiding van bezorgdheid {#separation-of-concerns}

Het is doorgaans een goede gewoonte om de logica (of het model) van een component los te houden van de opmaaksjabloon (of weergave). Er zijn verscheidene manieren om dat te bereiken, nochtans geadviseerd te gebruiken [ het Verdelen Modellen ](https://sling.apache.org/documentation/bundles/models.html) voor de logica en [ Taal van het Malplaatje van HTML ](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html) (HTML) voor de prijsverhoging, zoals de Componenten van de Kern ook doen.

Sling Models is een reeks aantekeningen van Java om tot noodzakelijke variabelen van POJOs gemakkelijk toegang te hebben, en daarom een eenvoudige, krachtige, en efficiënte manier te bieden om Java logica voor componenten uit te voeren.

HTL is ontworpen als een veilige en eenvoudige sjabloontaal die op AEM is afgestemd. Het kan vele vormen van logica noemen, die het zeer flexibel maakt.

## Herbruikbare componentpatronen {#reusable-component-patterns}

De richtlijnen in deze sectie kunnen ook voor om het even welk soort component worden gebruikt, maar zij zijn het meest logisch voor componenten die bedoeld zijn om over plaatsen of projecten, zoals de Componenten van de Kern worden opnieuw gebruikt. Deze richtlijnen kunnen daarom worden genegeerd voor componenten die slechts op één enkele plaats of project worden gebruikt.

### Vooraf configureerbare mogelijkheden {#pre-configurable-capabilities}

Naast het dialoogvenster Bewerken dat wordt gebruikt door auteurs van pagina&#39;s, kunnen componenten ook een ontwerpdialoogvenster hebben waarin sjabloonauteurs ze vooraf kunnen configureren. De [ Redacteur van het Malplaatje ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) staat aan opstelling toe al deze pre-configuraties, die &quot;Beleid&quot;worden genoemd.

Om componenten zo herbruikbaar mogelijk te maken, zouden zij van zinvolle opties moeten worden voorzien om vooraf te vormen. Hierdoor kunnen functies van de componenten worden in- of uitgeschakeld, zodat deze voldoen aan de specifieke behoeften van verschillende sites.

### Proxycomponentpatroon {#proxy-component-pattern}

Aangezien elke inhoudsbron een `sling:resourceType` bezit heeft dat verwijzingen de component om het terug te geven, is het gewoonlijk goede praktijk om deze eigenschappen te hebben die aan plaats-specifieke componenten richten, in plaats van het richten aan componenten die door veelvoudige plaatsen worden gedeeld. Dit zal meer flexibiliteit aanbieden en inhoud het refactoring vermijden als één plaats een verschillend gedrag voor een component nodig heeft, omdat deze aanpassing dan op de plaats-specifieke component kan worden bereikt en niet de andere plaatsen zal beïnvloeden.

Nochtans, voor de project-specifieke componenten om het even welke code niet te dupliceren, zouden zij elk naar de gedeelde oudercomponent met het `sling:resourceSuperType` bezit moeten verwijzen. Deze project-specifieke componenten die het meest enkel naar oudercomponenten verwijzen worden genoemd &quot;volmachtscomponenten&quot;. Proxycomponenten kunnen volledig leeg zijn als ze de functionaliteit volledig overnemen of als ze bepaalde aspecten van de component opnieuw kunnen definiëren.

>[!TIP]
>
>Zie [ Gebruikend de Componenten van de Kern ](/help/get-started/using.md#create-proxy-components) voor details op hoe te om volmachtscomponenten tot stand te brengen.

### Componentversie {#component-versioning}

Componenten moeten in de loop der tijd volledig compatibel blijven, maar soms zijn wijzigingen die niet compatibel kunnen worden gehouden noodzakelijk. Één oplossing aan deze tegengestelde behoeften is component het versioning door een aantal in hun middel typepad toe te voegen, en in volledig - gekwalificeerde de klassennamen van Java van hun implementaties. Dit versieaantal vertegenwoordigt een belangrijke versie zoals die door [ wordt bepaald semantische versioning richtlijnen ](https://semver.org/), die slechts voor veranderingen wordt verhoogd die niet achterwaarts-compatibel zijn.

Niet-compatibele wijzigingen in de volgende aspecten van componenten resulteren in een nieuwe versie ervan:

* Sling Models (volgens semantische versierichtlijnen)
* HTML-scripts en -sjablonen
* HTML Markup and CSS Selectors
* JSON-vertegenwoordiging
* Dialoogvensters

Voor verdere details, zie het [&#128279;](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) document van het Beleid van de Versioning  in GitHub.

De versioning van de component leidt tot een vorm van contract die voor verbeteringen belangrijk is aangezien het verduidelijkt wanneer iets zou kunnen moeten worden verfrist. Zie ook de sectie [ Verenigbaarheid van de Verbetering van Aanpassingen ](customizing.md#upgrade-compatibility-of-customizations), die verklaart welke overwegingen verschillende vormen van aanpassingen voor een verbetering vereisen.

Om pijnlijke inhoudsmigraties te vermijden, is het belangrijk om aan versioned componenten van inhoudsmiddelen nooit direct te richten. Als vuistregel geldt dat een `sling:resourceType` van de inhoud nooit een versienummer moet hebben, anders moet de inhoud bij het upgraden ook opnieuw worden bekeken. De beste manier om dit te vermijden is het [ hierboven beschreven Patroon van de Component van de Volmacht ](#proxy-component-pattern) te volgen.

### Modelinterfaces {#model-interfaces}

Dit patroon gaat over de `data-sly-use` instructie van HTML om naar een Java-interface te wijzen, terwijl de implementatie van het Sling Model zich ook registreert bij het brontype van de component.

Wanneer gecombineerd met het [ hierboven beschreven Patroon van de Component van de Volmacht ](#proxy-component-pattern), deze vorm van dubbele bindende aanbiedingen na aardige uitbreidingspunten:

1. Een site kan de implementatie van een Sling-model opnieuw definiëren door het te registreren bij het type resource van de proxycomponent, zonder rekening te houden met het HTML-bestand, dat nog steeds naar de interface kan verwijzen.
1. Een site kan de HTML-opmaak van een component opnieuw definiëren, zonder rekening te houden met de implementatielogica waarnaar deze moet verwijzen.

## Alles samenvoegen {#putting-it-all-together}

Hieronder volgt een overzicht van het volledige middeltype bindingsstructuur, die het voorbeeld van de Component van de Kern van de Titel neemt. Het illustreert hoe een plaats-specifieke volmachtscomponent toestaat om componentenversioning op te lossen, om te vermijden dat het inhoudsmiddel om het even welk versieaantal bevat. Het toont dan hoe het 2&rbrace; dossiergebruik van de component `title.html` [&#128279;](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html) HTML &lbrace;aan de modelinterface, terwijl de implementatie aan de specifieke versie van de component door [ het Schipen Model ](https://sling.apache.org/documentation/bundles/models.html) annotaties bindt.

![ Bindend Overzicht van het Middel ](/help/assets/chlimage_1-32.png)

Hieronder is een ander overzicht, dat niet de details van implementatiePOJO toont, maar openbaart hoe de bijbehorende [ malplaatjes en het beleid ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html) van verwijzingen worden voorzien.

De eigenschap `cq:allowedTemplates` geeft aan welke sjablonen voor een site kunnen worden gebruikt en de eigenschap `cq:template` geeft aan elke pagina door wat de bijbehorende sjabloon is. Elke sjabloon bestaat uit de volgende drie delen:

* **structuur** - bevat de middelen die op elke pagina zullen worden gedwongen om aanwezig te zijn, en dat de paginaauteur niet, zoals bijvoorbeeld de paginakop en footer componenten zal kunnen schrappen.
* **aanvankelijk** - bevat de aanvankelijke inhoud die aan de pagina zal worden gedupliceerd wanneer het wordt gecreeerd.
* **beleid** - bevat voor elke component de afbeelding aan een beleid, dat de pre-configuratie van de component is. Deze afbeelding maakt het mogelijk dat beleid opnieuw wordt gebruikt in verschillende sjablonen en dus centraal wordt beheerd.

![ Malplaatjes en het Overzicht van het Beleid ](/help/assets/screen_shot_2018-12-07at093102.png)

## AEM Project Archetype {#aem-project-archetype}

[ het Archetype van het Project van AEM ](/help/developing/archetype/overview.md) leidt tot een minimaal project van Adobe Experience Manager als uitgangspunt voor uw eigen projecten, met inbegrip van een voorbeeld van douaneHTML componenten met SlingModels voor de logica en juiste implementatie van de Componenten van de Kern met het geadviseerde volmachtspatroon.

**Lees daarna:**

* [ Gebruikend de Componenten van de Kern ](/help/get-started/using.md) - wordt in werking gesteld met de Componenten van de Kern in uw eigen project.
* [ het Aanpassen van de Componenten van de Kern ](customizing.md) - leren hoe te om de kerncomponenten te stileren en aan te passen.
