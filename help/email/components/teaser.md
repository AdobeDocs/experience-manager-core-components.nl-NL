---
title: E-mailteascomponent
description: De component E-mailtaser kan een afbeelding, een titel, tekst met opmaak en eventueel een koppeling naar andere inhoud weergeven.
role: Architect, Developer, Admin, User
exl-id: d6123b22-7cba-406c-986d-b6f00322d135
source-git-commit: 3abc29e0c186a84f079d5938b8b716f4c7378d65
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 0%

---


# E-mailteascomponent {#email-teaser-component}

De component E-mailtaser kan een afbeelding, een titel, tekst met opmaak en eventueel een koppeling naar andere inhoud weergeven.

## Gebruik {#usage}

Met de component E-mailtaser kan de auteur van de inhoud eenvoudig een gummetje maken met een afbeelding, titel of tekst met opmaak en een koppeling maken naar andere inhoud of andere handelingen.

* De sjabloonauteur kan de opdracht [ontwerpdialoogvenster](#design-dialog) om te bepalen als de opties om vraag-aan-acties tot stand te brengen en verbindingen toe te voegen beschikbaar zijn evenals het onbruikbaar maken van diverse vertoningsopties.
* De auteur van de inhoud kan de [dialoogvenster configureren](#configure-dialog) om een afbeelding in te stellen, CTA&#39;s te definiëren, titels en beschrijvingen in te stellen en koppelingen naar het afzonderlijke Taser te configureren.
* De [dialoogvenster bewerken](image.md#edit-dialog) van de [E-mailafbeeldingscomponent](image.md) kan worden geopend om de teasafbeelding te wijzigen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de E-mailtasercomponent is v1, die in oktober 2022 is geïntroduceerd met release x van de Email Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatibel | - |

### Technische details {#technical-details}

De meest recente technische documentatie over de E-maillasercomponent [kan op GitHub worden gevonden.](https://adobe.com/go/aem_cmp_tech_email_teaser_v1)

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [De ontwikkelaarsdocumentatie van de Componenten van de kern.](/help/developing/overview.md)

## Dialoogvenster configureren {#configure-dialog}

De auteur van de inhoud kan het dialoogvenster Configure gebruiken om de eigenschappen van de afzonderlijke teaser te definiëren. Er is ook een [dialoogvenster bewerken](#edit-dialog) om de laserafbeelding te wijzigen als deze is geselecteerd.

### Tabblad Koppelingen {#links-tab}

![Dialoogvenster Koppelingen in dialoogvenster E-mailteascomponent](/help/email/assets/email-teaser-edit-links.png)

De teastitel, beschrijving en afbeelding kunnen worden overgeërfd van de gekoppelde inhoud of van de inhoud die is gekoppeld in de eerste oproep tot actie. Als noch een verbinding noch een vraag-aan-actie wordt gespecificeerd, dan zullen de titel, de beschrijving, en het beeld van de huidige inhoud worden geërft.

* **Koppeling** - Dit bestand is gekoppeld aan inhoud, externe URL of anker.
   * Klik op het pictogram Campagne om het dialoogvenster [Adobe Campaign-variabele selecteren](/help/email/campaign-variables.md) om dynamische inhoud uit Adobe Campaign in te voegen.
* **Oproep tot actie** - Met deze optie kunt u koppelingen naar meerdere doelen maken.
   * De pagina verbonden in de eerste vraag-aan-actie wordt gebruikt wanneer het erven van de teastitel, de beschrijving, of het beeld.
   * Klik op het pictogram Campagne om het dialoogvenster [Adobe Campaign-variabele selecteren](/help/email/campaign-variables.md) om dynamische inhoud uit Adobe Campaign in te voegen.

### Tabblad Tekst {#text-tab}

![Teksttabblad van het dialoogvenster voor bewerken van de component E-mail](/help/email/assets/email-teaser-edit-text.png)

* **Pretitle** - De voortitel wordt vóór de titel van de taser weergegeven.
* **Titel** - Definieert een titel die moet worden weergegeven als de kop voor het gummetje.
   * Klik op het pictogram Campagne om het dialoogvenster [Adobe Campaign-variabele selecteren](/help/email/campaign-variables.md) om dynamische inhoud uit Adobe Campaign in te voegen.
   * **Titel ophalen van gekoppelde pagina** - Als deze optie is ingeschakeld, wordt de titel van de gekoppelde pagina ingevuld.
* **Beschrijving** - Definieert een beschrijving die moet worden weergegeven als subcode van het gummetje.
   * Klik op de knop **Adobe Campaign-variabele selecteren** pictogram om het [Adobe Campaign-variabele selecteren](/help/email/campaign-variables.md) om dynamische inhoud uit Adobe Campaign in te voegen.
   * **Beschrijving ophalen van gekoppelde pagina** - Als deze optie is ingeschakeld, wordt de beschrijving gevuld met de beschrijving van de gekoppelde pagina.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML bepalen.
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende inhoud te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor CSS.

### Tabblad Element {#asset-tab}

![Het tabblad Afbeelding van het dialoogvenster E-mailteasercomponent bewerken](/help/email/assets/email-teaser-edit-image.png)

* **Weergegeven afbeelding overnemen van pagina** - Gebruik de afbeelding die is gedefinieerd in de pagina-eigenschappen van de gekoppelde pagina of de huidige pagina als er geen is gevonden.
* **Afbeeldingselement** - Middelen neerzetten vanaf de [middelenbrowser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of tik op **doorbladeren** uploaden vanuit een lokaal bestandssysteem.
   * Tik of klik op **Wissen** om de selectie van de geselecteerde afbeelding op te heffen.
   * Tik of klik op **Bewerken** tot [de uitvoeringen van het actief beheren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in de Asset Editor.
* **Alternatieve tekst voor toegankelijkheid** - In dit veld kunt u een beschrijving van de afbeelding definiëren voor visueel gehandicapte gebruikers.
   * **Alternatieve tekst van pagina overnemen** - Bij deze optie wordt de alternatieve beschrijving van de waarde van het gekoppelde element van de optie `dc:description` metagegevens in DAM of van de huidige pagina als er geen element is gekoppeld.
* **Geen alternatieve tekst bieden** - Deze optie markeert dat de afbeelding wordt genegeerd door ondersteunende hulpmiddelen, zoals schermlezers, wanneer de afbeelding zuiver decoratief is of anderszins geen aanvullende informatie naar de pagina overbrengt.

>[!NOTE]
>
>[Dynamic Media-functies](image.md#dynamic-media) zijn momenteel niet beschikbaar in de Taser-component.

### Tabblad Stijlen {#styles-tab-edit}

De component Email Teaser ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling)

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in worden gevormd [ontwerpdialoogvenster](#design-dialog) zodat het tabblad beschikbaar is.

## Dialoogvenster Bewerken {#edit-dialog}

De component Email Teaser delegeert het renderen van afbeeldingen aan de [Afbeeldingscomponent](image.md). Daarom [dialoogvenster bewerken](image.md#edit-dialog) van de Afbeeldingscomponent is beschikbaar voor de auteur van de inhoud om de laserafbeelding te bewerken.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de teasopties definiëren die de auteur van de inhoud heeft bij het gebruik van deze component.

### Taser Tab {#teaser-tab}

![Ontwerpdialoogvenster van de component E-mail](/help/email/assets/email-teaser-design.png)

* **Toegestane kopelementen** - Gebruik de vervolgkeuzelijst om te definiëren welke HTML-elementen van de kop door de auteur kunnen worden geselecteerd voor het titeltype van het gummetje.
* **Standaardkopelement van de titel** - Het standaardelement heading HTML dat wordt gebruikt voor het titeltype van de teaser
* **Oproep tot actie**
   * **Schakel Vraag-aan-Acties onbruikbaar** - Verberg de **Oproep tot actie** optie voor auteurs van inhoud
* **Elementen**
   * **Voortitel verbergen** - Verbergt de **Pretitle** optie voor auteurs van inhoud
   * **Titel verbergen** - Verbergt de **Titel** optie voor auteurs van inhoud
      * Als u **Type titel** is verborgen
   * **Titeltype tonen**
   * **Beschrijving verbergen** - Verberg de **Beschrijving** optie voor auteurs van inhoud
* **Afbeelding delegeren** - Informatieweergave die aangeeft aan welk onderdeel de e-mailtaser de beeldverwerking delegeert.

### Tabblad Stijlen {#styles-tab}

De component Email Teaser ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling)
