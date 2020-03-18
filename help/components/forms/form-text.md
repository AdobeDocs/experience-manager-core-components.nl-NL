---
title: Formuliertekstcomponent
description: Met de component Tekst van formulier voor kerncomponenttekst kan formuliertekst worden verzonden.
translation-type: tm+mt
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Formuliertekstcomponent{#form-text-component}

Met de component Tekst van formulier voor kerncomponenttekst kan formuliertekst worden verzonden.

## Gebruik {#usage}

Met de component Formuliertekst kunt u verschillende typen tekst verzenden. Deze component is bedoeld voor gebruik samen met de [component](form-container.md)van de formuliercontainer. Het type van tekstbevestiging, etiketten, en hulpberichten kunnen door de inhoudsredacteur in [vormen dialoog](#configure-dialog)worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Form Text is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatibel | Compatibel | Compatibel | Compatibel |
| [v1](/help/components/v1/form-text-v1.md) | Compatibel | Compatibel | Compatibel | - |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_form_text)voor meer informatie over de component Formuliertekst en voorbeelden van de configuratieopties ervan en over HTML- en JSON-uitvoer.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Tekst van de Vorm [kan op GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het type tekst definiëren dat moet worden ingevoerd, evenals standaardwaarden en -labels.

### Hoofdtabblad {#main-tab}

![](/help/assets/chlimage_1-23.png)

* **Restrictie** Het type tekst dat moet worden ingevoerd en waarvoor validatie wordt uitgevoerd
   * **Tekst**
   * **Tekstgebied**
   * **E-mail**
   * **Tel**
   * **Date**
   * **Getal**
   * **Wachtwoord**
* **Tekstregels** Aantal regels dat in het tekstgebied moet worden weergegeven (alleen wordt weergegeven wanneer **Restrictie** is ingesteld op **Tekstgebied**)
* **Label** Het label dat voor het veld wordt weergegeven
* **Verberg het label zodat het niet wordt weergegeven** Nodig als het label alleen nodig is voor toegankelijkheidsdoeleinden en geen aanvullende visuele informatie over het veld bevat
* **Elementnaam** De naam van het veld dat met de formuliergegevens wordt verzonden
* **Waarde** standaardwaarde die vooraf in het veld is ingevuld

### Info over Tab {#about-tab}

![](/help/assets/chlimage_1-24.png)

* **Help Message** A hint to the user of what can enter in the field
* **Help-bericht weergeven als tijdelijke aanduiding** Om het Help-bericht in de formulierinvoer weer te geven wanneer het leeg is en geen focus heeft

### Tabblad Restricties {#constraints-tab}

![](/help/assets/chlimage_1-25.png)

* **Restrictiebericht**
   * Bericht weergegeven als knopinfo bij het verzenden van het formulier als de waarde het gekozen type niet valideert
   * Niet weergegeven voor restrictietypen **Tekst** en **Tekstgebied**
* **Vereist** als deze optie is geselecteerd, moet de gebruiker een waarde invullen voordat het formulier wordt verzonden
* **Alleen**-lezen maken Als deze optie is geselecteerd, kan de gebruiker de waarde van het veld niet wijzigen

## Ontwerpdialoogvenster {#design-dialog}

Er is geen ontwerpdialoogvenster voor de component Formuliertekst.
