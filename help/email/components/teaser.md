---
title: E-mailteascomponent
description: De component E-mailtaser kan een afbeelding, een titel, tekst met opmaak en eventueel een koppeling naar andere inhoud weergeven.
role: Architect, Developer, Admin, User
exl-id: d6123b22-7cba-406c-986d-b6f00322d135
source-git-commit: 3abc29e0c186a84f079d5938b8b716f4c7378d65
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---


# E-mailteascomponent {#email-teaser-component}

De component E-mailtaser kan een afbeelding, een titel, tekst met opmaak en eventueel een koppeling naar andere inhoud weergeven.

## Gebruik {#usage}

Met de component E-mailtaser kan de auteur van de inhoud eenvoudig een gummetje maken met een afbeelding, titel of tekst met opmaak en een koppeling maken naar andere inhoud of andere handelingen.

* De malplaatjeauteur kan de [ ontwerpdialoog ](#design-dialog) gebruiken om te bepalen als de opties om vraag-aan-acties tot stand te brengen en verbindingen toe te voegen beschikbaar zijn evenals het onbruikbaar maken van diverse vertoningsopties.
* De inhoudauteur kan [ gebruiken vormt dialoog ](#configure-dialog) om een beeld te plaatsen, CTAs te bepalen, titels en beschrijvingen te plaatsen, en verbindingen aan het individuele meetapparaat te vormen.
* Het [ geeft dialoog uit ](image.md#edit-dialog) van de [ Component van het Beeld E-mail ](image.md) kan worden betreden om het teaser beeld te wijzigen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de E-mailtasercomponent is v1, die in oktober 2022 is geïntroduceerd met release x van de Email Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatibel | - |

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Teaser E-mail [ kan op GitHub worden gevonden.](https://adobe.com/go/aem_cmp_tech_email_teaser_v1)

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden.](/help/developing/overview.md)

## Dialoogvenster configureren {#configure-dialog}

De auteur van de inhoud kan het dialoogvenster Configure gebruiken om de eigenschappen van de afzonderlijke teaser te definiëren. Er is ook een [ uitgeeft dialoog ](#edit-dialog) om het teasbeeld te wijzigen als men wordt geselecteerd.

### Tabblad Koppelingen {#links-tab}

![ E-mailTeaser Component geeft dialoogverbindingen tabel uit van de Component ](/help/email/assets/email-teaser-edit-links.png)

De teastitel, beschrijving en afbeelding kunnen worden overgeërfd van de gekoppelde inhoud of van de inhoud die is gekoppeld in de eerste oproep tot actie. Als noch een verbinding noch een vraag-aan-actie wordt gespecificeerd, dan zullen de titel, de beschrijving, en het beeld van de huidige inhoud worden geërft.

* **Verbinding** - dit dossier verbindt met inhoud, externe URL, of anker.
   * Klik het pictogram van de Campagne om [ Uitgezochte de Variabele van Adobe Campaign ](/help/email/campaign-variables.md) dialoog te openen om dynamische inhoud van Adobe Campaign op te nemen.
* **vraag-aan-acties** - Deze optie staat het verbinden aan veelvoudige bestemmingen toe.
   * De pagina verbonden in de eerste vraag-aan-actie wordt gebruikt wanneer het erven van de teastitel, de beschrijving, of het beeld.
   * Klik het pictogram van de Campagne om [ Uitgezochte de Variabele van Adobe Campaign ](/help/email/campaign-variables.md) dialoog te openen om dynamische inhoud van Adobe Campaign op te nemen.

### Tabblad Tekst {#text-tab}

![ E-mailTeaser Component geeft dialoogtekst tabel van de component uit ](/help/email/assets/email-teaser-edit-text.png)

* **Pretitle** - de voortitel zal vóór de titel van het meetapparaat worden getoond.
* **Titel** - bepaalt een titel om als titel voor het meetapparaat te tonen.
   * Klik het pictogram van de Campagne om [ Uitgezochte de Variabele van Adobe Campaign ](/help/email/campaign-variables.md) dialoog te openen om dynamische inhoud van Adobe Campaign op te nemen.
   * **krijgt titel van verbonden pagina** - wanneer gecontroleerd, zal de titel met de verbonden titel van de pagina worden bevolkt.
* **Beschrijving** - bepaalt een beschrijving aan vertoning als onderverdeling van het gummetje.
   * Klik het **Uitgezochte de Variabele van Adobe Campaign** pictogram om [ Uitgezochte de Variabele van Adobe Campaign ](/help/email/campaign-variables.md) dialoog te openen om dynamische inhoud van Adobe Campaign op te nemen.
   * **krijgt beschrijving van verbonden pagina** - wanneer gecontroleerd, zal de beschrijving met de verbonden beschrijving van de pagina worden bevolkt.
* **identiteitskaart** - Deze optie staat het controleren van het unieke herkenningsteken van de component in HTML toe.
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende inhoud te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor CSS.

### Tabblad Element {#asset-tab}

![ E-mailTeaser Component geeft dialoogbeeld tabel van de component uit ](/help/email/assets/email-teaser-edit-image.png)

* **erven geprezen beeld van pagina** - gebruik het beeld dat in de paginaeigenschappen van de verbonden pagina wordt bepaald of de huidige pagina als niets wordt gevonden.
* **activa van het Beeld** - Daling een activa van [ activa browser ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of ontvang **doorbladert** optie om van een lokaal dossiersysteem te uploaden.
   * Tik of klik **Duidelijk** om het momenteel geselecteerde beeld te deselecteren.
   * Tik of klik **uitgeven** [ om de vertoningen van de activa ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in de Redacteur van Activa te beheren.
* **Alternatieve tekst voor toegankelijkheid** - Dit gebied staat u toe om een beschrijving van het beeld voor visueel gehandicapte gebruikers te bepalen.
   * **erven alternatieve tekst van pagina** - Deze optie gebruikt de alternatieve beschrijving van de verbonden activawaarde van de `dc:description` meta-gegevens in DAM of van de huidige pagina als geen activa wordt verbonden.
* **verstrekt geen alternatieve tekst** - Deze optie merkt het beeld dat door ondersteunende technologieën zoals het schermlezers voor gevallen wordt genegeerd waar het beeld zuiver decoratief is of anders geen extra informatie aan de pagina overbrengt.

>[!NOTE]
>
>{de eigenschappen van 0} Dynamic Media ](image.md#dynamic-media) zijn momenteel niet beschikbaar in de Component van het Taser.[

### Tabblad Stijlen {#styles-tab-edit}

De component E-mail van de Taser steunt het AEM [ Systeem van de Stijl.](/help/get-started/authoring.md#component-styling)

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [ ontwerpdialoog ](#design-dialog) worden gevormd opdat het lusje beschikbaar is.

## Dialoogvenster Bewerken {#edit-dialog}

De component E-mail van het Taser delegeert beeld dat aan de [ Component van het Beeld ](image.md) teruggeeft. Daarom geeft [ dialoog uit ](image.md#edit-dialog) van de Component van het Beeld is beschikbaar aan de inhoudauteur om het teaser beeld te manipuleren.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de teasopties definiëren die de auteur van de inhoud heeft bij het gebruik van deze component.

### Taser Tab {#teaser-tab}

![ het ontwerpdialoog van de Component van de Teaser E-mail ](/help/email/assets/email-teaser-design.png)

* **Toegestane Elementen van de Kop** - gebruik drop-down om te bepalen welke HTML elementen van de rubriek die door een auteur voor het de titeltype van het apparaat kunnen worden geselecteerd.
* **StandaardElement van de Kop van de Titel** - het HTML element standaard van de kopbal dat voor het de titeltype van het apparaat wordt gebruikt
* **vraag-aan-Acties**
   * **maak vraag-aan-Acties** onbruikbaar - verberg **vraag-aan-Acties** optie voor inhoudsauteurs
* **Elementen**
   * **Verberg pretitle** - verbergt de **optie van de Pretitle** voor inhoudsauteurs
   * **Verberg titel** - verbergt de **optie van de Titel** voor inhoudsauteurs
      * Wanneer geselecteerd wordt het **Type van Titel** verborgen
   * **toon titeltype**
   * **Verberg beschrijving** - verberg de **optie van de Beschrijving** voor inhoudsauteurs
* **Afgevaardigde van het Beeld** - Informatieve vertoning die op welke component wijst e-mailTeaser beeld behandeling delegeert.

### Tabblad Stijlen {#styles-tab}

De component E-mail van de Taser steunt het AEM [ Systeem van de Stijl.](/help/get-started/authoring.md#component-styling)
