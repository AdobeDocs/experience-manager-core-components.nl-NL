---
title: Basiscomponenten gebruiken
description: '"Om aan de slag te gaan met de Componenten van de Kern in uw eigen project, zijn er drie stappen te volgen: download en installeer, creeer volmachtscomponenten, laad de kernstijlen, en sta de componenten op uw malplaatjes toe."'
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Basiscomponenten gebruiken{#using-core-components}

Om aan de slag te gaan met de Componenten van de Kern in uw eigen project, zijn er vier stappen, die individueel in secties hieronder worden beschreven:

1. [Downloaden en installeren](#download-and-install)
1. [Proxycomponenten maken](#create-proxy-components)
1. [De kernstijlen laden](#load-the-core-styles)
1. [De componenten inschakelen](#allow-the-components)

>[!NOTE]
>
>Alternatief, voor bredere instructies op hoe te om van begin met de projectopstelling, de Componenten van de Kern, Bewerkbare Malplaatjes, de Bibliotheken van de Cliënt en componentenontwikkeling te beginnen, zou de volgende multi-part leerprogramma van belang kunnen zijn:\
>[Aan de slag met AEM-sites - WKND-zelfstudie](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

## Downloaden en installeren {#download-and-install}

Een van de drijvende ideeën achter de kerncomponenten is flexibiliteit. Als u vaker nieuwe versies van de Core Components publiceert, kan Adobe flexibeler werken met nieuwe functies. Ontwikkelaars kunnen op hun beurt flexibel zijn in welke onderdelen zij kiezen om in hun projecten te integreren en hoe vaak zij deze willen bijwerken.

Daarom maken de Core Components geen deel uit van de snelstartprocedure wanneer de productiemodus wordt gestart (zonder voorbeeldinhoud). Daarom is uw eerste stap het recentste vrijgegeven inhoudspakket van GitHub [te](https://github.com/adobe/aem-core-wcm-components/releases/latest) downloaden en het op uw milieu&#39;s te installeren AEM.

Er zijn verschillende manieren om dit te automatiseren, maar de eenvoudigste manier om een inhoudspakket op een instantie snel te installeren is door de Manager van het Pakket te gebruiken; zie Pakketten [installeren](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#installing-packages). Wanneer u een publicatie-instantie ook hebt uitgevoerd, moet u dat pakket ook naar de uitgever repliceren. zie [Replicating Packages](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#replicating-packages).

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:42:59.142-0400

Should we be promoting embedding the core-component package as an artifact in a customer application, reasoning as follows: 1) a customer application is required to leverage core components (at a minimum, proxy components must be defined) 2) a customer application must be updated to leverage new versions of core components (since it requires adjusting the sling:resourceSuperType to point at the new version of the component) It seems the only time theres an advantage to installing a release directly is if a bug-fix (non version-changing) release of core-components is cut, and it doesnt coincide with an application deployment. WDYT? For example, recommend doing this for ACS Commons which has a similar use-case (https://adobe-consulting-services.github.io/acs-aem-commons/pages/maven.html) We can of course keep the instructions for manually deploying, since some will want to do this, or the bug-fix use-case will appear.

 -->

## Proxycomponenten maken {#create-proxy-components}

Om redenen die in de sectie Patroon [van de Component van de Volmacht](/help/developing/guidelines.md#proxy-component-pattern) worden verklaard, moeten de Componenten van de Kern niet direct van de inhoud worden van verwijzingen voorzien. Om dat te vermijden, behoren zij allen tot een verborgen componentengroep ( `.core-wcm` of `.core-wcm-form`), die hen zal verhinderen direct in de redacteur te verschijnen.

In plaats daarvan moeten er sitespecifieke componenten worden gemaakt, die de gewenste componentnaam en -groep definiëren voor weergave bij paginaauteurs en die elk naar een Core-component verwijzen als het supertype. Deze plaats-specifieke componenten worden soms genoemd &quot;volmachtscomponenten&quot;, omdat zij om het even wat niet te hoeven bevatten en vooral te dienen om de versie van een component te bepalen voor de plaats te gebruiken. Nochtans, wanneer het aanpassen van de Componenten [van de](/help/developing/customizing.md)Kern, spelen deze volmachtscomponenten een essentiële rol voor prijsverhoging en logische aanpassing.

Dus voor elke Core-component die voor een site moet worden gebruikt, moet u:

1. Maak een overeenkomende proxycomponent in de map met componenten van de site.

   **Voorbeeld** onder `/apps/my-site/components` maken van een titelknooppunt van het type `cq:Component`

1. Verwijs naar de corresponderende versie van de Core Component met het supertype.

   **Voorbeeld** Volgende eigenschap toevoegen:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. Definieer de groep, titel en eventueel beschrijving van de component. Deze waarden zijn projectspecifiek en dicteren hoe de component aan auteurs wordt blootgesteld.

   **Voorbeeld** Volgende eigenschappen toevoegen:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Bijvoorbeeld, bekijk de [titelcomponent van de Web.Retail verwijzingsplaats](https://github.com/Adobe-Marketing-Cloud/aem-sample-we-retail/blob/master/ui.apps/src/main/content/jcr_root/apps/weretail/components/content/title/.content.xml), die een goed voorbeeld van een volmachtscomponent is die op die manier wordt gebouwd.

## De kernstijlen laden {#load-the-core-styles}

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:57:16.414-0400

Styles is odd in that most Core Components do not have CSS; very few even have structural CSS (breadcrumbs, list) It may be more apt to title this section: Load the Core JavaScript and CSS or Load the Core Client Libraries ?

 -->

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:41:37.115-0400

This section seems to cover the "sites" clientlibs for core components; Do we need a section for ensuring the editor clientlibs are loaded in the Page Editor? Pending: https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/issues/15

 -->

<!-- 

Comment Type: annotation
Last Modified By: cotescu
Last Modified Date: 2018-03-09T10:45:52.812-0500

Load the Core Client Libraries sounds way better

 -->

1. Als u dit nog niet hebt gedaan, maakt u een [clientbibliotheek](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/clientlibs.html) die alle CSS- en JS-bestanden bevat die nodig zijn voor uw site.
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

## De componenten toestaan {#allow-the-components}

De volgende stappen worden uitgevoerd in de [Sjablooneditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

1. Selecteer in de Sjablooneditor de container met layout en open het bijbehorende beleid.
1. Selecteer in de lijst Toegestane componenten de proxycomponenten die eerder zijn gemaakt. Deze moeten worden weergegeven onder de componentgroep die aan deze componenten is toegewezen. Breng de wijzigingen vervolgens aan.
1. Optioneel, voor de componenten die een ontwerpdialoog hebben, kunnen zij pre-gevormd zijn.

Dat is het! Op de pagina&#39;s die met de bewerkte sjabloon zijn gemaakt, moet u nu de nieuw gemaakte componenten kunnen gebruiken.

**Volgende lezen:**

* [Kerncomponenten](/help/developing/customizing.md) aanpassen - voor meer informatie over het opmaken en aanpassen van de kerncomponenten.
* [Componentrichtlijnen](/help/developing/guidelines.md) - voor het leren van de implementatiepatronen van de Core Components.
