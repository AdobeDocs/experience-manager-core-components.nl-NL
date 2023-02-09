---
title: Adaptive Forms Core Component - Tekst
description: De Adaptive Forms Text Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
source-git-commit: 1e6460d318f4f9a5dfdcbb81723da01b51b72f3f
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 1%

---


# Tekst {#text-adaptive-forms-core-component}

In een adaptief formulier verwijst de tekst naar de inhoud die op het formulier wordt weergegeven en die de gebruiker kan lezen. Dit kan de tekst omvatten die wordt gebruikt om een groep vormelementen, zoals tekstgebieden, evenals om het even welke extra instructies of informatie te etiketteren die aan de gebruiker wordt verstrekt.

Hierdoor kan de structuur van een formulier ook worden opgedeeld in logische secties, zodat gebruikers het formulier eenvoudiger kunnen begrijpen en invullen. Bovendien kan het worden gebruikt voor toegankelijkheidsdoeleinden om een korte beschrijving te geven van het element waaraan het is gekoppeld. Een dergelijk tekstveld wordt doorgaans weergegeven in de buurt van de formuliercomponenten, bijvoorbeeld ervóór of erna.

**Voorbeeld**

![](/help/adaptive-forms/assets/text.png)

## Gebruik {#reasons-to-use-text-label}

Er zijn verschillende redenen om tekst in een formulier te gebruiken:

* **Instructies opgeven**: Tekst kan worden gebruikt om instructies te geven over het invullen van het formulier of over de vereiste informatie.

* **Context leveren**: Tekst kan worden gebruikt om context voor het formulier te bieden, zoals het doel van het formulier of de organisatie die de informatie verzamelt.

* **Het formulier opsplitsen in logische secties**: Met tekst kunt u een formulier opsplitsen in logische secties, zodat gebruikers het formulier eenvoudiger kunnen begrijpen en invullen.

* **Branding en identiteit**: Tekst kan worden gebruikt voor branding en identiteitsdoeleinden, zoals het opnemen van de naam van de organisatie in het formulier.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Text Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/versions.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Core Components-versies](/help/versions.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Ga voor de meest recente informatie over de Adaptive Forms Text Core Component naar de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/text/v1/text). Raadpleeg de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de tekstervaring voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig tekstopties definiëren voor een naadloze gebruikerservaring.

![Het tabblad Basis](/help/adaptive-forms/assets/text_properties.png)

* **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

* **Bindverwijzing** - Een bind verwijzing is een verwijzing naar een gegevenselement dat in een externe gegevensbron wordt opgeslagen en in een vorm wordt gebruikt. Met de bind-verwijzing kunt u gegevens dynamisch binden aan formuliervelden, zodat in het formulier de meest actuele gegevens uit de gegevensbron kunnen worden weergegeven. Een bind-verwijzing kan bijvoorbeeld worden gebruikt om de naam en het adres van een klant in een formulier weer te geven op basis van de id van de klant die in het formulier is ingevoerd. De bind verwijzing kan ook worden gebruikt om de gegevensbron met gegevens bij te werken ingegaan in de vorm. Op deze manier kunt u in AEM Forms formulieren maken die interageren met externe gegevensbronnen, zodat u een naadloze gebruikerservaring hebt voor het verzamelen en beheren van gegevens.
* **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.
* **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.


## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Text te definiëren en te beheren.


### Tabblad Stijlen {#styles-tab}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Text Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

**Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Text Core-component.

**Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight&quot; opgeven: vet&quot;. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.
