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
>Het nieuwste AEM Projectarchetype en de bijbehorende technische documentatie [kan op GitHub worden gevonden.](https://github.com/adobe/aem-project-archetype)

## Waarom het Archetype gebruiken {#why-use-the-archetype}

Het gebruiken van het AEM Archetype van het Project plaatst u op de weg naar de bouw van een op best-praktijken-gebaseerd AEM project met enkel een paar aanslagen. Door het archetype te gebruiken, zullen alle stukken reeds op zijn plaats zijn zodat terwijl het resulterende project minimaal is, het reeds alle [sleutelfuncties](/help/developing/archetype/using.md#what-you-get) AEM zodat je alleen maar verder moet bouwen en uitbreiden.

Natuurlijk zijn er veel elementen die in aanmerking komen [een succesvol AEM project,](/help/developing/success.md) maar het gebruik van het AEM Project Archetype is een goede basis en wordt sterk aanbevolen voor elk AEM project.

## Functies {#features}

* **Beste praktijken:** Bootstrap uw site met alle aanbevolen procedures van de Adobe.
* **Lage code:** Bewerk uw sjablonen, maak inhoud, implementeer uw CSS en uw site is klaar om live te gaan.
* **Klaar voor cloud:** Indien gewenst, gebruik [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html) om binnen enkele dagen te gaan wonen en schaalbaarheid en onderhoud te vergemakkelijken.
* **Dispatcher:** Een project is alleen voltooid met een [Dispatcher-configuratie](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html) dat snelheid en veiligheid verzekert.
* **Meerdere sites:** Indien nodig genereert het archetype de inhoudsstructuur voor een [meertalige installatie en installatie voor meerdere regio&#39;s](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html).
* **Kernonderdelen:** Auteurs kunnen bijna elke lay-out maken met onze veelzijdige [reeks gestandaardiseerde componenten](/help/introduction.md).
* **Bewerkbare sjablonen:** Bijna alles samenstellen [sjabloon zonder code](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html)en definieert wat de auteurs mogen bewerken.
* **Responsieve lay-out:** Op sjablonen of afzonderlijke pagina&#39;s [definiëren hoe de elementen opnieuw worden geplaatst](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html) voor de gedefinieerde onderbrekingspunten.
* **Koptekst en voettekst:** U kunt ze samenstellen en lokaliseren zonder code, met de opdracht [lokalisatiefuncties van de componenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html).
* **Stijlsysteem:** U kunt aangepaste componenten niet maken door auteurs toe te staan [verschillende stijlen toepassen](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html) aan hen.
* **Front-end build:** Ontwikkelaars aan de voorzijde kunnen [AEM pagina&#39;s modelleren en clientbibliotheken maken](front-end.md) met Webpack, TypeScript en SASS.
* **WebApp-Ready:** Voor sites die React of Angular gebruiken, gebruikt u de [SPA SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/developing.html) behouden [contextontwerp van de app](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html).
* **Handel ingeschakeld:** Voor projecten die willen integreren [AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html) met handelsoplossingen zoals [Magento](https://magento.com/) met de [Core Components](https://github.com/adobe/aem-core-cif-components).
* **Voorbeeldcode:** Controle uit de component HelloWorld, en de steekproefmodellen, servlets, filters, en planners.
* **Open Bronnen:** Als iets anders is dan zou moeten, [bijdragen](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) uw verbeteringen!

## Verdere lezing {#further-reading}

* **[AEM Project Archetype GitHub](https://github.com/adobe/aem-project-archetype)** - Voor volledig gebruik en technische details van het archetype
* **[Het gebruiken van Archetype](using.md)** - Een overzicht van hoe te om archetype in uw project en de resulterende geproduceerde modules te gebruiken
* **[Front-end ontwikkeling met het AEM Project Archetype](front-end.md)** - Hoe te om de front-end module van archetype te gebruiken
* **De volgende zelfstudies zijn gebaseerd op het archetype:**
   * **[WKND-site](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** - Leer hoe u een nieuwe website kunt starten.
   * **[WKND App met één pagina](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** - Leer hoe u een React- of Angular-webapp ontwikkelt die volledig in AEM kan worden geschreven.
