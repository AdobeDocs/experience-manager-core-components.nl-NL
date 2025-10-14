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
>Het recentste Archetype van het Project van AEM en bijbehorende technische documentatie [&#x200B; kunnen op GitHub worden gevonden.](https://github.com/adobe/aem-project-archetype)

{{traditional-aem}}

## Waarom het Archetype gebruiken {#why-use-the-archetype}

Met het AEM Project Archetype zet u de weg in naar het bouwen van een AEM-project op basis van best practices met slechts enkele toetsaanslagen. Door archetype te gebruiken, zullen alle stukken reeds op zijn plaats zijn zodat terwijl het resulterende project minimaal is, voert het reeds alle [&#x200B; zeer belangrijke eigenschappen &#x200B;](/help/developing/archetype/using.md#what-you-get) van AEM uit zodat alles u moet doen op bovenkant bouwt en zich uitbreidt.

Natuurlijk zijn er vele elementen die in [&#x200B; een succesvol project van AEM gaan, &#x200B;](/help/developing/success.md) maar het gebruiken van het Archetype van het Project van AEM is een correcte stichting en sterk geadviseerd voor om het even welk project van AEM.

## Functies {#features}

* **Beste praktijken:** Bootstrap uw plaats met alle laatste aanbevolen praktijken van Adobe.
* **Laag-Code:** geef uw malplaatjes uit, creeer inhoud, stel uw CSS op, en uw plaats is klaar voor go-live.
* **wolk-Klaar:** Indien gewenst, gebruik [&#x200B; AEM as a Cloud Service &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=nl-NL) om in enkele dagen te gaan-leven en gemak scalability en onderhoud.
* **Dispatcher:** Een project van A is volledig slechts met de configuratie van a [&#x200B; Dispatcher &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html?lang=nl-NL) die snelheid en veiligheid verzekert.
* **Multi-Site:** Indien nodig, produceert het archetype de inhoudsstructuur voor a [&#x200B; meertalige en multi-regio opstelling &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html?lang=nl-NL).
* **Componenten van de Kern:** de Auteurs kunnen bijna om het even welke lay-out met onze veelzijdige [&#x200B; reeks gestandaardiseerde componenten &#x200B;](/help/introduction.md) tot stand brengen.
* **Bewerkbare Malplaatjes:** assembleer vrijwel om het even welk [&#x200B; malplaatje zonder code &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html?lang=nl-NL), en bepaal wat de auteurs worden toegestaan uit te geven.
* **Responsieve Lay-out:** op malplaatjes of individuele pagina&#39;s, [&#x200B; bepalen hoe de elementen &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=nl-NL) voor de bepaalde breekpunten opnieuw plaatsen.
* **Kopbal en Voettekst:** assembleer en vertaal hen zonder code, gebruikend de [&#x200B; localisatieeigenschappen van de componenten &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=nl-NL).
* **Systeem van de Stijl:** vermijd bouwend douanecomponenten door auteurs toe te staan om verschillende stijlen [&#128279;](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html?lang=nl-NL) op hen toe te passen.
* **voorste-Eind bouwt:** Voorste-eindontwikkelaars kunnen [&#x200B; AEM pagina&#39;s modelleren en cliëntbibliotheken &#x200B;](front-end.md) met Webpack, TypeScript, en SASS bouwen.
* **WebApp-Klaar:** voor plaatsen die Reageren of Angular gebruiken, gebruik [&#x200B; SDK van het KUUROORD &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/developing.html?lang=nl-NL) om [&#x200B; in-context het auteursrecht van app &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=nl-NL) te behouden.
* **Commerce Toegelaten:** voor projecten die [&#x200B; Commerce van AEM &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html?lang=nl-NL) met handelsoplossingen zoals [&#x200B; Magento &#x200B;](https://magento.com/) willen integreren gebruikend de [&#x200B; Componenten van de Kern van Commerce &#x200B;](https://github.com/adobe/aem-core-cif-components).
* **Code van het Voorbeeld:** Controle de component HelloWorld, en de steekproefmodellen, servlets, filters, en planners.
* **Open Gefeliciteerd:** als iets niet is zoals het zou moeten, [&#x200B; bijdragen &#x200B;](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) uw verbeteringen!

## Verdere lezing {#further-reading}

* **[Archetype GitHub van het Project van AEM &#x200B;](https://github.com/adobe/aem-project-archetype)** - voor volledig gebruik en technische details van archetype
* **[Gebruikend Archetype](using.md)** - een overzicht van hoe te om het archetype in uw project en de resulterende geproduceerde modules te gebruiken
* **[Voorste-Eind Ontwikkeling met het Archetype van het Project van AEM](front-end.md)** - hoe te om de front-end module van archetype te gebruiken
* **de volgende leerprogramma&#39;s zijn gebaseerd van archetype:**
   * **[Plaats WKND &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=nl-NL)** - leer hoe te om een nieuwe website te beginnen.
   * **[WKND de Enige Toepassing van de Pagina &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=nl-NL)** - Leer hoe te om React te bouwen of Angular webapp die volledig authorable in AEM is.
