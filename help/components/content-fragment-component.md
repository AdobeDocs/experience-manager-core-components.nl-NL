---
title: Component Inhoudsfragment
description: Met de component Inhoudsfragment van de kerncomponent kunt u een inhoudsfragment weergeven.
role: Architect, Developer, Admin, User
exl-id: 551ff2a1-f8db-490c-84a3-4255b364fc83
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 0%

---

# Component Inhoudsfragment{#content-fragment-component}

De component van het Fragment van de Inhoud van de Component van de Kern staat voor de vertoning van a [ inhoudsfragment ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=nl-NL) toe.

>[!NOTE]
>
>Voorafgaand aan versie 2.4.0 van de Componenten van de Kern, was de component van het Fragment van de Inhoud beschikbaar als uitbreiding aan de kerncomponenten en moest afzonderlijk worden gedownload en uitdrukkelijk worden toegelaten.

## Gebruik {#usage}

De component van het Fragment van de Inhoud van de Component van de Kern staat voor de opneming van a [ inhoudsfragment ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=nl-NL) op een pagina toe.

* Het fragment en zijn eigenschappen kunnen in [ worden geselecteerd vormen dialoog ](#configure-dialog).
* De types van middel om bepaalde beelden en netten te behandelen kunnen in de [ ontwerpdialoog ](#design-dialog) worden bepaald.
* De Edit optie zal het geselecteerde fragment binnen de [ redacteur van het inhoudsfragment ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html?lang=nl-NL) openen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Content Fragment Component is v1, die in oktober 2017 is geïntroduceerd met release 1.1.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.17.4 ](/help/versions.md) en vroeger | Compatibel | Compatibel | Compatibel |

>[!NOTE]
>
>Vóór versie 2.4.0 bevindt de component Content Fragment zich in de map extensions.
>
> `apps/core/wcm/extension/components/contentfragment/v1/contentfragment`
> 
>Vanaf 2.4.0 is het verplaatst naar de volgende locatie.
>
>`apps/core/wcm/components/contentfragment/v1/contentfragment`
>
>Hoewel beide v1 zijn, vereist om het even welke component van het Fragment van de Inhoud die van de omslag van uitbreidingen werd gebruikt een migratie van zijn verwante volmachtscomponenten om het nieuwe middeltype te gebruiken wanneer het bevorderen om 2.4.0 of hoger van de Componenten van de Kern vrij te geven.

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van het Fragment van de Inhoud te ervaren evenals voorbeelden van zijn configuratieopties evenals de output van HTML en JSON te zien, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_cf).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van het Fragment van de Inhoud [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_cf_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud definiëren welk inhoudsfragment en de elementen van dat fragment moeten worden opgenomen.

### Tabblad Eigenschappen {#properties-tab}

![ Component van het Fragment van de Inhoud ](/help/assets/content-fragment-edit-properties.png)

* **het Fragment van de Inhoud**

   * Pad naar het gewenste inhoudsfragment
   * De **Dialoog van de Selectie** kan worden gebruikt om van het fragment de plaats te bepalen

* **Wijze van de Vertoning**
   * **Enig Element van de Tekst** - laat selectie van één multiline tekstelement toe en laat paragraafcontroleopties toe
   * **Veelvoudige Elementen** - staat selectie van één of meerdere elementen van het geselecteerde inhoudsfragment toe
* **Element** - het element of de elementen van het inhoudsfragment om te omvatten
* **Variatie** - welke variatie van het inhoudsfragment om te gebruiken (gebreken aan **Hoofd**)

* **Paragraaf**

   * **allen** - toon alle paragrafen
   * **Waaier**

      * Bereiken opgeven voor alinea&#39;s die moeten worden weergegeven, gescheiden door een puntkomma
      * Als u bijvoorbeeld `1;3-5;7;9-*` de eerste, de derde tot de vijfde, de zevende en de negende alinea tot de laatste alinea wilt opnemen
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Alinealijn {#paragraph-control-tab}

Dit lusje is niet beschikbaar wanneer **de Veelvoudige wijze van Elementen** wordt geselecteerd.

![ Component van het Fragment van de Inhoud ](/help/assets/content-fragment-edit-paragraph.png)

* **Paragraaf** - sta selectie van alle paragrafen of een waaier toe
* **de rubriek van het Handvat als hun eigen paragrafen**

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de typen bronnen definiëren die worden gebruikt voor het verwerken van afbeeldingen met gemengde media en responsieve rasters.

![ dialoog van het Ontwerp van de Component van het Fragment van de Inhoud ](/help/assets/content-fragment-design.png)

* **Intern ontvankelijk net**

   * Het Sling-brontype dat wordt gebruikt voor het interne responsieve raster

## Adobe Client Data Layer {#data-layer}

De component van het Fragment van de Inhoud steunt de [ Laag van de Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
