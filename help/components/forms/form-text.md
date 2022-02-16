---
title: Formuliertekstcomponent
description: Met de component Tekst van formulier voor kerncomponenttekst kan formuliertekst worden verzonden.
role: Architect, Developer, Admin, User
exl-id: e8fa3881-51fb-4726-9654-8f93acfb7464
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 2%

---

# Formuliertekstcomponent{#form-text-component}

Met de component Tekst van formulier voor kerncomponenttekst kan formuliertekst worden verzonden.

## Gebruik {#usage}

Met de component Formuliertekst kunt u verschillende typen tekst verzenden. Deze component is bedoeld voor gebruik samen met de component [formuliercontainercomponent](form-container.md). Het type tekstvalidatie, labels en Help-berichten kan worden gedefinieerd door de inhoudseditor in het dialoogvenster [dialoogvenster configureren](#configure-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Form Text is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel | Compatibel |
| [v1](/help/components/v1/form-text-v1.md) | Compatibel | Compatibel | - |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de component Formuliertekst wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_form_text).

### Technische details {#technical-details}

De meest recente technische documentatie over de component Form Text [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_form_text_v2).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het type tekst definiëren dat moet worden ingevoerd, evenals standaardwaarden en -labels.

### Tabblad Eigenschappen {#properties-tab}

![Eigenschappen, tabblad](/help/assets/form-text-edit-properties.png)

* **Restrictie** - Het type tekst dat moet worden ingevoerd en waarvoor validatie wordt uitgevoerd
   * **Tekst**
   * **Tekstgebied**
   * **E-mail**
   * **Tel**
   * **Date**
   * **Getal**
   * **Wachtwoord**
* **Tekstregels** - Aantal regels dat in het tekstgebied moet worden weergegeven (alleen wordt weergegeven wanneer **Restrictie** is ingesteld op **Tekstgebied**)
* **Label** - Het label dat voor het veld wordt weergegeven
* **Het label verbergen zodat het niet wordt weergegeven** - Nodig als het etiket alleen voor toegankelijkheidsdoeleinden vereist is en geen aanvullende visuele informatie over het veld
* **Elementnaam** - De naam van het veld dat met de formuliergegevens wordt verzonden
* **Waarde** - Standaardwaarde die vooraf is ingevuld in het veld
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Info over Tab {#about-tab}

![Over, tabblad](/help/assets/form-text-edit-about.png)

* **Help-bericht** - Een tip voor de gebruiker wat in het veld kan worden ingevoerd
* **Help-bericht weergeven als tijdelijke aanduiding** - Het Help-bericht weergeven in de formulierinvoer als deze leeg en niet geconcentreerd is

### Tabblad Restricties {#constraints-tab}

![Tabblad Restricties](/help/assets/form-text-edit-constraints.png)

* **Restrictiebericht**
   * Bericht weergegeven als knopinfo bij het verzenden van het formulier als de waarde het gekozen type niet valideert
   * Niet weergegeven voor **Tekst** en **Tekstgebied** typen beperkingen
* **Vereist** - Als deze optie is geselecteerd, moet de gebruiker een waarde invullen voordat het formulier wordt verzonden
   * **Vereist bericht** - Bericht weergegeven als knopinfo als het veld leeg blijft
* **Alleen-lezen maken** - Indien geselecteerd kan de gebruiker de waarde van het veld niet wijzigen

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component Formuliertekst ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
