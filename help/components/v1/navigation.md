---
title: Navigatiecomponent (v1)
description: Met de navigatiecomponent kunnen gebruikers gemakkelijk door een geglobaliseerde sitestructuur navigeren.
role: Architect, Developer, Admin, User
exl-id: 0b7de79a-e0c7-4cf9-b5a9-c78cbc3ecd2f
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 0%

---

# Navigatiecomponent (v1) {#navigation-component}

Met de navigatiecomponent kunnen gebruikers gemakkelijk door een geglobaliseerde sitestructuur navigeren.

## Gebruik {#usage}

De navigatiecomponent geeft een lijst met pagina&#39;s weer, zodat gebruikers van een site gemakkelijk door de sitestructuur kunnen navigeren.

De navigatiecomponent kan automatisch de geglobaliseerde sitestructuur van uw site detecteren en [automatisch aanpassen aan een gelokaliseerde pagina.](#localized-site-structure) Bovendien kan het elke willekeurige sitestructuur ondersteunen door [omleidingspagina&#39;s schaduwen](#shadow-structure) om een andere structuur te vertegenwoordigen dan de belangrijkste inhoudsstructuur.

De [dialoogvenster bewerken](#edit-dialog) Hiermee kan de auteur van de inhoud de basispagina voor navigatie definiëren samen met de diepte van de navigatie. De [ontwerpdialoogvenster](#design-dialog) Hiermee kan de sjabloonauteur standaardwaarden definiëren voor de basis en diepte van de navigatie.

## Versie en compatibiliteit {#version-and-compatibility}

In dit document wordt versie 1 van de Navigation Component beschreven, die in januari 2018 is geïntroduceerd met release 2.0.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 1 van de navigatiecomponent beschreven.
>
>Zie voor meer informatie over de huidige versie van de navigatiecomponent de sectie [Navigatie-component](/help/components/navigation.md) document.

## Ondersteuning voor gelokaliseerde sitestructuur {#localized-site-structure}

Websites worden vaak in meerdere talen aangeboden voor verschillende regio&#39;s. Doorgaans bevat elke gelokaliseerde pagina een navigatie-element dat is opgenomen als onderdeel van de paginasjabloon. Met de navigatiecomponent kunt u de component één keer op een sjabloon plaatsen voor alle pagina&#39;s van uw site. Vervolgens wordt de component automatisch aangepast voor de afzonderlijke gelokaliseerde pagina&#39;s op basis van uw geglobaliseerde sitestructuur.

* Voor een voorbeeld van hoe de localisatiefunctie van de Component van de Navigatie werkt, zie [het onderstaande gedeelte](#example-localization).
* Voor een voorbeeld van hoe de lokalisatiefuncties van de Core Components samenwerken, raadpleegt u de [Localisatiefuncties van de pagina Core Components](/help/get-started/localization.md).

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

Voor de plaats WKND, zou u waarschijnlijk de Component van de Navigatie op een paginamalplaatje als deel van de kopbal willen plaatsen. Als een deel van de sjabloon is gemaakt, kunt u de **Navigatieroot** van de component `/content/wknd/language-masters/en` omdat dat de plaats is waar uw master inhoud voor die plaats begint. Misschien wilt u ook de **Navigatiestructuurdiepte** te worden `2` aangezien u waarschijnlijk niet de volledige inhoudsboom door de component, maar eerder de eerste twee niveaus wilt worden getoond zodat dient het als overzicht.

Met de **Navigatieroot** waarde, weet de component van de Navigatie dat na `/content/wknd/language-masters/en` dat de navigatie begint en navigatieopties kan genereren door de structuur van de site twee niveaus omlaag te recurderen (zoals gedefinieerd door de **Navigatiestructuurdiepte** waarde).

Ongeacht welke gelokaliseerde pagina een gebruiker bekijkt, kan de component van de Navigatie de overeenkomstige gelokaliseerde pagina vinden door de plaats van de huidige pagina te kennen, achterwaarts te werken aan de wortel, en dan door:sturen aan de overeenkomstige pagina.

Dus als een bezoeker bekijkt `/content/ch/de/experience/arctic-surfing-in-lofoten`kan de component de navigatiestructuur genereren op basis van `/content/wknd/language-masters/de`. Evenzo als de bezoeker de weergave uitvoert `/content/us/en/experience/arctic-surfing-in-lofoten`kan de component de navigatiestructuur genereren op basis van `/content/wknd/language-masters/en`.

## Ondersteuning voor schaduwsitestructuur {#shadow-structure}

Soms is het nodig om een navigatiemenu voor de bezoeker te maken dat afwijkt van de daadwerkelijke sitestructuur. Mogelijk moet een aanbieding bepaalde inhoud in het menu benadrukken door de lijst met inhoud opnieuw in te delen. Met behulp van schaduwpagina&#39;s, die eenvoudig worden omgeleid naar andere inhoudspagina&#39;s, kan de navigatiecomponent elke willekeurige navigatiestructuur genereren die nodig is.

Hiervoor moet u:

1. Schaduwpagina&#39;s maken als lege pagina&#39;s die uw gewenste sitestructuur voorstellen. Dit wordt vaak een schaduwsitestructuur genoemd.
1. Stel de **Omleiden** De waarden in de pagina-eigenschappen op deze pagina&#39;s wijzen naar de werkelijke inhoudspagina&#39;s.
1. Stel de **Verbergen in navigatie** in de pagina-eigenschappen van de schaduwpagina&#39;s.
1. Stel de **Navigatieroot** waarde van de component Navigation om naar de hoofdmap van de nieuwe structuur van de schaduwsite te wijzen.

De component Navigation geeft het menu vervolgens weer op basis van de structuur van de schaduwsite. De koppelingen die door de component worden gerenderd, verwijzen naar de inhoudspagina&#39;s die de schaduwpagina&#39;s omleiden en niet naar de schaduwpagina&#39;s zelf. Bovendien geeft de component de namen van de werkelijke pagina&#39;s weer en wordt de actieve pagina correct gemarkeerd, zelfs als de navigatie is gebaseerd op schaduwpagina&#39;s. De component Navigation maakt de schaduwpagina&#39;s volledig transparant voor de bezoeker.

>[!NOTE]
>Schaduwpagina&#39;s maken uw navigatieopties veel flexibeler, maar houd er rekening mee dat het onderhoud van deze structuur dan volledig handmatig is. Als u de eigenlijke site-inhoud opnieuw rangschikt of inhoud toevoegt/verwijdert, moet u de schaduwstructuur desgewenst handmatig bijwerken.

>[!NOTE]
>Bij het renderen van een schaduwsitestructuur worden alleen de schaduwpagina&#39;s teruggezet door de navigatielogica. De logica recurdeert niet de structuur van de omleidingsbestemmingen.

## Omleiding in navigatie {#redirects}

Wanneer een pagina een omleidingsdoel heeft (ongeacht of deze naar een externe URL of naar een andere AEM pagina verwijst), dan een navigatiecomponent die koppelingen naar dat punt rechtstreeks naar de URL van het omleidingsdoel bevat.

### Voorbeeld {#redirect-example}

* Maak een pagina A die wordt omgeleid naar pagina B.
* Een pagina C maken waarnaar wordt omgeleid `https://aemcomponents.dev`
* Voeg op pagina D een navigatie- of navigatiecomponent in die pagina A en C bevat
* De respectievelijke koppelingen die vervolgens worden gegenereerd, verwijzen rechtstreeks naar pagina B en `https://aemcomponents.dev`

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de navigatiecomponent wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_navigation).

## Technische details {#technical-details}

De meest recente technische documentatie over de navigatiecomponent [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_navigation_v1).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

>[!NOTE]
>
>Vanaf versie 2.1.0 van Core Components (Basiscomponenten) ondersteunt de Navigation Component [schema.org-microgegevens](https://schema.org).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de basispagina voor navigatie en de diepte van de navigatiestructuur definiëren.

### Tabblad Eigenschappen {#properties-tab}

![Eigenschappen tabblad van dialoogvenster Bewerken van navigatiecomponent](/help/assets/navigation-edit-properties.png)

* **Navigatieroot** - De basispagina, die wordt gebruikt om de boomstructuur te genereren.
* **Basisniveaus uitsluiten** - Vaak mag de hoofdmap niet in de navigatie worden opgenomen. Met deze optie kunt u opgeven hoeveel niveaus boven het basisniveau u wilt uitsluiten. Bijvoorbeeld:
   * 0 = basisniveau weergeven
   * 1 = sluit het wortelniveau uit
   * 2 = sluit de wortel uit en 1 meer niveau omhoog
   * enz.
* **Alle onderliggende pagina&#39;s verzamelen** - Verzamel alle pagina&#39;s die afstammen van de basisnavigatie.
* **Navigatiestructuurdiepte** - Definieert hoeveel niveaus onder de navigatiestructuur de component moet weergeven ten opzichte van de hoofdmap van de navigatie (alleen beschikbaar als **Alle onderliggende pagina&#39;s verzamelen** is niet geselecteerd).
* **Schaduwen uitschakelen** - Als de pagina in de hiërarchie een omleiding is, wordt de naam van de omleidingspagina weergegeven in plaats van het doel. Zie de [Ondersteuning voor schaduwsitestructuur](#shadow-structure) voor meer informatie .
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheidstabblad van dialoogvenster Navigatiecomponent bewerken](/help/assets/navigation-edit-accessibility.png)

Op de **Toegankelijkheid** tab, waarden kunnen worden ingesteld voor [Toegankelijkheid ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) labels voor de component.

* **Label** - Waarde van een ARIA-labelkenmerk voor de component

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de standaardwaarden instellen voor de basispagina van de navigatie en de diepte die aan de auteurs van de inhoud worden gepresenteerd.

### Tabblad Eigenschappen {#properties-tab-design}

![Ontwerpdialoogvenster van navigatiecomponent](/help/assets/navigation-design.png)

* **Navigatieroot** - De standaardwaarde van de basispagina van de navigatiestructuur, die wordt gebruikt om de navigatiestructuur te genereren en die standaard wordt ingesteld wanneer de auteur van de inhoud de component aan de pagina toevoegt.
* **Basisniveaus uitsluiten** - Vaak mag de hoofdmap niet in de navigatie worden opgenomen. Met deze optie kunt u de standaardinstelling opgeven voor hoeveel niveaus boven het basisniveau u wilt uitsluiten. Bijvoorbeeld:
   * 0 = basisniveau weergeven
   * 1 = sluit het wortelniveau uit
   * 2 = sluit de wortel uit en 1 meer niveau omhoog
   * enz.
* **Alle onderliggende pagina&#39;s verzamelen** - De standaardwaarde van de optie om alle pagina&#39;s te verzamelen die afstammelingen van de basisnavigatie zijn.
* **Navigatiestructuurdiepte** - De standaardwaarde van de diepte van de navigatiestructuur.
* **Schaduwen uitschakelen** - De standaardwaarde of schaduwen moet worden uitgeschakeld bij het toevoegen van een navigatiecomponent

### Tabblad Stijlen {#styles-tab}

De navigatiecomponent ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De navigatiecomponent ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
