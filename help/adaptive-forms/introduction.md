---
title: Inleiding AEM Adaptive Forms Core Components
description: Maak aantrekkelijke inschrijvingservaringen (formulieren) met de flexibiliteit van de Adaptive Forms Core Components en lever deze met de kracht van Adobe Experience Manager.
role: Architect, Developer, Admin, User
exl-id: 6d0f2845-bbb8-4488-a254-b69d7a6290b1
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '2123'
ht-degree: 0%

---


# Adaptieve Forms Core-componenten  {#adaptive-forms-core-components-introduction}

Met de Adaptive Forms Core Components in Adobe Experience Manager kunt u aantrekkelijke inschrijvingservaringen creëren.

{{traditional-aem}}

## Kernonderdelen {#overview}

In Adobe Experience Manager (AEM) zijn componenten de bouwstenen die worden gebruikt om pagina&#39;s en formulieren te maken. Ze bieden auteurs een eenvoudige en krachtige manier om inhoud te maken en te beheren en bieden ontwikkelaars ook de flexibiliteit en uitbreidbaarheid die nodig zijn om aangepaste componenten te maken. Deze zijn ontworpen om de ontwikkelingstijd te versnellen en de onderhoudskosten voor websites en formulieren te verlagen, flexibel te zijn en eenvoudig te kunnen worden aangepast aan de specifieke behoeften van een website en formulier.

De Core Components zijn ook ontworpen om responsief te zijn en ondersteuning te bieden voor een groot aantal apparaten, zoals desktops, tablets en smartphones. Ze houden zich ook aan de nieuwste webstandaarden en best practices, waardoor ze een robuuste en betrouwbare oplossing zijn voor het maken van webinhoud.

Over het algemeen vormen de Core Components een essentieel instrument voor het maken en beheren van webinhoud in AEM en bieden zij een krachtige en flexibele oplossing die de ontwikkelingstijd en onderhoudskosten kan helpen verlagen en tevens een geweldige gebruikerservaring voor de websitebezoekers kan bieden.

## Adaptieve Forms Core-componenten

De Adaptive Forms Core Components zijn een set van 30 opensource, BEM-compatibele componenten die op de basis van de Adobe Experience Manager WCM Core Components zijn gebouwd. Deze zijn speciaal ontworpen voor het maken van Adaptief Forms. Dit zijn formulieren die worden aangepast aan het apparaat, de browser en de schermgrootte van de gebruiker.

Deze componenten kunnen worden gebruikt om buitengewone ervaringen met het vastleggen en inschrijven van gegevens te maken door een groot aantal opties voor formuliervelden te bieden, zoals tekstvelden, selectievakjes, vervolgkeuzemenu&#39;s en nog veel meer. Ze bevatten ook functies zoals validatie, voorwaardelijke logica en responsief ontwerp, waarmee u formulieren kunt maken die gebruiksvriendelijk en gebruiksvriendelijk zijn.

Bovendien, aangezien deze componenten open-bron zijn, hebben de ontwikkelaars de capaciteit om de componenten gemakkelijk aan te passen en uit te breiden om aan de specifieke behoeften van hun organisatie te passen. Deze componenten zijn gebaseerd op de BEM-methode, die ervoor zorgt dat ze schaalbaar en onderhoudsbaar zijn.

![ adaptief vormbeeld ](assets/sample-adaptive-form.png)

## Functies {#features}

|  |  |
|---|---|
| Gereed voor productie | De Adaptive Forms Core-componenten zijn 24 robuuste WCM-componenten. |
| Klaar voor cloud | Beschikbaar voor [ AEM Forms as a Cloud Service ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html?lang=nl-NL). |
| Veelzijdig | De componenten vertegenwoordigen algemene concepten waarmee de Forms-auteurs bijna elke lay-out kunnen samenstellen. |
| Configureerbaar | Sjabloon-niveau [ inhoudsbeleid ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=nl-NL#content-policies) bepaalt welke eigenschappen worden toegestaan om te gebruiken of niet te gebruiken. |
| Toegankelijk | Ze bieden ARIA-labels, ondersteunen toetsenbordnavigatie en tekst voor ondersteunende hulpmiddelen, zoals schermlezers. |
| Thema | De componenten voeren het [ Systeem van de Stijl ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=nl-NL) uit, en de prijsverhoging volgt [ CSS van BEM overeenkomsten ](https://getbem.com/). |
| Aanpasbaar | Met verschillende patronen kunt u de HTML eenvoudig aanpassen, van het aanpassen aan geavanceerde functies tot hergebruik. |
| Versioning | Het [ versioning beleid ](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) zorgt ervoor dat de Componenten van de Kern uw plaats niet zullen breken wanneer het verbeteren van dingen die u zouden kunnen beïnvloeden. |
| Open Bronnen | Als iets anders is dan zou moeten, draagt u bij aan uw verbetering. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## Voordelen {#benefits}

Ervaringen met het vastleggen van gegevens zijn van cruciaal belang voor het genereren en inschrijven van leads en de Adaptive Forms Core Components bieden een krachtige oplossing voor het maken van formulieren die zijn geoptimaliseerd voor het vastleggen van gegevens. Enkele redenen om de Componenten van de Kern te gebruiken om deze ervaringen over stichtingscomponenten te creëren zijn:

* **[Beschikbaarheid op GitHub ](https://github.com/adobe/aem-core-forms-components)**: De Aangepaste Componenten van de Kern van Forms van AEM zijn open-source en beschikbaar op GitHub, samen met uitvoerige documentatie. Dit maakt het voor ontwikkelaars gemakkelijker om de componenten te begrijpen en hoe zij werken, en aan hun ontwikkeling bij te dragen. De {[&#128279;](https://www.aemcomponents.dev/) website 0} aemcomponents.dev is ook een waardevol middel, waar de ontwikkelaars de componenten in actie kunnen zien en tot gedetailleerde documentatie toegang hebben.

* **[BEM Model voor het Stijlen ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: De Componenten van de Kern volgen het model BEM (de Modifier van het Element van het Blok) voor het stileren, dat een gevestigde en wijd gebruikte methodologie voor het organiseren van CSS is. Op deze manier kunnen ontwikkelaars gemakkelijker begrijpen hoe de stijlen zijn ingedeeld en hoe ze aan hun specifieke behoeften kunnen worden aangepast.

* **geen Vertrouwen op de Bibliotheken van de Derde**: Één van de voordelen van de Componenten van de Kern is dat zij geen gebiedsdeel op de bibliotheken van derdeJavaScript, met inbegrip van JQuery en Onderstrepingsteken hebben. Hierdoor worden de componenten sneller en lichter, maar ook eenvoudiger te integreren in een bestaande AEM-implementatie.

* **concentreert zich op Prestaties en Toegankelijkheid**: De Componenten van de Kern worden gebouwd met prestaties en toegankelijkheid in mening, die in hun hoge Lighthouse en Web vitals scores van Google weerspiegeld wordt. Op die manier kunnen ontwikkelaars gemakkelijker toegankelijke en goed presterende webpagina&#39;s maken, wat steeds belangrijker wordt in het huidige digitale landschap.

* **Componenten van de Vorm in Plaatsen 30 Malplaatje en Thema&#39;s**: De Componenten van de Kern verlenen steun voor vormcomponenten in het malplaatje en de thema&#39;s van Plaatsen 30, die het voor ontwikkelaars gemakkelijker maken om vormen binnen AEM tot stand te brengen en aan te passen.

* **[Gemakkelijker aan Stijl ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: De Componenten van de Kern zijn gemakkelijker om dan hun tegenhangers van de stichtingscomponent te vormen. Het proces voor het maken van thema&#39;s lijkt op Sites, waarbij u hetzelfde thema/CSS kunt overnemen van de bovenliggende pagina Sites. Bovendien maakt het BEM-model voor opmaak het eenvoudiger om de stijlen te begrijpen en wijzigen.

* **Toegankelijkheid**: De adaptieve Componenten van de Kern van Forms steunen toegankelijkheidsnormen en richtlijnen om ervoor te zorgen dat de vormen door mensen met handicaps, met inbegrip van die kunnen worden gebruikt die ondersteunende technologieën zoals het schermlezers gebruiken.

* **[Versioning ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/add-comments-annotations-versioning-adaptive-form-core-components)**: U kunt veelvoudige versies van een op Aangepast Forms gebaseerde Componenten van de Kern tot stand brengen en beheren, aan samenwerkingsbesprekingen door commentaren, aangaan en annotaties aan specifieke vormcomponenten vastmaken, daardoor verbeterend de algemene vorm-bouwende ervaring.

## Beschikbare componenten: een uitsplitsing naar componenttype

De huidige versie van AEM Forms heeft de volgende Componenten van de Kern, [ Componenten van de Stichting ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/create-an-adaptive-form-on-forms-cs/introduction-forms-authoring#component-toolbar), en [ Componenten van het Blok van de Vorm (Edge Delivery Services) ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/edge-delivery/build-forms/forms-references/form-components).

| Onderdelen | Elementaire componenten | Kernonderdelen | Componenten voor formulierblokken | Aanvullende informatie |
|------------|:---------------------:|:---------------:|:---------------------:|-----------------------|
| Adobe Sign Block | ✔️ | | | [ de integratie van het Ondertekenen van Adobe ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/integrate/services/adobe-sign-integration-adaptive-forms#adobe-acrobat-sign-for-government) is beschikbaar slechts voor de Componenten van de Stichting. |
| Accordeon | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/accordion.md)</span> | | Voor de Componenten van de Stichting, kunt u de accordeonlay-out in [ eigenschappen van de paneelcomponent ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) vormen. |
| Adaptief formulierfragment | ✔️ | ✔️ | | Voor de Componenten van de Stichting, kunt u [ een fragment ](https://experienceleague.adobe.com/nl/docs/experience-manager-65/content/forms/adaptive-forms-basic-authoring/adaptive-form-fragments#insert-a-fragment-in-an-adaptive-form) van Browser van Assets toevoegen. |
| Adaptief formulier reCAPTCHA | ✔️ | ✔️ | ✔️ | Voor de Componenten van de Stichting, gebruik de component Captcha om [ Google reCaptcha aan een vorm ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms#google-reCAPTCHA) toe te voegen. |
| Knop | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/button.md)</span> | ✔️ | |
| Diagram | ✔️ | | | |
| Selectievakje | ✔️ | ✔️ | | |
| Selectievakjesgroep | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/checkbox-group.md)</span> | ✔️ | Voor de Componenten van de Stichting, gebruik de checkbox component om veelvoudige checkboxes toe te voegen |
| Datuminvoerveld | ✔️ | | | Voor de Componenten van de Kern, gebruik de [&#128279;](/help/adaptive-forms/components/date-picker.md) component van de plukker van 0&rbrace; datum.  U kunt afzonderlijke [ textbox ](/help/adaptive-forms/components/text-box.md) of [ numerieke doos ](/help/adaptive-forms/components/numeric-box.md) componenten ook toevoegen om de dag, de maand, en het jaar te vangen. |
| Datumkiezer | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/date-picker.md)</span> | ✔️ | |
| Vervolgkeuzelijst | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/drop-down-list.md)</span> | ✔️ | |
| E-mail | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/email.md)</span> | ✔️ | |
| Bestandsbijlage | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/file-attachment.md)</span> | ✔️ | |
| Lijst met bestandsbijlagen | ✔️ | | | |
| Voettekst | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/footer.md)</span> | ✔️ | |
| Plaatsaanduiding voetnoot | ✔️ | | | |
| Formuliercontainer | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/form-container.md)</span> | ✔️ | Voor de Componenten van de Stichting, gebruik de [ component van het Comité van de Wortel ](https://experienceleague.adobe.com/nl/docs/experience-manager-learn/cloud-service/forms/create-first-af/configure-root-panel). |
| Formuliertitel | ✔️ | ✔️ | | Gebruik de titelcomponent voor Foundation Components. |
| hCaptcha | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/hcaptcha.md)</span> |  | Voor de Componenten van de Stichting, kunt u [ uw adaptieve vormen met hCaptcha ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile.html?lang=nl-NL) voor stichtingscomponenten verbinden gebaseerde vormen. |
| Koptekst | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/header.md)</span> | ✔️ | |
| Horizontale tabs | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/horizontal-tabs.md)</span> | | Voor de Componenten van de Stichting, kunt u de [ lusjes bovenop (horizontale lusjes) lay-out ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) in de eigenschappen van de paneelcomponent vormen. |
| Afbeelding | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/image.md)</span> | ✔️ | |
| Volgende knop | ✔️ | ✔️ | | Gebruik de [ tovenaar component ](/help/adaptive-forms/components/wizard.md) voor volgende en vorige knopen om zich tussen veelvoudige panelen te bewegen. |
| Numeriek vak | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/numeric-box.md)</span> | ✔️ | |
| Numerieke stap | ✔️ | | | |
| Deelvenster | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/panel.md)</span> | ✔️ | |
| Telefoon/telefoon | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/phone.md)</span> | ✔️ | |
| Vorige knop | ✔️ | ✔️ | | Gebruik de [ tovenaar component ](/help/adaptive-forms/components/wizard.md) voor volgende en vorige knopen om zich tussen veelvoudige panelen te bewegen. |
| Groep keuzerondjes | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/radio-button.md)</span> | ✔️ | |
| Knop Opnieuw instellen | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/reset-button.md)</span> | ✔️ | |
| Controleren |  | <span style="color:blue">[✔️](/help/adaptive-forms/components/reset-button.md)</span> |  | |
| Krabbelhandtekening | ✔️ | | | |
| Scheidingsteken | ✔️ | | | De component van WCM [ Beheerder ](/help/components/separator.md) gebruiken |
| Verzendknop | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/submit-button.md)</span> | ✔️ | |
| Samenvattingsstap | ✔️ | | | |
| Overschakelen | ✔️ | <span style="color:blue"> [✔️](/help/adaptive-forms/components/adaptive-form-switch.md) | | |
| Tabel | ✔️ | | | |
| Voorwaarden en bepalingen | ✔️ | ✔️ | | |
| Tekst | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text.md)</span> | ✔️ | |
| Tekstvak | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text-box.md)</span> | ✔️ | |
| Turnstile Captcha | ✔️ | | | [ Turnstile Captcha ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile) is beschikbaar slechts voor de Componenten van de Stichting. |
| Verticale tabs | ✔️ | ✔️ | | Voor de Componenten van de Stichting, kunt u de [ lusjes op de linkerlay-out (verticale lusjes) ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) in eigenschappen van de paneelcomponent vormen |
| Wizard | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/wizard.md)</span> | ✔️ | Voor de Componenten van de Stichting, kunt u de [ tovenaar lay-out ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout) in de eigenschappen van de paneelcomponent vormen |

<!--| Password Box | ✔️ | ✔️| ✔️ | |
| Image Choice | ✔️ | | | |
-->


>[!NOTE]
>
>
> * Naast de hierboven vermelde componenten, steunt het blok van Forms alle geldige [ HTML5 inputtypes ](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#input_types) en [ tekstgebied ](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea) als componenten.
> * Hebt u een component nodig die hierboven niet wordt vermeld? Vraag het aan door aem-forms-ea@adobe.com van uw officiële adres te e-mailen.


<!-- >
* [Accordion](/help/adaptive-forms/components/accordion.md)
* [Adaptive Form Fragment](/help/adaptive-forms/components/adaptive-form-fragment.md)
* [Adaptive Form Switch](/help/adaptive-forms/components/adaptive-form-switch.md)
* [Button](/help/adaptive-forms/components/button.md)
* [Check Box Group](/help/adaptive-forms/components/checkbox-group.md)
* [Date Picker](/help/adaptive-forms/components/date-picker.md)
* [Drop-down list](/help/adaptive-forms/components/drop-down-list.md)
* [Email](/help/adaptive-forms/components/email.md)
* [Form Container](/help/adaptive-forms/components/form-container.md)
* [File Attachment](/help/adaptive-forms/components/file-attachment.md)
* [Footer](/help/adaptive-forms/components/footer.md)
* [Header](/help/adaptive-forms/components/header.md)
* [Horizontal Tabs](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Numeric Box](/help/adaptive-forms/components/numeric-box.md)
* [Panel](/help/adaptive-forms/components/panel.md)
* [Phone](/help/adaptive-forms/components/phone.md)
* [Radio Button](/help/adaptive-forms/components/radio-button.md)
* [Adaptive Form reCAPTCHA](/help/adaptive-forms/components/adaptive-form-recaptcha.md)
* [Reset Button](/help/adaptive-forms/components/reset-button.md)
* [Submit Button](/help/adaptive-forms/components/submit-button.md)
* [Text Box](/help/adaptive-forms/components/text-box.md)
* [Text](/help/adaptive-forms/components/text.md)
* [Form Title](/help/adaptive-forms/components/form-title.md)
* [Wizard](/help/adaptive-forms/components/wizard.md)

-->

## Eenvoudig te gebruiken formuliereditor

De editor voor op Core Components gebaseerde Adaptive Forms is vergelijkbaar met de editor die u al gebruikt voor het maken van AEM Sites-pagina&#39;s. Dit is wat je krijgt:


* **Vertrouwde elementen UI en montages**: Wanneer het vormen van eigenschappen voor vormcomponenten, ziet u een eigenschappendialoog enkel als degenen kijkt u aan voor de Componenten van de Kern WCM gebruikt. Hierdoor wordt het sneller om de opties te vinden u wenst. Net als WCM Core Components, verschijnt voor formuliercomponenten het dialoogvenster Eigenschappen in het midden van de editor met duidelijke tabbladen waarin de basis- en geavanceerde opties, Help-tekst en toegankelijkheidsinformatie worden gescheiden. Dit venster ziet u allemaal in tabs-indeling voor eenvoudige navigatie.

* **[Redacteur van de Regel ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/rule-editor-core-components)**: U kunt logica en dynamische eigenschappen aan uw vormen toevoegen zonder code te schrijven. U kunt de ingebouwde regelredacteur gebruiken aan:
   * Velden weergeven of verbergen op basis van gebruikersopties
   * Een object in- of uitschakelen
   * Een waarde instellen voor een object
   * Berekeningen uitvoeren
   * Eigenschap van een object instellen
   * Gegevensinvoer valideren
   * Een service aanroepen (externe functionaliteit aanroepen)
   * Ingebouwde functies gebruiken (vooraf gedefinieerde functies voor algemene taken)
   * Aangepaste functies gebruiken (uw eigen code voor specifieke behoeften)
   * Valideer velden en deelvensters (controleer of de gegevens aan de vereisten voldoen)
   * De waarde van een object valideren
   * Functies uitvoeren om de waarde van een object te berekenen
   * Roep de service Form Data Model (FDM) aan en voer een bewerking uit
   * Dynamisch stijlen toevoegen (weergave wijzigen op basis van voorwaarden)
   * Andere regels maken (kettinghandelingen en logica)
   * en meer!

  De regelredacteur heeft niet de coderedacteur. U kunt [ douanefuncties ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-and-use-custom-functions) gebruiken om uw eigen code voor specifieke behoeften aan de regelredacteur toe te voegen.



* **Vullingsvormen**: U kunt bepaalde gebieden in een vorm met bestaande gegevens automatisch bevolken wanneer een gebruiker het opent. Dit bespaart gebruikers tijd en moeite door de behoefte te elimineren om informatie manueel in te gaan die reeds beschikbaar zou kunnen zijn. De editor Core Components biedt een OOTB-service om formuliervelden te vullen met behulp van een formuliergegevensmodel. U kunt de diensten van de douane ook tot stand brengen vooraf ingevulde voor complexere scenario&#39;s.

* **[Document van Verslag (DoR) ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components)**: Een Document van Verslag (DoR) verwijst naar een formele, bedrukbare vertegenwoordiging van de gegevens die door de vorm worden voorgelegd. Het dient als een permanent verslag van de informatie een gebruiker inging, die een momentopname van de voorgelegde gegevens in een gebruikersvriendelijk formaat, typisch een document van PDF verstrekt. U kunt de redacteur gebruiken om een douanemalplaatje gemakkelijk te vormen of een malplaatje OTB te gebruiken om een DoR te produceren.

* **[Model van de Gegevens van de Vorm ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)**: Een Adaptief Model van de Gegevens van Forms (FDM) handelt als brug tussen uw Aangepaste Forms en uw gegevensbronnen. In feite wordt hiermee de structuur en organisatie gedefinieerd van de gegevens die uw formulieren verzamelen en waarmee ze werken. U kunt de editor gebruiken om een formulier eenvoudig te verbinden met een Forms Data Model (FDM).

* **[de Indieningen van de Vorm ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form)**: De vormvoorlegging verwijst naar het proces van gebruikers die hun ingevulde vormen invullen en verzenden. Hierdoor wordt een reeks handelingen geactiveerd die in de configuratie van het formulier zijn gedefinieerd, wat uiteindelijk leidt tot de opslag of verwerking van de verzonden gegevens. De Adaptive Forms-editor biedt verschillende opties voor het configureren van formulierverzendingen. Enkele gemeenschappelijke acties voor het indienen van voorstellen zijn:

   * [ verzendt e-mail ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form.)
   * [ aanhaalt een Macht automatisch stroom ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/integrate/services/forms-microsoft-power-automate-integration)
   * [ voorleggen aan SharePoint ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-sharepoint)
   * [ Roep een Fusie van Workfront ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20a%20Workfront%20Fusion) aan
   * [ voorleggen gebruikend het Model van de Gegevens van de Vorm (FDM) ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)
   * [ voorleggen aan Azure BlobOpslag ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Submit%20to%20Azure%20Blob%20Storage)
   * [ voorleggen aan REST eindpunt ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-restpoint)
   * [ voorleggen aan OneDrive ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=to%20REST%20endpoint-,Submit%20to%20OneDrive,-Invoke%20an%20AEM)
   * [ Roep een Werkschema van AEM ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20an%20AEM%20Workflow) aan


* [ de Aangepaste Componenten van de Kern van Forms van in de redacteur van de Pagina van Plaatsen ](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page): U kunt de Aangepaste Componenten van de Kern van Forms in de Redacteur van de Pagina van AEM en de Fragments van de Ervaring van AEM toelaten en gebruiken om gegevens te creëren vangen ervaring samen met het bouwen van een pagina van Plaatsen.

  >[!VIDEO](https://video.tv.adobe.com/v/3419284?quality=12&learn=on)


<!-- 
* **Preview Forms**: You can use the editor to  simulates how the form would appear on various devices like desktops, tablets, and smartphones.
-->



## Adaptieve Forms Core-componenten inschakelen

Door Adaptieve Forms Core-componenten in te schakelen op AEM Forms as a Cloud Service, kunt u beginnen met het maken, publiceren en leveren van Core Components based Adaptive Forms en Headless Forms met uw AEM Forms Cloud Service-instanties naar meerdere kanalen. Voor gedetailleerde instructies om de Aangepaste Componenten van de Kern van de Vorm toe te laten, zie [ Aangepaste Componenten van de Kern van Forms op AEM Forms as a Cloud Service en lokale ontwikkelomgeving ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=nl-NL) toelaten.

De Adaptive Forms Core Components hebben de volgende vereisten.

| AEM-versie | AEM Forms-invoegtoepassing | Adaptieve Forms Core-componenten |
|---|---|---|
| AEM as a Cloud Service | Forms - Digitale inschrijving | [ Versie 2.0.10 ](version.md)+ |
| AEM 6.5 | Forms-invoegtoepassing | [ Versie 1.1.12 ](version.md)+ |

Als uw versie van SDK van de Dienst van de Wolk van AEM ouder dan 2023.02.0, [ ervoor zorgt dat u `prerelease` vlag hebt die op uw milieu ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=nl-NL#new-features) wordt toegelaten aangezien de Adaptieve Componenten van de Kern van Forms deel van pre-lease vóór de versie 2023.02.0 vormden.


## Een adaptief formulier op basis van kerncomponenten maken

U kunt de volgende handelingen uitvoeren in zowel AEM Forms as a Cloud Service- als AEM 6.5 Forms-omgevingen:

| Handeling | AEM Forms-versie |
|--------|------------------|
| Een zelfstandig adaptief formulier maken | [ AEM Forms als Cloud Service ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=nl-NL) |
| Een adaptief formulier maken op een AEM Sites-pagina | [ AEM 6.5 Forms ](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=nl-NL#create-an-adaptive-form-in-sites-editor-or-experience-fragment), [ AEM Forms als Cloud Service ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=nl-NL#create-an-adaptive-form-in-sites-editor-or-experience-fragment) |
| Een adaptief formulier maken in AEM Experience Fragment | [ AEM 6.5 Forms ](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=nl-NL#create-an-adaptive-form-in-experience-fragment), [ AEM Forms als Cloud Service ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=nl-NL#create-an-adaptive-form-in-experience-fragment) |
| Een adaptief formulier converteren naar een ervaringsfragment | [ AEM 6.5 Forms ](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=nl-NL#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment), [ AEM Forms als Cloud Service ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=nl-NL#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment) |





<!-- >, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. 

<!-- Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->

## Zie ook {#see-also}

{{see-also}}
