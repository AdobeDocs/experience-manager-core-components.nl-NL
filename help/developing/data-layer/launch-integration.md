---
title: De gegevenslaag van de Cliënt van Adobe gebruiken om de Componenten van de Kern en de Lancering van Adobe te integreren
description: Adobe Launch configureren voor het registreren van Core Component-gebeurtenissen met Adobe Launch
translation-type: tm+mt
source-git-commit: f930a0d6004a29369b189137dd9c52e637ea3a61
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---


# De gegevenslaag van de Cliënt van Adobe gebruiken om de Componenten van de Kern en de Lancering van Adobe te integreren {#launch-integration}

De kerncomponenten kunnen worden geïntegreerd met Adobe Launch met behulp van de Adobe Client Data Layer. In dit document wordt beschreven hoe u Adobe Launch configureert om klikgebeurtenissen voor afbeeldingscomponenten bij te houden.

Wanneer gevormd, zal de Lancering de volgende output in de browser console veroorzaken wanneer een component van het Beeld van de Kern wordt geklikt.

![Voorbeeld van uitvoer van console](/help/assets/launch-console-output.png)

## Integratie met AEM starten {#launch-aem}

De eerste keer dat Adobe Launch wordt gestart, moet deze zijn geïntegreerd met uw AEM-site.

### Stap 1 - Een integratie maken in Adobe I/O {#create-io-integration}

Meld u eerst aan bij de Adobe I/O om een integratie te configureren.

1. Ga naar `https://console.adobe.io`.
1. Meld u aan met uw Adobe-id.
1. Klik in de sectie Snel starten op Integratie **** maken.
1. Selecteer **Toegang tot API** en klik **verdergaan**.
1. Selecteer **Experience Platform Launch API** onder Adobe Experience Platform en klik op **Doorgaan**.

### Stap 2 - creeer een Configuratie IMS in AEM {#ims-configuration}

In AEM moet u de integratie bepalen die u in Adobe I/O begon te vormen.

1. Ga naar de startpagina van AEM, klik **Hulpmiddelen -> Veiligheid -> de Configuraties** van Adobe IMS.
1. Klik op **Maken**.
1. Als **Cloud-oplossing** selecteert u **Adobe Launch**.
1. Schakel **Nieuw certificaat** maken in.
1. Voer een alias voor het certificaat in, bijvoorbeeld een **aem-launch-certificate**.
1. Klik op **Certificaat** maken en klik in het pop-upvenster op **OK** om het certificaat te maken.
1. Klik op Openbare sleutel **** downloaden en klik in het pop-upvenster op **Downloaden**.

### Stap 3 - Adobe I/O-configuratie voltooien {#finish-io}

Met het certificaat en de sleutel die in de configuratie van AEM IMS worden gecreeerd, kunt u uw configuratie van Adobe I/O voltooien.

1. Ga terug naar de Adobe I/O-console zoals in [stap 1.](#create-io-integration)
1. Voer in het venster **Een nieuwe integratie** maken een naam en beschrijving in, zoals de gegevenslaag **voor het starten van** AEM.
1. Upload onder **Openbare sleutelcertificaten** het certificaat dat u in [stap 2 hebt gemaakt.](#ims-configuration)
1. Selecteer het profiel **Start - Prod**.
1. Klik op Integratie **maken**.
1. Klik op **Doorgaan naar integratiegegevens**. U hebt deze details later nodig om de IMS-configuratie in uw AEM-instantie te voltooien.

### Stap 4 - Voltooi IMS-configuratie {#finish-ims}

Met de Adobe I/O-integratiedetails kunt u de AEM IMS-configuratie voltooien.

1. Klik op het tabblad AEM op het tabblad Configuratie **technische account van** Adobe IMS van [stap 2 op](#ims-configuration) Volgende ****.
1. Voer een titel in, zoals de **IMS-configuratie voor het starten** van Adobe.
1. Kopieer op het tabblad Adobe I/O de **API-sleutel (client-id)**.
1. Plak op het tabblad AEM de voormalige gekopieerde sleutel in het veld **** API-sleutel.
1. Klik in Adobe I/O op **Client Secret** ophalen en kopieer deze.
1. Plak het op het tabblad AEM in het veld **Clientgeheim** .
1. Selecteer op het tabblad Adobe I/O het tabblad **JWT** en kopieer de URL, bijvoorbeeld `https://ims-na1.adobelogin.com`.
1. Plak op het tabblad AEM de URL in het veld **Autorisatieserver** .
1. Kopieer op het tabblad Adobe I/O de JWT-payload (de code tussen de haakjes).
1. Plak het op het tabblad AEM in het veld **Payload** .
1. Klik op **Maken** om de IMS-configuratie in AEM te maken.

### Stap 5a - Een eigenschap maken in Adobe Launch {#create-property}

Een eigenschap definieert functies die met Starten op uw site kunnen worden geïnjecteerd.

1. Ga naar Adobe Launch om `https://launch.adobe.com`.
1. Meld u aan met uw Adobe-id.
1. Klik op **Nieuwe eigenschap**.
1. Voer een naam in, zoals AEM-gegevenslaag **** starten.
1. Voer uw domein in.
1. Click **Save**.

### Stap 5b - Een regel maken bij het starten {#launch-rule}

Met de eigenschap die u hebt gemaakt, kunt u een regel definiëren die aangeeft wat er moet gebeuren wanneer een handeling plaatsvindt.

1. Klik op de nieuw toegevoegde eigenschap uit [stap 5](#create-property) AEM-gegevenslaag **** starten.
1. Selecteer het tabblad **Regels** en klik op **Nieuwe regel** maken.
1. Voer een naam in, bijvoorbeeld **klikken** op afbeelding.
1. Klik op de knop **+** onder **Gebeurtenissen**.
1. Selecteer **Kern** als **Uitbreiding**, **klik** als Type **van** Gebeurtenis en ga **.cmp-image** **** in als CSS selecteur.
1. Klik op Wijzigingen **behouden**.
1. Klik op de knop **+** onder **Handelingen**.
1. Selecteer **Kern** als **Uitbreiding**, **Douane Code** als Type **van** Actie en klik **Open Redacteur**.
1. Voer in de editor de volgende code in: `console.log("DOM click event tracked by Launch for image: ", event.target.src);`
1. Click **Save**.
1. Klik op Wijzigingen **behouden**.
1. Klik op **Opslaan** om de nieuwe regel te maken.

### Stap 6 - Publiceer de Regel van de Lancering {#publish-rule}

Als u de nieuwe regel beschikbaar wilt maken voor uw AEM-site, moet u deze publiceren.

1. Selecteer op het tabblad **Adobe Launch** het tabblad **Publishing** .
1. Klik op Nieuwe bibliotheek **toevoegen**.
1. Voer de gewenste **naam** in, bijvoorbeeld **demo-1**.
1. Selecteer voor **Milieu** de juiste keuze, zoals **Ontwikkeling (ontwikkeling)**.
1. Klik op Een bron **toevoegen**.
1. Selecteer **Regels -> afbeelding-klik -> Laatste** en klik op **Selecteren en een nieuwe revisie** maken.
1. Klik op **Opslaan en bouwen voor ontwikkeling**.
1. Klik in de pop-up op Updates **toepassen en doorgaan**.
1. Wanneer de bibliotheek is gemaakt, klikt u op het pictogram voor de ovaal en selecteert u **Verzenden voor goedkeuring**.
1. Klik in de pop-up op **Verzenden**.
1. Klik op het pictogram voor de ovaal en selecteer **Genereren voor opslaan**.
1. Wanneer de build gereed is, klikt u op het ellipspictogram en selecteert u **Goedkeuren voor publiceren**.
1. Klik in het pop-upvenster op **Goedkeuren**.
1. Klik op het pictogram voor de ovaal en selecteer **Genereren en publiceren naar productie**.
1. Klik in het pop-upvenster op **Publiceren**.

### Stap 7 - Cloud Configurations inschakelen voor uw site {#enable-configurations}

Als u de integratie wilt gebruiken, moet deze worden toegewezen in AEM als een cloudconfiguratie.

1. In the AEM console, click **Tools -> General -> Configuration Browser**.
1. Controleer de Voorbeelden **van de** Componenten van de Kern en klik **Eigenschappen**.
1. Check the **Cloud Configurations** and click **Save &amp; Close**.

### Step 8 - Create a Launch Integration with Your Site in AEM {#create-launch-integration}

Een integratie van de Lancering is noodzakelijk voor AEM om met Lancering te werken

1. In the AEM console, click **Tools -> Cloud Services -> Adobe Launch Configurations**.
1. Select **Core Component Examples** and click **Create**.
1. Enter a **Title** such as **Launch configuration**.
1. Select the IMS configuration that you created in [step 4.](#finish-ims)
1. Als **Bedrijf** selecteert u de gewenste keuze.
1. As **Property** select the newly added Launch property created in [step 5.](#create-property)
1. Move the **Include Production Code on Author** slider to the right and click **Next**.
1. Klik op **Next**.
1. Klik op **Next**.
1. Klik op **Maken**.

### Stap 9 - Verbind uw AEM Plaats met de Integratie van de Lancering {#connect-aem}

Voor AEM om de integratie van de Lancering te gebruiken moet het als wolkenconfiguratie worden toegewezen.

1. Klik in de AEM-console op **Sites** en controleer de site **Core** Components.
1. Klik op **Eigenschappen**.
1. Selecteer het tabblad **Geavanceerd** .
1. Als **Cloud-configuratie** selecteert u de Voorbeelden **van** kerncomponenten en klikt u op **Selecteren**.
1. Klik op **Opslaan en sluiten**.

### Stap 10 - Controleer of de Starterslogica is toegepast op de pagina {#verify-launch}

Test of de stappen tot nu toe succesvol zijn geweest.

1. Open de pagina Afbeelding van de Core Components Library in de voorvertoningsmodus: `http://<lhost&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Klik op een afbeelding en controleer of het bericht in de browserconsole `A Core Image was clicked` wordt weergegeven.

## De Integratie van de lancering met AEM en de Laag van Gegevens {#data-layer-launch}

Nu de Integratie tussen AEM en Lancering opstelling is, kunnen wij met de Laag van Gegevens integreren.

### Stap 1 - Een regel maken in Adobe Launch {#create-rule}

Herhaal de stappen in [stap 5](#launch-rule) om een nieuwe regel toe te voegen in Adobe Launch met de volgende waarden.

* Naam: `image-click-data-layer`
* GEBEURTENISSEN:
   * Extensie: Kern
   * Event Type: DOM Ready
* ACTIES:
   * Extensie: Kern
   * Type handeling: Aangepaste code
   * Code:

      ```
        function onImageClick(event) {
          console.log("Data layer click event tracked by Launch for image: " + event.info.path);
          console.log("dataLayer.getState(): ", adobeDataLayer.getState()); 
        }
        adobeDataLayer.addEventListener('image clicked', onImageClick);
      ```

### Stap 2 - Publiceer de Regel van de Lancering om het aan Uw Plaats van AEM ter beschikking te stellen {#publish-rule-2}

Herhaal de stappen in [stap 6](#publish-rule) om de nieuwe regel te publiceren.

### Stap 3 - verifieer dat de Logica van de Lancering op de Pagina wordt toegepast {#verify}

1. Open de pagina Afbeelding van de Core Components Library in de voorvertoningsmodus: `http://<host&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Click an image and verify that the following message is displayed in the browser console:

   ![Uitvoer gegevenslaagconsole](/help/assets/data-layer-console-output.png)
