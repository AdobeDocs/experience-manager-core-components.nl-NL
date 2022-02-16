---
title: Component Inhoudsfragment
description: Met de component Inhoudsfragment van de kerncomponent kunt u een inhoudsfragment weergeven.
role: Architect, Developer, Admin, User
exl-id: 551ff2a1-f8db-490c-84a3-4255b364fc83
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 1%

---

# Component Inhoudsfragment{#content-fragment-component}

De component van het Fragment van de Inhoud van de Component van de Kern staat voor de vertoning van toe [inhoudsfragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html).

>[!NOTE]
>
>Voorafgaand aan versie 2.4.0 van de Componenten van de Kern, was de component van het Fragment van de Inhoud beschikbaar als uitbreiding aan de kerncomponenten en moest afzonderlijk worden gedownload en uitdrukkelijk worden toegelaten.

## Gebruik {#usage}

Met de component Core Component Content Fragment kunt u een [inhoudsfragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) op een pagina.

* Het fragment en de bijbehorende eigenschappen kunnen worden geselecteerd in het dialoogvenster [dialoogvenster configureren](#configure-dialog).
* De typen bronnen voor het verwerken van bepaalde afbeeldingen en rasters kunnen worden gedefinieerd in het dialoogvenster [ontwerpdialoogvenster](#design-dialog).
* Met de optie Bewerken wordt het geselecteerde fragment geopend in het dialoogvenster [inhoudsfragmenteditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html).

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Content Fragment Component is v1, die in oktober 2017 is geïntroduceerd met release 1.1.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel met<br>[release 2.17.4](/help/versions.md) en eerdere | Compatibel | Compatibel |

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

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de component Inhoudsfragment wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_cf).

## Technische details {#technical-details}

De meest recente technische documentatie over de component Content Fragment [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_cf_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud definiëren welk inhoudsfragment en de elementen van dat fragment moeten worden opgenomen.

### Tabblad Eigenschappen {#properties-tab}

![Component Inhoudsfragment](/help/assets/content-fragment-edit-properties.png)

* **Inhoudsfragment**

   * Pad naar het gewenste inhoudsfragment
   * De **Dialoogvenster Selectie** kan worden gebruikt om het fragment te zoeken

* **Weergavemodus**
   * **Element voor één tekst** - Schakelt de selectie van één tekstelement met meerdere regels in en schakelt de opties voor alineacontrole in
   * **Meerdere elementen** - Hiermee kunt u een of meer elementen van het geselecteerde inhoudsfragment selecteren
* **Element** - Het element of de elementen van het inhoudsfragment dat moet worden opgenomen
* **Variatie** - Welke variatie van het inhoudfragment moet worden gebruikt (standaard ingesteld op **Master**)

* **Alinea&#39;s**

   * **Alles** - Alle alinea&#39;s weergeven
   * **Bereik**

      * Bereiken opgeven voor alinea&#39;s die moeten worden weergegeven, gescheiden door een puntkomma
      * Bijvoorbeeld `1;3-5;7;9-*` de eerste, de derde tot de vijfde, de zevende en de negende alinea
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Alinealijn {#paragraph-control-tab}

Dit tabblad is niet beschikbaar als **Meerdere elementen** is geselecteerd.

![Component Inhoudsfragment](/help/assets/content-fragment-edit-paragraph.png)

* **Alinea&#39;s** - Selectie van alle alinea&#39;s of een bereik toestaan
* **Koptekst verwerken als eigen alinea&#39;s**

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de typen bronnen definiëren die worden gebruikt voor het verwerken van afbeeldingen met gemengde media en responsieve rasters.

![Het dialoogvenster Ontwerpen van de component Content Fragment](/help/assets/content-fragment-design.png)

* **Intern responsief raster**

   * Het Sling-brontype dat wordt gebruikt voor het interne responsieve raster

## Gegevenslaag Adobe-client {#data-layer}

De component Inhoudsfragment ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
