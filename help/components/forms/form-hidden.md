---
title: Verborgen component van formulier
description: Met de component Core Component Form Hidden kunt u een verborgen veld weergeven.
translation-type: tm+mt
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Verborgen component van formulier{#form-hidden-component}

Met de component Core Component Form Hidden kunt u een verborgen veld weergeven.

## Gebruik {#usage}

Met de component Core Component Form Hidden kunt u verborgen velden maken die informatie over de huidige pagina teruggeven aan AEM. Deze component is bedoeld voor gebruik samen met de [component](form-container.md)van de formuliercontainer.

De veldeigenschappen kunnen door de inhoudsredacteur in [vormen dialoog](form-hidden.md)worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de component Form Hidden is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatibel | Compatibel | Compatibel | Compatibel |
| [v1](/help/components/v1/form-hidden-v1.md) | Compatibel | Compatibel | Compatibel | - |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_form_hidden)voor meer informatie over de component Formulier Verborgen en voorbeelden van de bijbehorende configuratieopties en over HTML- en JSON-uitvoer.

### Technische details {#technical-details}

De recentste technische documentatie over de Vorm Verborgen Component [kan op GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud de parameters van het verborgen veld definiëren.

![](/help/assets/chlimage_1-26.png)

* **Naam** De naam van het veld dat met de formuliergegevens wordt verzonden
* **Waarde** De waarde van het veld dat met de formuliergegevens wordt verzonden
* **Id** De id moet uniek zijn op de pagina en kan worden gebruikt om scripts aan dit formulierveld te binden

Omdat de component Formulier verborgen normaal geen zichtbare kenmerken heeft, geeft de tijdelijke aanduiding van de component in de editor de waarden van de velden **Naam** en **Waarde** weer als deze zijn toegewezen, zodat de auteur de juiste component Formulier verborgen kan identificeren.

![](/help/assets/screenshot_2018-10-19at094927.png)

## Ontwerpdialoogvenster {#design-dialog}

Er is geen dialoogvenster voor het ontwerp van de component Formulier verborgen.
