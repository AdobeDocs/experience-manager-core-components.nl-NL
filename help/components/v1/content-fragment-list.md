---
title: Component lijst met inhoudsfragmenten (v1)
description: Met de component Lijst met inhoudfragmenten van de kerncomponent kunt u een lijst met inhoudsfragmenten weergeven.
role: Architect, Developer, Admin, User
exl-id: 37d6632d-360d-4081-8279-8efbb369a82e
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---


# Component lijst met inhoudsfragmenten (v1) {#content-fragment-list-component}

De component van de Lijst van het Fragment van de Lijst van de Inhoud van de Component van de Kern staat voor de vertoning van een lijst van [ inhoudsfragmenten ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=nl-NL) toe.

## Gebruik {#usage}

De component van de Lijst van het Fragment van de Lijst van de Inhoud van de Component van de Kern staat voor de opneming van een lijst van [ inhoudsfragmenten ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=nl-NL) op een pagina toe die op een model van het Fragment van de Inhoud wordt gebaseerd. Dit kan vooral nuttig zijn om [ zonder kop inhoud ](https://helpx.adobe.com/nl/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) te creëren die gemakkelijk door andere toepassingen kan worden verbruikt.

* De lijst en zijn eigenschappen kunnen in [ worden geselecteerd vormen dialoog ](#configure-dialog).
* De stijlen kunnen op de component in de [ ontwerpdialoog ](#design-dialog) worden toegepast.

## Versie en compatibiliteit {#version-and-compatibility}

In het document wordt versie 1 van de Content Fragment Component beschreven. Deze is in mei 2019 geïntroduceerd met release 2.4.0 van de Core Components.

>[!CAUTION]
>
>In dit document wordt versie 1 van de component Lijst met inhoudsfragmenten beschreven.
>
>Voor details van de huidige versie van de Component van de Lijst van het Fragment van de Inhoud, zie het [&#128279;](/help/components/content-fragment-list.md) document van de Component van de Lijst van het Fragment van 0&rbrace; Inhoud.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Om de Component van de Lijst van het Fragment van de Inhoud te ervaren evenals voorbeelden van zijn configuratieopties evenals HTML en output JSON, bezoek de [ Bibliotheek van de Component ](https://adobe.com/go/aem_cmp_library_cflist).

## Technische details {#technical-details}

De recentste technische documentatie over de Component van de Lijst van het Fragment van de Inhoud [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_cflist_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster voor configureren kan de auteur van de inhoud definiëren welke inhoudsfragmenten de lijst vormen en welke elementen van die fragmenten moeten worden opgenomen.

### Tabblad Eigenschappen

Het **lusje van Eigenschappen** bepaalt welke Fragmenten van de Inhoud in de lijst inbegrepen zijn. Dit is voornamelijk gebaseerd op een geselecteerd inhoudsfragmentmodel, maar er zijn andere filteropties beschikbaar.

![ het lusje van Eigenschappen van uitgeeft dialoog van de Component van de Lijst van het Fragment van de Inhoud ](/help/assets/content-fragment-list-properties.png)

* **Model** - Weg aan het Model van het Fragment van de Inhoud waarop de lijst gebaseerd is.
   * Door gebrek, zijn alle inhoudsfragmenten van het model dat als **wordt bepaald ModelWeg** inbegrepen in de lijst.
* **de Weg van de Ouder** - de weg van de Ouder waarvan de lijst zou moeten worden gebouwd.
   * De inhoudsfragmenten die op het geselecteerde **ModelWeg** worden gebaseerd zullen aan die op de gespecificeerde **Weg van de Ouder** worden gefiltreerd.
      * Klik of tik de **Open Dialoog van de Selectie** knoop bij de rechterkant van het gebied om de weg te specificeren.
* **Markeringen** - slechts zullen de Fragmenten van de Inhoud met de gespecificeerde markeringen in de lijst worden omvat.
   * Klik of tik de **Open Dialoog van de Selectie** knoop bij de rechterkant van het gebied om de markeringen te specificeren.
   * Klik of tik op de X naast de geselecteerde tags om deze te verwijderen.
* **orde door** - Gebied van het model van het inhoudsfragment waardoor de lijst zal worden bevolen
   * Alleen tekstvelden (inclusief numeriek, datum en tijd) kunnen worden geselecteerd.
* **de Orde van de Soort** - hoe de lijst door het **Bestelling door** gebied zal worden gesorteerd
   * Oplopend of aflopend
* **Max Punten** - Maximum aantal punten dat in de lijst moet worden getoond
   * Geen waarde retourneert alle items.
* **identiteitskaart** - Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de [ Laag van Gegevens te controleren ](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

>[!NOTE]
>De **Orde door**, **Orde van de Sortering**, en **Max Punten** opties werden geïntroduceerd met versie 2.7.0 van de Componenten van de Kern.

### Het tabblad Elements

Door gebrek, zullen alle elementen van het Model van het Fragment van de Inhoud in de lijst (tenzij beperkt door het **Max gebied van Punten**) worden omvat. Het **lusje van Elementen** staat u toe om slechts specifieke elementen te specificeren om te omvatten.

![ Elementen lusje van uitgeeft dialoog van de Component van de Lijst van het Fragment van de Inhoud ](/help/assets/content-fragment-list-elements.png)

* **Elementen** - slechts zullen de elementen van de inhoudsfragmenten in de gespecificeerde lijst verschijnen.
   * Klik of tik **toevoegen** knoop om een nieuw element toe te voegen.
   * Klik of tik de **knoop van de Schrapping** om een geselecteerd element te verwijderen.
   * Sleep het **handvat van de Orde** om de orde van de elementen te herschikken.

## Ontwerpdialoogvenster {#design-dialog}

In het dialoogvenster Ontwerpen kan de sjabloonauteur de stijlen definiëren die zijn toegepast op de component Lijst met inhoudsfragmenten.
