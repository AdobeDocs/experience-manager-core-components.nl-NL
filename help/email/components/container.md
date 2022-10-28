---
title: E-mailcontainercomponent
description: Met de component E-mailcontainer kunt u een container maken voor meerdere aanvullende componenten in uw e-mailinhoud.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 1%

---


# E-mailcontainercomponent {#email-container-component}

Met de component E-mailcontainer kunt u een container maken voor meerdere aanvullende componenten in uw e-mailinhoud.

## Gebruik {#usage}

Met de component E-mailcontainer kunt u een container maken voor meerdere aanvullende componenten in uw e-mailinhoud. U kunt deze component gebruiken om andere componenten te groeperen en een algemene stijl of indeling toe te passen.

* De eigenschappen van de container kunnen worden geselecteerd in het dialoogvenster [configureren, dialoogvenster.](#configure-dialog)
* De standaardinstellingen voor de component E-mailcontainer wanneer deze aan een pagina wordt toegevoegd, kunnen worden gedefinieerd in het dialoogvenster [ontwerpdialoogvenster.](#design-dialog)

Nadat een component E-mailcontainer aan een pagina is toegevoegd, kan de auteur van de inhoud er aanvullende componenten in slepen en neerzetten.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de E-mailcontainer-component is v1, die in oktober 2022 is geïntroduceerd met release X van de e-mailkern-componenten, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van e-mail Core Component [Core Components-versies e-mailen.](/help/email/versions.md)

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga voor meer informatie over de component E-mailcontainer en de configuratieopties en de uitvoer van HTML en JSON naar de [Componentbibliotheek.](https://adobe.com/go/aem_cmp_library_email_container)

## Technische details {#technical-details}

De meest recente technische documentatie over de Container Component [kan op GitHub worden gevonden.](https://adobe.com/go/aem_cmp_tech_email_container_v1)

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [De ontwikkelaarsdocumentatie van de Componenten van de kern.](/help/developing/overview.md)

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud het containeritem definiëren en bepalen hoe het zich gedraagt en in uw inhoud wordt weergegeven.

![Dialoogvenster E-mailcontainer-component bewerken](/help/email/assets/email-container-configure.png)

* **Layout** - Met deze optie definieert u het gedrag of het lay-outgedrag van de component E-mailcontainer.
   * **volledige breedte**
   * **half|half**
   * **eenderde|tweederde**
   * **tweederde|eenderde**
   * **derde|derde|derde**
* **Achtergrondkleur** - Definieerbaar als vrije-vorm RGB-waarden of met de kleurkiezer, [afhankelijk van de configuratie](#container-settings-tab)
* **Achtergrondafbeelding** - Definieert een achtergrondafbeelding voor de container. [afhankelijk van de configuratie](#container-settings-tab)
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML bepalen.
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende inhoud te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor CSS.

### Tabblad Stijlen {#styles-tab-edit}

De component Email Container ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling)

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in worden gevormd [ontwerpdialoogvenster](#design-dialog) zodat het tabblad beschikbaar is.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de component E-mailcontainer gebruikt.

### Tabblad Toegestane componenten {#allowed-components-tab}

De **Toegestane componenten** wordt gebruikt om te definiëren welke componenten door de auteur van de inhoud kunnen worden toegevoegd als items aan de E-mailcontainer-component.

De **Toegestane componenten** tabfuncties werken op dezelfde manier als het tabblad met dezelfde naam wanneer [het definiëren van het beleid en de eigenschappen van een container voor layout in de Sjablooneditor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Tabblad Standaardcomponenten {#default-components-tab}

De **Standaardcomponenten** tab wordt gebruikt om te definiëren welke component aan de component wordt toegevoegd wanneer een bepaald elementtype op de container wordt neergezet, vergelijkbaar met [hoe standaardcomponenten worden gedefinieerd op de paginasjabloon.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Tabblad Containerinstellingen {#container-settings-tab}

De **Containerinstellingen** wordt gedefinieerd of de auteur een achtergrondafbeelding of -kleur kan definiëren.

![Containerinstellingen, tabblad van het dialoogvenster Ontwerp van de E-mailcontainer-component](/help/email/assets/email-container-design-container-settings.png)

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
   * **Opnieuw rangschikken** - Tik of klik en sleep om de stalen opnieuw te ordenen.

### Tabblad Stijlen {#styles-tab}

De component Email Container ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling)