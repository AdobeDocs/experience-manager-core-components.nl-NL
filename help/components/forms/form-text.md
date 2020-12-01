---
title: Formuliertekstcomponent
description: Met de component Tekst van formulier voor kerncomponenttekst kan formuliertekst worden verzonden.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 2%

---


# Formuliertekstcomponent{#form-text-component}

Met de component Tekst van formulier voor kerncomponenttekst kan formuliertekst worden verzonden.

## Gebruik {#usage}

Met de component Formuliertekst kunt u verschillende typen tekst verzenden. Deze component is bedoeld voor gebruik samen met de component [form container](form-container.md). Het type van tekstbevestiging, etiketten, en hulpberichten kunnen door de inhoudsredacteur in [vorm dialoog](#configure-dialog) worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Form Text is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatibel | Compatibel | Compatibel |
| [v1](/help/components/v1/form-text-v1.md) | Compatibel | Compatibel | - |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_form_text) voor meer informatie over de component Formuliertekst en voorbeelden van de configuratieopties ervan en over HTML- en JSON-uitvoer.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Tekst van de Vorm [kan op GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster {#configure-dialog} configureren

In het dialoogvenster Configureren kan de auteur van de inhoud het type tekst definiëren dat moet worden ingevoerd, evenals standaardwaarden en -labels.

### Tabblad Eigenschappen {#properties-tab}

![Eigenschappen, tabblad](/help/assets/form-text-edit-properties.png)

* **Restrictie**  - Het type tekst dat moet worden ingevoerd en waartegen moet worden gevalideerd
   * **Tekst**
   * **Tekstgebied**
   * **E-mail**
   * **Tel**
   * **Date**
   * **Getal**
   * **Wachtwoord**
* **Tekstregels**  - Aantal regels dat in het tekstgebied moet worden weergegeven (alleen wordt weergegeven wanneer  **** Restricties zijn ingesteld op  **Tekstgebied**)
* **Label**  - Het label dat voor het veld wordt weergegeven
* **Het label verbergen zodat het niet kan worden weergegeven** . Dit is nodig als het label alleen nodig is voor toegankelijkheidsdoeleinden en geen aanvullende visuele informatie over het veld bevat
* **Elementnaam**  - De naam van het veld dat met de formuliergegevens wordt verzonden
* **Waarde**  - Standaardwaarde die vooraf in het veld is ingevuld
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Info over Tab {#about-tab}

![Over, tabblad](/help/assets/form-text-edit-about.png)

* **Help-bericht**  - Een tip voor de gebruiker wat in het veld kan worden ingevoerd
* **Help-bericht weergeven als tijdelijke aanduiding**  - Het Help-bericht weergeven in de formulierinvoer als het leeg en niet gefocust is

### Tabblad Beperkingen {#constraints-tab}

![Tabblad Restricties](/help/assets/form-text-edit-constraints.png)

* **Restrictiebericht**
   * Bericht weergegeven als knopinfo bij het verzenden van het formulier als de waarde het gekozen type niet valideert
   * Niet weergegeven voor restrictietypen **Tekst** en **Tekstgebied**
* **Vereist**  - Als deze optie is geselecteerd, moet de gebruiker een waarde invullen voordat het formulier wordt verzonden
   * **Vereist bericht**  - Bericht weergegeven als knopinfo als het veld leeg blijft
* **Alleen** -lezen maken - Als deze optie is geselecteerd, kan de gebruiker de waarde van het veld niet wijzigen

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component van de Tekst van de Vorm steunt het AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
