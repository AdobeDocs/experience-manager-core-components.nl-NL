---
title: Adaptieve Forms Core-component - Formuliercontainer
description: Voeg een adaptief formulier toe aan een webpagina.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 86a30bc396d89340106177deb08323bfc5640e0e
workflow-type: tm+mt
source-wordcount: '1525'
ht-degree: 0%

---

# Formuliercontainer {#form-container-adaptive-forms-core-component}

<span class="preview"> Dit artikel bespreekt **Concepten** <!--and **Hamburger Menu Support** --> eigenschap, die een pre-versieeigenschap is. De pre-vrijlatingseigenschap is toegankelijk slechts door ons [ pre-vrijgavekanaal ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html#new-features).</span>

Forms stelt bezoekers van websites in staat om te communiceren met de website door waardevolle informatie te verstrekken, die de betrokkenheid en gebruikerstevredenheid kan verhogen. Met een adaptieve formuliercontainer in Adobe Experience Manager-sites (AEM) kunnen eigenaars van websites gemakkelijk formulieren toevoegen aan hun pagina&#39;s. Hierdoor wordt de communicatie tussen websitebezoekers en de eigenaar of organisatie van de website vergemakkelijkt doordat bezoekers op een gestroomlijnde manier feedback kunnen geven, vragen kunnen stellen en andere handelingen kunnen uitvoeren

## Gebruik {#reasons-to-use-forms-container}

Er zijn verschillende redenen waarom een formulier aan een website kan worden toegevoegd:
- **de inzameling van Gegevens**: Forms kan worden gebruikt om gegevens van websitebezoekers voor diverse doeleinden, zoals marktonderzoek, gebruikersgedragsanalyse en meer te verzamelen.

- **Loodgeneratie**: Een vorm kan worden gebruikt om informatie van potentiële klanten, zoals naam en e-mailadres, te verzamelen om lood voor verkoop en marketing inspanningen te produceren.

- **e-commerce**: Forms kan voor online het winkelen worden gebruikt, toestaand klanten om orden te plaatsen en betalingen door de website te verrichten.

- **Contact**: Een contactvorm staat websitebezoekers toe om uit aan de websiteeigenaar of organisatie gemakkelijk te bereiken.

- **Enquêtes en opiniepeilingen**: Forms kan worden gebruikt om terugkoppelen en meningen van websitebezoekers door onderzoeken en opiniepeilingen te verzamelen.

- **de registratie van de Gebeurtenis**: Forms kan voor gebeurtenisregistratie worden gebruikt, toestaand websitebezoekers om omhoog voor gebeurtenissen of webinars te ondertekenen.

- **Abonnementen**: Forms kan voor websiteabonnementen worden gebruikt, toestaand bezoekers om omhoog voor een nieuwsbrief of andere regelmatige mededelingen te ondertekenen.

- **de authentificatie van de Gebruiker**: Forms kan voor gebruikersauthentificatie worden gebruikt, toestaand websitebezoekers om rekeningen tot stand te brengen en login om tot exclusieve inhoud of eigenschappen toegang te hebben.

- **de omzettingspercentage van de verhoging**: Een goed-ontworpen vorm kan de omzettingspercentage verhogen door het voor gebruikers gemakkelijk te maken om een gewenste actie te voltooien, zoals het kopen van een product of het ondertekenen omhoog voor de dienst.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/adaptive-forms/version.md) en later | Compatibel met <br>[ versie 1.1.12 ](/help/adaptive-forms/version.md) en later maar minder dan 2.0.0. |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het ](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0}.[
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Krijg de recentste informatie over de Adaptieve Component van de Kern van de Container van Forms in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de ervaring van uw formuliercontainer eenvoudig aanpassen voor bezoekers. U kunt ook eenvoudig opties voor formuliercontainers definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![ Basis lusje ](/help/adaptive-forms/assets/formcontainer_basictab1.png)

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bovenop de component. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

- **vooraf ingevulde diensten** - Deze optie staat de gebruiker toe om een prefill dienst voor het terugwinnen van gegevens te selecteren wanneer de Aangepaste Vorm wordt teruggegeven. Leer meer over [ om een prefill dienst ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=en#aem-forms-custom-prefill-service) tot stand te brengen en te vormen.

- **Rol**: De rol is een attribuut van HTML dat wordt gebruikt om het doel van een element van HTML aan ondersteunende technologieën zoals het schermlezers te specificeren. Het rolattribuut wordt gebruikt om extra context en semantische betekenis aan een element te verstrekken, die het voor schermlezers gemakkelijker maken om de inhoud te interpreteren en aan de gebruiker aan te kondigen. In AEM Forms heeft het label van een formulierveld bijvoorbeeld de rol &quot;label&quot; en kan het invoerveld de rol &quot;textbox&quot; hebben. Hierdoor kan de schermlezer de relatie tussen het label en het invoerveld begrijpen en deze correct aan de gebruiker meedelen.

- **de categorie van de Bibliotheek van de Cliënt** - de gebruiker kan de bibliotheek van de douaneJavaScript per Aangepast Vorm vormen. Het wordt aanbevolen alleen de herbruikbare functies in de bibliotheek te behouden, die afhankelijk zijn van bibliotheken van derden jquery en underscore.js.
Soms, als er **complexe bevestigingsregels** zijn, verblijft het nauwkeurige bevestigingsmanuscript in douanefuncties en de gebruikers roepen deze douanefuncties van de uitdrukking van de gebiedsbevestiging. Als u deze aangepaste functiebibliotheek bekend en beschikbaar wilt maken tijdens het uitvoeren van validaties op de server, kan de gebruiker de naam van AEM clientbibliotheek configureren onder het tabblad **[!UICONTROL Basic]** Adaptief formulier Container-eigenschappen.
De gebruiker kan de aangepaste JavaScript-bibliotheek per adaptief formulier configureren. Houd in de bibliotheek alleen de herbruikbare functies die afhankelijk zijn van bibliotheken van derden jquery en underscore.js.

<!--
- **Enable the hamburger menu for mobile view** - Select the checkbox to integrate a hamburger menu into your form for mobile view. Represented by three horizontal lines stacked vertically, this menu provides a clear and uncluttered display for panels on smaller devices, especially on mobile devices. For more information about the hamburger menu, refer to the [Learn more about the hamburger menu](#learn-more-about-the-hamburger-menu) section. -->


### Tabblad Gegevensmodel {#data-model-tab}

![ Verzending tabel ](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

Met het formuliergegevensmodel kunt u een formulier verbinden met een gegevens-Source en gegevens verzenden en ontvangen op basis van gebruikersacties. U kunt een formulier ook verbinden met een JSON-schema om de verzonden gegevens in een vooraf gedefinieerde indeling te ontvangen. Afhankelijk van de vereiste verbinding, sluit uw formulier aan op een JSON-schema of formuliergegevensmodel:
- Een JSON-schema maken en uploaden naar uw omgeving
- Een formuliergegevensmodel maken

### Concepten

![ Verzending tabel ](/help/adaptive-forms/assets/formcontainer_autosavetab.png)

- **sparen automatisch concepten**: Selecteer **automatisch sparen concepten** controlevakje om het bewaren van vormen als concepten toe te laten.
- **sparen Voorkeur**: Vorm **sparen Voorkeur** als **sparen concepten met regelmatige intervallen**, om de vorm na een specifiek tijdsinterval auto-sparen.
  **sparen intervalfrequentie (Seconden)**: specificeer het tijdinterval (in seconden) om de duur te plaatsen die de automatische besparing van de vorm bij het bepaalde interval teweegbrengt.

### Tabblad Verzending {#submission-tab}

Gebruikers kunnen verschillende handelingen configureren voor het verzenden van een adaptief formulier.

- **Redirect URL/Weg** - Deze optie staat gebruiker toe om een pagina voor elke vorm te vormen, waaraan de vormgebruikers na het voorleggen van een Aangepast Vorm opnieuw worden gericht. Klik hier voor meer informatie over [ hoe te om opnieuw te richten pagina&#39;s ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html) te vormen.

![ Verzending tabel ](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **toon Bericht** - Deze optie staat gebruikers toe om een bericht toe te voegen dat wordt getoond wanneer de Aangepaste Vorm met succes wordt voorgelegd. De vooraf gedefinieerde tekst wordt opgenomen in het dialoogvenster en kan door de gebruiker worden gewijzigd. Het dialoogvenster Bericht tonen ondersteunt gereedschappen voor tekstopmaak waarmee gebruikers de toegevoegde tekst kunnen opmaken.

![ toon het lusje van het Bericht ](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **legt Actie** voor - een Submit Actie wordt teweeggebracht wanneer een gebruiker de Submit knoop op een AanpassingsVorm klikt. Gebruikers kunnen in de vervolgkeuzelijst de optie Handelingen verzenden selecteren die in het vak worden ondersteund. Leer hoe te [ vormen een Submit Actie in het lusje van de Verzending ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#supporting-custom-functions-in-validation-expressions-br).

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component Form Container te definiëren en te beheren.

### Tabblad Toegestane componenten {#allowed-components-tab}

![ dialoog van het Ontwerp stond componentenlusje ](/help/adaptive-forms/assets/formcontainer-allowedcomponents.png) toe

Het **Toegestane lusje van Componenten** staat malplaatjeredacteur toe om de componenten te plaatsen die als punten aan de panelen in de component in de Aangepaste redacteur van Forms kunnen worden toegevoegd.

### Tabblad Standaardcomponenten {#default-components-tab}

![ de dialoog standaardcomponentenlusje van het Ontwerp {](/help/adaptive-forms/assets/formcontainer-defaultcomponents.png)

Het **Standaardlusje van Componenten** staat de malplaatjeredacteur toe om de componenten te specificeren die door gebrek als punten in de component van de vormcontainer in de Aangepaste redacteur van Forms zichtbaar zijn.

### Tab Instellingen voor responsief {#responsive-tab}

![ de dialoog van het Ontwerp ontvankelijke montages tabel ](/help/adaptive-forms/assets/formcontainer-responsivestyle.png)

Het **Responsieve lusje van Montages** staat de malplaatjeredacteur toe om het aantal kolommen in het net binnen de component van de vormcontainer in de Adaptieve redacteur van Forms te specificeren.

### Tabblad Stijlen {#styles-tab}

De adaptieve Component van de Kern van de Bijlage van het Dossier van Forms steunt het AEM [ Systeem van de Stijl ](/help/get-started/authoring.md#component-styling).

![ Dialoog van het Ontwerp ](/help/adaptive-forms/assets/formcontainer-styletab.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de Aangepaste Component van de Kern van de Container van de Vorm van Forms verstrekken.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Tabblad Aangepaste eigenschappen

![ de Dialoog van Eigenschappen van de Douane ](/help/adaptive-forms/assets/formcontainer-custompropertiestab.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.

- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de orde van de naam van het douanebezit en de waarde van het douanebezit te herschikken.

<!--
## Learn more about the hamburger menu

A hamburger menu, often referred to as a mobile menu or navigation drawer, is a popular design element in mobile user interfaces. It features three horizontal lines stacked vertically, resembling a hamburger. The design efficiently conserves screen space by hiding secondary navigation options until they are needed, especially on smaller devices such as mobile. AEM forms can be efficiently organized within the hamburger menu, enabling users to access various panels within a form without overwhelming the main interface.

Consider a scenario, where a financial institution offers an online loan application form that requires users to provide detailed information across several panels, such as personal details, financial information, loan preferences, and supporting documents. The form includes multiple panels and options that can clutter the interface, especially on mobile devices. Users need an organized way to navigate through these panels without feeling overwhelmed. The hamburger menu is implemented to enhance the user experience on mobile devices.

### Components of hamburger menu

![Hamburger Menu](/help/adaptive-forms/assets/hamburger-menu.png){width=50%, align=center}

**A. Hamburger menu**: The hamburger menu features a navigation panel that slides out or drops down when the hamburger icon is clicked or tapped. The menu displays the panel headings, and selecting a panel shifts the focus to that panel. It allows users to easily navigate between different panels.

![Hamburger Menu](/help/adaptive-forms/assets/hamburger-menu-icon.png){width=50%}

**B. Breadcrumb**: Breadcrumbs indicate the user’s current location within the form. They offer a hierarchical trail that shows the user’s navigation path and helps them understand their position in the form.

**C. Active panel**: The active panel refers to the section or part of the form that is currently being displayed. When a user selects an option from the hamburger menu, the corresponding panel becomes the active panel, showing the relevant fields and information for that section.

### Points to consider while working with the hamburger menu

- The hamburger menu displays only the names of the panels. Here are different scenarios illustrating how the panel name appears in the navigation pane of the hamburger menu based on the configuration properties of the panel:  
  
  - If you set the properties of the panel to hidden, the panel's name does not appear in the navigation pane of the hamburger menu. For example, if you configure the properties of the `Financial Information` panel as `hidden`, the panel name does not appear in the navigation pane of the hamburger menu.
    
    ![Hidden panel](/help/adaptive-forms/assets/hidden-panel.png){width=50%}

  - If you set the properties of the panel to `disabled`, its name appears in the navigation pane of the hamburger menu, but you cannot select or edit it. For example, if you configure the properties of the `Financial Information` panel as `disabled`, the panel name appears in the navigation pane, but it cannot be selected or edited. 
     
    ![Disabled panel](/help/adaptive-forms/assets/disabled-panel.png){width=50%}

  - If you hide the  title of the panel, it does not appear in the navigation pane of the hamburger menu. A blank space shows up instead, but you can navigate to the fields of the panel by clicking on that space. For example, if you hide the title of the `Financial Information` panel, the blank space appears in its place in the navigation pane of the hamburger menu. You can navigate to the fields of the panel by clicking on the blank space.
    
    ![Hidden title panel](/help/adaptive-forms/assets/hidden-title-panel.png){width=50%}

- By default, the navigation pane in the breadcrumb component supports up to three levels of navigation. However, with the custom component, you can configure the navigation hierarchy to accommodate as many levels as needed.
- When using the hamburger menu, the user can navigate between panels using arrows. However, once a panel is selected, the menu automatically closes, and focus shifts to the fields within the chosen panel.

### Advantages to use hamburger menu

- **Space efficiency**: By hiding form navigation options until needed, the hamburger menu maximizes screen space, which is especially beneficial on smaller devices.

- **Clutter reduction**: It minimizes visual clutter by consolidating various form navigation links into a single, collapsible menu.

- **Improved focus**: With fewer visible navigation elements, users can concentrate on the main content of the form without being distracted by secondary options.

- **Simplified design**: It creates a more streamlined user interface, resulting in a cleaner and more organized form layout.

- **Enhanced mobile experience**: On mobile devices, where screen space is limited, the hamburger menu offers an efficient way to access all form navigation options without overwhelming the user.

### How to enable hamburger menu for your form?

To enable hamburger menu for form, perform the following steps:

1. Open form in an edit mode.
1. Open the Content browser, and select the **[!UICONTROL Guide Container]** component of your Adaptive Form. 
1. Click the Guide Container properties ![Guide properties](/help/adaptive-forms/assets/configure_icon.png) icon. The Adaptive Form Container dialog box opens. 
1. Click the  **[!UICONTROL Basic]** tab. 
1. Select the **[!UICONTROL Add hamburger menu support]** checkbox.
1. Click **[!UICONTROL Done]**.

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab.png)
-->

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}