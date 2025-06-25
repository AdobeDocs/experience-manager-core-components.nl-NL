---
title: Navigatie-component
description: Met de navigatiecomponent kunnen gebruikers gemakkelijk door een geglobaliseerde sitestructuur navigeren.
role: Architect, Developer, Admin, User
exl-id: 9154f2a3-3d1e-4865-a413-298748fa66d3
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '1544'
ht-degree: 0%

---


# Navigatie-component{#navigation-component}

Met de navigatiecomponent kunnen gebruikers gemakkelijk door een geglobaliseerde sitestructuur navigeren.

{{traditional-aem}}

## Gebruik {#usage}

In de navigatiecomponent wordt een boomstructuur met pagina&#39;s weergegeven, zodat gebruikers van een site gemakkelijk door de sitestructuur kunnen navigeren.

De component van de Navigatie kan automatisch de geglobaliseerde plaatsstructuur van uw plaats ontdekken en [ aanpassen automatisch aan een gelokaliseerde pagina.](#localized-site-structure) Bovendien kan het om het even welke willekeurige plaatsstructuur steunen door [ schaduw te gebruiken herleidt pagina&#39;s ](#shadow-structure) om een andere structuur buiten uw belangrijkste inhoudsstructuur te vertegenwoordigen.

Het [ geeft dialoog uit ](#edit-dialog) staat de inhoudauteur toe om de pagina van de navigatiekarakter samen met de diepte van navigatie te bepalen. De [ ontwerpdialoog ](#design-dialog) staat de malplaatjeauteur toe om standaardwaarden voor de navigatiekartel en de diepte te bepalen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Navigation Component is v2, die in februari 2022 werd geïntroduceerd met versie 2.18.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | - | Compatibel | Compatibel | Compatibel |
| [ v1 ](v1/navigation.md) | Compatibel | Compatibel | - | Compatibel |

Voor meer informatie over de versies en versies van de Component van de Kern, zie de Versies van de Componenten van de Document [ Kern ](/help/versions.md).

## Ondersteuning voor gelokaliseerde sitestructuur {#localized-site-structure}

Websites worden vaak in meerdere talen aangeboden voor verschillende gebieden. Doorgaans bevat elke gelokaliseerde pagina een navigatie-element dat is opgenomen als onderdeel van de paginasjabloon. Met de navigatiecomponent kunt u de component één keer op een sjabloon plaatsen voor alle pagina&#39;s van uw site. Vervolgens wordt de component automatisch aangepast voor de afzonderlijke gelokaliseerde pagina&#39;s op basis van uw geglobaliseerde sitestructuur.

* Voor een voorbeeld van hoe de localisatieeigenschap van de Component van de Navigatie werkt, zie [ de sectie hieronder ](#example-localization).
* Voor een voorbeeld van hoe de localisatieeigenschappen van de Componenten van de Kern samenwerken, zie de [ Eigenschappen van de Localisatie van de pagina van de Componenten van de Kern ](/help/get-started/localization.md).

### Voorbeeld {#example-localization}

Laten we zeggen dat uw inhoud er ongeveer als volgt uitziet:

```
/content
+-- wknd
   +-- language-masters
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- es
      +-- fr
      \-- it
   +-- us
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      \-- es
   \-- ch
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Voor de plaats WKND, zou u waarschijnlijk de Component van de Navigatie op een paginamalplaatje als deel van de kopbal willen plaatsen. Zodra een deel van het malplaatje, kunt u de **Wortel van de Navigatie** van de component aan `/content/wknd/language-masters/en` plaatsen aangezien dat is waar uw hoofdinhoud voor die plaats begint. U zou misschien ook de **Diepte van de Structuur van de Navigatie** willen plaatsen om `2` te zijn aangezien u waarschijnlijk niet de volledige inhoudsboom door de component moet worden getoond, maar eerder de eerste twee niveaus zodat dient het als overzicht.

Met de **waarde van de Wortel van de Navigatie**, weet de Component van de Navigatie dat na `/content/wknd/language-masters/en` dat de navigatie begint en het navigatieopties kan produceren door de structuur van de plaats twee niveaus neer te recurderen (zoals die door de **waarde van de Diepte van de Structuur van de Navigatie** wordt bepaald).

Ongeacht welke gelokaliseerde pagina een gebruiker bekijkt, kan de component van de Navigatie de overeenkomstige gelokaliseerde pagina vinden door de plaats van de huidige pagina te kennen, achterwaarts te werken aan de wortel, en dan door:sturen aan de overeenkomstige pagina.

Dus als een bezoeker `/content/ch/de/experience/arctic-surfing-in-lofoten` bekijkt, weet de component dat de navigatiestructuur moet worden gegenereerd op basis van `/content/wknd/language-masters/de` . Op dezelfde manier als de bezoeker `/content/us/en/experience/arctic-surfing-in-lofoten` bekijkt, weet de component dat de navigatiestructuur moet worden gegenereerd op basis van `/content/wknd/language-masters/en` .

## Ondersteuning voor schaduwsitestructuur {#shadow-structure}

Soms is het nodig om een navigatiemenu voor de bezoeker te maken dat afwijkt van de daadwerkelijke sitestructuur. Mogelijk moet een aanbieding bepaalde inhoud in het menu benadrukken door de lijst met inhoud opnieuw in te delen. Met behulp van schaduwpagina&#39;s, die eenvoudig worden omgeleid naar andere inhoudspagina&#39;s, kan de navigatiecomponent elke willekeurige navigatiestructuur genereren die nodig is.

Hiervoor moet u:

1. Schaduwpagina&#39;s maken als lege pagina&#39;s die uw gewenste sitestructuur voorstellen. Dit wordt vaak een schaduwsitestructuur genoemd.
1. Plaats de **omleiden** waarden in de paginaeigenschappen op deze pagina&#39;s om aan de daadwerkelijke inhoudspagina&#39;s te richten.
1. Plaats de **Verbergen in Navigatie** optie in de paginaeigenschappen van de schaduwpagina&#39;s.
1. Plaats de **waarde van de Wortel van de Navigatie** &lbrace;van de Component van de Navigatie om aan de wortel van de nieuwe structuur van de schaduwplaats te richten.

De component Navigation geeft het menu vervolgens weer op basis van de structuur van de schaduwsite. De koppelingen die door de component worden gerenderd, verwijzen naar de inhoudspagina&#39;s die de schaduwpagina&#39;s omleiden en niet naar de schaduwpagina&#39;s zelf. Bovendien geeft de component de namen van de werkelijke pagina&#39;s weer en wordt de actieve pagina correct gemarkeerd, zelfs als de navigatie is gebaseerd op schaduwpagina&#39;s. De component Navigation maakt de schaduwpagina&#39;s volledig transparant voor de bezoeker.

>[!NOTE]
>Schaduwpagina&#39;s maken uw navigatieopties veel flexibeler, maar houd er rekening mee dat het onderhoud van deze structuur dan volledig handmatig is. Als u de eigenlijke site-inhoud opnieuw rangschikt of inhoud toevoegt/verwijdert, moet u de schaduwstructuur desgewenst handmatig bijwerken.

>[!NOTE]
>Bij het renderen van een schaduwsitestructuur worden alleen de schaduwpagina&#39;s teruggezet door de navigatielogica. De logica recurdeert niet de structuur van de omleidingsbestemmingen.

## Omleiding in navigatie {#redirects}

Wanneer een pagina een omleidingsdoel heeft (ongeacht of deze naar een externe URL of naar een andere AEM-pagina verwijst), dan een navigatiecomponent die koppelingen naar dat punt rechtstreeks naar de URL van het omleidingsdoel bevat.

### Voorbeeld {#redirect-example}

* Maak een pagina A die wordt omgeleid naar pagina B.
* Een pagina C maken die wordt omgeleid naar `https://aemcomponents.dev`
* Voeg op pagina D een navigatie- of navigatiecomponent in die pagina A en C bevat
* De respectievelijke koppelingen die worden gegenereerd, verwijzen vervolgens rechtstreeks naar pagina B en `https://aemcomponents.dev`

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Navigatie te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output te zien JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_navigation).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Navigatie [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_navigation_v2) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

>[!NOTE]
>
>Vanaf versie 2.1.0 van de Componenten van de Kern, steunt de Component van de Navigatie [ schema.org microdata ](https://schema.org).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de basispagina voor navigatie en de diepte van de navigatiestructuur definiëren.

### Tabblad Eigenschappen {#properties-tab}

![ de component van de Navigatie geeft dialoogeigenschappen tabel uit ](/help/assets/navigation-edit-properties.png)

* **Basis van de Navigatie** - de wortelpagina, die zal worden gebruikt om de navigatieboom te produceren.
* **sluit de Niveaus van de Wortel** uit - vaak zou de wortel niet in de navigatie moeten worden omvat. Met deze optie kunt u opgeven hoeveel niveaus boven het basisniveau u wilt uitsluiten. Bijvoorbeeld:
   * 0 = basisniveau weergeven
   * 1 = sluit het wortelniveau uit
   * 2 = sluit de wortel uit en 1 meer niveau omhoog
   * enz.
* **verzamel alle kindpagina&#39;s** - verzamel alle pagina&#39;s die nakomelingen van de navigatiewortel zijn.
* **de Diepte van de Structuur van de Navigatie** - bepaalt hoeveel niveaus onderaan de navigatieboom de component met betrekking tot de navigatiewortel (slechts beschikbaar wanneer **verzamel alle kindpagina&#39;s** niet wordt geselecteerd) zou moeten tonen.
* **maak schaduw** onbruikbaar - als de pagina in de hiërarchie een omleiding is, zal de naam van de het omleiden pagina in plaats van het doel worden getoond. Zie de [ Steun van de Structuur van de Plaats van de Schaduw ](#shadow-structure) voor meer informatie.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Toegankelijkheid {#accessibility-tab}

![ de component van de Navigatie geeft dialoogtoegankelijkheid tabel uit ](/help/assets/navigation-edit-accessibility.png)

Op het **lusje van de Toegankelijkheid**, kunnen de waarden voor [ de toegankelijkheidslabels van ARIA ](https://www.w3.org/WAI/standards-guidelines/aria/) voor de component worden geplaatst.

* **Etiket** - Waarde van een ARIA etiketattribuut voor de component

### Tabblad Stijlen {#styles-tab-edit}

De Component van de Navigatie steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [ ontwerpdialoog ](#design-dialog) worden gevormd opdat het drop-down menu beschikbaar is.

![ Stijlen lusje van uitgeeft dialoog van de Component van de Navigatie ](/help/assets/navigation-edit-styles.png)

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de standaardwaarden instellen voor de basispagina van de navigatie en de diepte die aan de auteurs van de inhoud worden gepresenteerd.

### Tabblad Eigenschappen {#properties-tab-design}

![ het ontwerpdialoog van de Component van de Navigatie ](/help/assets/navigation-design.png)

* **Wortel van de Navigatie** - de standaardwaarde van de wortelpagina van de navigatiestructuur, die zal worden gebruikt om de navigatieboom te produceren en in gebreke te blijven wanneer de inhoudauteur de component aan de pagina toevoegt.
* **sluit de Niveaus van de Wortel** uit - vaak zou de wortel niet in de navigatie moeten worden omvat. Met deze optie kunt u de standaardinstelling opgeven voor hoeveel niveaus boven het basisniveau u wilt uitsluiten. Bijvoorbeeld:
   * 0 = basisniveau weergeven
   * 1 = sluit het wortelniveau uit
   * 2 = sluit de wortel uit en 1 meer niveau omhoog
   * enz.
* **verzamel alle kindpagina&#39;s** - de standaardwaarde van de optie om alle pagina&#39;s te verzamelen die nakomelingen van de navigatiewortel zijn.
* **Diepte van de Structuur van de Navigatie** - de standaardwaarde van de diepte van de navigatiestructuur.
* **maak schaduw** onbruikbaar - de standaardwaarde van als het schaduwen zou moeten worden onbruikbaar gemaakt wanneer het toevoegen van een navigatiecomponent

### Tabblad Stijlen {#styles-tab}

De component van de Navigatie steunt het Systeem van de Stijl van AEM [&#128279;](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

De Component van de Navigatie steunt de [ Laag van de Gegevens van de Cliënt van Adobe.](/help/developing/data-layer/overview.md)
