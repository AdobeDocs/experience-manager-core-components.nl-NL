---
title: AEM Project Archetype
description: Meer informatie over het AEM Project Archetype dat als sjabloon dient voor AEM-toepassingen.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: 5994133947ff697f7c866fe61598c58e37e77008
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---


# AEM Project Archetype {#aem-project-archetype}

Het AEM Project Archetype is een Maven-sjabloon waarmee een minimaal Adobe Experience Manager-project (AEM) op basis van best practices wordt gemaakt als startpunt voor uw website. Deze documentatie verstrekt een overzicht van de voordelen van archetype en algemeen gebruik. Gedetailleerde technische instructies en documentatie kunnen in de archetype bewaarplaats worden gevonden GitHub.

>[!TIP]
>
>Het recentste Archetype van het Project van AEM en bijbehorende technische documentatie [ kunnen op GitHub worden gevonden.](https://github.com/adobe/aem-project-archetype)

{{traditional-aem}}

## Waarom het Archetype gebruiken {#why-use-the-archetype}

Met het AEM Project Archetype zet u de weg in naar het bouwen van een AEM-project op basis van best practices met slechts enkele toetsaanslagen. Door archetype te gebruiken, zullen alle stukken reeds op zijn plaats zijn zodat terwijl het resulterende project minimaal is, voert het reeds alle [ zeer belangrijke eigenschappen ](/help/developing/archetype/using.md#what-you-get) van AEM uit zodat alles u moet doen op bovenkant bouwt en zich uitbreidt.

Natuurlijk zijn er vele elementen die in [ een succesvol project van AEM gaan, ](/help/developing/success.md) maar het gebruiken van het Archetype van het Project van AEM is een correcte stichting en sterk geadviseerd voor om het even welk project van AEM.

## Functies {#features}

* **Beste praktijken:** Bootstrap uw plaats met alle laatste aanbevolen praktijken van Adobe.
* **Laag-Code:** geef uw malplaatjes uit, creeer inhoud, stel uw CSS op, en uw plaats is klaar voor go-live.
* **wolk-Klaar:** Indien gewenst, gebruik [ AEM as a Cloud Service ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html) om in enkele dagen te gaan-leven en gemak scalability en onderhoud.
* **Dispatcher:** Een project van A is volledig slechts met de configuratie van a [ Dispatcher ](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html) die snelheid en veiligheid verzekert.
* **Multi-Site:** Indien nodig, produceert het archetype de inhoudsstructuur voor a [ meertalige en multi-regio opstelling ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html).
* **Componenten van de Kern:** de Auteurs kunnen bijna om het even welke lay-out met onze veelzijdige [ reeks gestandaardiseerde componenten ](/help/introduction.md) tot stand brengen.
* **Bewerkbare Malplaatjes:** assembleer vrijwel om het even welk [ malplaatje zonder code ](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html), en bepaal wat de auteurs worden toegestaan uit te geven.
* **Responsieve Lay-out:** op malplaatjes of individuele pagina&#39;s, [ bepalen hoe de elementen ](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html) voor de bepaalde breekpunten opnieuw plaatsen.
* **Kopbal en Voettekst:** assembleer en vertaal hen zonder code, gebruikend de [ localisatieeigenschappen van de componenten ](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html).
* **Systeem van de Stijl:** vermijd bouwend douanecomponenten door auteurs toe te staan om verschillende stijlen [&#128279;](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html) op hen toe te passen.
* **voorste-Eind bouwt:** Voorste-eindontwikkelaars kunnen [ AEM pagina&#39;s modelleren en cliëntbibliotheken ](front-end.md) met Webpack, TypeScript, en SASS bouwen.
* **WebApp-Klaar:** voor plaatsen die Reageren of Angular gebruiken, gebruik [ SDK van het KUUROORD ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/developing.html) om [ in-context het auteursrecht van app ](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html) te behouden.
* **Commerce Toegelaten:** voor projecten die [ Commerce van AEM ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html) met handelsoplossingen zoals [ Magento ](https://magento.com/) willen integreren gebruikend de [ Componenten van de Kern van Commerce ](https://github.com/adobe/aem-core-cif-components).
* **Code van het Voorbeeld:** Controle de component HelloWorld, en de steekproefmodellen, servlets, filters, en planners.
* **Open Gefeliciteerd:** als iets niet is zoals het zou moeten, [ bijdragen ](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) uw verbeteringen!

## Verdere lezing {#further-reading}

* **[Archetype GitHub van het Project van AEM ](https://github.com/adobe/aem-project-archetype)** - voor volledig gebruik en technische details van archetype
* **[Gebruikend Archetype](using.md)** - een overzicht van hoe te om het archetype in uw project en de resulterende geproduceerde modules te gebruiken
* **[Voorste-Eind Ontwikkeling met het Archetype van het Project van AEM](front-end.md)** - hoe te om de front-end module van archetype te gebruiken
* **de volgende leerprogramma&#39;s zijn gebaseerd van archetype:**
   * **[Plaats WKND ](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** - leer hoe te om een nieuwe website te beginnen.
   * **[WKND de Enige Toepassing van de Pagina ](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** - Leer hoe te om React te bouwen of Angular webapp die volledig authorable in AEM is.
