---
title: Component Inhoudsfragment
description: Met de component Inhoudsfragment van de kerncomponent kunt u een inhoudsfragment weergeven.
role: Architect, Developer, Admin, User
exl-id: 551ff2a1-f8db-490c-84a3-4255b364fc83
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 1%

---

# Component Inhoudsfragment{#content-fragment-component}

Met de component Inhoudsfragment van kerncomponent kunt u een [inhoudsfragment](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) weergeven.

>[!NOTE]
>
>Voorafgaand aan versie 2.4.0 van de Componenten van de Kern, was de component van het Fragment van de Inhoud beschikbaar als uitbreiding aan de kerncomponenten en moest afzonderlijk worden gedownload en uitdrukkelijk worden toegelaten.

## Gebruik {#usage}

De component van het Fragment van de Inhoud van de Component van de Kern staat voor de opneming van een [inhoudsfragment](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) op een pagina toe.

* Het fragment en zijn eigenschappen kunnen in [vorm dialoog](#configure-dialog) worden geselecteerd.
* De types van middelen om bepaalde beelden en netten te behandelen kunnen in [ontwerpdialoog](#design-dialog) worden bepaald.
* Met de optie Bewerken wordt het geselecteerde fragment geopend in de [inhoudfragmenteditor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Content Fragment Component is v1, die in oktober 2017 is geïntroduceerd met release 1.1.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel | Compatibel | Compatibel |

>[!NOTE]
>
>Voorafgaand aan versie 2.4.0, werd de component van het Fragment van de Inhoud gevestigd in de omslag van uitbreidingen.
>
> `apps/core/wcm/extension/components/contentfragment/v1/contentfragment`
> 
>Vanaf 2.4.0 is het verplaatst naar de volgende locatie.
>
>`apps/core/wcm/components/contentfragment/v1/contentfragment`
>
>Hoewel beide v1 zijn, vereist om het even welke component van het Fragment van de Inhoud die van de omslag van uitbreidingen werd gebruikt een migratie van zijn verwante volmachtscomponenten om het nieuwe middeltype te gebruiken wanneer het bevorderen om 2.4.0 of hoger van de Componenten van de Kern vrij te geven.

Voor meer informatie over de versies en versies van de Component van de Kern, zie het document [de Versies van de Componenten van de Kern](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_cf) om de component Content Fragment te bekijken en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van het Fragment van de Inhoud [kan op GitHub](https://adobe.com/go/aem_cmp_tech_cf_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud definiëren welk inhoudsfragment en de elementen van dat fragment moeten worden opgenomen.

### Tabblad Eigenschappen {#properties-tab}

![Component Inhoudsfragment](/help/assets/content-fragment-edit-properties.png)

* **Inhoudsfragment**

   * Pad naar het gewenste inhoudsfragment
   * Het dialoogvenster **Selectie** kan worden gebruikt om het fragment te zoeken

* **Weergavemodus**
   * **Single Text Element**  - Schakelt selectie van één tekstelement met meerdere regels in en schakelt opties voor alinealijnbeheer in
   * **Meerdere elementen**  - Hiermee kunt u een of meer elementen van het geselecteerde inhoudsfragment selecteren
* **Element**  - Het element of de elementen van het inhoudsfragment dat moet worden opgenomen
* **Variatie**  - Welke variatie van het inhoudfragment moet worden gebruikt (standaard ingesteld op  **Master**)

* **Alinea&#39;s**

   * **Alles**  - Alle alinea&#39;s weergeven
   * **Bereik**

      * Bereiken opgeven voor alinea&#39;s die moeten worden weergegeven, gescheiden door een puntkomma
      * Als u bijvoorbeeld `1;3-5;7;9-*` wilt opnemen in de eerste, de derde tot de vijfde, de zevende en de negende alinea tot de laatste alinea
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Alinealijn {#paragraph-control-tab}

Dit tabblad is niet beschikbaar wanneer de modus **Meerdere elementen** is geselecteerd.

![Component Inhoudsfragment](/help/assets/content-fragment-edit-paragraph.png)

* **Alinea** - Selectie van alle alinea&#39;s of een bereik toestaan
* **Koptekst verwerken als eigen alinea&#39;s**

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de typen bronnen definiëren die worden gebruikt voor het verwerken van afbeeldingen met gemengde media en responsieve rasters.

![Het dialoogvenster Ontwerpen van de component Content Fragment](/help/assets/content-fragment-design.png)

* **Intern responsief raster**

   * Het Sling-brontype dat wordt gebruikt voor het interne responsieve raster

## Gegevenslaag Adobe-client {#data-layer}

De component van het Fragment van de Inhoud steunt [de Laag van de Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
