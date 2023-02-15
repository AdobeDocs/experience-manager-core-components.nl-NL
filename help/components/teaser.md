---
title: Teaser-component
description: De teaser-component kan een afbeelding, een titel, RTF-tekst en eventueel een koppeling naar andere inhoud weergeven.
role: Architect, Developer, Admin, User
exl-id: ec75e168-6f3b-4dff-8df6-06ca7dc18688
source-git-commit: cfc86203051739cbcdc30be0fb10ccffa7d583a5
workflow-type: tm+mt
source-wordcount: '988'
ht-degree: 0%

---

# Teaser-component {#teaser-component}

De component van de Teaser Component van de Kern kan een beeld, een titel, rijke-tekst, en naar keuze verbinding aan verdere inhoud tonen.

## Gebruik {#usage}

Met de component Taser kan de auteur van de inhoud eenvoudig een gummetje maken om inhoud te verfraaien met een afbeelding, titel of tekst met opmaak en een koppeling naar andere inhoud of andere handelingen tot stand te brengen.

De sjabloonauteur kan de opdracht [ontwerpdialoogvenster](#design-dialog) om te bepalen als de opties om vraag-aan-acties tot stand te brengen en verbindingen toe te voegen beschikbaar zijn evenals het onbruikbaar maken van diverse vertoningsopties. De auteur van de inhoud kan de [dialoogvenster configureren](#configure-dialog) om een afbeelding in te stellen, CTA&#39;s te definiëren, titels en beschrijvingen in te stellen en koppelingen naar het afzonderlijke Taser te configureren. De [dialoogvenster bewerken](image.md#edit-dialog) van de [Afbeeldingscomponent](image.md) kan worden geopend om de teasafbeelding te wijzigen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Teaser Component is v2, die in februari 2022 werd geïntroduceerd met versie 2.18.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | - | Compatibel | Compatibel |
| [v1](v1/teaser.md) | Compatibel | Compatibel | Compatibel |

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de Taser-component wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_teaser).

### Technische details {#technical-details}

De meest recente technische documentatie over de Teaser Component [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_teaser_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

De auteur van de inhoud kan het dialoogvenster Configure gebruiken om de eigenschappen van de afzonderlijke teaser te definiëren. Er is ook een [dialoogvenster bewerken](#edit-dialog) om de laserafbeelding te wijzigen als deze is geselecteerd.

### Tabblad Koppelingen {#links-tab}

![Het tabblad Bewerkdialoogvensters van de Teaser Component](/help/assets/teaser-edit-links.png)

De teastitel, beschrijving en afbeelding kunnen worden overgenomen van de gekoppelde pagina of van de pagina die is gekoppeld in de eerste aanroep naar de handeling. Als er geen koppeling of actielijn is opgegeven, worden de titel, beschrijving en afbeelding overgenomen van de huidige pagina.

* **Koppeling** - Dit bestand is gekoppeld aan een inhoudspagina, externe URL of pagina-anker.
* **Koppeling openen op nieuw tabblad** - Indien ingeschakeld, wordt de koppeling geopend in een nieuw browsertabblad.
* **Oproep tot actie** - Met deze optie kunt u koppelingen naar meerdere doelen maken.
   * De pagina verbonden in de eerste vraag-aan-actie wordt gebruikt wanneer het erven van de teastitel, de beschrijving, of het beeld.

### Tabblad Tekst {#text-tab}

![Het teksttabblad van het dialoogvenster Bewerken van de component Teaser](/help/assets/teaser-edit-text.png)

* **Pretitle** - De voortitel wordt vóór de titel van de taser weergegeven.
* **Titel** - Definieert een titel die moet worden weergegeven als de kop voor het gummetje.
   * **Titel ophalen van gekoppelde pagina** - Als deze optie is ingeschakeld, wordt de titel van de gekoppelde pagina ingevuld.
* **Beschrijving** - Definieert een beschrijving die moet worden weergegeven als subcode van het gummetje.
   * **Beschrijving ophalen van gekoppelde pagina** - Als deze optie is ingeschakeld, wordt de beschrijving gevuld met de beschrijving van de gekoppelde pagina.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Element {#asset-tab}

![Het tabblad Afbeelding van het dialoogvenster Bewerken van de Teasercomponent](/help/assets/teaser-edit-image.png)

* **Weergegeven afbeelding overnemen van pagina** - Gebruik de afbeelding die is gedefinieerd in de pagina-eigenschappen van de gekoppelde pagina of de huidige pagina als er geen is gevonden.
* **Afbeeldingselement** - Middelen neerzetten vanaf de [middelenbrowser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of tik op **doorbladeren** uploaden vanuit een lokaal bestandssysteem.
   * Tik of klik op **Wissen** om de selectie van de geselecteerde afbeelding op te heffen.
   * Tik of klik op **Bewerken** tot [de uitvoeringen van het actief beheren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in de middeleneditor.
* **Alternatieve tekst voor toegankelijkheid** - In dit veld kunt u een beschrijving van de afbeelding definiëren voor visueel gehandicapte gebruikers.
   * **Alternatieve tekst van pagina overnemen** - Bij deze optie wordt de alternatieve beschrijving van de waarde van het gekoppelde element van de optie `dc:description` metagegevens in DAM of van de huidige pagina als er geen element is gekoppeld.
* **Geen alternatieve tekst bieden** - Deze optie markeert dat de afbeelding wordt genegeerd door ondersteunende hulpmiddelen, zoals schermlezers, wanneer de afbeelding zuiver decoratief is of anderszins geen aanvullende informatie naar de pagina overbrengt.

### Tabblad Stijlen {#styles-tab-edit}

![Het tabblad Stijlen van het dialoogvenster voor het bewerken van de component Taser List](/help/assets/teaser-edit-styles.png)

De component Taser ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in worden gevormd [ontwerpdialoogvenster](#design-dialog) zodat het vervolgkeuzemenu beschikbaar is.

## Dialoogvenster Bewerken {#edit-dialog}

De component Teaser delegeert het renderen van afbeeldingen aan de [Afbeeldingscomponent](image.md). Daarom [dialoogvenster bewerken](image.md#edit-dialog van de component Image is beschikbaar voor de auteur van de inhoud om de teasafbeelding te bewerken.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de teasopties definiëren die de auteur van de inhoud heeft bij het gebruik van deze component.

### Taser Tab {#teaser-tab}

![Ontwerpdialoogvenster van de Teaser Component](/help/assets/teaser-design.png)

* **Oproep tot actie**
   * **Schakel Vraag-aan-Acties onbruikbaar** - Verberg de **Oproep tot actie** optie voor auteurs van inhoud
* **Elementen**
   * **Voortitel verbergen** - Verbergt de **Pretitle** optie voor auteurs van inhoud
   * **Titel verbergen** - Verbergt de **Titel** optie voor auteurs van inhoud
      * Als u **Type titel** is verborgen
   * **Beschrijving verbergen** - Verberg de **Beschrijving** optie voor auteurs van inhoud
* **Standaardtiteltype** - Definieert de tag H die moet worden gebruikt door de titel van het gummetje.
* **Afbeelding delegeren** - Informatieweergave die aangeeft aan welke component de Taser de beeldverwerking delegeert.

### Tabblad Stijlen {#styles-tab}

De component Taser ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component Teaser ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
