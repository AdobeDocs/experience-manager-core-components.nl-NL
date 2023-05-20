---
title: Component lijst met inhoudsfragmenten (v1)
description: Met de component Lijst met inhoudfragmenten van de kerncomponent kunt u een lijst met inhoudsfragmenten weergeven.
role: Architect, Developer, Admin, User
exl-id: 37d6632d-360d-4081-8279-8efbb369a82e
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---

# Component lijst met inhoudsfragmenten (v1) {#content-fragment-list-component}

De component van de Lijst van het Fragment van de Lijst van de Inhoud van de Component van de Kern staat voor de vertoning van een lijst van [inhoudsfragmenten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html).

## Gebruik {#usage}

De component van de Lijst van het Fragmentlijst van de Inhoud van de Component van de Kern staat voor de opneming van een lijst van [inhoudsfragmenten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) op een pagina die is gebaseerd op een model van een inhoudsfragment. Dit is vooral handig voor het maken van [inhoud zonder kop](https://helpx.adobe.com/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) die gemakkelijk door andere toepassingen kunnen worden verbruikt.

* De lijst en de bijbehorende eigenschappen kunnen worden geselecteerd in het dialoogvenster [dialoogvenster configureren](#configure-dialog).
* Stijlen kunnen worden toegepast op de component in het dialoogvenster [ontwerpdialoogvenster](#design-dialog).

## Versie en compatibiliteit {#version-and-compatibility}

In het document wordt versie 1 van de Content Fragment Component beschreven. Deze is in mei 2019 geïntroduceerd met release 2.4.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Lijst met inhoudsfragmenten beschreven.
>
>Zie voor meer informatie over de huidige versie van de component Content Fragment List de klasse [Component lijst met inhoudsfragmenten](/help/components/content-fragment-list.md) document.

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

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de stijlen definiëren die zijn toegepast op de component Lijst met inhoudsfragmenten.
