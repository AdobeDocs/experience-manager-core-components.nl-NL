---
title: Component lijst met inhoudsfragmenten
description: Met de component Lijst met inhoudfragmenten van de kerncomponent kunt u een lijst met inhoudsfragmenten weergeven.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 0%

---


# Component lijst met inhoudsfragmenten{#content-fragment-list-component}

Met de component Lijst met inhoudfragmenten van de kerncomponent kunt u een lijst met [inhoudsfragmenten](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html)weergeven.

## Gebruik {#usage}

Met de component Lijst met fragmentfragmenten voor kerncomponenten kunt u een lijst met [inhoudsfragmenten](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) opnemen op een pagina die is gebaseerd op een model van een inhoudsfragment. Dit kan vooral handig zijn voor het maken van inhoud [zonder](https://helpx.adobe.com/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) kop die gemakkelijk kan worden verbruikt door andere toepassingen.

* De lijst en zijn eigenschappen kunnen in [vormen dialoog](#configure-dialog)worden geselecteerd.
* Stijlen kunnen worden toegepast op de component in het [ontwerpdialoogvenster](#design-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Content Fragment Component is v1, die in mei 2019 is geïntroduceerd met versie 2.4.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel | Compatibel | Compatibel |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_cflist)om de component Lijst met inhoudsfragmenten te ervaren en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te zien.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Lijst van het Fragment van de Inhoud [kan op GitHub](https://adobe.com/go/aem_cmp_tech_cflist_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud definiëren welke inhoudsfragmenten de lijst vormen en welke elementen van die fragmenten moeten worden opgenomen.

### Tabblad Eigenschappen

Op het tabblad **Eigenschappen** wordt gedefinieerd welke inhoudsfragmenten in de lijst worden opgenomen. Dit is voornamelijk gebaseerd op een geselecteerd inhoudsfragmentmodel, maar er zijn andere filteropties beschikbaar.

![Het tabblad Eigenschappen van het dialoogvenster Bewerken van de component Lijst met inhoudsfragmenten](/help/assets/content-fragment-list-properties.png)

* **Model** - Pad naar het model van het inhoudsfragment waarop de lijst is gebaseerd.
   * Standaard worden alle inhoudsfragmenten van het model dat is gedefinieerd als **modelpad** , opgenomen in de lijst.
* **Bovenliggend pad** - Bovenliggend pad waarvan de lijst moet worden gemaakt.
   * De inhoudsfragmenten op basis van het geselecteerde **modelpad** worden gefilterd naar de fragmenten op het opgegeven **bovenliggende pad**.
      * Klik of tik op de knop Dialoogvenster **Selectie** openen rechts in het veld om het pad op te geven.
* **Tags** - Alleen de inhoudsfragmenten met de opgegeven tags worden in de lijst opgenomen.
   * Klik of tik op de knop Dialoogvenster **Selectie** openen rechts in het veld om de labels op te geven.
   * Klik of tik op de X naast de geselecteerde tags om deze te verwijderen.
* **Volgorde door** - Veld van het fragmentmodel van de inhoud waarmee de lijst wordt geordend
   * Alleen tekstvelden (inclusief numeriek, datum en tijd) kunnen worden geselecteerd.
* **Sorteervolgorde** - Hoe de lijst wordt gesorteerd op het veld **Volgorde op** .
   * Oplopend of aflopend
* **Max. items** - Maximum aantal items dat in de lijst moet worden weergegeven
   * Geen waarde retourneert alle items.
* **ID** - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

>[!NOTE]
>De opties **Volgorde door**, **Sorteervolgorde** en **Max. items** zijn geïntroduceerd met versie 2.7.0 van de Core Components.

### Het tabblad Elements

Standaard worden alle elementen van het inhoudsfragmentmodel opgenomen in de lijst (tenzij deze worden beperkt door het veld **Max. items** ). Op het tabblad **Elements** kunt u alleen specifieke elementen opgeven die u wilt opnemen.

![Het tabblad Elementen van het dialoogvenster Bewerken van de component Lijst met inhoudsfragmenten](/help/assets/content-fragment-list-elements.png)

* **Elementen** - Alleen de elementen van de inhoudsfragmenten in de opgegeven lijst worden weergegeven.
   * Klik op de knop **Toevoegen** of tik erop om een nieuw element toe te voegen.
   * Klik of tik op de knop **Verwijderen** om een geselecteerd element te verwijderen.
   * Sleep de handgreep **Volgorde** om de volgorde van de elementen te wijzigen.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de stijlen definiëren die zijn toegepast op de component Lijst met inhoudsfragmenten.
