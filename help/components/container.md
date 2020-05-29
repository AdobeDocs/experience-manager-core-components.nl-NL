---
title: Containercomponent
description: Met de component Core Component Container kunt u een container maken voor meerdere aanvullende componenten op een pagina.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 1%

---


# Containercomponent{#container-component}

Met de component Core Component Container kunt u een container maken voor meerdere aanvullende componenten op een pagina.

## Gebruik {#usage}

Met de component Core Component Container kunt u een container maken voor meerdere aanvullende componenten op een pagina. U kunt deze component gebruiken om andere componenten te groeperen en een algemene stijl of lay-out toe te passen.

* De eigenschappen van de container kunnen in [vormen dialoog](#configure-dialog)worden geselecteerd.
* Standaardinstellingen voor de Container-component wanneer deze aan een pagina wordt toegevoegd, kunnen in het [ontwerpdialoogvenster](#design-dialog)worden gedefinieerd.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Container Component is v1, die in juni 2019 met versie 2.5.0 van de Core Components is geïntroduceerd, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel | Compatibel | Compatibel |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_container)om de Container-component te bekijken en voorbeelden van de configuratieopties en de HTML- en JSON-uitvoer te bekijken.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Container [kan op GitHub](https://adobe.com/go/aem_cmp_tech_container_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster configureren kan de auteur van de inhoud het containeritem definiëren en bepalen hoe het zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

![Dialoogvenster Containercomponent bewerken](/help/assets/container-edit.png)

* **Layout** - Met deze optie definieert u het gedrag of het lay-outgedrag van de Container-component.
   * **Eenvoudig** - Definieert een container als een eenvoudige verzameling componenten
   * **Responsief raster** - Definieert een container als een responsieve lay-out voor [AEM](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)
* **Achtergrondkleur** : kan worden gedefinieerd als vrije RGB-waarden of met de kleurkiezer, [afhankelijk van de configuratie](#background-tab)
* **Achtergrondafbeelding** - Definieert een achtergrondkleur voor de container, [afhankelijk van de configuratie](#background-tab)
* **ID** - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de Container-component gebruikt.

### Tabblad Toegestane componenten {#allowed-components-tab}

Het tabblad **Toegestane componenten** wordt gebruikt om te definiëren welke componenten door de auteur van de inhoud als items aan de Container-component kunnen worden toegevoegd.

Het tabblad Toegestane componenten werkt op dezelfde manier als het tabblad met dezelfde naam wanneer u het beleid en de eigenschappen van een container voor de layout in de Sjablooneditor [definieert.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Tabblad Standaardcomponenten {#default-components-tab}

Het tabblad Standaardcomponenten wordt gebruikt om te definiëren welke component aan de component wordt toegevoegd wanneer een bepaald elementtype op de container wordt neergezet, net als [hoe standaardcomponenten op de paginasjabloon](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)worden gedefinieerd.

### Tab Instellingen voor responsief {#responsive-settings-tab}

![Het tabblad Responsieve instellingen van het dialoogvenster Ontwerp van de Container-component](/help/assets/container-design-responsive.png)

* **Kolommen** - Hiermee definieert u het aantal kolommen in het raster van de resulterende container.

### Tabblad Achtergrond {#background-tab}

![Achtergrondtabblad van het dialoogvenster Ontwerp van de Containercomponent](/help/assets/container-design-background.png)

* **Achtergrondafbeelding**
   * **Achtergrondafbeelding** inschakelen - Selecteer deze optie om de auteur van de inhoud in staat te stellen een achtergrondafbeelding voor de container te definiëren.
* **Achtergrondkleur**
   * **Achtergrondkleur** inschakelen - Selecteer deze optie om de auteur van de inhoud in staat te stellen een achtergrondkleur voor de container te definiëren.
   * **Alleen** stalen - Selecteer deze optie als u wilt dat de auteur van de inhoud vooraf gedefinieerde kleurstalen kan selecteren voor de achtergrondkleur van de container.
      * Alleen beschikbaar als **Achtergrondkleur** inschakelen is geselecteerd
* **Stalen** toegestaan - Definieer vooraf gedefinieerde kleuren waaruit de auteur van de inhoud de achtergrondkleur van de container kan selecteren
   * Voeg met de knop **Toevoegen** een vooraf gedefinieerde kleurstaal toe. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:
   * **Waarde** - De kleur handmatig definiëren met RGB-waarden
      * Tik of klik op de kleurkiezer om een kleur eenvoudiger te selecteren door afzonderlijke RGB-waarden aan te passen of een hexadecimale waarde te definiëren.
   * **Verwijderen** - Tik of klik om een staal te verwijderen.
   * **Herschikken** - Tik of klik en sleep om de volgorde van de stalen te wijzigen.

### Tabblad Stijlen {#styles-tab}

De component Container ondersteunt het AEM- [stijlsysteem](/help/get-started/authoring.md#component-styling).
