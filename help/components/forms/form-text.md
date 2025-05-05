---
title: Formuliertekstcomponent
description: Met de component Tekst van formulier voor kerncomponenttekst kan formuliertekst worden verzonden.
role: Architect, Developer, Admin, User
exl-id: e8fa3881-51fb-4726-9654-8f93acfb7464
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Formuliertekstcomponent{#form-text-component}

Met de component Tekst van formulier voor kerncomponenttekst kan formuliertekst worden verzonden.

## Gebruik {#usage}

De component van de Tekst van de Vorm staat voor de voorlegging van verschillende types van tekst toe en is bedoeld om samen met de [ component van de vormcontainer ](form-container.md) worden gebruikt. Het type van tekstbevestiging, etiketten, en hulpberichten kunnen door de inhoudsredacteur in [ worden bepaald vormen dialoog ](#configure-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Form Text is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | Compatibel systeem met <br>[ versie 2.17.4 ](/help/versions.md) en vroeger | Compatibel | Compatibel | Compatibel |
| [ v1 ](/help/components/v1/form-text-v1.md) | Compatibel | Compatibel | - | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Tekst van de Vorm te ervaren evenals voorbeelden van zijn configuratieopties evenals uitvoer te zien HTML en JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_form_text).

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Tekst van de Vorm [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_form_text_v2) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het type tekst definiëren dat moet worden ingevoerd, evenals standaardwaarden en -labels.

### Tabblad Eigenschappen {#properties-tab}

![ Eigenschappen tabel ](/help/assets/form-text-edit-properties.png)

* **Beperking** - het type van tekst dat moet worden ingevoerd en tegen zal worden bevestigd
   * **Tekst**
   * **Gebied van de Tekst**
   * **E-mail**
   * **Tel**
   * **Datum**
   * **Aantal**
   * **Wachtwoord**
* **lijnen van de Tekst** - Aantal lijnen die op het tekstgebied (slechts getoond worden wanneer **Beperking** aan **Gebied van de Tekst** wordt geplaatst)
* **Etiket** - het etiket dat voor het gebied zal worden getoond
* **Verberg het etiket wordt getoond** - Nodig als het etiket slechts voor toegankelijkheidsdoeleinden wordt vereist en geen extra visuele informatie over het gebied impart
* **Naam van het Element** - de naam van het gebied dat met de vormgegevens wordt voorgelegd
* **Waarde** - Gebrek waarde die op het gebied vooraf bevolkt is
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Info over Tab {#about-tab}

![ Ongeveer lusje ](/help/assets/form-text-edit-about.png)

* **Bericht van de Hulp** - een wenk aan de gebruiker van wat op het gebied kan zijn ingegaan
* **het hulpbericht van de Vertoning als placeholder** - om het hulpbericht binnen de vorminput te tonen wanneer het leeg en niet geconcentreerd is

### Tabblad Restricties {#constraints-tab}

![ Beperkingen tabel ](/help/assets/form-text-edit-constraints.png)

* **Bericht van de Beperking**
   * Bericht weergegeven als knopinfo bij het verzenden van het formulier als de waarde het gekozen type niet valideert
   * Niet getoond voor **Tekst** en **de beperkingstypes van het Gebied van de Tekst**
* **Vereist** - als geselecteerd de gebruiker een waarde moet invullen alvorens de vorm voor te leggen
   * **Vereist Bericht** - Bericht dat als tooltip wordt getoond als het gebied leeg is
* **maak slechts lezen** - als geselecteerd kan de gebruiker niet de waarde van het gebied wijzigen

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component van de Tekst van de Vorm steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).
