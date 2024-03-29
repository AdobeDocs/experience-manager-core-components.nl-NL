---
title: Localisatiefuncties van de kerncomponenten
description: Localisatiefuncties van de kerncomponenten
role: Architect, Developer, Admin, User
exl-id: 9140b65a-6dd7-4ec9-9095-6e8243ec8424
source-git-commit: 888719359f9a1d1c9dccff97fb639b332f2be54c
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 0%

---

# Localisatiefuncties van de kerncomponenten {#localization-features-of-the-core-components}

Veel websites vereisen dat inhoud wordt geleverd in een gelokaliseerde indeling voor verschillende talen en geografische regio&#39;s. Geselecteerde kerncomponenten hebben een slimme verwijzingsresolutie, zodat u eenvoudig een uniforme sjabloon kunt maken voor al uw gelokaliseerde inhoud die automatisch wordt aangepast op basis van uw gelokaliseerde sitestructuur.

## Voorbeeld - Gelokaliseerde pagina met navigatie en voetteksten {#example}

Voor de meeste sites is een voettekst vereist die op alle pagina&#39;s aanwezig is. Deze voetteksten zijn over het algemeen consistent in alle inhoud van de pagina. Voor een gelokaliseerde inhoudspagina moet echter een gelokaliseerde versie van die kop- of voettekst worden weergegeven.

Een navigatiecomponent moet gewoonlijk ook op alle pagina&#39;s worden getoond. De inhoud van de gelokaliseerde pagina&#39;s moet echter wel in de code worden opgenomen.

De lokalisatiefuncties van de [Navigation Core-component](/help/components/navigation.md) en [Ervaar de kerncomponent Fragmentatie](/help/components/experience-fragment.md) samen met de [bewerkbare sjablonen van AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)Dit wordt een eenvoudige taak. Het voorbeeld zou verder kunnen worden uitgebreid om het [Taalnavigatie-component](/help/components/language-navigation.md) ook.

## De inhoudsstructuur {#content-structure}

Alle lokalisatiefuncties van AEM en de bijbehorende kerncomponenten zijn afhankelijk van een duidelijke en logische inhoudsstructuur voor uw gelokaliseerde inhoud.

Laat ons zeggen dat uw site eenvoudig wordt genoemd `my-site` en bevindt zich hier:

```
/content/my-site
```

Laten we ook zeggen dat u uw site in het Engels hebt geschreven en ook in het Frans hebt aangeboden. Dus als je een eenvoudige pagina hebt, genaamd `my-page` deze bevindt zich in twee lokalisatiekanalen in de inhoudsstructuur van uw site:

```
/content
\-- my-site
   +-- en
       \-- my-page
   \-- fr
       \-- my-page
```

In deze vertakkingen voor lokalisatie maakt u extra sitepagina&#39;s.

De voetteksten van de pagina worden over het algemeen gemaakt gebruikend de Fragmenten van de Ervaring zodat zult u een Engelse en Franse versie net als uw pagina&#39;s nodig hebben. Ervaar fragmenten zijn echter geen pagina&#39;s, maar onderdelen van pagina&#39;s die op verschillende pagina&#39;s opnieuw kunnen worden gebruikt, zodat ze niet direct onder `/content` als de rest van uw pagina&#39;s. In plaats daarvan leven ze onder hun eigen map, maar omdat ze ook gelokaliseerd moeten zijn, moet hun structuur de lokalisatiestructuur van uw site weerspiegelen.

```
/content
+-- experience-fragments
   +-- en
      \-- footer
   \-- fr
      \-- footer
\-- my-site
   +-- en
      \-- my-page
   \-- fr
      \-- my-page
```

De Core Components kunnen via de gespiegelde lokalisatiestructuur de vereiste gelokaliseerde inhoud voor een overeenkomende pagina vinden.

## Paginavoettekst - Ervaar fragment {#xf-footer}

De Experience Fragment-component is zeer flexibel en goed geschikt voor een paginakop of -voettekst.

Omdat onze hypothetische website in het Engels en Frans wordt aangeboden, moeten we twee Experience Fragments maken, beide genaamd `footer` [op de locaties die we eerder beschreven hebben.](#content-structure)

![](/help/assets/screen-shot-2019-09-09-11.08.28.png)

## Paginasjabloon {#template}

Omdat de voettekst op elke pagina wordt weergegeven, moeten we het fragment Experience toevoegen aan onze standaardpaginasjabloon.

Onze sjabloon wordt gewoon genoemd `my-template` en bevindt zich bij onze andere sjablonen:

```
/conf/my-site/settings/wcm/templates/my-template
```

Aan dit malplaatje zullen wij de basiscomponenten toevoegen die wij onze pagina&#39;s willen worden gebaseerd op.

* [Navigatie-component](/help/components/navigation.md)
   * De navigatiecomponent wordt boven aan elke pagina weergegeven.
   * In de navigatiecomponent definiëren we de basiscode voor de navigatie, waarbij de component wordt aangegeven waar de navigatiestructuur van de site begint.
   * Op basis van de basis van de navigatie kan de component de overeenkomstige gelokaliseerde inhoud automatisch vinden.
* [Containercomponent](/help/components/container.md)
   * Elke pagina bevat een bewerkbare Container-component, zodat auteurs aanvullende inhoud op de pagina kunnen plaatsen.
* [Ervaar fragment](/help/components/experience-fragment.md)
   * We wijzen de Experience Fragment-component naar het fragmentpad in onze ontwerptaal van het fragment dat de voettekst vertegenwoordigt.
   * Op basis van het pad van dat fragment en de structuur van de ervaringsfragmenten die de gelokaliseerde paginastructuur weerspiegelen, kan de component de overeenkomstige gelokaliseerde inhoud automatisch vinden.

   ![](/help/assets/screen-shot-2019-09-09-11.20.10.png)

## Pagina&#39;s {#pages}

Door hard te werken aan het instellen van de sitestructuur en sjabloon, moet de auteur van de inhoud gewoon de benodigde inhoud aan de pagina&#39;s toevoegen. Dankzij de sjablonen en de lokalisatielogica van de componenten worden de navigatie- en voetteksten automatisch toegevoegd aan de pagina en gelokaliseerd.

De auteur hoeft bijvoorbeeld alleen inhoud, zoals een tekstcomponent, toe te voegen aan de Engelse en Franse pagina&#39;s (weergegeven in het blauw hieronder).

De component Navigatiecomponent en Experience Fragment komen uit de paginasjabloon en weten automatisch de juiste inhoud weer te geven op basis van de lokalisatiestructuur en de locatie van de pagina zelf (weergegeven in het wit hieronder).

![](/help/assets/screen-shot-2019-09-09-11.22.14.png)

## Alles samenvoegen {#fitting-it-all-together}

Hier is het volledige beeld van hoe deze eenvoudige, maar krachtige elementen samenwerken om gelokaliseerde pagina&#39;s voor de auteurs van de inhoud te leveren.

![](/help/assets/screen-shot-2019-09-09-11.27.58.png)
