---
title: Component Form Container
description: Met de Core Component Form Container Component kunnen eenvoudige verzendformulieren worden gemaakt.
role: Architect, Developer, Admin, User
exl-id: 552f9dd5-6a3a-42d9-9969-e62a1f36e811
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 0%

---

# Component Form Container {#form-container-component}

Met de Core Component Form Container Component kunnen eenvoudige verzendformulieren worden gemaakt.

## Gebruik {#usage}

Met de component Form Container kunt u formulieren en functies voor eenvoudige informatieverzending maken door eenvoudige WCM-formulieren te ondersteunen en door een geneste structuur te gebruiken om extra formuliercomponenten toe te staan.

Door [ te gebruiken vormt dialoog ](#configure-dialog) de inhoudsleider kan de actie bepalen die door vormvoorlegging wordt teweeggebracht, URl die de voorlegging zou moeten behandelen, en of een werkschema zou moeten worden teweeggebracht. De malplaatjeauteur kan de [ ontwerpdialoog ](#design-dialog) gebruiken om de toegestane componenten en hun afbeeldingen te bepalen gelijkend op de ontwerpdialoog voor de [ standaardlay-outcontainer in de malplaatjedacteur ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=nl-NL).

>[!NOTE]
>
>De kerncomponenten Form Container Component ondersteunen alleen het gebruik van basiscomponenten van componenten (knop, tekst, verborgen enz.). Het gebruiken van [ stichtingscomponenten ](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/siteandpage/default-components-foundation.html?lang=nl-NL) vormcomponenten binnen de kerncomponenten van container (en vice versa) wordt niet gesteund.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Form Container Component is v2, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | Compatibel systeem met <br>[ versie 2.17.4 ](/help/versions.md) en vroeger | Compatibel | Compatibel | Compatibel |
| [ v1 ](/help/components/v1/form-container-v1.md) | Compatibel | Compatibel | - | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Container van de Vorm te ervaren evenals voorbeelden van zijn configuratieopties evenals uitvoer te zien HTML en JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_form_container).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Container van de Vorm [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_form_container_v2) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud definiëren welke handelingen worden uitgevoerd wanneer de component wordt verzonden.

Afhankelijk van het geselecteerde **Type van Actie**, zullen de beschikbare opties binnen de container veranderen. De beschikbare actietypen zijn:

* [Formuliergegevens verzenden](#post-data)
* [Mail](#mail)
* [Winkelinhoud](#store-content)

Ongeacht het type, zijn er [ algemene montages ](#general-settings) die op elke actie van toepassing zijn.

### Formuliergegevens verzenden {#post-data}

Wanneer het formulier wordt verzonden, worden de ingediende gegevens door het actietype voor postformuliergegevens doorgegeven aan een derde als JSON voor verwerking.

![ de opties van de Gegevens van de Vorm in de Edit dialoog van de Component van de Container van de Vorm ](/help/assets/form-container-edit-post.png)

* **Eindpunt** - de volledig-gekwalificeerde dienst HTTPS die de gegevens zal verwerken
* **Bericht van de Fout** - Bericht om te tonen als de voorlegging niet succesvol is

>[!TIP]
>Er zijn extra time-outopties die een systeembeheerder kan aanpassen om de verwerking van doorgestuurde formuliergegevens af te handelen. [ zie de technische documentatie op GitHub voor meer informatie.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/actions/rpc)

### Mail {#mail}

Wanneer het formulier wordt verzonden, verzendt het type e-mailactie een e-mail naar aangewezen ontvangers.

![ de opties van de Post in de Edit dialoog van de Component van de Container van de Vorm ](/help/assets/form-container-edit-mail.png)

* **Onderwerp** - Het onderwerp van e-mail dat als vormvoorlegging zal worden verzonden
* **van** - de van e-mailadres van e-mail die op vormvoorlegging zal worden verzonden
* **aan** - de adressen van de ontvangers die een e-mail op vormvoorlegging zullen ontvangen
   * Tik of klik **voeg** knoop toe om extra adressen toe te voegen
   * Tik of klik de **Schrapping** knoop om een e-mailadres te verwijderen
* **CC** - de adressen van ontvangers die een koolstofkopie zullen ontvangen e-mail die op vormvoorlegging wordt verzonden
   * Tik of klik **voeg** knoop toe om extra adressen toe te voegen
   * Tik of klik de **Schrapping** knoop om een e-mailadres te verwijderen

### Winkelinhoud {#store-content}

Wanneer het formulier wordt verzonden, wordt de inhoud van het formulier opgeslagen in een aangewezen opslagplaats.

![ de inhoudopties van de opslag in de Edit dialoog van de Container van de Vorm ](/help/assets/form-container-edit-store.png)

* **Weg van de Inhoud** - de weg van de bewaarplaats van de Inhoud waar de voorgelegde inhoud wordt opgeslagen
* **Gegevens van de Mening** - Tik of klik om opgeslagen voorgelegde gegevens als JSON te bekijken
* **Werkschema van het Begin** - vorm om een werkschema met de opgeslagen inhoud als nuttige lading op vormvoorlegging te beginnen

>[!NOTE]
>
>Om het beheer van gebruikersgegevens eenvoudiger te maken en scheiding van zorgen af te dwingen, wordt het over het algemeen niet aanbevolen door gebruikers gegenereerde inhoud in de opslagplaats op te slaan.
>
>In plaats daarvan gebruik het [ de actietype van de Gegevens van de Vorm van het Post ](#post-data) om gebruikersinhoud tot een specifieke dienstverlener over te gaan.

### Algemene instellingen {#general-settings}

Ongeacht het geselecteerde handelingstype, kan een pagina van dank u altijd worden bepaald.

![ Algemene opties in de Edit dialoog van de Component van de Container van de Vorm ](/help/assets/form-container-edit-general.png)

* **Dank u pagina** - de gebruiker zal aan de gespecificeerde pagina na voltooiing van de vormvoorlegging worden opnieuw gericht.
   * Gebruik het dialoogvenster Selectie om een bron in AEM te selecteren.
   * Geef de absolute URL op als de pagina Bedankt niet in AEM staat. Niet-absolute URL&#39;s worden geïnterpreteerd ten opzichte van AEM.
   * Laat leeg om het formulier na verzending opnieuw weer te geven.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

De ontwerpdialoog staat de malplaatjeauteur toe om de toegestane componenten en hun afbeeldingen voor de container te bepalen gelijkend op de ontwerpdialoog voor de [ standaardlay-outcontainer in de malplaatjedacteur ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=nl-NL).

### Tabblad Stijlen {#styles-tab}

De component van de Container van de Vorm steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).
