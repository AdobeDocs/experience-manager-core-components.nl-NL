---
title: Component lijst met inhoudsfragmenten
description: Met de component Lijst met inhoudfragmenten van de kerncomponent kunt u een lijst met inhoudsfragmenten weergeven.
role: Architect, Developer, Admin, User
exl-id: 0f2295b1-d287-4f72-8ee4-fa98c4850e53
source-git-commit: 395a1669cf3e17f649c23852addc37316b923bfd
workflow-type: tm+mt
source-wordcount: '831'
ht-degree: 0%

---

# Component lijst met inhoudsfragmenten{#content-fragment-list-component}

De component van de Lijst van het Fragment van de Lijst van de Inhoud van de Component van de Kern staat voor de vertoning van een lijst van [inhoudsfragmenten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html).

## Gebruik {#usage}

De component van de Lijst van het Fragmentlijst van de Inhoud van de Component van de Kern staat voor de opneming van een lijst van [inhoudsfragmenten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) op een pagina die is gebaseerd op een model van een inhoudsfragment. Dit is vooral handig voor het maken van [inhoud zonder kop](https://helpx.adobe.com/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) die gemakkelijk door andere toepassingen kunnen worden verbruikt.

* De lijst en de bijbehorende eigenschappen kunnen worden geselecteerd in het dialoogvenster [dialoogvenster configureren](#configure-dialog).
* Stijlen kunnen worden toegepast op de component in het dialoogvenster [ontwerpdialoogvenster](#design-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Content Fragment Component is v2, die in februari 2022 is geïntroduceerd met release 2.18.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|---|----|---|---|
| v2 | - | Compatibel | Compatibel |
| [v1](v1/content-fragment-list.md) | Compatibel | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de component Lijst met inhoudsfragmenten wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_cflist).

## Technische details {#technical-details}

De meest recente technische documentatie over de component Content Fragment List [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_cflist_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud definiëren welke inhoudsfragmenten de lijst vormen en welke elementen van die fragmenten moeten worden opgenomen.

### Tabblad Eigenschappen

De **Eigenschappen** bepaalt welke inhoudsfragmenten in de lijst worden opgenomen. Dit is voornamelijk gebaseerd op een geselecteerd inhoudsfragmentmodel, maar er zijn andere filteropties beschikbaar.

![Het tabblad Eigenschappen van het dialoogvenster Bewerken van de component Lijst met inhoudsfragmenten](/help/assets/content-fragment-list-properties.png)

* **Model** - Pad naar het inhoudsfragmentmodel waarop de lijst is gebaseerd.
   * Standaard worden alle inhoudsfragmenten van het model gedefinieerd als **Modelpad** worden in de lijst opgenomen.
* **Bovenliggend pad** - Bovenliggend pad waaruit de lijst moet worden opgebouwd.
   * De inhoudsfragmenten op basis van de geselecteerde **Modelpad** wordt gefilterd naar de op de **Bovenliggend pad**.
      * Klik of tik op **Dialoogvenster Selectie openen** aan de rechterkant van het veld om het pad op te geven.
* **Tags** - Alleen de inhoudsfragmenten met de opgegeven labels worden opgenomen in de lijst.
   * Klik of tik op **Dialoogvenster Selectie openen** aan de rechterkant van het veld om de tags op te geven.
   * Klik of tik op de X naast de geselecteerde tags om deze te verwijderen.
* **Bestellen op** - Veld van het fragmentmodel van de inhoud waarmee de lijst wordt gerangschikt
   * Alleen tekstvelden (inclusief numeriek, datum en tijd) kunnen worden geselecteerd.
* **Sorteervolgorde** - Hoe wordt de lijst gesorteerd door de **Bestellen op** field
   * Oplopend of aflopend
* **Max. items** - Maximumaantal items dat in de lijst moet worden weergegeven
   * Geen waarde retourneert alle items.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

>[!NOTE]
>De **Bestellen op**, **Sorteervolgorde**, en **Max. items** Er zijn opties geïntroduceerd met versie 2.7.0 van de Core Components.

### Het tabblad Elements

Standaard worden alle elementen van het Content Fragment-model opgenomen in de lijst (tenzij deze worden beperkt door de **Max. items** veld). De **Elementen** kunt u alleen specifieke elementen opgeven die u wilt opnemen.

![Het tabblad Elementen van het dialoogvenster Bewerken van de component Lijst met inhoudsfragmenten](/help/assets/content-fragment-list-elements.png)

* **Elementen** - Alleen de elementen van de inhoudsfragmenten in de opgegeven lijst worden weergegeven.
   * Klik of tik op **Toevoegen** om een nieuw element toe te voegen.
   * Klik of tik op **Verwijderen** om een geselecteerd element te verwijderen.
   * Sleep de **Volgorde** om de volgorde van de elementen te wijzigen.

### Tabblad Stijlen {#styles-tab-edit}

![Het tabblad Stijlen van het dialoogvenster Inhoud-fragmentlijstcomponent bewerken](/help/assets/content-fragment-list-styles.png)

De component Lijst van inhoudsfragmenten ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in worden gevormd [ontwerpdialoogvenster](#design-dialog) zodat het vervolgkeuzemenu beschikbaar is.

## Ontwerpdialoogvenster {#design-dialog}

### Tabblad Stijlen {#styles-tab}

De component Lijst van inhoudsfragmenten ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
