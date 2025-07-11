---
title: Hoe krijgt u voorbeeldthema's en sjablonen voor AEM Forms Core Components?
description: AEM Forms Core Components biedt voorbeelden van adaptieve formulierthema's, sjablonen en modellen met formuliergegevens.
solution: Experience Manager Forms
topic: Administration
role: Admin, User
level: Intermediate
exl-id: aef6e88b-dcae-4777-9893-9257d7702f43
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 0%

---

# Voorbeeldthema&#39;s, sjablonen en modellen formuliergegevens {#sample-themes-templates-and-data-models}

[!DNL AEM Forms] Core Components biedt gebruiksklare voorbeeldthema&#39;s, sjablonen en modellen van formuliergegevens om snel flexibele formulieren te maken. Deze helpen ook vormauteurs om de rekbaarheid, het aanpassingsvermogen, en de ontvankelijkheid van [ Aangepaste Componenten van de Kern van Forms ](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=nl-NL) te leren om eenvoudige vormen in geen tijd en complexe vormen gemakkelijk te creëren terwijl het verbinden met het gegevensbestand foutloos.

De voorbeeldthema&#39;s, sjablonen en modellen van formuliergegevens in het pakket met referentie-inhoud zijn:

| Sjablonen | Thema&#39;s | Formuliergegevensmodellen |
---------|----------|---------
| [ Lege ](#Blank) | [ Canvas ](#Canvas) | Microsoft® Dynamics 365 |
| [ Contact ons ](#Contact-Us) | [ WKND ](#WKND) | Salesforce |
| [ update van de Details van het Contact ](#Contact-Details-Update) | [ Easel ](#Easel) |   |
| [ Toestemming vorm ](#Consent-Form) | [ FSI ](#FSI) |  |
| [ de dienstverzoek van het Logboek ](#Log-Service-Request) | [ Gezondheidszorg ](#Healthcare) |  |
| [ geef terugkoppelen ](#Give-Feedback) |  |  |
| [ Voordelen inschrijving ](#Benefits-Enrollment) |  |   |
| [ Overzicht van de beloningen van de Werknemer ](#Employee-Benefits-Summary) |   |   |
| [ Verzoek om rekeningsverklaring ](#Request-for-Account-Statement) |   |   |
| [ de inspectievorm van de Veiligheid ](#Safety-Inspection) |   |   |
| [ de controleinspectie van de Kwaliteit ](#Quality-Control-Inspection) |   |   |
| [ verzoek van de Aankoop ](#Purchase-Request) |  |  |

{{traditional-aem}}

## Voorbeeldthema&#39;s {#Sample-Themes}

Met referentiemonsteringsthema&#39;s kunnen auteurs stijlen voor formulieren gebruiken, definiëren en aanpassen, zodat auteurs met zelfs een basiskennis van CSS het thema naar behoefte kunnen aanpassen.

**hoe te om deze thema&#39;s te krijgen?**
U krijgt deze thema&#39;s door de volgende hieronder gegeven stappen voor **AEM as a Cloud Service** milieu te gebruiken:

1. [ laat de Aangepaste Componenten van de Kern van de Vorm toe ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=nl-NL)
1. [ stel een project van Archetype 47 van AEM of later aan uw milieu op ](https://github.com/adobe/aem-project-archetype)


Wanneer u een Archetype van AEM opstelt, kunt u de thema&#39;s OTB in uw vormen slechts gebruiken, om de thema&#39;s zoals per uw vereisten aan te passen, [ Gebruik de front-end pijpleiding ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html?lang=nl-NL) om de thema&#39;s op te stellen.

>[!NOTE]
>
> * De thema&#39;s zijn niet beschikbaar voor **AEM 6.5** milieu.

<!--

1. **AEM 6.5**

    1. [Enable Adaptive Form Core Components](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/enable-adaptive-forms-core-components.html?lang=nl-NL)
    1. [Deploy an AEM Archetype 47 or later project to your environment](https://github.com/adobe/aem-project-archetype)


    When you deploy an AEM Archetype, you can only use the OOTB themes in your forms, To customize the themes as per your requirements, [Use the front-end pipeline](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.html?lang=nl-NL) to deploy the themes.

-->


<!--

### Deploying an AEM Archetype 47 or later project to your environment {#using-archetype-to-deploy-themes}

You can get these themes by deploying an [AEM Archetype 47 or later](https://github.com/adobe/aem-project-archetype) to your **AEM Forms as a Cloud Service** or **AEM 6.5** Forms environment.

### Enable core components and use front-end pipeline to deploy themes {#use-front-end-pipeline-to-deploy-themes}

1. To get these themes on **Forms as a Cloud Service** environment, [enable Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=nl-NL) and use the [front-end pipeline](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html?lang=nl-NL) to deploy these themes.
    
1. To get these themes on **AEM 6.5 Forms** environment, [enable Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/enable-adaptive-forms-core-components.html?lang=nl-NL) and use the [Package Manager](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.html?lang=nl-NL) to deploy these themes.

[Learn to use and customize themes in AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html?lang=nl-NL). 

[Learn to use and customize themes in AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.html?lang=nl-NL).

-->

**uit de doos** [ de Adaptieve Componenten van de Kern van de Vorm ](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=nl-NL) thema&#39;s zijn:

![ OOTB thema&#39;s ](/help/adaptive-forms/assets/archetype-45-themes-1.png)

### Canvas {#Canvas}

Canvas-thema is het standaardthema voor formulieren en benadrukt het gebruik van basiskleuren, transparantie en platte pictogrammen. In de onderstaande schermafbeelding kunt u zien hoe het thema Canvas eruitziet.

![ het thema van Canvas ](/help/adaptive-forms/assets/Safety-Inspection-Theme-Canvas.png)

### WKND {#WKND}

Het WKND-thema belichaamt een levendig, verbeeldend en boeiend ontwerp om uw formulieren een stijlvol uiterlijk te geven. Het thema is gebaseerd op de verschijning en het stileren van [ plaats WKND ](https://wknd.site/us/en.html) die een reis en een avontuurwebsite is bouwt op [ de Componenten van de Kern van Adobe Experience Manager ](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=nl-NL) voort.

![ WKND thema ](/help/adaptive-forms/assets/Safety-Inspection-Form-Theme.png)


### Easel {#Easel}

Met het thema Easel kunt u een aantrekkelijk en eenvoudig in te stellen formulier maken dat is aangepast aan de eenvoud en gebruiksvriendelijkheid. Het eenvoudige thema is gebaseerd op het concept waarin kunstenaars een draagbare standaard gebruiken om een canvas te ondersteunen terwijl ze aan hun schilderijen werken.

![ Easel thema ](/help/adaptive-forms/assets/Safety-Inspection-Theme-Easel.png)

### FSI (Financiële diensten en verzekeringen) {#FSI}

In het FSI-thema wordt de nadruk gelegd op het geven van een schone, praktische look aan uw formulier. De lichte blauwe kleurtoon wordt toegepast op het formulier wanneer u het FSI-thema toepast, zoals u kunt zien in de afbeelding.

![ FSI Thema ](/help/adaptive-forms/assets/fsi-theme-new1.png)


### Gezondheidszorg {#Healthcare}

Het thema Gezondheid maakt gebruik van rijke, verdorvene tonen om elementen zoals lusjes, panelen, tekstvakjes, en knopen binnen uw vorm te benadrukken.

![ Thema van de Gezondheidszorg ](/help/adaptive-forms/assets/healthcare-new-theme.png)


## Voorbeeldsjablonen {#Sample-templates}

Sjablonen definiëren de initiële formulierstructuur, inhoud en handelingen die in het formulier moeten worden herhaald of gebruiken een vergelijkbare sjabloonstructuur als het formulier, zoals Goedkeuring, Voordelen, Inschrijvingsformulier en nog veel meer.

**hoe te om deze malplaatjes te krijgen?**

U kunt deze malplaatjes krijgen door [ AEM Archetype 47 of later ](https://github.com/adobe/aem-project-archetype) aan uw **as a Cloud Service van AEM Forms** milieu of **AEM 6.5 Forms** milieu op te stellen.

<!--

>[!NOTE]
>
> * If you have [enabled core components and used front-end pipeline to deploy themes](#use-front-end-pipeline-to-deploy-themes), you need not to deploy an AEM Archetype.
> * You can find list of all OOTB templates when you create a form.

-->


**uit de doos** [ de Aangepaste Componenten van de Kern van de Vorm ](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=nl-NL) zijn:

![ de Malplaatjes van de Verwijzing ](/help/adaptive-forms/assets/reference-templates-core-components.png)

<!--

### Basic {#Basic}

A basic template helps you quickly create an enrollment experience form. You can also use it to preview the functionality of [Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=nl-NL). It provides a wizard layout for section-by-section presentation of data.

![Basic Template](/help/adaptive-forms/assets/Basic-template-desktop-view.png)

-->

### Leeg {#Blank}

Een lege canvassjabloon wordt gebruikt om een adaptieve formulierstructuur, inhoud en helemaal nieuwe regels te maken. Er zijn geen formuliercomponenten vooraf opgenomen in de lege sjabloon.

![ Leeg Malplaatje ](/help/adaptive-forms/assets/Blank-temp-desktop-view.png)

### Contact opnemen {#Contact-Us}

Met de formuliersjabloon Contact opnemen wordt een formulier gemaakt waarmee bezoekers van de website en formulierbeheerders gemakkelijker kunnen communiceren. Gebruikers kunnen via het formulier query&#39;s, feedback of ondersteuningsverzoeken verzenden.

![ het Malplaatje van het Contact van ons ](/help/adaptive-forms/assets/Contact-us-desktop-view.png)

### Update contactgegevens {#Contact-Details-Update}

Auteurs van de updatesjabloon voor contactgegevens kunnen een formulier maken voor het bijwerken van adres- en contactgegevens van klanten. Het formulier helpt klanten ook bij het bijwerken van persoonlijke informatie met betrekking tot abonnementen of voordelen, zodat u een naadloze communicatie en ononderbroken toegang tot de services of voordelen kunt garanderen.

![ contact-details-update ](/help/adaptive-forms/assets/Contact-details-update.png)

### Goedkeuringsformulier {#Consent-Form}

Het toestemmingsformulier wordt gebruikt om een formulier te maken voor de aanschaf van een juridisch document van deelnemers die deelnemen aan een specifieke activiteit, een onderzoeksstudie, een medische procedure of een situatie waarin hun persoonlijke informatie of rechten betrokken kunnen zijn. Het formulier zorgt voor transparantie, beschermt de rechten van de deelnemer en geeft een duidelijk inzicht in wat het individu ermee instemt.

![ Goedgekeurde Vorm ](/help/adaptive-forms/assets/Consent-form-desktop-view.png)

### Aanvraag voor logservice {#Log-Service-Request}

De de dienstverzoekmalplaatje van het logboek helpt tot een vorm leiden die logboek-specifieke het registreren diensten van een dienstverlener vraagt. Het formulier fungeert als een formeel verzoek om een ticket te maken voor gebeurtenissen, activiteiten of gegevenslogboeken voor het controleren of bijhouden van de status.

![ Malplaatje van het Verzoek van de Dienst van het Logboek ](/help/adaptive-forms/assets/Log-service-request-desktop-view.png)


### Feedback geven {#Give-Feedback}

Met een feedbackformuliersjabloon kunt u een formulier samenstellen om een andere persoon of een ander team constructieve feedback te geven. Het formulier helpt ervoor te zorgen dat die feedback duidelijk, specifiek en actioneerbaar is en open communicatie en verbetering bevordert.

![ geef het Malplaatje van de Terugkoppeling ](/help/adaptive-forms/assets/Give-feedback-desktop-view.png)


### Inschrijving voordelen {#Benefits-Enrollment}

Het inschrijvingsformuliersjabloon wordt gebruikt om een formulier te maken voor het verzamelen van essentiële informatie van hun werknemers over hun voorkeursvoordelen en dekkingsopties. Het gaat doorgaans vergezeld van de jaarlijkse periode waarin uitkeringen worden ingeschreven.

![ Malplaatje van de Inschrijving van Voordelen ](/help/adaptive-forms/assets/Benefits-enrollment-form-template.png)


### Overzicht personeelsbeloningen {#Employee-Benefits-Summary}

Samenvattingsformuliersjabloon voor personeelsbeloningen wordt gebruikt om een formulier te maken voor het verzamelen van essentiële details over de prestaties van een individu. Het helpt om dekking snel en nauwkeurig te evalueren, die een uitvoerig overzicht voor efficiënte hulp en steun verstrekken.
![ Overzicht van de Voordelen van de Werknemer ](/help/adaptive-forms/assets/Employee-benefits-summary.png)


### Verzoek om accountverklaring {#Request-for-Account-Statement}

Een verzoek om de malplaatjes van de rekeningsverklaring van de rekening helpt om een vorm tot stand te brengen die het proces om een nauwkeurige en bijgewerkte verklaring van klanten in werking te stellen. Het overzicht bevat een gedetailleerd overzicht van financiële transacties, activiteiten of andere relevante informatie over klanten die dit formulier gebruiken.

![ verzoek-voor-rekening-verklaring ](/help/adaptive-forms/assets/Request-for-account-statment.png)

### Veiligheidscontrole {#Safety-Inspection}

Met het sjabloon van het formulier voor veiligheidscontroles kunt u een formulier maken om gegevens in te voeren voor een veilige werkomgeving. Door regelmatige inspecties uit te voeren met behulp van dit formulier kunnen mogelijke gevaren worden geïdentificeerd. Het formulier heeft betrekking op diverse aspecten, zoals nooduitgangen, brandveiligheid, elektrische veiligheid, gevaarlijke materialen, persoonlijke beschermingsmiddelen, ergonomie van het werkstation voor de veiligheid en het welzijn van werknemers, bezoekers en klanten.

![ Vorm van de Inspectie van de Veiligheid ](/help/adaptive-forms/assets/Safety-inspection-form.png)

### Kwaliteitscontrole {#Quality-Control-Inspection}

Met het voorbeeldformulier voor kwaliteitscontrole kunt u een formulier maken voor het beoordelen en documenteren van de visuele weergave, afmetingen, functionaliteit, documentatie, testresultaten en algemene kwaliteit van een product of item. Het helpt gebreken, afwijkingen, en correctieve acties identificeren noodzakelijk om naleving van kwaliteitsnormen te verzekeren.

![ Inspectie van de Controle van de Kwaliteit ](/help/adaptive-forms/assets/Quality-Control-Inspection.png)


### Aankoopaanvraag {#Purchase-Request}

Met een formulier voor inkoopaanvragen kunt u een formulier maken waarmee het aanbestedingsproces kan worden geïnitieerd en werknemers de mogelijkheid krijgen formeel de aankoop van goederen of diensten aan te vragen die nodig zijn voor hun werk. In het formulier worden essentiële gegevens opgenomen, zoals de beschrijving van de artikelen, de hoeveelheid, de leverancier van de voorkeursleverancier (indien van toepassing), de toewijzing van het budget, de rechtvaardiging voor de aankoop, de leveringsinformatie en de vereiste goedkeuringen.

![ aankoop-verzoek-vorm ](/help/adaptive-forms/assets/Purchase-request-form.png)

## Referentieformuliergegevensmodellen {#reference-models}

Nadat u een Aangepast Vorm creeert dat op [ wordt gebaseerd de Component van de Kern ](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html?lang=nl-NL), kunt u uw vorm met gegevensbestand Microsoft® Dynamics 365 en de servers van Salesforce verbinden om bedrijfswerkschema&#39;s toe te laten. Bijvoorbeeld:

* Schrijf gegevens in Microsoft® Dynamics 365 en Salesforce over het verzenden van adaptieve formulieren.
* Schrijf gegevens in Microsoft® Dynamics 365 en Salesforce via aangepaste entiteiten die zijn gedefinieerd in het Form Data Model en vice versa.
* Vraag Microsoft® Dynamics 365 en Salesforce-server naar gegevens en vul Adaptive Forms vooraf in.
* Lees gegevens van Microsoft® Dynamics 365 en Salesforce server.

U kunt de volgende Modellen van de Gegevens van de Vorm krijgen door het [ inhoudspakket van de Verwijzing ](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-forms-reference-content.ui.content-2.1.0.zip) te installeren:

* Microsoft® Dynamics 365
* Salesforce

Voor informatie bij het gebruiken van deze modellen, zie [ de Dynamica 365 van Microsoft® en de wolkendiensten van Salesforce ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/configure-msdynamics-salesforce.html?lang=nl-NL#configure-dynamics-cloud-service) vormen
