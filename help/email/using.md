---
title: De e-mailkerncomponenten gebruiken
description: Leer over de basisinstallatie, de configuratie, en het gebruik van de Componenten E-mailCore.
role: Architect, Developer, Admin, User
exl-id: 0e79ca8f-eb0a-4519-b1e8-a9d3b0b99987
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 1%

---


# De e-mailkerncomponenten gebruiken {#using}

Leer over de basisinstallatie, de configuratie, en het gebruik van de Componenten E-mailCore.

## De onderdelen van de e-mailkern installeren {#installation}

De e-mailCore-componenten kunnen worden gebruikt met AEM 6.5. Zie de [ sectie van Vereisten van het document van de Inleiding van de Componenten E-mailKern ](introduction.md#requirements) voor meer informatie.

### Core Components installeren {#core-components}

De e-mailCore-componenten zijn gebaseerd op de AEM Core-componenten. Aangezien de Core Components niet bij AEM 6.5 worden geleverd, moet u eerst de AEM Core Components installeren voordat u de Email Core Components installeert.

Zie de sectie [ Download en installeer ](/help/get-started/using.md#download-and-install) sectie van het document Gebruikend de Componenten van de Kern voor details op hoe te om de Componenten van de Kern te installeren.

### E-mailkerncomponenten installeren {#email-core-components}

Wanneer de Core Components in uw exemplaar is geïnstalleerd, moet u ook de Email Core Components installeren. De e-mailkerncomponenten maken nog geen deel uit van het AEM Project Archetype. U moet ze dus handmatig aan uw project toevoegen. Volg de documentatie in [ de e-mailComponenten GitHub van de Kern om te installeren.](https://github.com/adobe/aem-core-email-components/wiki/Adding-to-Existing-Project)

U kunt dezelfde instructies volgen als u een bestaand project wilt aanpassen en de E-mailkerncomponenten wilt gebruiken.

## Configuratie {#configuration}

Na het installeren van de Componenten van de Kern, zou u twee belangrijke configuratiestappen moeten voltooien.

### Campagne configureren {#configure-campaign}

U moet de integratie tussen AEM en Adobe Campaign instellen om de twee oplossingen te laten communiceren.

* Uw Adobe Campaign-integratie configureren
   * Adobe Campaign Classic: [ Integrerend met Adobe Campaign Classic ](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignonpremise.html?lang=nl-NL)
   * Adobe Campaign Standard: [ Integrerend met Adobe Campaign Standard ](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html?lang=nl-NL)
* [ verbind de de integratieconfiguratie van Adobe Campaign ](/help/email/components/page.md#cloud-services-tab) met de inhoudspagina waar u de Componenten van de Kern E-mail zult gebruiken

### Filter voor AEM-brontype toevoegen voor e-mailcomponenten {#aem-resource-filter}

Adobe Campaign kan alleen e-mailberichten weergeven op basis van de e-mailkerncomponenten als er een filter is ingesteld in Campagne.

1. Meld u met de clientconsole aan bij Adobe Campaign als beheerder.

1. Selecteer **Hulpmiddelen** -> **Ontdekkingsreiziger** van de menubar.

1. In de ontdekkingsreiziger, navigeer aan het **Beleid** -> **Platform** -> **de knoop van Opties**.

1. Selecteer de optie `AEMResourceTypeFilter` in de lijst.

1. Op het **gebied van de Waarde**, voeg `core/email/components/page/<v1>/page` toe als het niet reeds aanwezig is.

   * Vervang `<v1>` met de huidige versie van de Componenten van de Kern E-mail [ Component van de Pagina ](/help/email/components/page.md) zoals `v1`.
   * Merk op dat de waarden op het **gebied van Waarden** komma-afgebakend moeten zijn.

1. Klik **sparen**.

## De e-mailkerncomponenten gebruiken {#using-components}

Nadat de e-mailcomponenten zijn geïnstalleerd en de integratie met Adobe Campaign is geconfigureerd, kunt u de e-mailcomponenten gebruiken om e-mailinhoud in AEM te maken en die inhoud vervolgens via Adobe Campaign naar ontvangers verzenden. Hieronder volgt een overzicht van de workflow.

| Stap | Beschrijving | Oplossing |
|---|---|---|
| 1 | Auteurs maken een ongeformuleerde hiërarchische structuur van mappen en e-mailinhoud als pagina&#39;s. | AEM |
| 2 | Gebruikend de [ malplaatjeredacteur, ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=nl-NL) de auteurs vormen een e-mailkopbal en/of footer die onder alle e-mailpagina&#39;s uit dit paginamalplaatje zou worden gedeeld. | AEM |
| 3 | De auteurs gebruiken de [ paginaredacteur ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/editing-content.html?lang=nl-NL) om e-mailinhoud tot stand te brengen gebruikend de tekstredacteur waar zij de variabelen van Adobe Campaign kunnen kiezen en de Component van de Segmentatie aan voorwaardelijke showinformatie gebruiken als de ontvanger aan bepaalde criteria voldoet. | AEM |
| 4 | Wanneer de e-mailinhoud volledig is, [ wordt een werkschema in werking gesteld ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/workflows/overview.html?lang=nl-NL) om de inhoud goed te keuren en naar Campagne te verzenden. | AEM |
| 5 | Er wordt een levering gemaakt, die een lijst met ontvangers definieert. | Campagne |
| 6 | De inhoud die in AEM is gemaakt, wordt geselecteerd als de inhoud van de levering. | Campagne |
| 7 | De inhoud wordt naar de ontvangers verzonden, waarbij de Adobe Campaign-variabelen worden vervangen door de gepersonaliseerde informatie van de ontvangers. | Campagne |

Zie de volgende bronnen voor een voorbeeld van het maken van e-mailinhoud in AEM en het leveren in Adobe Campaign.

* AEM 6.5: [ het Werken met Adobe Campaign Classic en Adobe Campaign Standard ](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html?lang=nl-NL)
