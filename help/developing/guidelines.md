---
title: Componentrichtlijnen
description: De componenten van de Kern volgen moderne implementatiepatronen die vrij verschillend van de stichtingscomponenten zijn.
role: Architect, Developer, Admin
exl-id: e8c58fa5-c991-433c-8d38-575dacfc3433
source-git-commit: ee18626280f74a51a799f16d6bf3f5b0be9cd6b9
workflow-type: tm+mt
source-wordcount: '1267'
ht-degree: 0%

---

# Componentrichtlijnen {#component-guidelines}

De [Kernonderdelen](overview.md) moderne implementatiepatronen volgen die heel anders zijn dan de basiscomponenten.

Deze pagina verklaart deze patronen, en wanneer om hen te gebruiken om uw eigen authorable componenten te bouwen. De eerste sectie [Algemene componentpatronen](#general-component-patterns) is van toepassing op alle onderdelen, terwijl de tweede sectie [Herbruikbare componentpatronen](#reusable-component-patterns) is van toepassing op componenten die bedoeld zijn om op plaatsen of projecten, zoals de Componenten van de Kern worden hergebruikt bijvoorbeeld.

## Algemene componentpatronen {#general-component-patterns}

De richtlijnen in deze sectie worden geadviseerd voor om het even welk soort component, ongeacht of de component voor één enkel project specifiek is, of of de component bedoeld om over plaatsen of projecten wijd te worden hergebruikt.

### Configureerbare componenten {#configurable-components}

Componenten kunnen dialoogvensters met diverse opties hebben. Dit zou moeten worden leveraged om componenten flexibel en configureerbaar te maken, en het uitvoeren van veelvoudige componenten te vermijden die hoofdzakelijk variaties van elkaar zijn.

Als een draadframe of ontwerp variaties van vergelijkbare elementen bevat, moeten deze variaties gewoonlijk niet als verschillende componenten worden geïmplementeerd, maar als één component met opties om te kiezen tussen de variaties.

Als u deze stap verder wilt uitvoeren, raadpleegt u de [Vooraf configureerbare mogelijkheden](#pre-configurable-capabilities) sectie.

### Scheiding van bezorgdheid {#separation-of-concerns}

Het is doorgaans een goede gewoonte om de logica (of het model) van een component los te houden van de opmaaksjabloon (of weergave). Er zijn verschillende manieren om dat te bereiken, maar het aanbevolen is om [Verkoopmodellen](https://sling.apache.org/documentation/bundles/models.html) voor de logica en de [HTML Sjabloontaal](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html) (HTL) voor de markering, zoals de Componenten van de Kern ook doen.

Sling Models is een reeks aantekeningen van Java om tot noodzakelijke variabelen van POJOs gemakkelijk toegang te hebben, en daarom een eenvoudige, krachtige, en efficiënte manier te bieden om Java logica voor componenten uit te voeren.

HTML is ontworpen als een veilige en eenvoudige sjabloontaal die is toegesneden op AEM. Het kan vele vormen van logica noemen, die het zeer flexibel maakt.

## Herbruikbare componentpatronen {#reusable-component-patterns}

De richtlijnen in deze sectie kunnen ook voor om het even welk soort component worden gebruikt, maar zij zijn het meest logisch voor componenten die bedoeld zijn om over plaatsen of projecten, zoals de Componenten van de Kern worden opnieuw gebruikt. Deze richtlijnen kunnen daarom worden genegeerd voor componenten die slechts op één enkele plaats of project worden gebruikt.

### Vooraf configureerbare mogelijkheden {#pre-configurable-capabilities}

Naast het dialoogvenster Bewerken dat wordt gebruikt door auteurs van pagina&#39;s, kunnen componenten ook een ontwerpdialoogvenster hebben waarin sjabloonauteurs ze vooraf kunnen configureren. De [Sjablooneditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) staat aan opstelling toe al deze pre-configuraties, die &quot;Beleid&quot;worden genoemd.

Om componenten zo herbruikbaar mogelijk te maken, zouden zij van zinvolle opties moeten worden voorzien om vooraf te vormen. Hierdoor kunnen functies van de componenten worden in- of uitgeschakeld, zodat deze voldoen aan de specifieke behoeften van verschillende sites.

### Proxycomponentpatroon {#proxy-component-pattern}

Aangezien elke inhoudsbron een `sling:resourceType` eigenschap die verwijst naar de component om deze te renderen, is het meestal een goede gewoonte om deze eigenschappen te laten verwijzen naar sitespecifieke componenten in plaats van te verwijzen naar componenten die door meerdere sites worden gedeeld. Dit zal meer flexibiliteit aanbieden en inhoud het refactoring vermijden als één plaats een verschillend gedrag voor een component nodig heeft, omdat deze aanpassing dan op de plaats-specifieke component kan worden bereikt en niet de andere plaatsen zal beïnvloeden.

Nochtans, voor de project-specifieke componenten om het even welke code niet te dupliceren, zouden zij elk naar de gedeelde oudercomponent met moeten verwijzen `sling:resourceSuperType` eigenschap. Deze project-specifieke componenten die het meest enkel naar oudercomponenten verwijzen worden genoemd &quot;volmachtscomponenten&quot;. Proxycomponenten kunnen volledig leeg zijn als ze de functionaliteit volledig overnemen of als ze bepaalde aspecten van de component opnieuw kunnen definiëren.

>[!TIP]
>
>Zie de [Basiscomponenten gebruiken](/help/get-started/using.md#create-proxy-components) voor details over hoe te om volmachtscomponenten tot stand te brengen.

### Componentversie {#component-versioning}

Componenten moeten in de loop der tijd volledig compatibel blijven, maar soms zijn wijzigingen die niet compatibel kunnen worden gehouden noodzakelijk. Één oplossing aan deze tegengestelde behoeften is component het versioning door een aantal in hun middel typepad toe te voegen, en in volledig - gekwalificeerde de klassennamen van Java van hun implementaties te introduceren. Dit versienummer vertegenwoordigt een hoofdversie zoals gedefinieerd door [semantische versierichtlijnen](https://semver.org/), die alleen wordt verhoogd voor wijzigingen die niet compatibel zijn met oudere versies.

Niet-compatibele wijzigingen in de volgende aspecten van componenten resulteren in een nieuwe versie ervan:

* Sling Models (volgens semantische versierichtlijnen)
* HTML-scripts en -sjablonen
* HTML Markup en CSS-kiezers
* JSON-vertegenwoordiging
* Dialoogvensters

Zie voor meer informatie de [Versioningsbeleid](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) document in GitHub.

De versioning van de component leidt tot een vorm van contract die voor verbeteringen belangrijk is aangezien het verduidelijkt wanneer iets zou kunnen moeten worden verfrist. Zie ook de sectie [Compatibiliteit van aanpassingen upgraden](customizing.md#upgrade-compatibility-of-customizations), waarin wordt uitgelegd welke overwegingen verschillende aanpassingen vereisen voor een upgrade.

Om pijnlijke inhoudsmigraties te vermijden, is het belangrijk om aan versioned componenten van inhoudsmiddelen nooit direct te richten. Als vuistregel geldt dat een `sling:resourceType` van de inhoud mag er nooit een versienummer in staan of voor het upgraden van componenten moet de inhoud ook opnieuw worden bekeken. De beste manier om dit te voorkomen is het volgen van de [Proxycomponentpatroon](#proxy-component-pattern) hierboven beschreven.

### Modelinterfaces {#model-interfaces}

Dit patroon gaat over HTML `data-sly-use` instructie om naar een Java-interface te wijzen, terwijl de implementatie van het Sling Model ook wordt geregistreerd naar het bronnentype van de component.

Indien gecombineerd met de [Proxycomponentpatroon](#proxy-component-pattern) Hierboven beschreven, biedt deze vorm van dubbel-bindende aanbiedingen volgende aardige uitbreidingspunten:

1. Een site kan de implementatie van een Sling-model opnieuw definiëren door het te registreren bij het type resource van de proxycomponent, zonder rekening te houden met het HTML-bestand, dat nog steeds naar de interface kan verwijzen.
1. Een site kan de HTML-opmaak van een component opnieuw definiëren, zonder rekening te houden met de implementatielogica waarnaar deze moet verwijzen.

## Alles samenvoegen {#putting-it-all-together}

Hieronder volgt een overzicht van het volledige middeltype bindingsstructuur, die het voorbeeld van de Component van de Kern van de Titel neemt. Het illustreert hoe een plaats-specifieke volmachtscomponent toestaat om componentenversioning op te lossen, om te vermijden dat het inhoudsmiddel om het even welk versieaantal bevat. Vervolgens wordt getoond hoe de component `title.html` [HTL](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html) het dossier gebruikt aan de modelinterface, terwijl de implementatie aan de specifieke versie van de component door bindt [Verkoopmodel](https://sling.apache.org/documentation/bundles/models.html) annotaties.

![Overzicht van binding met bronnen](/help/assets/chlimage_1-32.png)

Hieronder volgt een ander overzicht, dat niet de details van de implementatie POJO toont, maar onthult hoe geassocieerd [sjablonen en beleidsregels](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html) worden genoemd.

De `cq:allowedTemplates` eigenschap bepaalt welke sjablonen voor een site kunnen worden gebruikt, en de `cq:template` geeft voor elke pagina aan wat de bijbehorende sjabloon is. Elke sjabloon bestaat uit de volgende drie delen:

* **structuur** - Bevat de bronnen die op elke pagina moeten worden afgedwongen om aanwezig te zijn en die de auteur van de pagina niet kan verwijderen, zoals bijvoorbeeld de pagina-kop- en voettekstcomponenten.
* **initiaal** - Bevat de eerste inhoud die op de pagina wordt gedupliceerd wanneer deze wordt gemaakt.
* **beleid** - Bevat voor elke component de afbeelding aan een beleid, dat preconfiguration van de component is. Deze afbeelding maakt het mogelijk dat beleid opnieuw wordt gebruikt in verschillende sjablonen en dus centraal wordt beheerd.

![Overzicht van sjablonen en beleid](/help/assets/screen_shot_2018-12-07at093102.png)

## Projectarchetype AEM {#aem-project-archetype}

[Het AEM Project Archetype](/help/developing/archetype/overview.md) leidt tot een minimaal Adobe Experience Manager project als uitgangspunt voor uw eigen projecten, met inbegrip van een voorbeeld van douaneHTML componenten met SlingModels voor de logica en juiste implementatie van de Componenten van de Kern met het geadviseerde volmachtspatroon.

**Volgende lezen:**

* [Basiscomponenten gebruiken](/help/get-started/using.md) - Ga aan de slag met Core Components in uw eigen project.
* [Kerncomponenten aanpassen](customizing.md) - leren hoe u de basiscomponenten kunt vormgeven en aanpassen.
