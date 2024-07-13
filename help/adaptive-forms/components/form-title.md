---
title: Adaptive Forms Core Component - Titel
description: De Adaptive Forms Title Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: 33eac885-8d66-4a5c-9a32-0ba11e6de293
source-git-commit: 8bba79956a04020647d5d04f9fe6fa674affedf1
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 0%

---

# Component titel van formulier{#title-input-adaptive-forms-core-component}

In een adaptief formulier verwijst een &quot;titel&quot; naar de tekst die boven aan het formulier wordt weergegeven, meestal onder de koptekst. De titel wordt opgegeven met de component Titel. Deze component kan worden toegevoegd aan de formulierindeling en de tekst ervan kan worden bewerkt, zodat deze overeenkomt met het doel of het onderwerp van het formulier. De titel dient als een label of korte beschrijving van het formulier voor de gebruiker en helpt het formulier van anderen te onderscheiden.

**Voorbeeld**

![ voorbeeld van titel ](/help/adaptive-forms/assets/title.png)

## Gebruik {#reasons-to-use-title-in-an-adaptive-form}

Er zijn verschillende redenen waarom het een goede gewoonte is om een titel in een formulier te gebruiken:

- **Duidelijkheid**: Een titel identificeert duidelijk het doel van de vorm, die gebruikers helpt begrijpen welke informatie zij moeten verstrekken.

- **Organisatie**: Een titel kan helpen om vormen door onderwerp of doel te organiseren, dat het voor gebruikers gemakkelijker maakt om de vorm te vinden zij nodig hebben.

- **Toegankelijkheid**: Een titel is een zeer belangrijk element voor gebruikers met toegankelijkheidsbehoeften, aangezien het hardop door het schermlezers wordt gelezen, die gebruikers helpen de context van de vorm begrijpen.

- **Branding**: Een titel kan ook worden gebruikt om de naam van een bedrijf of organisatie te tonen, die helpt om een gevoel van vertrouwen en vertrouwdheid met de gebruiker tot stand te brengen.

- **Navigatie**: Een titel kan ook nuttig zijn om door de vorm te navigeren, vooral als de vorm lang of complex is.

- **Optimalisering van de Motor van het Onderzoek (SEO)**: Het hebben van een titel op de vorm helpt ook in SEO, aangezien de onderzoeksmotoren de titel gebruiken om de relevantie van een Web-pagina aan een onderzoeksvraag te bepalen.

Over het algemeen is de titel van een formulier een belangrijk aspect van de gebruikerservaring en moet deze worden gebruikt om een duidelijk en beknopt label voor het formulier te bieden waarmee gebruikers de context en het doel van het formulier kunnen begrijpen.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/adaptive-forms/version.md) en later | Compatibel met <br>[ versie 1.1.12 ](/help/adaptive-forms/version.md) en later maar minder dan 2.0.0. |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het ](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0}.[

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technische details {#technical-details}

Krijg de recentste informatie over de AanpassingsComponent van de Kern van de Titel van Forms in de technische documentatie over [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/title/v1/title). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u uw ervaringen met titels eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig titels definiëren voor een naadloze gebruikerservaring.

![ Basis lusje ](/help/adaptive-forms/assets/title_properties.png)

In het dialoogvenster Bewerken kan de auteur van de inhoud de titeltekst definiëren en het kopniveau selecteren.

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bovenop de component. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **Type /Size** - bepaalt het kopniveau van de titel.
- **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de Laag van Gegevens te controleren.
   - Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   - Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   - Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

Het tabblad Ontwerp wordt gebruikt om CSS-stijlen voor de component Titel van het formulier te definiëren en te beheren.

### Titel

Op het tabblad Titel kunnen sjabloonauteurs de standaardelementen en toegestane HTML-kopelementen voor formulierauteurs instellen:

![ lusje van de de dialoogtitel van het Ontwerp ](/help/adaptive-forms/assets/title_heading.png)

- **Toegestane Elementen van de Kop**: Een lijst met veelvoudige opties die de malplaatjeauteur laat kiezen welke rubrieken auteur voor Titel kunnen vormen.

- **Standaard het Element van de Kop**: Een drop-down lijst die het standaardelement van de Kop voor de component van de Titel plaatst.

### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De adaptieve de datum-plukkerComponent van de Kern van Forms steunt het AEM [ Systeem van de Stijl ](/help/get-started/authoring.md#component-styling).

![ lusje van de de dialoogtitel van het Ontwerp ](/help/adaptive-forms/assets/title_styles.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de Aangepaste Component van de Kern van de Titel van Forms verstrekken.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Tabblad Opmaak {#format-tab}

Op het tabblad Indelingen kunt u standaard- en aangepaste datumnotaties opgeven.

![ het Lusje van het Formaat ](/help/adaptive-forms/assets/title_styles.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Verwante artikelen {#related-articles}


{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}