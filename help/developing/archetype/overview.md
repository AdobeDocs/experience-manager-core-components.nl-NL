---
title: Projectarchetype AEM
description: Leer over het AEM Archetype van het Project dat als malplaatje voor AEM-gebaseerde toepassingen dient.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: 8940285f4c5e5870b6a135dac674f06e4c1d8b5a
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---


# Projectarchetype AEM {#aem-project-archetype}

Het AEM Project Archetype is een Geweven malplaatje dat tot een minimaal, op best-praktijken-gebaseerd Adobe Experience Manager (AEM) project als uitgangspunt voor uw website leidt. Deze documentatie verstrekt een overzicht van de voordelen van archetype en algemeen gebruik. Gedetailleerde technische instructies en documentatie kunnen in de archetype bewaarplaats worden gevonden GitHub.

>[!TIP]
>
>Het recentste AEM Archetype van het Project en bijbehorende technische documentatie [ kunnen op GitHub worden gevonden.](https://github.com/adobe/aem-project-archetype)

## Waarom het Archetype gebruiken {#why-use-the-archetype}

Het gebruiken van het AEM Archetype van het Project plaatst u op de weg naar de bouw van een op best-praktijken-gebaseerd AEM project met enkel een paar aanslagen. Door archetype te gebruiken, zullen alle stukken reeds op zijn plaats zijn zodat terwijl het resulterende project minimaal is, voert het reeds alle [ zeer belangrijke eigenschappen ](/help/developing/archetype/using.md#what-you-get) van AEM uit zodat alles u moet doen op bovenkant bouwt en zich uitbreidt.

Natuurlijk zijn er vele elementen die in [ een succesvol AEM project gaan, ](/help/developing/success.md) maar het gebruiken van het AEM Archetype van het Project is een correcte stichting en sterk geadviseerd voor om het even welk AEM project.

## Functies {#features}

* **Beste praktijken:** Bootstrap uw plaats met alle recentste geadviseerde praktijken van de Adobe.
* **Laag-Code:** geef uw malplaatjes uit, creeer inhoud, stel uw CSS op, en uw plaats is klaar voor go-live.
* **wolk-Klaar:** Indien gewenst, gebruik [ AEM as a Cloud Service ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=nl-NL) om in enkele dagen te gaan-leven en gemak scalability en onderhoud.
* **Dispatcher:** Een project van A is volledig slechts met de configuratie van a [ Dispatcher ](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html?lang=nl-NL) die snelheid en veiligheid verzekert.
* **Multi-Site:** Indien nodig, produceert het archetype de inhoudsstructuur voor a [ meertalige en multi-regio opstelling ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html?lang=nl-NL).
* **Componenten van de Kern:** de Auteurs kunnen bijna om het even welke lay-out met onze veelzijdige [ reeks gestandaardiseerde componenten ](/help/introduction.md) tot stand brengen.
* **Bewerkbare Malplaatjes:** assembleer vrijwel om het even welk [ malplaatje zonder code ](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html?lang=nl-NL), en bepaal wat de auteurs worden toegestaan uit te geven.
* **Responsieve Lay-out:** op malplaatjes of individuele pagina&#39;s, [ bepalen hoe de elementen ](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=nl-NL) voor de bepaalde breekpunten opnieuw plaatsen.
* **Kopbal en Voettekst:** assembleer en vertaal hen zonder code, gebruikend de [ localisatieeigenschappen van de componenten ](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=nl-NL).
* **Systeem van de Stijl:** vermijd bouwend douanecomponenten door auteurs toe te staan om verschillende stijlen [&#128279;](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html?lang=nl-NL) op hen toe te passen.
* **voorste-Eind bouwt:** Voorste-eindontwikkelaars kunnen [ AEM pagina&#39;s controleren en cliëntbibliotheken ](front-end.md) met Webpack, TypeScript, en SASS bouwen.
* **WebApp-Klaar:** voor plaatsen die Reageren of Angular gebruiken, gebruik [ SPA SDK ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/developing.html?lang=nl-NL) om [ in-context het auteursrecht van app ](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=nl-NL) te behouden.
* **Commerce Toegelaten:** voor projecten die [ AEM Commerce ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html?lang=nl-NL) met handelsoplossingen zoals [ Magento ](https://magento.com/) willen integreren gebruikend de [ Componenten van de Kern van Commerce ](https://github.com/adobe/aem-core-cif-components).
* **Code van het Voorbeeld:** Controle de component HelloWorld, en de steekproefmodellen, servlets, filters, en planners.
* **Open Gefeliciteerd:** als iets niet is zoals het zou moeten, [ bijdragen ](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) uw verbeteringen!

## Verdere lezing {#further-reading}

* **[AEM Archetype GitHub van het Project ](https://github.com/adobe/aem-project-archetype)** - voor volledig gebruik en technische details van archetype
* **[Gebruikend Archetype](using.md)** - een overzicht van hoe te om het archetype in uw project en de resulterende geproduceerde modules te gebruiken
* **[Voorste-Eind Ontwikkeling met het AEM Archetype van het Project](front-end.md)** - hoe te om de front-end module van archetype te gebruiken
* **de volgende leerprogramma&#39;s zijn gebaseerd van archetype:**
   * **[Plaats WKND ](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=nl-NL)** - leer hoe te om een nieuwe website te beginnen.
   * **[WKND de Enige Toepassing van de Pagina ](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=nl-NL)** - Leer hoe te om React te bouwen of webapp van de Angular die volledig authorable in AEM is.
