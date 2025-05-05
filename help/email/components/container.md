---
title: E-mailcontainercomponent
description: Met de component E-mailcontainer kunt u een container maken voor meerdere aanvullende componenten in uw e-mailinhoud.
role: Architect, Developer, Admin, User
exl-id: 3b271e95-0093-4cb1-bb83-8446ba12a821
source-git-commit: 91969e4956bef1a511b8d588d5290a7999bf86ec
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 0%

---


# E-mailcontainercomponent {#email-container-component}

Met de component E-mailcontainer kunt u een container maken voor meerdere aanvullende componenten in uw e-mailinhoud.

## Gebruik {#usage}

Met de component E-mailcontainer kunt u een container maken voor meerdere aanvullende componenten in uw e-mailinhoud. U kunt deze component gebruiken om andere componenten te groeperen en een algemene stijl of indeling toe te passen.

* De eigenschappen van de container kunnen in [ worden geselecteerd vormen dialoog.](#configure-dialog)
* De gebreken voor de Component van de Container E-mail wanneer het toevoegen van het aan een pagina kunnen in de [ ontwerpdialoog worden bepaald.](#design-dialog)

Nadat een component E-mailcontainer aan een pagina is toegevoegd, kan de auteur van de inhoud er aanvullende componenten in slepen en neerzetten.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de E-mailcontainer-component is v1, die in oktober 2022 is geïntroduceerd met release X van de e-mailkern-componenten, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel | - | - |

Voor meer informatie over de versies en versies van de Component van de Kern E-mailE-mail van de Component, zie de Versies van de Componenten van de Document [ E-mailKern.](/help/email/versions.md)

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Container [ kan op GitHub worden gevonden.](https://adobe.com/go/aem_cmp_tech_email_container_v1)

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden.](/help/developing/overview.md)

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het containeritem definiëren en bepalen hoe het zich gedraagt en in uw inhoud wordt weergegeven.

![ geef dialoog van de Component van de Container E-mail uit ](/help/email/assets/email-container-configure.png)

* **Lay-out** - deze optie bepaalt het gedrag of het lay-outgedrag van de Component van de Container E-mail.
   * **volledig-breedte**
   * **half|half**
   * **één-derde|twee-derde**
   * **twee-derde|één-derde**
   * **derde|derde|derde**
* **Achtergrondkleur** - bepaalt of als vrij-vormRGB waarden of door de kleurkiezer te gebruiken, [ afhankelijk van configuratie ](#container-settings-tab)
* **Achtergrondbeeld** - bepaalt een achtergrondbeeld voor de container, [ afhankelijk van configuratie ](#container-settings-tab)
* **identiteitskaart** - Deze optie staat het controleren van het unieke herkenningsteken van de component in HTML toe.
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende inhoud te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor CSS.

### Tabblad Stijlen {#styles-tab-edit}

De component E-mailContainer steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling)

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [ ontwerpdialoog ](#design-dialog) worden gevormd opdat het lusje beschikbaar is.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de component E-mailcontainer gebruikt.

### Tabblad Toegestane componenten {#allowed-components-tab}

Het **Toegestane lusje van Componenten** wordt gebruikt om te bepalen welke componenten als punten aan de Component van de Container E-mail door de inhoudauteur kunnen worden toegevoegd.

**Toegestane Componenten** tabfuncties op dezelfde manier als het lusje van de zelfde naam wanneer [ het bepalen van het beleid en de eigenschappen van een Container van de Lay-out in de Redacteur van het Malplaatje.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=nl-NL)

### Tabblad Standaardcomponenten {#default-components-tab}

Het **StandaardComponenten** lusje wordt gebruikt om te bepalen welke component aan de component wordt toegevoegd wanneer een bepaald activatype op de container wordt gelaten vallen, gelijkend op [ hoe de standaardcomponenten op het paginamalplaatje worden bepaald.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=nl-NL)

### Tabblad Containerinstellingen {#container-settings-tab}

Het **lusje van de Montages van de Container** bepaalt als de auteur een achtergrondbeeld of een kleur kan bepalen.

![ lusje van de Montages van de Container van de ontwerpdialoog van de Component E-mail van de Container ](/help/email/assets/email-container-design-container-settings.png)

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
   * **herschikt** - Tik of klik en sleep om monsters opnieuw te rangschikken.

### Tabblad Stijlen {#styles-tab}

De component E-mailContainer steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling)
