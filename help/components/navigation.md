---
title: Navigatie-component
description: Met de navigatiecomponent kunnen gebruikers gemakkelijk door een geglobaliseerde sitestructuur navigeren.
translation-type: tm+mt
source-git-commit: ff943aeca0333b13e2b9aaf11f316457f001d507
workflow-type: tm+mt
source-wordcount: '1369'
ht-degree: 0%

---


# Navigatie-component{#navigation-component}

Met de navigatiecomponent kunnen gebruikers gemakkelijk door een geglobaliseerde sitestructuur navigeren.

## Gebruik {#usage}

De navigatiecomponent geeft een lijst met pagina&#39;s weer, zodat gebruikers van een site gemakkelijk door de sitestructuur kunnen navigeren.

De component Navigatie kan automatisch de geglobaliseerde sitestructuur van uw site detecteren en automatisch [aanpassen aan een gelokaliseerde pagina.](#localized-site-structure) Bovendien kan de toepassing elke willekeurige sitestructuur ondersteunen door [schaduwomleidingspagina](#shadow-structure) &#39;s te gebruiken om een andere structuur dan de belangrijkste inhoudsstructuur weer te geven.

In het dialoogvenster [](#edit-dialog) Bewerken kan de auteur van de inhoud de basispagina voor navigatie en de diepte van de navigatie definiëren. In het [ontwerpdialoogvenster](#design-dialog) kan de sjabloonauteur standaardwaarden definiëren voor de basiswaarde en diepte van de navigatie.

## Ondersteuning voor gelokaliseerde sitestructuur {#localized-site-structure}

Websites worden vaak in meerdere talen aangeboden voor verschillende regio&#39;s. Doorgaans bevat elke gelokaliseerde pagina een navigatie-element dat is opgenomen als onderdeel van de paginasjabloon. Met de navigatiecomponent kunt u de component één keer op een sjabloon plaatsen voor alle pagina&#39;s van uw site. Vervolgens wordt de component automatisch aangepast voor de afzonderlijke gelokaliseerde pagina&#39;s op basis van uw geglobaliseerde sitestructuur.

* Zie [de onderstaande](#example-localization)sectie voor een voorbeeld van de werking van de lokalisatiefunctie van de navigatiecomponent.
* Zie de [lokalisatiefuncties van de pagina](/help/get-started/localization.md)Core Components voor een voorbeeld van hoe de lokalisatiefuncties van de Core Components samenwerken.

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

Voor de plaats WKND, zou u waarschijnlijk de Component van de Navigatie op een paginamalplaatje als deel van de kopbal willen plaatsen. Als u eenmaal een deel van de sjabloon hebt gemaakt, kunt u de **navigatieroot** van de component instellen op `/content/wknd/language-masters/en` aangezien dat de plaats is waar de master inhoud van die site begint. U zou misschien ook de diepte **van de** Navigatiestructuur willen plaatsen om te zijn `2` aangezien u waarschijnlijk niet de volledige inhoudsboom door de component, maar eerder de eerste twee niveaus wilt worden getoond zodat het als overzicht dient.

Met de waarde van de **Basis** van de Navigatie, weet de Component van de Navigatie dat na `/content/wknd/language-masters/en` dat de navigatie begint en het navigatieopties kan produceren door de structuur van de plaats twee niveaus neer (zoals die door de waarde van de Diepte **van de Structuur van de** Navigatie wordt bepaald) te recurseren.

Ongeacht welke gelokaliseerde pagina een gebruiker bekijkt, kan de component van de Navigatie de overeenkomstige gelokaliseerde pagina vinden door de plaats van de huidige pagina te kennen, achterwaarts te werken aan de wortel, en dan door:sturen aan de overeenkomstige pagina.

Dus als een bezoeker `/content/ch/de/experience/arctic-surfing-in-lofoten`de navigatie bekijkt, weet de component dat hij de navigatiestructuur moet genereren op basis van `/content/wknd/language-masters/de`. Op dezelfde manier als de bezoeker `/content/us/en/experience/arctic-surfing-in-lofoten`de navigatiestructuur bekijkt, weet de component dat de navigatiestructuur op basis van `/content/wknd/language-masters/en`.

## Ondersteuning voor schaduwsitestructuur {#shadow-structure}

Soms is het nodig om een navigatiemenu voor de bezoeker te maken dat afwijkt van de daadwerkelijke sitestructuur. Mogelijk moet een aanbieding bepaalde inhoud in het menu benadrukken door de lijst met inhoud opnieuw in te delen. Met behulp van schaduwpagina&#39;s, die eenvoudig worden omgeleid naar andere inhoudspagina&#39;s, kan de navigatiecomponent elke willekeurige navigatiestructuur genereren die nodig is.

Hiervoor moet u:

1. Schaduwpagina&#39;s maken als lege pagina&#39;s die uw gewenste sitestructuur voorstellen. Dit wordt vaak een schaduwsitestructuur genoemd.
1. Stel de waarden voor **Omleiding** in de pagina-eigenschappen op deze pagina&#39;s in om naar de werkelijke inhoudspagina&#39;s te wijzen.
1. Stel de optie **Verbergen in navigatie** in de pagina-eigenschappen van de schaduwpagina&#39;s in.
1. Stel de **basiswaarde van de navigatie** van de navigatiecomponent zo in dat deze naar de hoofdmap van de nieuwe structuur van de schaduwsite wijst.

De component Navigation geeft het menu vervolgens weer op basis van de structuur van de schaduwsite. De koppelingen die door de component worden gerenderd, verwijzen naar de inhoudspagina&#39;s die de schaduwpagina&#39;s omleiden en niet naar de schaduwpagina&#39;s zelf. Bovendien geeft de component de namen van de werkelijke pagina&#39;s weer en wordt de actieve pagina correct gemarkeerd, zelfs als de navigatie is gebaseerd op schaduwpagina&#39;s. De component Navigation maakt de schaduwpagina&#39;s volledig transparant voor de bezoeker.

>[!NOTE]
>Schaduwpagina&#39;s maken uw navigatieopties veel flexibeler, maar houd er rekening mee dat het onderhoud van deze structuur dan volledig handmatig is. Als u de eigenlijke site-inhoud opnieuw rangschikt of inhoud toevoegt/verwijdert, moet u de schaduwstructuur desgewenst handmatig bijwerken.

>[!NOTE]
>Bij het renderen van een schaduwsitestructuur worden alleen de schaduwpagina&#39;s teruggezet door de navigatielogica. De logica recurdeert niet de structuur van de omleidingsbestemmingen.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Navigation Component is v1, die in januari 2018 is geïntroduceerd met versie 2.0.0 van de Core Components, en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatibel | Compatibel | Compatibel |

Zie het document [Core Components Versions](/help/versions.md)voor meer informatie over Core Component-versies en -versies.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Ga naar de [componentbibliotheek](https://adobe.com/go/aem_cmp_library_navigation)om de navigatiecomponent te bekijken en voorbeelden van de configuratieopties en de HTML- en JSON-uitvoer te bekijken.

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Navigatie [kan op GitHub](https://adobe.com/go/aem_cmp_tech_navigation_v1)worden gevonden.

Meer details over het ontwikkelen van de Componenten van de Kern kunnen in de de ontwikkelaarsdocumentatie [van de](/help/developing/overview.md)Componenten worden gevonden.

>[!NOTE]
>
>Vanaf versie 2.1.0 van de Componenten van de Kern, steunt de Component van de Navigatie [schema.org microdata](https://schema.org).

## Dialoogvenster Bewerken {#edit-dialog}

In het dialoogvenster Bewerken kan de auteur van de inhoud de basispagina voor navigatie en de diepte van de navigatiestructuur definiëren.

### Tabblad Eigenschappen {#properties-tab}

![Eigenschappen tabblad van dialoogvenster Bewerken van navigatiecomponent](/help/assets/navigation-edit-properties.png)

* **Navigation Root** - De hoofdpagina, die wordt gebruikt om de boomstructuur te genereren.
* **Exclusief basisniveaus** - vaak moet de hoofdmap niet worden opgenomen in de navigatie. Met deze optie kunt u opgeven hoeveel niveaus boven het basisniveau u wilt uitsluiten. Bijvoorbeeld:
   * 0 = basisniveau weergeven
   * 1 = sluit het wortelniveau uit
   * 2 = sluit de wortel uit en 1 meer niveau omhoog
   * enz.
* **Alle onderliggende pagina&#39;s** verzamelen - Alle pagina&#39;s die onderliggende waarden zijn van de basisnavigatie verzamelen.
* **Navigatiestructuurdiepte** - Hiermee wordt gedefinieerd hoeveel niveaus onder de navigatiestructuur de component moet weergeven ten opzichte van de basisnavigatie (alleen beschikbaar als **Alle onderliggende pagina** &#39;s verzamelen niet is geselecteerd).
* **Schaduwen** uitschakelen - Als de pagina in de hiërarchie een omleiding is, wordt de naam van de omleidingspagina weergegeven in plaats van het doel. Zie Ondersteuning [van](#shadow-structure) schaduwsitestructuren voor meer informatie.
* **ID** - Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de [gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

### Tabblad Toegankelijkheid {#accessibility-tab}

![Toegankelijkheidstabblad van dialoogvenster Navigatiecomponent bewerken](/help/assets/navigation-edit-accessibility.png)

Op het tabblad **Toegankelijkheid** kunnen waarden worden ingesteld voor [ARIA-toegankelijkheidslabels](https://www.w3.org/WAI/standards-guidelines/aria/) voor de component.

* **Label** - waarde van een ARIA-labelkenmerk voor de component

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de standaardwaarden instellen voor de basispagina van de navigatie en de diepte die aan de auteurs van de inhoud worden gepresenteerd.

### Tabblad Eigenschappen {#properties-tab-design}

![Ontwerpdialoogvenster van navigatiecomponent](/help/assets/navigation-design.png)

* **Navigation Root** - De standaardwaarde van de basispagina van de navigatiestructuur, die wordt gebruikt om de navigatiestructuur te genereren en die standaard wordt ingesteld wanneer de auteur van de inhoud de component aan de pagina toevoegt.
* **Exclusief basisniveaus** - vaak moet de hoofdmap niet worden opgenomen in de navigatie. Met deze optie kunt u de standaardinstelling opgeven voor hoeveel niveaus boven het basisniveau u wilt uitsluiten. Bijvoorbeeld:
   * 0 = basisniveau weergeven
   * 1 = sluit het wortelniveau uit
   * 2 = sluit de wortel uit en 1 meer niveau omhoog
   * enz.
* **Alle onderliggende pagina&#39;s** verzamelen - De standaardwaarde van de optie om alle pagina&#39;s te verzamelen die afstammen van de basisnavigatie.
* **Navigatiestructuurdiepte** - De standaardwaarde van de diepte van de navigatiestructuur.
* **Schaduwen** uitschakelen - De standaardwaarde als schaduwen moet worden uitgeschakeld bij het toevoegen van een navigatiecomponent

### Tabblad Stijlen {#styles-tab}

De component Navigation ondersteunt het [Stijlsysteem](/help/get-started/authoring.md#component-styling)AEM.
