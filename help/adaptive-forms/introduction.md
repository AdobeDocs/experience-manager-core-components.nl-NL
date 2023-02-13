---
title: Inleiding Adaptive Forms Core Components AEM
description: Maak aantrekkelijke inschrijvingservaringen (formulieren) met de flexibiliteit van de Adaptive Forms Core Components en lever deze met de kracht van Adobe Experience Manager.
role: Architect, Developer, Admin, User
source-git-commit: b378fbd5695f82b8fc9de3a2d53a8387099ae33b
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 1%

---


# Inleiding Adaptive Forms Core Components {#adaptive-forms-core-components-introduction}

Met behulp van de Adaptive Forms Core Components in Adobe Experience Manager kunt u aantrekkelijke inschrijvingservaringen creëren door de beschikbare flexibiliteit- en aanpassingsopties te gebruiken.

## Kernonderdelen  {#overview}

In Adobe Experience Manager (AEM) zijn componenten de bouwstenen die worden gebruikt om pagina&#39;s en formulieren te maken. Ze bieden auteurs een eenvoudige en krachtige manier om inhoud te maken en te beheren en bieden ontwikkelaars ook de flexibiliteit en uitbreidbaarheid die nodig zijn om aangepaste componenten te maken. Deze zijn ontworpen om de ontwikkelingstijd te versnellen en de onderhoudskosten voor websites en formulieren te verlagen, flexibel te zijn en eenvoudig te kunnen worden aangepast aan de specifieke behoeften van een website en formulier.

De Core Components zijn ook ontworpen om responsief te zijn en ondersteuning te bieden voor een groot aantal apparaten, zoals desktops, tablets en smartphones. Ze houden zich ook aan de nieuwste webstandaarden en best practices, waardoor ze een robuuste en betrouwbare oplossing zijn voor het maken van webinhoud.

Over het algemeen vormen de Core Components een essentieel instrument voor het maken en beheren van webinhoud in AEM, dat een krachtige en flexibele oplossing biedt die kan helpen de ontwikkelingstijd en onderhoudskosten te verlagen en tevens de bezoekers van de website een geweldige gebruikerservaring biedt.

## Adaptieve Forms Core-componenten

De Adaptive Forms Core Components zijn een set van 24 opensource, BEM-compatibele componenten die op de basis van de Adobe Experience Manager WCM Core Components zijn gebouwd. Deze zijn speciaal ontworpen voor het maken van Adaptief Forms. Dit zijn formulieren die worden aangepast aan het apparaat, de browser en de schermgrootte van de gebruiker.

Deze componenten kunnen worden gebruikt om buitengewone ervaringen met het vastleggen en inschrijven van gegevens te maken door een groot aantal opties voor formuliervelden te bieden, zoals tekstvelden, selectievakjes, vervolgkeuzemenu&#39;s en nog veel meer. Ze bevatten ook functies zoals validatie, voorwaardelijke logica en responsief ontwerp, waarmee u formulieren kunt maken die gebruiksvriendelijk en gebruiksvriendelijk zijn.

Bovendien, aangezien deze componenten open-bron zijn, hebben de ontwikkelaars de capaciteit om de componenten gemakkelijk aan te passen en uit te breiden om aan de specifieke behoeften van hun organisatie te passen. Deze componenten zijn gebaseerd op BEM-methoden die ervoor zorgen dat ze schaalbaar en onderhoudsbaar zijn.

![](assets/sample-adaptive-form.png)

## Functies {#features}

|  |  |
|---|---|
| Gereed voor productie | De Adaptive Forms Core-componenten zijn 24 robuuste WCM-componenten. |
| Klaar voor cloud | Beschikbaar voor  [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html). |
| Veelzijdig | De componenten vertegenwoordigen algemene concepten waarmee de Forms-auteurs bijna elke lay-out kunnen samenstellen. |
| Configureerbaar | Sjabloonniveau [inhoudsbeleid](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html#content-policies) bepalen welke functies wel of niet mogen worden gebruikt. |
| Toegankelijk | Ze bieden ARIA-labels, ondersteunen toetsenbordnavigatie ([bekende problemen](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)) en tekst voor ondersteunende hulpmiddelen, zoals schermlezers. |
| Thema | De componenten implementeren de [Stijlsysteem](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html)en volgt de markering [BEM CSS-conventies](https://getbem.com/). |
| Aanpasbaar | Met verschillende patronen kunt u de HTML eenvoudig aanpassen, van het aanpassen tot het opnieuw gebruiken van de geavanceerde functionaliteit. |
| Versioning | De [versiebeleid](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) zorgt ervoor dat de componenten van de Kern uw plaats niet breken wanneer het verbeteren van dingen die u zouden kunnen beïnvloeden. |
| Open Bronnen | Als iets anders is dan zou moeten, draagt u bij aan uw verbetering. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## Voordelen {#benefits}

Ervaringen met het vastleggen van gegevens zijn van cruciaal belang voor het genereren en inschrijven van leads en de Adaptive Forms Core Components bieden een krachtige oplossing voor het maken van formulieren die zijn geoptimaliseerd voor het vastleggen van gegevens. Enkele redenen om de Componenten van de Kern te gebruiken om deze ervaringen over stichtingscomponenten tot stand te brengen zijn:

* **Beschikbaarheid op GitHub en uitvoerige documentatie**: De AEM Adaptieve Componenten van de Kern van Forms zijn open-bron en beschikbaar op GitHub, samen met uitvoerige documentatie. Dit maakt het voor ontwikkelaars gemakkelijker om de componenten te begrijpen en hoe zij werken, en aan hun ontwikkeling bij te dragen. De [aemcomponents.dev](https://www.aemcomponents.dev/) de website is ook een waardevolle bron , waar ontwikkelaars de componenten in actie kunnen zien en toegang hebben tot gedetailleerde documentatie .

* **BEM-model voor opmaken**: De kerncomponenten volgen het BEM-model (Block Element Modifier) voor opmaak. Dit is een gangbare en veelgebruikte methode voor het ordenen van CSS. Op deze manier kunnen ontwikkelaars gemakkelijker begrijpen hoe de stijlen zijn ingedeeld en hoe ze aan hun specifieke behoeften kunnen worden aangepast.

* **Geen afhankelijkheid van bibliotheken van derden**: Een van de voordelen van de Core Components is dat deze niet afhankelijk zijn van JavaScript-bibliotheken van derden, waaronder JQuery en Underscore. Hierdoor worden de componenten sneller en lichter, maar ook eenvoudiger te integreren in een bestaande AEM.

* **Focus op prestaties en toegankelijkheid**: De Core Components zijn gebouwd met het oog op prestaties en toegankelijkheid, wat wordt weerspiegeld in hun hoge Google Lighthouse- en web vitals-scores. Op die manier kunnen ontwikkelaars gemakkelijker toegankelijke en goed presterende webpagina&#39;s maken, wat steeds belangrijker wordt in het huidige digitale landschap.

* **Formuliercomponenten in Sites 30-sjabloon en -thema&#39;s**: De kerncomponenten bieden ondersteuning voor formuliercomponenten in de Sites 30-sjabloon en -thema&#39;s, zodat ontwikkelaars gemakkelijker formulieren kunnen maken en aanpassen binnen AEM.

* **Eenvoudigere stijl**: De componenten van de Kern zijn gemakkelijker om dan hun stichtingscomponenten te stichten. Het proces voor het maken van thema&#39;s lijkt op Sites, waarbij u hetzelfde thema/CSS kunt overnemen van de bovenliggende pagina Sites. Bovendien maakt het BEM-model voor opmaak het eenvoudiger om de stijlen te begrijpen en wijzigen.

* **Toegankelijkheid**: Aangepaste Forms Core-componenten ondersteunen toegankelijkheidsstandaarden en -richtlijnen om ervoor te zorgen dat formulieren kunnen worden gebruikt door mensen met een handicap, inclusief personen die gebruik maken van ondersteunende hulpmiddelen zoals schermlezers


<!-- >, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. 

<!-- Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->



## Vereisten {#requirements}

De Adaptive Forms Core Components hebben de volgende vereisten.

| AEM | AEM Forms-invoegtoepassing | Kernonderdelen |
|---|---|---|
| AEM as a Cloud Service | Forms - Digitale inschrijving | [Release 2.20.8](/help/versions.md)+ |


## Adaptieve Forms Core-componenten {#components}

U kunt [Adaptieve Forms-editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html) om een basiscomponent te maken op basis van Adaptive Forms. De huidige versie van de Adaptive Forms Core Components is voorzien van de hieronder vermelde componenten.

* Accordeon
* Knop
* Groep selectievakjes
* Datumkiezer
* Vervolgkeuzelijst
* E-mailinvoer
* Formuliercontainer
* Bestandsbijlage
* Voettekst
* Koptekst
* Horizontale tabs
* Afbeelding
* Nummerinvoer
* Deelvenstercontainer
* Keuzerondje
* Knop Opnieuw instellen
* Verzendknop
* Telefooninvoer
* Tekstinvoer
* Tekst
* Titel
* Wizard

