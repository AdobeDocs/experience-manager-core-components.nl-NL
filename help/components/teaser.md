---
title: Teaser-component
description: De teaser-component kan een afbeelding, een titel, RTF-tekst en eventueel een koppeling naar andere inhoud weergeven.
translation-type: tm+mt
source-git-commit: e7aeff3a24cff14fbcd468561632ee1927c07b4e
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 1%

---


# Taser-component {#teaser-component}

De component van de Teaser Component van de Kern kan een beeld, een titel, rijke-tekst, en naar keuze verbinding aan verdere inhoud tonen.

## Gebruik {#usage}

Met de component Taser kan de auteur van de inhoud eenvoudig een gummetje maken om inhoud te verfraaien met een afbeelding, titel of tekst met opmaak en een koppeling naar andere inhoud of andere handelingen tot stand te brengen.

De malplaatjeauteur kan [ontwerpdialoog](#design-dialog) gebruiken om te bepalen als de opties om vraag-aan-acties tot stand te brengen en verbindingen toe te voegen beschikbaar zijn evenals het onbruikbaar maken van diverse vertoningsopties. De auteur van de inhoud kan [het dialoogvenster configureren](#configure-dialog) gebruiken om een afbeelding in te stellen, CTA&#39;s te definiëren, titels en beschrijvingen in te stellen en koppelingen naar de afzonderlijke teaser te configureren. Het [bewerkingsdialoogvenster](image.md#edit-dialog) van de [Afbeeldingscomponent](image.md) kan worden geopend om de laserafbeelding te wijzigen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Teaser Component is v1, die in juli 2018 is geïntroduceerd met versie 2.1.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel | Compatibel | Compatibel |

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_teaser) om de Taser Component te ervaren en voorbeelden van de bijbehorende configuratieopties en HTML- en JSON-uitvoer te bekijken.

### Technische details {#technical-details}

De recentste technische documentatie over de Component van het Taser [kan op GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1) worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in [de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden](/help/developing/overview.md).

## Dialoogvenster {#configure-dialog} configureren

De auteur van de inhoud kan het dialoogvenster Configure gebruiken om de eigenschappen van de afzonderlijke teaser te definiëren. Er is ook een [bewerkingsdialoogvenster](#edit-dialog) om de laserafbeelding te wijzigen als er een is geselecteerd.

### Afbeelding {#image}

![Het tabblad Afbeelding van het dialoogvenster Bewerken van de Teasercomponent](/help/assets/teaser-edit-image.png)

* **Afbeeldingselement**
   * Zet een element neer vanuit de [assetbrowser](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of tik op de optie **browse** om te uploaden vanaf een lokaal bestandssysteem.
   * Tik of klik op **Wissen** om de selectie van de geselecteerde afbeelding ongedaan te maken.
   * Tik of klik op **Bewerken** om de uitvoeringen van het element te beheren](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in de elementeneditor.[

>[!NOTE]
>
>[Dynamic Media-](image.md#dynamic-media) functies zijn momenteel niet beschikbaar in de Taser-component.

### Tekst {#text}

![Het teksttabblad van het dialoogvenster Bewerken van de component Teaser](/help/assets/teaser-edit-text.png)

* **Pretitle**  - De voortitel wordt weergegeven vóór de titel van de teaser.
* **Titel**  - Definieert een titel die moet worden weergegeven als de kop voor het gummetje.
   * **Kopieer de titel van de gekoppelde pagina** . Als deze optie is ingeschakeld, wordt de titel van de gekoppelde pagina ingevuld.
* **Beschrijving**  - Definieert een beschrijving die moet worden weergegeven als subcode van het gummetje.
   * **Beschrijving ophalen van gekoppelde pagina** . Als deze optie is ingeschakeld, wordt de beschrijving gevuld met de beschrijving van de gekoppelde pagina.
* **ID**  - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de  [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Koppelingen en handelingen {#links-actions}

![Het tabblad voor het dialoogvenster voor het bewerken van de component Teaser](/help/assets/teaser-edit-link.png)

* **Koppeling**  - Koppeling toegepast op het taser. Gebruik de padbrowser om het doel van de koppeling te selecteren.
* **Laat vraag-aan-Acties**  toe wanneer gecontroleerd, laat definitie van vraag-aan-Acties toe. De eerste vraag-aan-actie verbinding in de lijst wordt gebruikt als verbinding voor andere teaser elementen.

## Dialoogvenster {#edit-dialog} bewerken

De component Teaser delegeert het renderen van afbeeldingen aan de [Image Component](image.md). Daarom is het dialoogvenster [bewerken](image.md#edit-dialog van de Image Component beschikbaar voor de auteur van de inhoud om de teasafbeelding te bewerken.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de teasopties definiëren die de auteur van de inhoud heeft bij het gebruik van deze component.

### Tabblad Taser {#teaser-tab}

![Ontwerpdialoogvenster van de Teaser Component](/help/assets/teaser-design.png)

* **Oproep tot actie**
   * **Schakel Vraag-aan-Acties**  uit - verberg de  **vraag-aan-** Actie optie voor inhoudsauteurs
* **Elementen**
   * **Voortitel**  verbergen - Hiermee verbergt u de optie  **** Voorkeuren voor auteurs van inhoud
   * **Titel**  verbergen - Hiermee verbergt u de optie  **** Titel voor auteurs van inhoud
      * Als deze optie is geselecteerd, wordt het **Titeltype** verborgen
   * **Beschrijving**  verbergen - De optie  **** Omschrijving verbergen voor auteurs van inhoud
* **Titeltype**  - Hiermee definieert u de tag H die moet worden gebruikt door de titel van het gummetje.
* **Koppelingen**
   * **Koppel de afbeelding**  niet. Als deze optie is geselecteerd, wordt de laserafbeelding niet gekoppeld
   * **De titel**  niet koppelen. Als deze optie is geselecteerd, is de teastitel niet gekoppeld
* **Afbeelding gedelegeerd**  - Informatieweergave die aangeeft aan welke component de taser de beeldverwerking delegeert.

### Tabblad Stijlen {#styles-tab}

De component Teaser ondersteunt het AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).
