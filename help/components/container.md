---
title: Containercomponent
description: Met de component Core Component Container kunt u een container maken voor meerdere aanvullende componenten op een pagina.
role: Architect, Developer, Admin, User
exl-id: 53c7190d-44cb-42ff-bc1a-483c7875bcf8
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# Containercomponent{#container-component}

Met de component Core Component Container kunt u een container maken voor meerdere aanvullende componenten op een pagina.

## Gebruik {#usage}

Met de component Core Component Container kunt u een container maken voor meerdere aanvullende componenten op een pagina. U kunt deze component gebruiken om andere componenten te groeperen en een algemene stijl of lay-out toe te passen.

* De eigenschappen van de container kunnen worden geselecteerd in het dialoogvenster [dialoogvenster configureren](#configure-dialog).
* De standaardinstellingen voor de Container-component wanneer deze aan een pagina wordt toegevoegd, kunnen worden gedefinieerd in het dialoogvenster [ontwerpdialoogvenster](#design-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Container Component is v1, die in juni 2019 met versie 2.5.0 van de Core Components is geïntroduceerd, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de Container-component wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_container).

## Technische details {#technical-details}

De meest recente technische documentatie over de Container Component [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_container_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster configureren kan de auteur van de inhoud het containeritem definiëren en bepalen hoe het zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

![Dialoogvenster Containercomponent bewerken](/help/assets/container-edit.png)

* **Layout** - Met deze optie definieert u het gedrag of het lay-outgedrag van de Container-component.
   * **Eenvoudig** - Definieert een container als een eenvoudige verzameling componenten
   * **Responsief raster** - Definieert een container als een [Responsieve lay-out AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)
* **Achtergrondkleur** - Definieerbaar als vrije-vorm RGB-waarden of met de kleurkiezer, [afhankelijk van de configuratie](#background-tab)
* **Achtergrondafbeelding** - Definieert een achtergrondkleur voor de container.  [afhankelijk van de configuratie](#background-tab)
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de Container-component gebruikt.

### Tabblad Toegestane componenten {#allowed-components-tab}

De **Toegestane componenten** wordt gebruikt om te definiëren welke componenten door de auteur van de inhoud als items aan de Container-component kunnen worden toegevoegd.

Het tabblad Toegestane componenten werkt op dezelfde manier als het tabblad met dezelfde naam wanneer [het definiëren van het beleid en de eigenschappen van een container voor layout in de Sjablooneditor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Tabblad Standaardcomponenten {#default-components-tab}

Het tabblad Standaardcomponenten wordt gebruikt om te definiëren welke component aan de component wordt toegevoegd wanneer een bepaald elementtype op de container wordt neergezet, vergelijkbaar met [hoe standaardcomponenten op de paginasjabloon worden gedefinieerd](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html).

### Tab Instellingen voor responsief {#responsive-settings-tab}

![Het tabblad Responsieve instellingen van het dialoogvenster Ontwerp van de Container-component](/help/assets/container-design-responsive.png)

* **Kolommen** - Hiermee definieert u het aantal kolommen in het raster van de resulterende container.

### Tabblad Achtergrond {#background-tab}

![Achtergrondtabblad van het dialoogvenster Ontwerp van de Containercomponent](/help/assets/container-design-background.png)

* **Achtergrondafbeelding**
   * **Achtergrondafbeelding inschakelen** - Selecteer deze optie als u wilt dat de auteur van de inhoud een achtergrondafbeelding voor de container kan definiëren.
* **Achtergrondkleur**
   * **Achtergrondkleur inschakelen** - Selecteer deze optie als u wilt dat de auteur van de inhoud een achtergrondkleur voor de container kan definiëren.
   * **Alleen stalen** - Selecteer deze optie als u wilt dat de auteur van de inhoud alleen uit vooraf gedefinieerde kleurstalen voor de achtergrondkleur van de container kan kiezen.
      * Alleen beschikbaar als **Achtergrondkleur inschakelen** is geselecteerd
* **Toegestane stalen** - Vooraf gedefinieerde kleuren definiëren waaruit de auteur van de inhoud de achtergrondkleur van de container kan selecteren
   * Gebruik de **Toevoegen** om een vooraf gedefinieerde kleurstaal toe te voegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:
   * **Waarde** - De kleur handmatig definiëren met behulp van RGB-waarden
      * Tik of klik op de kleurkiezer om een kleur eenvoudiger te selecteren door afzonderlijke RGB-waarden aan te passen of een hexadecimale waarde te definiëren.
   * **Verwijderen** - Tik of klik om een staal te verwijderen.
   * **Opnieuw rangschikken** - Tik of klik en sleep om de volgorde van de stalen te wijzigen.

### Tabblad Stijlen {#styles-tab}

De component Container ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
