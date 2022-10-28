---
title: De e-mailkerncomponenten gebruiken
description: Leer over de basisinstallatie, de configuratie, en het gebruik van de Componenten E-mailCore.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 1%

---


# De e-mailkerncomponenten gebruiken {#using}

Leer over de basisinstallatie, de configuratie, en het gebruik van de Componenten E-mailCore.

## E-mailkerncomponenten installeren {#installation}

De onderdelen van de e-mailkern kunnen worden gebruikt met AEM 6.5. Zie de [Sectie Vereisten van het Inleiding-document voor e-mailkerncomponenten](introduction.md#requirements) voor meer informatie .

### Core Components installeren {#core-components}

De onderdelen van de e-mailkern zijn gebaseerd op de AEM Core Components. Omdat de Core Components niet bij AEM worden geleverd, moet u eerst de AEM Core Components installeren voordat u de Email Core Components installeert.

Zie de sectie [Downloaden en installeren](/help/get-started/using.md#download-and-install) in het document Core Components (Basiscomponenten gebruiken) voor meer informatie over het installeren van de Core Components (Basiscomponenten installeren).

### E-mailkerncomponenten installeren {#email-core-components}

Wanneer de Core Components in uw exemplaar is geïnstalleerd, moet u ook de Email Core Components installeren. De onderdelen van de e-mailkern maken nog geen deel uit van het AEM Project Archetype. U moet ze dus handmatig aan uw project toevoegen. Volg de documentatie in [de te installeren wiki van GitHub van de Componenten van de E-mailKern.](https://github.com/adobe/aem-core-email-components/wiki/Adding-to-Existing-Project)

U kunt dezelfde instructies volgen als u een bestaand project wilt aanpassen en de E-mailkerncomponenten wilt gebruiken.

## Configuratie {#configuration}

Na het installeren van de Componenten van de Kern, zou u twee belangrijke configuratiestappen moeten voltooien.

### Campagne configureren {#configure-campaign}

U moet opstelling de integratie AEM-Adobe Campaign opdat de twee oplossingen communiceren.

* Uw Adobe Campaign-integratie configureren
   * Adobe Campaign Classic: [Integreren met Adobe Campaign Classic](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignonpremise.html)
   * Adobe Campaign Standard: [Integreren met Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html)
* [De Adobe Campaign-integratieconfiguratie koppelen](/help/email/components/page.md#cloud-services-tab) naar de inhoudspagina waar u de E-mailkern-componenten gaat gebruiken

### Filter voor AEM brontype toevoegen voor e-mailcomponenten {#aem-resource-filter}

Adobe Campaign kan alleen e-mailberichten weergeven op basis van de e-mailkerncomponenten als er een filter is ingesteld in Campagne.

1. Meld u met de clientconsole aan bij Adobe Campaign als beheerder.

1. Selecteren **Gereedschappen** -> **Verkenner** in de menubalk.

1. Navigeer in de verkenner naar de **Beheer** -> **Platform** -> **Opties** knooppunt.

1. Selecteer `AEMResourceTypeFilter` in de lijst.

1. In de **Waarde** veld, toevoegen `core/email/components/page/<v1>/page` indien dit nog niet het geval is.

   * Vervangen `<v1>` met de huidige versie van de Email Core Components [Pagina-component](/help/email/components/page.md) zoals `v1`.
   * De waarden in het dialoogvenster **Waarden** veld moet door komma&#39;s worden gescheiden.

1. Klikken **Opslaan**.

## De e-mailkerncomponenten gebruiken {#using-components}

Nadat de e-mailcomponenten zijn geïnstalleerd en de integratie met Adobe Campaign is geconfigureerd, kunt u de e-mailcomponenten gebruiken om e-mailinhoud in AEM te maken en die inhoud vervolgens via Adobe Campaign naar ontvangers verzenden. Hieronder volgt een overzicht van de workflow.

| Stap | Beschrijving | Oplossing |
|---|---|---|
| 1 | Auteurs maken een ongeformuleerde hiërarchische structuur van mappen en e-mailinhoud als pagina&#39;s. | AEM |
| 2 | Met de [sjablooneditor,](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) auteurs configureren een e-mailkop- en/of voettekst die wordt gedeeld door alle e-mailpagina&#39;s die uit deze paginasjabloon voortvloeien. | AEM |
| 3 | Auteurs gebruiken de [paginaeditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/editing-content.html) om e-mailinhoud te maken met de teksteditor waar ze Adobe Campaign-variabelen kunnen kiezen en met de Segmenteringscomponent informatie onder voorwaarden kunnen weergeven als de ontvanger voldoet aan bepaalde criteria. | AEM |
| 4 | Wanneer de e-mailinhoud is voltooid, [een workflow wordt uitgevoerd](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/workflows/overview.html) om de inhoud goed te keuren en naar Campagne te verzenden. | AEM |
| 5 | Er wordt een levering gemaakt, die een lijst met ontvangers definieert. | Campagne |
| 6 | De inhoud die in AEM wordt gemaakt, wordt geselecteerd als de inhoud van de levering. | Campagne |
| 7 | De inhoud wordt naar de ontvangers verzonden en vervangt de Adobe Campaign-variabelen door de gepersonaliseerde informatie van de ontvangers. | Campagne |

Zie de volgende bronnen voor een voorbeeld van het maken van e-mailinhoud in AEM en het leveren in Adobe Campaign.

* AEM as a Cloud Service: [Campagnenieuwsbrieven maken met AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/campaign/creating-newsletters.html)
* AEM 6.5: [Werken met Adobe Campaign Classic en Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html)

