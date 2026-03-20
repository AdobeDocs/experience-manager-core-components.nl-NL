---
title: Ondersteuning voor externe Assets
description: Leer hoe u de Core Component Image en Teaser Components configureert om externe middelen te ondersteunen met Dynamic Media met OpenAPI.
role: Developer, Admin, User
exl-id: b462c1f3-a6c8-4a2a-abf4-d08ec82d4371
source-git-commit: 7ba1374bd64686c2e7ac44398d77fb187ff60949
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---


# Ondersteuning voor externe Assets {#remote-assets-support}

Leer hoe u de Core Component Image en Teaser Components configureert om externe middelen te ondersteunen met Dynamic Media met OpenAPI.

>[!NOTE]
>
>Dynamic Media met OpenAPI werd voorheen Dynamische media van de volgende generatie genoemd. De functionaliteit en het gebruik zijn identiek.

## De nieuwste AEM-versie ophalen {#latest}

Ondersteuning voor externe elementen met gebruik van Dynamic Media met OpenAPI is vereist:

* AEM 6.5 SP 18+ of AEM as a Cloud Service
* Core Components release 2.23.2 of hoger

## HTTPS configureren {#https}

Over het algemeen wordt aangeraden al uw productie-AEM-instanties uit te voeren met gebruik van HTTP&#39;s. Uw lokale ontwikkelomgevingen kunnen echter niet als zodanig worden ingesteld. Externe elementen die gebruik maken van Dynamic Media met OpenAPI hebben echter HTTPS nodig om te kunnen functioneren.

[&#x200B; Gebruik deze gids &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/security/use-the-ssl-wizard.html) om HTTPS te vormen waar u wenst om verre activa, met inbegrip van ontwikkelomgevingen te gebruiken.

## OSGi configureren {#osgi}

De plaats van de verre activa moet in een configuratie worden bepaald OSGi. Vorm de **Dynamische Configuratie van de Media van de Volgende Generatie** configuratie OSGi als volgt, die de waarden met die van uw ver activamilieu vervangen.

```text
imsClient="<ims-client-name>"
enabled=B"true"
imsOrg="<ims-org>@AdobeOrg"
repositoryId="<repo-id>.adobeaemcloud.com"
```

![&#x200B; het Next Generation Dynamische de configuratievenster van Media Config OSGi &#x200B;](/help/assets/remote-assets-osgi.png)

Voor details op hoe te om OSGi te vormen, gelieve de volgende documenten te zien:

* [&#x200B; het Vormen OSGi voor Adobe Experience Manager as a Cloud Service &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi.html) voor AEM as a Cloud Service
* [&#x200B; het Vormen OSGi &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/configuring/configuring-osgi.html) voor AEM 6.5

## Configuratie controleren {#verify}

Nu kunt u controleren of de functie voor externe elementen werkt met Dynamic Media met OpenAPI. Hiertoe kunt u de WKND-voorbeeldsite en Core Components installeren.

* [&#128279;](https://github.com/adobe/aem-core-wcm-components/releases/download/core.wcm.components.reactor-2.23.2/core.wcm.components.all-2.23.2.zip) versie 2.23.2 van de Componenten van de Kern van 0&rbrace; &lbrace;wordt vereist.
* {de plaats van de Steekproef van 0} WKND [&#128279;](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-3.2.0/aem-guides-wknd.all-3.2.0-classic.zip) versie 3.2.0 of later wordt vereist.

Nadat de Core Components en de WKND-site zijn geïnstalleerd, kunt u de functie op elke WKND-pagina testen.

1. Open het AEM-exemplaar met HTTPS.

1. Een WKND-demopagina openen in de pagina-editor, zoals `https://<host>:<httpsPort>/editor.html/content/wknd/language-masters/en/magazine/arctic-surfing.html`

1. Voeg een afbeeldingscomponent aan de pagina toe.

1. In Configure dialoog van de component, uncheck de optie **erven geprezen beeld van pagina** op het **3&rbrace; lusje van Activa &lbrace;en klik** Keuze **.**

1. Als de configuratie correct is, zal een drop-down met de opties **Lokale** en **Verre** verschijnen. Selecteer **Verre**.

   ![&#x200B; Verre en lokale oogst opties voor beeldselectie &#x200B;](/help/assets/remote-asset-selection.png)

1. Er wordt een dialoogvenster geopend waarin u zich bij de externe service moet verifiëren.

1. Zodra voor authentiek verklaard, zal middelenbrowser van de verre dienst openen. Selecteer de gewenste activa en tik of klik **Uitgezocht**.

   ![&#x200B; Selecterend een ver middel &#x200B;](/help/assets/remote-asset-picker.png)

Het externe element wordt toegevoegd aan uw lokale AEM-pagina en u hebt gecontroleerd of de functie correct is geconfigureerd.

## Externe Assets gebruiken {#using}

Zodra gevormd, kunnen de verre activa worden geselecteerd waar u activa gebruikend de Componenten van de Kern zoals in de [&#x200B; Component van het Beeld &#x200B;](/help/components/image.md) en de [&#x200B; Component van de Taser &#x200B;](/help/components/teaser.md) zou selecteren.
