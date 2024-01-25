---
title: Adaptive Forms Core Component - Titel
description: De Adaptive Forms Title Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: 33eac885-8d66-4a5c-9a32-0ba11e6de293
source-git-commit: 8388de05c86641d4887b48a9fd10901cb5a19998
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---

# Titel {#title-input-adaptive-forms-core-component}

In een adaptief formulier verwijst een &quot;titel&quot; naar de tekst die boven aan het formulier wordt weergegeven, meestal onder de koptekst. De titel wordt opgegeven met de component Titel. Deze component kan worden toegevoegd aan de formulierindeling en de tekst ervan kan worden bewerkt, zodat deze overeenkomt met het doel of het onderwerp van het formulier. De titel dient als een label of korte beschrijving van het formulier voor de gebruiker en helpt het formulier van anderen te onderscheiden.

**Voorbeeld**

![voorbeeld](/help/adaptive-forms/assets/title.png)

## Gebruik {#reasons-to-use-title-in-an-adaptive-form}

Er zijn verschillende redenen waarom het een goede gewoonte is om een titel in een formulier te gebruiken:

- **Helderheid**: Een titel geeft duidelijk het doel van het formulier aan, zodat gebruikers kunnen zien welke informatie ze moeten verstrekken.

- **Organisatie**: Een titel kan u helpen formulieren in te delen op onderwerp of doel, zodat gebruikers gemakkelijker het formulier kunnen vinden dat ze nodig hebben.

- **Toegankelijkheid**: Een titel is een belangrijk element voor gebruikers met toegankelijkheidsbehoeften omdat deze door schermlezers hardop wordt voorgelezen, zodat gebruikers de context van het formulier kunnen begrijpen.

- **Branding**: Een titel kan ook worden gebruikt om de naam van een bedrijf of organisatie weer te geven, zodat u een gevoel van vertrouwen en vertrouwdheid met de gebruiker krijgt.

- **Navigatie**: Een titel kan ook nuttig zijn om door het formulier te navigeren, vooral als het formulier lang of complex is.

- **SEO (Search Engine Optimization)**: Een titel op het formulier is ook handig in SEO, omdat zoekprogramma&#39;s de titel gebruiken om de relevantie van een webpagina voor een zoekopdracht te bepalen.

Over het algemeen is de titel van een formulier een belangrijk aspect van de gebruikerservaring en moet deze worden gebruikt om een duidelijk en beknopt label voor het formulier te bieden waarmee gebruikers de context en het doel van het formulier kunnen begrijpen.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.12](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## Technische details {#technical-details}

Lees de nieuwste informatie over de Adaptive Forms Title Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/title/v1/title). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u uw ervaringen met titels eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig titels definiëren voor een naadloze gebruikerservaring.

![Het tabblad Basis](/help/adaptive-forms/assets/title_properties.png)

In het dialoogvenster Bewerken kan de auteur van de inhoud de titeltekst definiëren en het kopniveau selecteren.

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **Type/grootte** - Definieert het kopniveau van de titel.
- **ID** - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de gegevenslaag.
   - Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   - Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   - Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Ontwerpdialoogvenster {#design-dialog}

Het tabblad Ontwerp wordt gebruikt om CSS-stijlen voor de titelcomponent te definiëren en te beheren.

### Titel

Op het tabblad Titel kunnen sjabloonauteurs de standaardelementen en toegestane HTML-kopelementen voor formulierauteurs instellen:

![Titel van dialoogvenster Ontwerp, tabblad](/help/adaptive-forms/assets/title_heading.png)

- **Toegestane kopelementen**: Een lijst met meerdere opties waarmee de sjabloonauteur kan kiezen welke koppen de auteur van het formulier kan gebruiken voor Titel.

- **Standaardkopelement**: Een vervolgkeuzelijst die het standaardelement Kop voor de component Title instelt.

### Tabblad Stijlen {#styles-tab}

Het tabblad wordt gebruikt om CSS-stijlen voor een component te definiëren en te beheren. De Adaptive Forms Date-Picker Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Titel van dialoogvenster Ontwerp, tabblad](/help/adaptive-forms/assets/title_styles.png)

- **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms Title Core-component.

- **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Tabblad Opmaak {#format-tab}

Op het tabblad Indelingen kunt u standaard- en aangepaste datumnotaties opgeven.

![Tabblad Indeling](/help/adaptive-forms/assets/title_styles.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}