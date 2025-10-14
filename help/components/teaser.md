---
title: Teaser-component
description: De teaser-component kan een afbeelding, een titel, RTF-tekst en eventueel een koppeling naar andere inhoud weergeven.
role: Architect, Developer, Admin, User
exl-id: ec75e168-6f3b-4dff-8df6-06ca7dc18688
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 0%

---


# Teaser-component {#teaser-component}

De component van de Teaser Component van de Kern kan een beeld, een titel, rijke-tekst, en naar keuze verbinding aan verdere inhoud tonen.

{{traditional-aem}}

## Gebruik {#usage}

Met de component Taser kan de auteur van de inhoud eenvoudig een gummetje maken om inhoud te verfraaien met een afbeelding, titel of tekst met opmaak en een koppeling maken naar andere inhoud of andere handelingen.

De malplaatjeauteur kan de [&#x200B; ontwerpdialoog &#x200B;](#design-dialog) gebruiken om te bepalen als de opties om vraag-aan-acties tot stand te brengen en verbindingen toe te voegen beschikbaar zijn evenals het onbruikbaar maken van diverse vertoningsopties. De inhoudauteur kan [&#x200B; gebruiken vormt dialoog &#x200B;](#configure-dialog) om een beeld te plaatsen, CTAs te bepalen, titels en beschrijvingen te plaatsen, en verbindingen aan het individuele meetapparaat te vormen. Het [&#x200B; geeft dialoog uit &#x200B;](image.md#edit-dialog) van de [&#x200B; Component van het Beeld &#x200B;](image.md) kan worden betreden om het teaser beeld te wijzigen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Taser Component is v2, die in februari 2022 werd geïntroduceerd met versie 2.18.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v2 | - | Compatibel | Compatibel | Compatibel |
| [&#x200B; v1 &#x200B;](v1/teaser.md) | Compatibel | Compatibel | - | Compatibel |

## Externe Assets-ondersteuning {#remote-assets}

De Component van het Taser (van [&#x200B; versie 2.23.2 &#x200B;](/help/versions.md)) steunt verre activa. [&#x200B; Zodra gevormd, &#x200B;](/help/developing/remote-assets.md) kunt u activa van de verre dienst voor uw lasercomponent selecteren.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van het Teken te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [&#x200B; Bibliotheek van de Component &#x200B;](https://adobe.com/go/aem_cmp_library_teaser).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van het Taser [&#x200B; kan op GitHub &#x200B;](https://adobe.com/go/aem_cmp_tech_teaser_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [&#x200B; de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden &#x200B;](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

De auteur van de inhoud kan het dialoogvenster Configure gebruiken om de eigenschappen van de afzonderlijke teaser te definiëren. Er is ook een [&#x200B; uitgeeft dialoog &#x200B;](#edit-dialog) om het teasbeeld te wijzigen als men wordt geselecteerd.

### Tabblad Koppelingen {#links-tab}

![&#x200B; de bewerkingsdialoog van de Component van de Taser verbindt tabel &#x200B;](/help/assets/teaser-edit-links.png)

De teastitel, beschrijving en afbeelding kunnen worden overgenomen van de gekoppelde pagina of van de pagina die is gekoppeld in de eerste call to action. Als er geen koppeling of call to action is opgegeven, worden de titel, beschrijving en afbeelding overgenomen van de huidige pagina.

* **Verbinding** - dit dossier verbindt met een inhoudspagina, externe URL, of paginaanker.
* **Open verbinding in nieuw lusje** - indien toegelaten, zal de verbinding in een nieuwe browser tabel openen.
* **vraag-aan-acties** - Deze optie staat het verbinden aan veelvoudige bestemmingen toe.
   * De pagina die is gekoppeld in de eerste call-to-action, wordt gebruikt wanneer u de teastitel, beschrijving of afbeelding overneemt.

### Tabblad Tekst {#text-tab}

![&#x200B; de Edit van de Component van de Taser de tekst van de de dialoogdoos tabel &#x200B;](/help/assets/teaser-edit-text.png)

* **Pretitle** - de voortitel zal vóór de titel van het meetapparaat worden getoond.
* **Titel** - bepaalt een titel om als titel voor het meetapparaat te tonen.
   * **krijgt titel van verbonden pagina** - wanneer gecontroleerd, zal de titel met de verbonden titel van de pagina worden bevolkt.
* **Beschrijving** - bepaalt een beschrijving aan vertoning als onderverdeling van het gummetje.
   * **krijgt beschrijving van verbonden pagina** - wanneer gecontroleerd, zal de beschrijving met de verbonden beschrijving van de pagina worden bevolkt.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [&#x200B; Laag van Gegevens te controleren &#x200B;](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Element {#asset-tab}

![&#x200B; de bewerkingsdialoog van de Component van de Taser het beeldlusje van de dialoog &#x200B;](/help/assets/teaser-edit-image.png)

* **erven geprezen beeld van pagina** - gebruik het beeld dat in de paginaeigenschappen van de verbonden pagina wordt bepaald of de huidige pagina als niets wordt gevonden.
* **activa van het Beeld** - Daling een activa van [&#x200B; activa browser &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=nl-NL) of ontvang **doorbladert** optie om van een lokaal dossiersysteem te uploaden.
   * Tik of klik **Duidelijk** om het momenteel geselecteerde beeld te deselecteren.
   * Tik of klik **Keuze** om [&#x200B; activa browser &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=nl-NL) te openen om een beeld te selecteren.
      * Als [&#x200B; Verre Steun van Assets &#x200B;](#remote-assets) wordt toegelaten, hebt u veelvoudige opties om activa te kiezen:
         * **Lokale** selecteert van de lokale de activabibliotheek van AEM.
         * **Verre** selecteert van een Dynamische bibliotheek van Media buiten uw instantie van AEM.
   * Tik of klik **uitgeven** [&#x200B; om de vertoningen van de activa &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=nl-NL) in de activaredacteur te beheren.
* **Alternatieve tekst voor toegankelijkheid** - Dit gebied staat u toe om een beschrijving van het beeld voor visueel gehandicapte gebruikers te bepalen.
   * **erven alternatieve tekst van pagina** - Deze optie gebruikt de alternatieve beschrijving van de verbonden activawaarde van de `dc:description` meta-gegevens in DAM of van de huidige pagina als geen activa wordt verbonden.
* **verstrekt geen alternatieve tekst** - Deze optie merkt het beeld dat door ondersteunende technologieën zoals het schermlezers voor gevallen wordt genegeerd waar het beeld zuiver decoratief is of anders geen extra informatie aan de pagina overbrengt.

### Tabblad Stijlen {#styles-tab-edit}

![&#x200B; het lusje van Stijlen van uitgeeft dialoog van de Component van de Lijst van de Taser &#x200B;](/help/assets/teaser-edit-styles.png)

De Component van het Taser steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [&#x200B; ontwerpdialoog &#x200B;](#design-dialog) worden gevormd opdat het drop-down menu beschikbaar is.

## Dialoogvenster Bewerken {#edit-dialog}

De Component van het Taser delegeert beeld dat aan de [&#x200B; Component van het Beeld &#x200B;](image.md) teruggeeft. Daarom geeft [ dialoog uit ] (image.md#edit-dialog van de Component van het Beeld is beschikbaar aan de inhoudauteur om het teaser beeld te manipuleren.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de teasopties definiëren die de auteur van de inhoud heeft bij het gebruik van deze component.

### Taser Tab {#teaser-tab}

{het ontwerpdialoog van de Component van 0} Taser ![&#128279;](/help/assets/teaser-design.png)

* **vraag-aan-Acties**
   * **maak vraag-aan-Acties** onbruikbaar - verberg **vraag-aan-Acties** optie voor inhoudsauteurs
* **Elementen**
   * **Verberg pretitle** - verbergt de **optie van de Pretitle** voor inhoudsauteurs
   * **Verberg titel** - verbergt de **optie van de Titel** voor inhoudsauteurs
      * Wanneer geselecteerd wordt het **Type van Titel** verborgen
   * **Verberg beschrijving** - verberg de **optie van de Beschrijving** voor inhoudsauteurs
* **Type Standaard van Titel** - bepaalt de markering van H die door de titel van het meetapparaat moet worden gebruikt.
* **Afgevaardigde van het Beeld** - Informatieve vertoning die op welke component wijst het Teaser beeld behandeling delegeert.

### Tabblad Stijlen {#styles-tab}

De Component van het Taser steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De Component van het Taser steunt de [&#x200B; Laag van Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
