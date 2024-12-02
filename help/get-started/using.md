---
title: Basiscomponenten gebruiken
description: 'Om aan de slag te gaan met de Componenten van de Kern in uw eigen project, zijn er drie stappen te volgen: download en installeer, creeer volmachtscomponenten, laad de kernstijlen, en sta de componenten op uw malplaatjes toe.'
role: Architect, Developer, Admin, User
exl-id: ee2d25e4-e2b8-4ecc-a62c-f0066de2bf2d
source-git-commit: 8beae61676340e8aafaee469018d865ea7ed934e
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 0%

---

# Basiscomponenten gebruiken{#using-core-components}

Om aan de slag te gaan met de Componenten van de Kern in uw eigen project, zijn er vier stappen, die individueel in secties hieronder worden beschreven:

1. [Downloaden en installeren](#download-and-install)
1. [Proxycomponenten maken](#create-proxy-components)
1. [De kernstijlen laden](#load-the-core-styles)
1. [De componenten inschakelen](#allow-the-components)

>[!TIP]
>
>Voor bredere instructies over hoe te om van begin met de projectopstelling, de Componenten van de Kern, Bewerkbare Malplaatjes, de Bibliotheken van de Cliënt en de componentenontwikkeling te beginnen, zou de volgende multi-part leerprogramma van belang kunnen zijn:\
>[ Begonnen het worden met AEM Sites - WKND Leerprogramma ](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

>[!TIP]
>
>Als u het [ AEM Archieftype van het Project gebruikt, ](/help/developing/archetype/overview.md) zijn de Componenten van de Kern automatisch inbegrepen in uw project dat op de aanbevelingen van best van de Adobe wordt gebaseerd.

## Downloaden en installeren {#download-and-install}

Een van de drijvende ideeën achter de kerncomponenten is flexibiliteit. Door nieuwe versies van de Core Components vrij te geven, kan de Adobe flexibeler zijn bij het aanbieden van nieuwe functies. Ontwikkelaars kunnen op hun beurt flexibel zijn in welke onderdelen zij kiezen om in hun projecten te integreren en hoe vaak zij deze willen bijwerken. Dit resulteert in een afzonderlijk releaseproces voor zowel AEM als de Core Components.

Daarom bepaalt de installatiestappen of u AEM als cloudservice of een service op locatie uitvoert.

### AEM as a Cloud Service {#aemaacs}

Er is geen enkele stap. AEM as a Cloud Service wordt automatisch geleverd met de nieuwste versie van de Core Components. Net zoals AEMaaCS u de nieuwste functies van AEM biedt, houdt AEMaaCS u automatisch bij met de nieuwste versie van de Core Components.

Bij het gebruik van de Core Components in AEMaaCS moet u rekening houden met een aantal punten:

* De kerncomponenten worden opgenomen in `/libs` .
* Het project bouwt pijpleiding zal waarschuwingen in het logboek produceren als het opnieuw de Componenten van de Kern als deel van `/apps` omvat en zal de versie negeren ingebed als deel van uw project.
   * In een volgende versie, zal het omvatten van de Componenten van de Kern opnieuw de pijpleiding bouwen ontbreken.
* Als uw project eerder de Componenten van de Kern in `/apps` omvatte, [ kunt u uw project moeten aanpassen.](/help/developing/overview.md#via-aemaacs)
* Hoewel de Core Components zich nu in `/libs` bevinden, wordt het niet aanbevolen om in `/apps` een overlay van hetzelfde pad te maken. [ het patroon van de volmachtscomponent ](/help/developing/guidelines.md#proxy-component-pattern) zou in plaats daarvan moeten worden gebruikt als om het even welk aspect van de componenten moet worden aangepast.
* Opdat de [ component van de Inhoudsopgave ](/help/components/tableofcontents.md) zijn inhoud teruggeeft, moet een filter in OSGi worden gevormd.
   * [ gelieve te zien de documentatie GitHub van de component ](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1) voor meer informatie.

### AEM 6.5 en eerder {#aem-65}

De kerncomponenten maken geen deel uit van de snelstartprocedure wanneer de productiemodus wordt gestart (zonder voorbeeldinhoud). Daarom moet uw eerste stap [ het recentste vrijgegeven inhoudspakket van GitHub ](https://github.com/adobe/aem-core-wcm-components/releases/latest) downloaden en het op uw AEM milieu&#39;s installeren.

Er zijn verscheidene manieren om dit te automatiseren, maar de eenvoudigste manier om een inhoudspakket op een instantie snel te installeren is door de Manager van het Pakket te gebruiken; zie [ Pakketten installeren ](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html#installing-packages). Ook, zodra u een publiceer instantie zult hebben die eveneens loopt, zult u dat pakket aan de uitgever moeten herhalen; zie [ het Repliceren van Pakketten ](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html#replicating-packages).

## Proxycomponenten maken {#create-proxy-components}

Om redenen die in de ](/help/developing/guidelines.md#proxy-component-pattern) sectie worden verklaard van het Patroon van de Component van de Volmacht [ {, moeten de Componenten van de Kern niet direct van de inhoud worden van verwijzingen voorzien. Om dat te voorkomen behoren ze allemaal tot een verborgen componentgroep ( `.core-wcm` of `.core-wcm-form` ), waardoor ze niet direct in de editor worden weergegeven.

In plaats daarvan moeten er sitespecifieke componenten worden gemaakt, die de gewenste componentnaam en -groep definiëren voor weergave bij paginaauteurs en die elk naar een Core-component verwijzen als het supertype. Deze plaats-specifieke componenten worden soms genoemd &quot;volmachtscomponenten&quot;, omdat zij om het even wat niet te hoeven bevatten en vooral te dienen om de versie van een component te bepalen voor de plaats te gebruiken. Nochtans, wanneer het aanpassen van de [ Componenten van de Kern ](/help/developing/customizing.md), spelen deze volmachtscomponenten een essentiële rol voor prijsverhoging en logische aanpassing.

Dus voor elke Core-component die voor een site moet worden gebruikt, moet u:

1. Maak een overeenkomende proxycomponent in de map met componenten van de site.

   **Voorbeeld**
Onder `/apps/my-site/components` een titelknooppunt van het type maken `cq:Component`

1. Verwijs naar de corresponderende versie van de Core Component met het supertype.

   **Voorbeeld**
Volgende eigenschap toevoegen:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. Definieer de groep, titel en eventueel beschrijving van de component. Deze waarden zijn projectspecifiek en dicteren hoe de component aan auteurs wordt blootgesteld.

   **Voorbeeld**
Voeg de volgende eigenschappen toe:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Bijvoorbeeld, bekijk de [ titelcomponent van de plaats WKND ](https://github.com/adobe/aem-guides-wknd/blob/master/ui.apps/src/main/content/jcr_root/apps/wknd/components/title/.content.xml), die een goed voorbeeld van een volmachtscomponent is die die manier wordt gebouwd.

## De kernstijlen laden {#load-the-core-styles}

1. Als nog niet gedaan, creeer de Bibliotheek van de a [ Cliënt ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html) die alle CSS en JS- dossiers bevat die voor uw plaats nodig zijn.
1. Voor de Bibliotheek van de Cliënt van uw plaats, voeg de gebiedsdelen aan de Componenten van de Kern toe die nodig zouden kunnen zijn. Dit wordt gedaan door een eigenschap `embed` toe te voegen.

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

## De componenten toestaan {#allow-the-components}

De volgende stappen worden uitgevoerd in de [ Redacteur van het Malplaatje ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html).

1. Selecteer in de Sjablooneditor de container met layout en open het bijbehorende beleid.
1. Selecteer in de lijst Toegestane componenten de proxycomponenten die eerder zijn gemaakt. Deze moeten worden weergegeven onder de componentgroep die aan deze componenten is toegewezen. Breng de wijzigingen vervolgens aan.
1. Optioneel, voor de componenten die een ontwerpdialoog hebben, kunnen zij pre-gevormd zijn.

Dat is het! Op de pagina&#39;s die met de bewerkte sjabloon zijn gemaakt, moet u nu de nieuw gemaakte componenten kunnen gebruiken.

**Lees daarna:**

* [ het Aanpassen van de Componenten van de Kern ](/help/developing/customizing.md) - leren hoe te om de kerncomponenten te stileren en aan te passen.
* [ Richtlijnen van de Component ](/help/developing/guidelines.md) - om de implementatiepatronen van de Componenten van de Kern te leren.
