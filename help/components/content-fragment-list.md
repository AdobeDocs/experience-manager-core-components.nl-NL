---
title: Component lijst met inhoudsfragmenten
description: Met de component Lijst met inhoudfragmenten van de kerncomponent kunt u een lijst met inhoudsfragmenten weergeven.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---


# Component Inhoudsfragmentlijst{#content-fragment-list-component}

De component van de Lijst van het Fragmentlijst van de Inhoud van de Component van de Kern staat voor de vertoning van een lijst van [inhoudsfragmenten](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) toe.

## Gebruik {#usage}

De component van de Lijst van het Fragmentlijst van de Inhoud van de Component van de Kern staat voor de opneming van een lijst van [inhoudsfragmenten](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) op een pagina toe die op een model van het Fragment van de Inhoud wordt gebaseerd. Dit kan met name handig zijn voor het maken van [inhoud zonder kop](https://helpx.adobe.com/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) die gemakkelijk kan worden verbruikt door andere toepassingen.

* De lijst en zijn eigenschappen kunnen in [vormen dialoog](#configure-dialog) worden geselecteerd.
* Stijlen kunnen worden toegepast op de component in het [ontwerpdialoogvenster](#design-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Content Fragment Component is v1, die in mei 2019 is geïntroduceerd met versie 2.4.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel | Compatibel | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_cflist) om de component Content Fragment List te bekijken en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Lijst van het Fragment van de Inhoud [kan op GitHub](https://adobe.com/go/aem_cmp_tech_cflist_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster {#configure-dialog} configureren

In het dialoogvenster voor configureren kan de auteur van de inhoud definiëren welke inhoudsfragmenten de lijst vormen en welke elementen van die fragmenten moeten worden opgenomen.

### Tabblad Eigenschappen

Het tabblad **Eigenschappen** definieert welke inhoudsfragmenten in de lijst worden opgenomen. Dit is voornamelijk gebaseerd op een geselecteerd inhoudsfragmentmodel, maar er zijn andere filteropties beschikbaar.

![Het tabblad Eigenschappen van het dialoogvenster Bewerken van de component Lijst van inhoudsfragmenten](/help/assets/content-fragment-list-properties.png)

* **Model**  - Pad naar het model van het inhoudsfragment waarop de lijst is gebaseerd.
   * Standaard worden alle inhoudsfragmenten van het model dat is gedefinieerd als **Model-pad** opgenomen in de lijst.
* **Bovenliggend pad**  - Bovenliggend pad waarvan de lijst moet worden gemaakt.
   * De inhoudsfragmenten die zijn gebaseerd op het geselecteerde **Model-pad** worden gefilterd naar de fragmenten op het opgegeven **Bovenliggend pad**.
      * Klik of tik **Dialoogvenster Selectie openen** knoop bij de rechterkant van het gebied om de weg te specificeren.
* **Tags**  - Alleen de inhoudsfragmenten met de opgegeven labels worden in de lijst opgenomen.
   * Klik of tik **Dialoogvenster Selectie openen** knoop bij de rechterkant van het gebied om de markeringen te specificeren.
   * Klik of tik op de X naast de geselecteerde tags om deze te verwijderen.
* **Volgorde door**  - Veld van het fragmentmodel van de inhoud waarmee de lijst wordt geordend
   * Alleen tekstvelden (inclusief numeriek, datum en tijd) kunnen worden geselecteerd.
* **Sorteervolgorde**  - Hoe de lijst wordt gesorteerd op het veld  **Order** Byfield
   * Oplopend of aflopend
* **Max. items**  - Maximum aantal items dat in de lijst moet worden weergegeven
   * Geen waarde retourneert alle items.
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

>[!NOTE]
>De **Volgorde door**, **Sorteervolgorde** en **Max Items** opties zijn geïntroduceerd met release 2.7.0 van de Core Components.

### Het tabblad Elements

Standaard worden alle elementen van het inhoudsfragmentmodel opgenomen in de lijst (tenzij beperkt door het veld **Max. items**). Op het tabblad **Elements** kunt u alleen specifieke elementen opgeven die u wilt opnemen.

![Het tabblad Elementen van het dialoogvenster Bewerken van de component Lijst met inhoudsfragmenten](/help/assets/content-fragment-list-elements.png)

* **Elements**  - Alleen de elementen van de inhoudsfragmenten in de opgegeven lijst worden weergegeven.
   * Klik of tik **Add** knoop om een nieuw element toe te voegen.
   * Klik of tik **Schrapping** knoop om een geselecteerd element te verwijderen.
   * Sleep de handgreep **Order** om de volgorde van de elementen te wijzigen.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de stijlen definiëren die zijn toegepast op de component Lijst met inhoudsfragmenten.
