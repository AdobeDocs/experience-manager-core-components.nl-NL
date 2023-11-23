---
title: Inleiding Adaptive Forms Core Components AEM
description: Maak aantrekkelijke inschrijvingservaringen (formulieren) met de flexibiliteit van de Adaptive Forms Core Components en lever deze met de kracht van Adobe Experience Manager.
role: Architect, Developer, Admin, User
exl-id: 6d0f2845-bbb8-4488-a254-b69d7a6290b1
source-git-commit: 1dbbb598c0856b76c076f322cdf0210bf38ee9e8
workflow-type: tm+mt
source-wordcount: '1267'
ht-degree: 0%

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

![adaptieve formulierafbeelding](assets/sample-adaptive-form.png)

## Functies {#features}

|  |  |
|---|---|
| Gereed voor productie | De Adaptive Forms Core-componenten zijn 24 robuuste WCM-componenten. |
| Klaar voor cloud | Beschikbaar voor  [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html). |
| Veelzijdig | De componenten vertegenwoordigen algemene concepten waarmee de Forms-auteurs bijna elke lay-out kunnen samenstellen. |
| Configureerbaar | Sjabloonniveau [inhoudsbeleid](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html#content-policies) bepalen welke functies wel of niet mogen worden gebruikt. |
| Toegankelijk | Ze bieden ARIA-labels, ondersteunen toetsenbordnavigatie en tekst voor ondersteunende hulpmiddelen, zoals schermlezers. |
| Thema | De componenten implementeren de [Stijlsysteem](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html)en volgt de markering [BEM CSS-conventies](https://getbem.com/). |
| Aanpasbaar | Met verschillende patronen kunt u de HTML eenvoudig aanpassen, van het aanpassen tot het opnieuw gebruiken van de geavanceerde functionaliteit. |
| Versioning | De [versiebeleid](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) zorgt ervoor dat de componenten van de Kern uw plaats niet breken wanneer het verbeteren van dingen die u zouden kunnen beïnvloeden. |
| Open Bronnen | Als iets anders is dan zou moeten, draagt u bij aan uw verbetering. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## Voordelen {#benefits}

Ervaringen met het vastleggen van gegevens zijn van cruciaal belang voor het genereren en inschrijven van leads en de Adaptive Forms Core Components bieden een krachtige oplossing voor het maken van formulieren die zijn geoptimaliseerd voor het vastleggen van gegevens. Enkele redenen om de Componenten van de Kern te gebruiken om deze ervaringen over stichtingscomponenten te creëren zijn:

* **Beschikbaarheid op GitHub en uitvoerige documentatie**: De AEM Adaptive Forms Core Components zijn open-source en beschikbaar op GitHub, samen met uitvoerige documentatie. Dit maakt het voor ontwikkelaars gemakkelijker om de componenten te begrijpen en hoe zij werken, en aan hun ontwikkeling bij te dragen. De [aemcomponents.dev](https://www.aemcomponents.dev/) de website is ook een waardevolle bron , waar ontwikkelaars de componenten in actie kunnen zien en toegang hebben tot gedetailleerde documentatie .

* **BEM-model voor opmaken**: De kerncomponenten volgen het BEM-model (Block Element Modifier) voor opmaak, een gangbare en veelgebruikte methode voor het ordenen van CSS. Op deze manier kunnen ontwikkelaars gemakkelijker begrijpen hoe de stijlen zijn ingedeeld en hoe ze aan hun specifieke behoeften kunnen worden aangepast.

* **Geen afhankelijkheid van bibliotheken van derden**: Een van de voordelen van de Core Components is dat deze niet afhankelijk zijn van JavaScript-bibliotheken van derden, waaronder JQuery en Underscore. Hierdoor worden de componenten sneller en lichter, maar ook eenvoudiger te integreren in een bestaande AEM.

* **Focus op prestaties en toegankelijkheid**: De Core Components zijn gebouwd met het oog op prestaties en toegankelijkheid. Dit wordt weerspiegeld in hun hoge Google Lighthouse- en web vitals-scores. Op die manier kunnen ontwikkelaars gemakkelijker toegankelijke en goed presterende webpagina&#39;s maken, wat steeds belangrijker wordt in het huidige digitale landschap.

* **Formuliercomponenten in Sites 30-sjabloon en -thema&#39;s**: De kerncomponenten bieden ondersteuning voor formuliercomponenten in de Sites 30-sjabloon en -thema&#39;s, zodat ontwikkelaars gemakkelijker formulieren kunnen maken en aanpassen binnen AEM.

* **Eenvoudigere stijl**: De componenten van de Kern zijn gemakkelijker om dan hun stichtingscomponenten te stichten. Het proces voor het maken van thema&#39;s lijkt op Sites, waarbij u hetzelfde thema/CSS kunt overnemen van de bovenliggende pagina Sites. Bovendien maakt het BEM-model voor opmaak het eenvoudiger om de stijlen te begrijpen en wijzigen.

* **Toegankelijkheid**: Adaptive Forms Core Components ondersteunt toegankelijkheidsstandaarden en -richtlijnen om ervoor te zorgen dat formulieren kunnen worden gebruikt door mensen met een handicap, inclusief personen die gebruik maken van ondersteunende hulpmiddelen zoals schermlezers

## Adaptieve Forms Core-componenten {#components}

De huidige versie van de Adaptive Forms Core Components is voorzien van de hieronder vermelde componenten.

* [Accordeon](/help/adaptive-forms/components/accordion.md)
* [Knop](/help/adaptive-forms/components/button.md)
* [Selectievakjesgroep](/help/adaptive-forms/components/checkbox-group.md)
* [Datumkiezer](/help/adaptive-forms/components/date-picker.md)
* [Vervolgkeuzelijst](/help/adaptive-forms/components/drop-down.md)
* [E-mailinvoer](/help/adaptive-forms/components/email-input.md)
* [Formuliercontainer](/help/adaptive-forms/components/form-container.md)
* [Bestandsbijlage](/help/adaptive-forms/components/file-attachment.md)
* [Voettekst](/help/adaptive-forms/components/footer.md)
* [Koptekst](/help/adaptive-forms/components/header.md)
* [Horizontale tabs](/help/adaptive-forms/components/horizontal-tabs.md)
* [Afbeelding](/help/adaptive-forms/components/image.md)
* [Nummerinvoer](/help/adaptive-forms/components/number-input.md)
* [Deelvenstercontainer](/help/adaptive-forms/components/panel-container.md)
* [Keuzerondje](/help/adaptive-forms/components/radio-button.md)
* [Knop Opnieuw instellen](/help/adaptive-forms/components/reset-button.md)
* [Verzendknop](/help/adaptive-forms/components/submit-button.md)
* [Telefooninvoer](/help/adaptive-forms/components/telephone-input.md)
* [Tekstinvoer](/help/adaptive-forms/components/text-input.md)
* [Tekst](/help/adaptive-forms/components/text.md)
* [Titel](/help/adaptive-forms/components/title.md)
* [Wizard](/help/adaptive-forms/components/wizard.md)

## Adaptieve Forms Core-componenten instellen

Als u Adaptive Forms Core Components inschakelt op AEM Forms as a Cloud Service, kunt u beginnen met het maken, publiceren en leveren van Core Components based Adaptive Forms and Headless Forms met uw AEM Forms Cloud Service-instanties naar meerdere kanalen. Voor gedetailleerde instructies voor het inschakelen van Adaptive Form Core Components, raadpleegt u [Adaptieve Forms Core-componenten inschakelen in de as a Cloud Service en lokale ontwikkelomgeving van AEM Forms](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html).

De Adaptive Forms Core Components hebben de volgende vereisten.

| AEM | AEM Forms-invoegtoepassing | Adaptieve Forms Core-componenten |
|---|---|---|
| AEM as a Cloud Service | Forms - Digitale inschrijving | [Release 2.0.10](version.md)+ |
| AEM 6,5 | Forms-invoegtoepassing | [Release 1.1.12](version.md)+ |

Als uw AEM Cloud Service SDK-versie ouder is dan 2023.02.0, [zorg ervoor dat u `prerelease` markering ingeschakeld in uw omgeving](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=en#new-features) omdat Adaptive Forms Core Components deel uitmaakten van de pre-lease vóór de release van 2023.02.0.


## Een adaptief formulier op basis van kerncomponenten maken

U kunt de volgende handelingen uitvoeren in zowel AEM Forms as a Cloud Service als AEM 6.5 Forms-omgevingen:

| Handeling | AEM Forms-versie |
|--------|------------------|
| Een zelfstandig adaptief formulier maken | [AEM Forms als Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html) |
| Een adaptief formulier maken op een AEM Sites-pagina | [AEM 6,5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=en#create-an-adaptive-form-in-sites-editor-or-experience-fragment), [AEM Forms als Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html#create-an-adaptive-form-in-sites-editor-or-experience-fragment) |
| Een adaptief formulier maken in AEM Experience Fragment | [AEM 6,5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=en#create-an-adaptive-form-in-experience-fragment), [AEM Forms als Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html#create-an-adaptive-form-in-experience-fragment) |
| Een adaptief formulier converteren naar een ervaringsfragment | [AEM 6,5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=en#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment), [AEM Forms als Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment) |





<!-- >, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. 

<!-- Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->

## Zie ook {#see-also}

{{see-also}}
