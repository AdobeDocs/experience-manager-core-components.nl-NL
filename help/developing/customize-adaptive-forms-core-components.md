---
title: Aangepaste Forms Core-componenten aanpassen
description: Leer om een Adaptive Forms Core Component uit te breiden of te creëren om functionaliteit te implementeren die op maat van uw organisatie is gemaakt.
role: Architect, Developer, Admin
exl-id: f3ab12aa-d48d-47e9-a965-15052cac6f18
source-git-commit: 5994133947ff697f7c866fe61598c58e37e77008
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%

---

# Aangepaste Forms Core-componenten aanpassen

Door de adaptieve Forms Core-componenten aan te passen kunt u de functionaliteit van de verpakking aanpassen aan uw specifieke behoeften. Deze gids begeleidt u door het proces om deze componenten aan te passen om een meer gepersonaliseerde ervaring tot stand te brengen.

{{traditional-aem}}

## Voorwaarde

Voordat u gaat overstappen op het aanpassen van Adaptive Forms Core-componenten,

* Leer over de [ architectuur van een Componenten van de Kern ](customizing.md#customizing-the-markup-customizing-the-markup) en ga door de [ officiële documentatie van de Componenten van de Kern van Adobe Experience Manager ](customizing.md). Deze uitgebreide bronnen fungeren tijdens het hele aanpassingsproces als leidraad.
* Stel uw ontwikkelomgeving in zodat u een vloeiende workflow hebt voor het aanbrengen van wijzigingen in de kerncomponenten. Gebruik bij het instellen van de ontwikkelomgeving een AEM Archetype-project dat is gebaseerd op het nieuwste project van AEM Archetype. Op basis van uw omgeving kunt u:

   * [ opstelling een lokale ontwikkelomgeving voor Forms as a Cloud Service ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/setup-local-development-environment.html).
   * [ opstelling een lokale ontwikkelomgeving voor AEM 6.5 Forms ](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html)

## Een adaptieve Forms Core-component aanpassen

Voer de onderstaande stappen uit om de weergave, het gedrag en de functionaliteit van een adaptieve Forms Core-component te wijzigen.

1. **identificeer en dupliceer de Component van de Kern**

   Tijdens het vormen van de ontwikkelomgeving, hebt u een op Archetype-Gebaseerd project gecreeerd. Geef in het AEM Archetype Project de specifieke Core-component op die u wilt aanpassen. Als deze eenmaal is geïdentificeerd, maakt u een duplicaat van de component in uw op AEM Archetype gebaseerde project. Houd deze parallel met andere adaptieve Forms Core-componenten. Deze stap zorgt ervoor dat uw aanpassingsinspanningen de originele component niet zullen beïnvloeden, die u toestaan om vrij te experimenteren.

1. **pas de Gekopieerde Component** aan

   Open de gedupliceerde component en breng de benodigde wijzigingen aan volgens uw vereisten:

   * **pas de Structuur van HTML** aan: Tailor de structuur van HTML om uw ontwerpbehoeften aan te passen terwijl het volgen van [ BEM (de Modifier van het Element van het Blok) ](https://github.com/adobe/aem-core-wcm-components/wiki/css-coding-conventions) het stileren praktijken voor handhaafbare en scalable code.
   * **etiket van de Update**: Werk het etiket van de component bij om een duidelijke en beschrijvende naam voor de aangepaste versie te verstrekken. Verwijs naar het verstrekte [ OOTB (uit de Doos) etiketmalplaatje ](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/label.html) voor consistentie.
   * **pas Widget** aan: Pas widget aan die binnen de component (dropdowns, checkboxes) wordt gebruikt om met uw specifiek gebruiksgeval te richten. Zie, de [ implementatie van de steekproefwidget ](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/textinput.html) voor verwijzing.
   * **Tekst en Tooltips van de Hulp**: Personaliseer de hulptekst of tooltips verbonden aan de component om context en begeleiding aan gebruikers aan te bieden. Gebruik het [ malplaatje van de hulptekst OTB ](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/questionMark.html) als uitgangspunt.
   * **Attributen van Gegevens**: Bouw alle noodzakelijke gegevensattributen binnen de elementen van HTML van de component op. Deze kenmerken zijn van cruciaal belang voor het correct functioneren van de component bij uitvoering. Raadpleeg de [ documentatie ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput) om de rol van gegevensattributen in de Adaptieve Componenten van de Kern van Forms te begrijpen.

1. **voert Achterste Logica** uit

   Als uw aanpassing achterwaartse logica vereist, kunt u bestaande hellingsmodellen uitbreiden. Verwijs naar het verstrekte [ voorbeeld ](https://github.com/adobe/aem-core-forms-components/blob/master/bundles/af-core/src/main/java/com/adobe/cq/forms/core/components/internal/models/v1/form/TextInputImpl.java) om de gewenste functionaliteit in uw aangepaste component foutloos te integreren.

1. **vorm de Dialoog van de Component**

   Configureer het dialoogvenster dat aan uw aangepaste component is gekoppeld. Gebruik de de componentendialoog van het voorbeeld [ ](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/_cq_dialog/.content.xml) in de documentatie wordt verstrekt om ervoor te zorgen dat gebruikersinteractie en de montages geschikt worden beheerd.

1. **stel en test de component op uw lokale ontwikkelomgeving op**

   Het gebruik [ wordt in kaart gebracht om de component ](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html#building-and-installing) op uw lokale ontwikkelomgeving te bouwen en op te stellen. Nadat de component is geïmplementeerd, maakt u een adaptief formulier om de aangepaste component te testen.

1. **stel de douanecomponent op uw productiemilieu** op

   Nadat u de component op uw lokale ontwikkelomgeving hebt getest, implementeert u de component in uw productieomgeving.
