---
title: Teaser-component
description: De teaser-component kan een afbeelding, een titel, RTF-tekst en eventueel een koppeling naar andere inhoud weergeven.
role: Architect, Developer, Admin, User
exl-id: ec75e168-6f3b-4dff-8df6-06ca7dc18688
source-git-commit: 5d2d79c96dc934efd7cccefb1a6a343813376483
workflow-type: tm+mt
source-wordcount: '1042'
ht-degree: 0%

---

# Teaser-component {#teaser-component}

De component van de Teaser Component van de Kern kan een beeld, een titel, rijke-tekst, en naar keuze verbinding aan verdere inhoud tonen.

## Gebruik {#usage}

Met de component Taser kan de auteur van de inhoud eenvoudig een gummetje maken om inhoud te verfraaien met een afbeelding, titel of tekst met opmaak en een koppeling maken naar andere inhoud of andere handelingen.

De malplaatjeauteur kan de [ ontwerpdialoog ](#design-dialog) gebruiken om te bepalen als de opties om vraag-aan-acties tot stand te brengen en verbindingen toe te voegen beschikbaar zijn evenals het onbruikbaar maken van diverse vertoningsopties. De inhoudauteur kan [ gebruiken vormt dialoog ](#configure-dialog) om een beeld te plaatsen, CTAs te bepalen, titels en beschrijvingen te plaatsen, en verbindingen aan het individuele meetapparaat te vormen. Het [ geeft dialoog uit ](image.md#edit-dialog) van de [ Component van het Beeld ](image.md) kan worden betreden om het teaser beeld te wijzigen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Taser Component is v2, die in februari 2022 werd geïntroduceerd met versie 2.18.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | - | Compatibel | Compatibel |
| [ v1 ](v1/teaser.md) | Compatibel | Compatibel | Compatibel |

## Externe Assets-ondersteuning {#remote-assets}

De Component van het Taser (van [ versie 2.23.2 ](/help/versions.md)) steunt verre activa. [ Zodra gevormd, ](/help/developing/remote-assets.md) kunt u activa van de verre dienst voor uw lasercomponent selecteren.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van het Teken te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_teaser).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van het Taser [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_teaser_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

De auteur van de inhoud kan het dialoogvenster Configure gebruiken om de eigenschappen van de afzonderlijke teaser te definiëren. Er is ook een [ uitgeeft dialoog ](#edit-dialog) om het teasbeeld te wijzigen als men wordt geselecteerd.

### Tabblad Koppelingen {#links-tab}

![ de bewerkingsdialoog van de Component van de Taser verbindt tabel ](/help/assets/teaser-edit-links.png)

De teastitel, beschrijving en afbeelding kunnen worden overgenomen van de gekoppelde pagina of van de pagina die is gekoppeld in de eerste aanroep naar de handeling. Als er geen koppeling of actielijn is opgegeven, worden de titel, beschrijving en afbeelding overgenomen van de huidige pagina.

* **Verbinding** - dit dossier verbindt met een inhoudspagina, externe URL, of paginaanker.
* **Open verbinding in nieuw lusje** - indien toegelaten, zal de verbinding in een nieuwe browser tabel openen.
* **vraag-aan-acties** - Deze optie staat het verbinden aan veelvoudige bestemmingen toe.
   * De pagina verbonden in de eerste vraag-aan-actie wordt gebruikt wanneer het erven van de teastitel, de beschrijving, of het beeld.

### Tabblad Tekst {#text-tab}

![ de Edit van de Component van de Taser de tekst van de de dialoogdoos tabel ](/help/assets/teaser-edit-text.png)

* **Pretitle** - de voortitel zal vóór de titel van het meetapparaat worden getoond.
* **Titel** - bepaalt een titel om als titel voor het meetapparaat te tonen.
   * **krijgt titel van verbonden pagina** - wanneer gecontroleerd, zal de titel met de verbonden titel van de pagina worden bevolkt.
* **Beschrijving** - bepaalt een beschrijving aan vertoning als onderverdeling van het gummetje.
   * **krijgt beschrijving van verbonden pagina** - wanneer gecontroleerd, zal de beschrijving met de verbonden beschrijving van de pagina worden bevolkt.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Element {#asset-tab}

![ de bewerkingsdialoog van de Component van de Taser het beeldlusje van de dialoog ](/help/assets/teaser-edit-image.png)

* **erven geprezen beeld van pagina** - gebruik het beeld dat in de paginaeigenschappen van de verbonden pagina wordt bepaald of de huidige pagina als niets wordt gevonden.
* **activa van het Beeld** - Daling een activa van [ activa browser ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of ontvang **doorbladert** optie om van een lokaal dossiersysteem te uploaden.
   * Tik of klik **Duidelijk** om het momenteel geselecteerde beeld te deselecteren.
   * Tik of klik **Keuze** om [ activa browser ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) te openen om een beeld te selecteren.
      * Als [ Verre Steun van Assets ](#remote-assets) wordt toegelaten, hebt u veelvoudige opties om activa te kiezen:
         * **Lokale** selecteert van de lokale bibliotheek van AEM activa.
         * **Verre** selecteert van een bibliotheek van Dynamic Media buiten uw AEM instantie.
   * Tik of klik **uitgeven** [ om de vertoningen van de activa ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in de activaredacteur te beheren.
* **Alternatieve tekst voor toegankelijkheid** - Dit gebied staat u toe om een beschrijving van het beeld voor visueel gehandicapte gebruikers te bepalen.
   * **erven alternatieve tekst van pagina** - Deze optie gebruikt de alternatieve beschrijving van de verbonden activawaarde van de `dc:description` meta-gegevens in DAM of van de huidige pagina als geen activa wordt verbonden.
* **verstrekt geen alternatieve tekst** - Deze optie merkt het beeld dat door ondersteunende technologieën zoals het schermlezers voor gevallen wordt genegeerd waar het beeld zuiver decoratief is of anders geen extra informatie aan de pagina overbrengt.

### Tabblad Stijlen {#styles-tab-edit}

![ het lusje van Stijlen van uitgeeft dialoog van de Component van de Lijst van de Taser ](/help/assets/teaser-edit-styles.png)

De Component van het Teken steunt het AEM [ Systeem van de Stijl.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [ ontwerpdialoog ](#design-dialog) worden gevormd opdat het drop-down menu beschikbaar is.

## Dialoogvenster Bewerken {#edit-dialog}

De Component van het Taser delegeert beeld dat aan de [ Component van het Beeld ](image.md) teruggeeft. Daarom geeft [ dialoog uit ] (image.md#edit-dialog van de Component van het Beeld is beschikbaar aan de inhoudauteur om het teaser beeld te manipuleren.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de teasopties definiëren die de auteur van de inhoud heeft bij het gebruik van deze component.

### Taser Tab {#teaser-tab}

{het ontwerpdialoog van de Component van 0} Taser ](/help/assets/teaser-design.png)![

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

De Component van het Taser steunt het AEM [ Systeem van de Stijl ](/help/get-started/authoring.md#component-styling).

## Gegevenslaag client-Adobe {#data-layer}

De Component van het Taser steunt de [ Gegevens van de Cliënt van de Adobe Laag.](/help/developing/data-layer/overview.md)
