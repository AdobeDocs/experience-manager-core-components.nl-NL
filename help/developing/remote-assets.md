---
title: Ondersteuning voor externe Assets
description: Leer hoe u de Core Component Image en Teaser Components configureert om externe middelen te ondersteunen met Dynamic Media met OpenAPI.
role: Architect, Developer, Admin, User
exl-id: b462c1f3-a6c8-4a2a-abf4-d08ec82d4371
source-git-commit: 36ef19d5b29fe21f86309719d1e3f6588e31a93b
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# Ondersteuning voor externe Assets {#remote-assets-support}

Leer hoe u de Core Component Image en Teaser Components configureert om externe middelen te ondersteunen met Dynamic Media met OpenAPI.

>[!NOTE]
>
>Dynamic Media met OpenAPI werd voorheen Dynamic Media van de volgende generatie genoemd. De functionaliteit en het gebruik zijn identiek.

## De nieuwste AEM versie ophalen {#latest}

Ondersteuning voor externe middelen met Dynamic Media met OpenAPI vereist:

* AEM 6.5 SP 18+ of AEM as a Cloud Service
* Core Components release 2.23.2 of hoger

## HTTPS configureren {#https}

Het wordt over het algemeen aanbevolen om al uw productie AEM instanties in werking te stellen die HTTPs gebruiken. Uw lokale ontwikkelomgevingen kunnen echter niet als zodanig worden ingesteld. Externe elementen die Dynamic Media met OpenAPI gebruiken, kunnen echter alleen functioneren als HTTPS is vereist.

[ Gebruik deze gids ](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/security/use-the-ssl-wizard.html) om HTTPS te vormen waar u wenst om verre activa, met inbegrip van ontwikkelomgevingen te gebruiken.

## OSGi configureren {#osgi}

De plaats van de verre activa moet in een configuratie worden bepaald OSGi. Vorm de **Volgende Configuratie van Dynamic Media Config van de Generatie** OSGi configuratie als volgt, die de waarden met die van uw ver activamilieu vervangen.

```text
imsClient="<ims-client-name>"
enabled=B"true"
imsOrg="<ims-org>@AdobeOrg"
repositoryId="<repo-id>.adobeaemcloud.com"
```

![ het volgende de configuratievenster van Dynamic Media Config OSGi van de Generatie ](/help/assets/remote-assets-osgi.png)

Voor details op hoe te om OSGi te vormen, gelieve de volgende documenten te zien:

* [ het Vormen OSGi voor Adobe Experience Manager as a Cloud Service ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi.html) voor AEM as a Cloud Service
* [ Vormend OSGi ](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/configuring/configuring-osgi.html) voor AEM 6.5

## Configuratie controleren {#verify}

Nu kunt u controleren of de functie voor externe middelen werkt met Dynamic Media met OpenAPI. Hiertoe kunt u de WKND-voorbeeldsite en Core Components installeren.

* ](https://github.com/adobe/aem-core-wcm-components/releases/download/core.wcm.components.reactor-2.23.2/core.wcm.components.all-2.23.2.zip) versie 2.23.2 van de Componenten van de Kern van 0} {wordt vereist.[
* {de plaats van de Steekproef van 0} WKND ](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-3.2.0/aem-guides-wknd.all-3.2.0-classic.zip) versie 3.2.0 of later wordt vereist.[

Nadat de Core Components en de WKND-site zijn geïnstalleerd, kunt u de functie op elke WKND-pagina testen.

1. Open de AEM instantie met HTTPS.

1. Een WKND-demopagina openen in de pagina-editor, zoals `https://<host>:<httpsPort>/editor.html/content/wknd/language-masters/en/magazine/arctic-surfing.html`

1. Voeg een afbeeldingscomponent aan de pagina toe.

1. In Configure dialoog van de component, uncheck de optie **erven geprezen beeld van pagina** op het **3} lusje van Activa {en klik** Keuze **.**

1. Als de configuratie correct is, zal een drop-down met de opties **Lokale** en **Verre** verschijnen. Selecteer **Verre**.

   ![ Verre en lokale oogst opties voor beeldselectie ](/help/assets/remote-asset-selection.png)

1. Er wordt een dialoogvenster geopend waarin u zich bij de externe service moet verifiëren.

1. Zodra voor authentiek verklaard, zal middelenbrowser van de verre dienst openen. Selecteer de gewenste activa en tik of klik **Uitgezocht**.

   ![ Selecterend een ver middel ](/help/assets/remote-asset-picker.png)

Het externe element wordt toegevoegd aan uw lokale AEM en u hebt gecontroleerd dat de functie correct is geconfigureerd.

## Externe Assets gebruiken {#using}

Zodra gevormd, kunnen de verre activa worden geselecteerd waar u activa gebruikend de Componenten van de Kern zoals in de [ Component van het Beeld ](/help/components/image.md) en de [ Component van de Taser ](/help/components/teaser.md) zou selecteren.
