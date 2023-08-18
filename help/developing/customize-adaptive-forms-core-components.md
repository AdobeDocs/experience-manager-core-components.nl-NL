---
title: Aangepaste Forms Core-componenten aanpassen
description: Leer om een Adaptive Forms Core Component uit te breiden of te creëren om functionaliteit te implementeren die op maat van uw organisatie is gemaakt.
role: Architect, Developer, Admin
source-git-commit: 9a80b453d6a6cf7b347128654d3b5e673a063505
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---


# Aangepaste Forms Core-componenten aanpassen

Door de adaptieve Forms Core-componenten aan te passen kunt u de functionaliteit van de verpakking aanpassen aan uw specifieke behoeften. Deze gids begeleidt u door het proces om deze componenten aan te passen om een meer gepersonaliseerde ervaring tot stand te brengen.

## Voorwaarde

Voordat u gaat overstappen op het aanpassen van Adaptive Forms Core-componenten,

* Meer informatie over de [architectuur van een kerncomponent](customizing.md#customizing-the-markup-customizing-the-markup) en ga door [officiële documentatie van Adobe Experience Manager Core Components](customizing.md). Deze uitgebreide bronnen fungeren tijdens het hele aanpassingsproces als leidraad.
* Stel uw ontwikkelomgeving in zodat u een vloeiende workflow hebt voor het aanbrengen van wijzigingen in de kerncomponenten. Bij het opzetten van de ontwikkelomgeving gebruikt u een project Archetype AEM op basis van het nieuwste project Archetype AEM. Op basis van uw omgeving kunt u:

   * [Een lokale ontwikkelomgeving instellen voor as a Cloud Service Forms](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/setup-local-development-environment.html).
   * [Een lokale ontwikkelomgeving instellen voor AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html)

## Een adaptieve Forms Core-component aanpassen

Voer de onderstaande stappen uit om de weergave, het gedrag en de functionaliteit van een adaptieve Forms Core-component te wijzigen.

1. **De kerncomponent identificeren en dupliceren**

   Tijdens het vormen van de ontwikkelomgeving, hebt u een op Archetype-Gebaseerd project gecreeerd. In het Project van AEM Archetype, identificeer de specifieke Component van de Kern u wenst aan te passen. Zodra geïdentificeerd, creeer een duplicaat van de component binnen uw op Archetype gebaseerd project AEM. Houd deze parallel met andere adaptieve Forms Core-componenten. Deze stap zorgt ervoor dat uw aanpassingsinspanningen de originele component niet zullen beïnvloeden, die u toestaan om vrij te experimenteren.

1. **De gekopieerde component aanpassen**

   Open de gedupliceerde component en breng de benodigde wijzigingen aan volgens uw vereisten:

   * **HTML-structuur aanpassen**: Stem de HTML-structuur af op uw ontwerpbehoeften en houd u daarbij aan [BEM (blokelement Modifier)](https://github.com/adobe/aem-core-wcm-components/wiki/css-coding-conventions) stijlen voor onderhoudsbare en schaalbare code.
   * **Label bijwerken**: Werk het label van de component bij om een duidelijke en beschrijvende naam voor de aangepaste versie te verstrekken. Zie de verstrekte informatie [Label-sjabloon OOTB (uit vak)](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/label.html) ter wille van de consistentie.
   * **Widget aanpassen**: Pas de widget die binnen de component wordt gebruikt (vervolgkeuzelijsten, selectievakjes) aan om deze uit te lijnen met uw specifieke gebruiksscenario. Zie, de [voorbeeldimplementatie](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/textinput.html) ter referentie.
   * **Help Tekst en knopinfo**: Pas de Help-tekst of knopinfo die aan de component is gekoppeld aan om context en begeleiding aan gebruikers aan te bieden. Gebruik de [OOTB Help-tekstsjabloon](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/questionMark.html) als uitgangspunt.
   * **Gegevenskenmerken**: Neem alle vereiste gegevenskenmerken op in de HTML-elementen van de component. Deze kenmerken zijn van cruciaal belang voor het correct functioneren van de component bij uitvoering. Raadpleeg de [documentatie](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput) inzicht te krijgen in de rol van gegevenskenmerken in Adaptive Forms Core Components.

1. **Implementeer back-endlogica**

   Als uw aanpassing achterwaartse logica vereist, kunt u bestaande hellingsmodellen uitbreiden. Zie de verstrekte informatie [voorbeeld](https://github.com/adobe/aem-core-forms-components/blob/master/bundles/af-core/src/main/java/com/adobe/cq/forms/core/components/internal/models/v1/form/TextInputImpl.java) om de gewenste functionaliteit naadloos in uw aangepaste component te integreren.

1. **Het dialoogvenster van de component configureren**

   Configureer het dialoogvenster dat aan uw aangepaste component is gekoppeld. Het voorbeeld gebruiken [dialoogvenster voor componenten](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/_cq_dialog/.content.xml) in de documentatie worden verstrekt om ervoor te zorgen dat de gebruikersinteractie en de montages correct worden beheerd.

1. **De component implementeren en testen in uw lokale ontwikkelomgeving**

   Gebruiken [gemaakt om de component te bouwen en te implementeren](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html#building-and-installing) in uw lokale ontwikkelomgeving. Nadat de component is geïmplementeerd, maakt u een adaptief formulier om de aangepaste component te testen.

1. **Implementeer de aangepaste component in uw productieomgeving**

   Nadat u de component op uw lokale ontwikkelomgeving hebt getest, implementeert u de component in uw productieomgeving.

