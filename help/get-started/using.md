---
title: Basiscomponenten gebruiken
description: '"Om aan de slag te gaan met de Componenten van de Kern in uw eigen project, zijn er drie stappen te volgen: download en installeer, creeer volmachtscomponenten, laad de kernstijlen, en sta de componenten op uw malplaatjes toe."'
translation-type: tm+mt
source-git-commit: 78202dc777b90f795f66873921c55e21ef8a239c
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 0%

---


# Core Components{#using-core-components} gebruiken

Om aan de slag te gaan met de Componenten van de Kern in uw eigen project, zijn er vier stappen, die individueel in secties hieronder worden beschreven:

1. [Downloaden en installeren](#download-and-install)
1. [Proxycomponenten maken](#create-proxy-components)
1. [De kernstijlen laden](#load-the-core-styles)
1. [De componenten inschakelen](#allow-the-components)

>[!NOTE]
>
>Alternatief, voor bredere instructies op hoe te om van begin met de projectopstelling, de Componenten van de Kern, Bewerkbare Malplaatjes, de Bibliotheken van de Cliënt en componentenontwikkeling te beginnen, zou de volgende multi-part leerprogramma van belang kunnen zijn:\
>[Aan de slag met AEM Sites - WKND-zelfstudie](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

## {#download-and-install} downloaden en installeren

Een van de drijvende ideeën achter de kerncomponenten is flexibiliteit. Door nieuwe versies van de Core Components vrij te geven, kan Adobe zich flexibeler opstellen bij het aanbieden van nieuwe functies. Ontwikkelaars kunnen op hun beurt flexibel zijn in welke onderdelen zij kiezen om in hun projecten te integreren en hoe vaak zij deze willen bijwerken.

Daarom maken de Core Components geen deel uit van de snelstartprocedure wanneer de productiemodus wordt gestart (zonder voorbeeldinhoud). Daarom is uw eerste stap aan [download het recentste vrijgegeven inhoudspakket van GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) en om het op uw AEM milieu&#39;s te installeren.

Er zijn verschillende manieren om dit te automatiseren, maar de eenvoudigste manier om een inhoudspakket op een instantie snel te installeren is door de Manager van het Pakket te gebruiken; zie [Pakketten installeren](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#installing-packages). Wanneer u een publicatie-instantie ook hebt uitgevoerd, moet u dat pakket ook naar de uitgever repliceren. zie [Replicating Packages](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#replicating-packages).

## Proxycomponenten maken {#create-proxy-components}

Om redenen die worden toegelicht in de sectie [Proxycomponentpatroon](/help/developing/guidelines.md#proxy-component-pattern), mogen kerncomponenten niet rechtstreeks vanuit de inhoud worden verwezen. Om dat te vermijden, behoren zij allen tot een verborgen componentengroep ( `.core-wcm` of `.core-wcm-form`), die hen zal verhinderen direct in de redacteur te verschijnen.

In plaats daarvan moeten er sitespecifieke componenten worden gemaakt, die de gewenste componentnaam en -groep definiëren voor weergave bij paginaauteurs en die elk naar een Core-component verwijzen als het supertype. Deze plaats-specifieke componenten worden soms genoemd &quot;volmachtscomponenten&quot;, omdat zij om het even wat niet te hoeven bevatten en vooral te dienen om de versie van een component te bepalen voor de plaats te gebruiken. Nochtans, wanneer het aanpassen van [de Componenten van de Kern ](/help/developing/customizing.md), spelen deze volmachtscomponenten een essentiële rol voor prijsverhoging en logische aanpassing.

Dus voor elke Core-component die voor een site moet worden gebruikt, moet u:

1. Maak een overeenkomende proxycomponent in de map met componenten van de site.

   ****
ExampleUnder  `/apps/my-site/components` maakt een titelknooppunt van het type  `cq:Component`

1. Verwijs naar de corresponderende versie van de Core Component met het supertype.

   ****
ExampleAdd volgende eigenschap:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. Definieer de groep, titel en eventueel beschrijving van de component. Deze waarden zijn projectspecifiek en dicteren hoe de component aan auteurs wordt blootgesteld.

   ****
ExampleAdd volgende eigenschappen:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Kijk bijvoorbeeld naar de [titelcomponent van de WKND-site](https://github.com/adobe/aem-guides-wknd/blob/master/ui.apps/src/main/content/jcr_root/apps/wknd/components/title/.content.xml), die een goed voorbeeld is van een proxycomponent die op die manier is gemaakt.

## De kernstijlen {#load-the-core-styles} laden

1. Als dit nog niet het geval is, maakt u een [Clientbibliotheek](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/clientlibs.html) die alle CSS- en JS-bestanden bevat die nodig zijn voor uw site.
1. Voor de Bibliotheek van de Cliënt van uw plaats, voeg de gebiedsdelen aan de Componenten van de Kern toe die nodig zouden kunnen zijn. Dit wordt gedaan door een `embed` bezit toe te voegen.

   Als u bijvoorbeeld de clientbibliotheken van alle v1 Core-componenten wilt opnemen, moet u de volgende eigenschap toevoegen:

   ```shell
   embed="[  
   core.wcm.components.image.v1,  
   core.wcm.components.list.v1,  
   core.wcm.components.breadcrumb.v1,  
   core.wcm.components.form.container.v1,  
   core.wcm.components.form.text.v1  
   ]"
   ```

Controleer of uw proxycomponenten en clientbibliotheken zijn geïmplementeerd in uw AEM-omgeving voordat u naar de volgende sectie gaat.

## De componenten {#allow-the-components} toestaan

De volgende stappen worden uitgevoerd in [Sjablooneditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

1. Selecteer in de Sjablooneditor de container met layout en open het bijbehorende beleid.
1. Selecteer in de lijst Toegestane componenten de proxycomponenten die eerder zijn gemaakt. Deze moeten worden weergegeven onder de componentgroep die aan deze componenten is toegewezen. Breng de wijzigingen vervolgens aan.
1. Optioneel, voor de componenten die een ontwerpdialoog hebben, kunnen zij pre-gevormd zijn.

Dat is het! Op de pagina&#39;s die met de bewerkte sjabloon zijn gemaakt, moet u nu de nieuw gemaakte componenten kunnen gebruiken.

**Volgende lezen:**

* [Kerncomponenten](/help/developing/customizing.md)  aanpassen - voor meer informatie over het opmaken en aanpassen van de kerncomponenten.
* [Componentrichtlijnen](/help/developing/guidelines.md)  - om de implementatiepatronen van de kerncomponenten te leren.
