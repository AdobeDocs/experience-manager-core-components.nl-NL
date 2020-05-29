---
title: Adobe Client Data Layer gebruiken om kerncomponenten en Adobe Analytics te integreren
description: Adobe Analytics configureren om gebeurtenissen uit de Core Component te registreren
translation-type: tm+mt
source-git-commit: f930a0d6004a29369b189137dd9c52e637ea3a61
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---


# Adobe Client Data Layer gebruiken om kerncomponenten en Adobe Analytics te integreren {#analytics-integration}

In dit document wordt beschreven hoe u een end-to-end configuratie instelt op basis van AEM, de gegevenslaag van de Adobe-client, Adobe Launch en Adobe Analytics om het volgende bij te houden:

* De pagina-id die in de gegevenslaag van de Adobe-client is opgeslagen wanneer een pagina wordt geladen
* Het afbeeldingspad dat is opgeslagen in de gegevenslaag van de Adobe-client wanneer op een afbeelding wordt geklikt

Dit gebruikt de kerncomponenten als voorbeeld maar kan voor uw eigen douanecomponenten worden gebruikt.

##  Stap 1 - De rapportsuite maken in Adobe Analytics {#create-report-suite}

Om uw gegevens te verzamelen en te analyseren, moet eerst een rapportreeks worden gecreeerd.

1. Ga naar `https://analytics.adobe.com`.
1. Meld u aan met uw Adobe-id.
1. Klik op het pictogram **Analytics** .
1. Ga naar **Beheer -> Rapportagesuites**.
1. Klik op **Nieuw maken -> Rapportsuite**.
1. Vul het formulier:
   1. **ID** rapportsuite: `yourSuiteID`
   1. **Titel** site: `Your suite description`
   1. **Tijdzone**: Indien nodig
   1. **Live datum**: datum van vandaag of in voorkomend geval
   1. **Geschatte paginaweergaven per dag**: 100 of naar gelang van het geval
1. Klik op **Rapportsuite** maken.

Als het lukt, ontvangt u het volgende bericht in het groen: `Report Suite <yourReportSuite> has been successfully created.`

## Stap 2 - Maak de Reeks van het Rapport zichtbaar {#make-visible}

Als u de nieuwe rapportsuite wilt gebruiken, moet deze zichtbaar zijn.

1. Ga naar `https://adminconsole.adobe.com`.
1. Meld u aan met uw Adobe-id.
1. Klik op de **Adobe Analytics - &lt;yourSite>** -kaart
1. Klik op de koppeling **Adobe Analytics - &lt;yourSite>**
1. Het tabblad **Machtigingen** selecteren
1. Klik op de knop **Bewerken** van de rij **Rapporten** .
1. Klik op de knop **+** van de rapportsuite die u in [stap 1](#create-report-suite) hebt gemaakt om deze toe te voegen aan de categorie Items **voor** opgenomen machtigingen.
1. Click **Save**.

## Stap 3 - Integreer uw AEM-site met het starten van Adobe {#integrate-launch}

Starten moet zijn geïntegreerd met uw AEM-site om gegevens te genereren.

Voer de stappen in de Adobe Client Data Layer [gebruiken uit om Core Components en Adobe Launch](launch-integration.md) -document te integreren.

## Stap 4 - De Adobe Analytics-extensie installeren en configureren in Adobe Launch {#install-extension}

Met de extensie Adobe Analytics kunt u Analytics integreren met Launch.

1. Selecteer in Adobe Launch de nieuwe eigenschap die u in [stap 3 hebt gemaakt.](#integrate-launch)
1. Navigeer naar het tabblad **Extensies** en selecteer **Catalogus**.
1. Zoek naar **Adobe Analytics**.
1. Klik op **Installeren**.
1. Configureer de extensie.
   1. Voer de **Analytics Report Suite-id** in die in [stap 1](#create-report-suite) voor de juiste omgevingen is gemaakt
   1. Tekenset **** instellen op UTF-8
1. Klik op Opslaan

## Stap 5 - Een gegevenselement maken in Adobe Launch voor de pagina-id {#create-data-element}

Er is een gegevenselement vereist in Launch om de pagina-id te kunnen bijhouden.

1. Selecteer in Adobe Launch de eigenschap die u in [stap 3 hebt gemaakt.](#integrate-launch)
1. Selecteer het tabblad **Gegevenselementen** en klik op Gegevenselement **** toevoegen:
   1. **Naam**: `dl-page-id`
   1. **Extensie**: **Kern**
   1. **Type** gegevenselement: **Aangepaste code**
1. Klik op Editor **openen**
1. Voer in de editor de code in: `return adobeDataLayer.getState().page.id;`
1. Click **Save**.
1. Klik op **Opslaan** om het gegevenselement te maken.

## Stap 6 - Maak een regel in Adobe Launch om de pagina-id bij te houden in Analytics {#track-page}

Regels staan het volgen van het doorbladeren attributen zoals pagina ID in Analytics toe.

Herhaal de stappen in deel 5b van de Adobe Client Data Layer [Using Core Components and Adobe Launch](launch-integration.md#launch-rule) document om de volgende regel toe te voegen in Adobe Launch:

* **Naam**: `track-dl-page-id`
* GEBEURTENISSEN:
   * **Extensie**: **Kern**
   * **Type** gebeurtenis: **Pagina onder**
* ACTIE 1:
   * **Extensie**: **Adobe Analytics**
   * **Type** handeling: **Variabelen instellen**
   * **prop1**: `%dl-page-id%`
* ACTIE 2:
   * **Extensie**: **Adobe Analytics**
   * **Type** handeling: **Band verzenden**
   * Check **s.t(): Gegevens verzenden naar Adobe Analytics en deze behandelen als paginaweergave**

## Stap 7 - Maak een regel in Adobe Launch om de gebeurtenis voor klikken op afbeelding te registreren {#register-click}

De regels staan het volgen van het doorbladeren attributen zoals klikgebeurtenissen in Analytics toe.

Herhaal de stappen in deel 5b van de Adobe Client Data Layer [Using Core Components and Adobe Launch](launch-integration.md#launch-rule) document om de volgende regel toe te voegen in Adobe Launch:

* **Naam**: `register-dl-image-click`
* GEBEURTENISSEN:
   * **Extensie**: **Kern**
   * **Type** gebeurtenis: **Pagina onder**
* ACTIE 1:
   * **Extensie**: **Kern**
   * **Type** handeling: **Aangepaste code**
   * Editor: Voer de volgende code in

      ```
      var myListener = function(event) {
        _satellite.track('dlImageClicked', event.info.path);
      };
      adobeDataLayer.addEventListener('image clicked', myListener());
      ```

## Stap 8 - Maak een regel in Adobe Launch om de gebeurtenis voor klikken op afbeelding bij te houden in Analyse {#track-click}

De regels staan het volgen van het doorbladeren attributen zoals klikgebeurtenissen in Analytics toe.

Herhaal de stappen in deel 5b van de Adobe Client Data Layer [Using Core Components and Adobe Launch](launch-integration.md#launch-rule) document om de volgende regel toe te voegen in Adobe Launch:

* **Naam**: `track-dl-image-click`
* GEBEURTENISSEN:
   * **Extensie**: **Kern**
   * **Type** gebeurtenis: **Directe oproep**
   * **Id**: `dlImageClicked`
* ACTIE 1:
   * **Extensie**: **Adobe Analytics**
   * **Type** handeling: **Variabelen instellen**
   * **prop2**: Instellen als `%event.detail%`
* ACTIE 2:
   * **Extensie**: **Adobe Analytics**
   * **Type** handeling: **Band verzenden**
   * Check **s.t(): Gegevens verzenden naar Adobe Analytics en deze behandelen als paginaweergave**

## Stap 9 - Publiceer de Code van de Lancering aan Uw Website {#publish-launch}

Om het volgen van deze regels en eigenschappen in Lancering toe te laten, moet de code worden gepubliceerd.

1. Selecteer op het tabblad **Adobe Launch** het tabblad **Publishing** .
1. Klik op Nieuwe bibliotheek **toevoegen**.
1. Als **naam** voert u in: `data-layer-analytics-1`.
1. Als **Milieu** selecteer **Ontwikkeling (ontwikkeling)**.
1. Klik op Alle gewijzigde bronnen **toevoegen**.
1. Voor elk van de drie regels (`track-dl-page-id`, `register-dl-image-click` en `track-dl-image-click`):
1. Selecteer **Regels -> regel -> Laatste** en klik op **Selecteren en een nieuwe revisie** maken.
1. Klik op **Opslaan en bouwen voor ontwikkeling**.

## Stap 10 - Trigger Uw pagina om informatie naar de Analyse van Adobe te verzenden {#trigger-page}

In deze stap installeert u de Chrome-extensie **Launch en DTM Switch**. Met deze uitbreiding moet u slechts de code van de Lancering aan het milieu van de Ontwikkeling bouwen en opstellen. Het is niet nodig om de het Opvoeren en milieu&#39;s van de Productie op te stellen.

1. Installeer de Chrome-extensie **Launch en de DTM-switch** van Discovery.
1. Klik het pictogram van de Schakelaar **van de** Lancering en plaats zuivert aan *AAN*.
1. Laad de pagina opnieuw `http://<host>:<port>/content/core-components-examples/library/image.html`.
1. Open de browserconsole en u zou iets gelijkaardigs aan het volgende moeten zien.

![Uitvoer van analyseconsole](/help/assets/analytics-console-output.png)

>[!TIP]
>
>U kunt ook de extensie **Experience Cloud Debugger** voor Chrome installeren om specifieke informatie over de pagina weer te geven voor Adobe Launch en Analytics.

## Stap 11 - De bijgehouden informatie weergeven in Adobe Analytics {#view-info}

U kunt nu de gebeurtenissen weergeven die u in Adobe Analytics hebt geactiveerd.

1. Ga naar `https://analytics.adobe.com`.
1. Meld u aan met uw Adobe-id.
1. Klik op het pictogram **Analytics** .
1. Selecteer het tabblad **Rapporten** .
1. Selecteer in de vervolgkeuzelijst rechtsboven de rapportsuite die u in [stap 1 hebt gemaakt.](#create-report-suite)
1. In de eerste kolom selecteert u **Aangepast verkeer -> Aangepast verkeer 1-10 -> Aangepast inzicht 1** om de bijgehouden pagina-id&#39;s (paden) weer te geven die in de gegevenslaag zijn opgeslagen. Het moet er ongeveer als volgt uitzien.

   ![Aangepast inzicht 1](/help/assets/custom-insight-1.png)

1. Open Inzicht 2 **van de** Douane om de gevolgde beeldwegen te bekijken die in de Laag van Gegevens worden opgeslagen. Het moet er ongeveer als volgt uitzien.

   ![Aangepast inzicht 2](/help/assets/custom-insight-2.png)
