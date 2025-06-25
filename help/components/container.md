---
title: Containercomponent
description: Met de component Core Component Container kunt u een container maken voor meerdere aanvullende componenten op een pagina.
role: Architect, Developer, Admin, User
exl-id: 53c7190d-44cb-42ff-bc1a-483c7875bcf8
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---


# Containercomponent{#container-component}

Met de component Core Component Container kunt u een container maken voor meerdere aanvullende componenten op een pagina.

{{traditional-aem}}

## Gebruik {#usage}

Met de component Core Component Container kunt u een container maken voor meerdere aanvullende componenten op een pagina. U kunt deze component gebruiken om andere componenten te groeperen en een algemene stijl of lay-out toe te passen.

* De eigenschappen van de container kunnen in [ worden geselecteerd vormen dialoog ](#configure-dialog).
* De gebreken voor de Component van de Container wanneer het toevoegen van het aan een pagina kunnen in de [ ontwerpdialoog ](#design-dialog) worden bepaald.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Container Component is v1, die in juni 2019 met versie 2.5.0 van de Core Components is geïntroduceerd, en in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.17.4 ](/help/versions.md) en vroeger | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Container te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_container).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Container [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_container_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster configureren kan de auteur van de inhoud het containeritem definiëren en bepalen hoe het zich gedraagt en wordt weergegeven voor een bezoeker van de pagina.

![ geef dialoog van de Component van de Container uit ](/help/assets/container-edit.png)

* **Lay-out** - deze optie bepaalt het gedrag of het lay-outgedrag van de Component van de Container.
   * **Eenvoudig** - bepaalt een container als eenvoudige inzameling van componenten
   * **Responsief Net** - bepaalt een container als [ AEM Responsieve Lay-out ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)
* **Achtergrondkleur** - bepaalt of als vrij-vormRGB waarden of door de kleurkiezer te gebruiken, [ afhankelijk van configuratie ](#background-tab)
* **Achtergrondbeeld** - bepaalt een achtergrondkleur voor de container, [ afhankelijk van configuratie ](#background-tab)
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de Container-component gebruikt.

### Tabblad Toegestane componenten {#allowed-components-tab}

Het **Toegestane lusje van Componenten** wordt gebruikt om te bepalen welke componenten als punten aan de Component van de Container door de inhoudauteur kunnen worden toegevoegd.

De toegelaten Componenten lusjefuncties op de zelfde manier zoals het lusje van de zelfde naam wanneer [ het bepalen van het beleid en de eigenschappen van een Container van de Lay-out in de Redacteur van het Malplaatje.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Tabblad Standaardcomponenten {#default-components-tab}

Het lusje Standaard van Componenten wordt gebruikt om te bepalen welke component aan de component wordt toegevoegd wanneer een bepaald activatype op de container wordt gelaten vallen, gelijkend op [ hoe de standaardcomponenten op het paginamalplaatje ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) worden bepaald.

### Tab Instellingen voor responsief {#responsive-settings-tab}

![ Responsieve montageslusje van de ontwerpdialoog van de Component van de Container ](/help/assets/container-design-responsive.png)

* **Kolommen** - bepaalt het aantal kolommen in het net van de resulterende container.

### Tabblad Achtergrond {#background-tab}

![ Achtergrond lusje van de ontwerpdialoog van de Component van de Container ](/help/assets/container-design-background.png)

* **Achtergrondbeeld**
   * **laat achtergrondbeeld** toe - selecteer deze optie om de inhoudauteur toe te laten om een achtergrondbeeld voor de container te bepalen.
* **Achtergrondkleur**
   * **laat achtergrondkleur** toe - selecteer deze optie om de inhoudauteur toe te laten om een achtergrondkleur voor de container te bepalen.
   * **slechts Monsters** - selecteer deze optie om de tevreden auteur slechts toe te staan om van vooraf bepaalde kleurenstalen voor de container achtergrondkleur te selecteren.
      * Slechts beschikbaar wanneer **achtergrondkleur** toelaat wordt geselecteerd
* **Toegestane Monsters** - bepaal vooraf bepaalde kleuren waarvan de inhoudsauteur de container achtergrondkleur kan selecteren
   * Gebruik **toevoegen** knoop om een vooraf bepaald kleurenmonster toe te voegen. Nadat een item is toegevoegd, wordt het toegevoegd aan de lijst met de volgende kolommen:
   * **Waarde** - bepaal manueel de kleur via de waarden van RGB
      * Tik of klik op de kleurkiezer om een kleur eenvoudiger te selecteren door afzonderlijke RGB-waarden aan te passen of een hexadecimale waarde te definiëren.
   * **Schrapping** - Tik of klik om een monster te schrappen.
   * **herschikt** - Tik of klik en sleep om de orde van de monsters te herschikken.

### Tabblad Stijlen {#styles-tab}

De component van de Container steunt het Systeem van de Stijl van AEM [ ](/help/get-started/authoring.md#component-styling).
