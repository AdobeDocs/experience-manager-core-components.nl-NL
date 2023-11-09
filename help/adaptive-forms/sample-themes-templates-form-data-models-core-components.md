---
title: Hoe krijgt u voorbeeldthema's en sjablonen voor AEM Forms Core Components?
description: AEM Forms Core Components biedt voorbeelden van adaptieve formulierthema's, sjablonen en modellen met formuliergegevens.
solution: Experience Manager Forms
topic: Administration
role: Admin, User
level: Intermediate
exl-id: aef6e88b-dcae-4777-9893-9257d7702f43
source-git-commit: 1dd55fdd836dff89763887d88af2671ed1f9ce2b
workflow-type: tm+mt
source-wordcount: '1304'
ht-degree: 0%

---

# Voorbeeldthema&#39;s, sjablonen en modellen formuliergegevens {#sample-themes-templates-and-data-models}

[!DNL AEM Forms] Core Components biedt gebruiksklare voorbeeldthema&#39;s, sjablonen en modellen van formuliergegevens om snel flexibele formulieren te maken. Deze helpen auteurs ook om de uitbreidbaarheid, het aanpassingsvermogen en de responssnelheid van te leren [Adaptieve Forms Core-componenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html) om eenvoudige formulieren in een handomdraai en eenvoudig complexe formulieren te maken terwijl u naadloos verbinding maakt met de database.

De voorbeeldthema&#39;s, sjablonen en modellen van formuliergegevens in het pakket met referentie-inhoud zijn:

| Sjablonen | Thema&#39;s | Formuliergegevensmodellen |
---------|----------|---------
| [Leeg](#Blank) | [Canvas](#Canvas) | Microsoft® Dynamics 365 |
| [Contact opnemen](#Contact-Us) | [WKND](#WKND) | Salesforce |
| [Update van contactgegevens](#Contact-Details-Update) | [Easel](#Easel) |   |
| [Formulier voor goedkeuring](#Consent-Form) | [FSI](#FSI) |  |
| [Aanvraag voor logservice](#Log-Service-Request) | [Gezondheidszorg](#Healthcare) |  |
| [Feedback geven](#Give-Feedback) |  |  |
| [Inschrijving voor voordelen](#Benefits-Enrollment) |  |   |
| [Overzicht van personeelsbeloningen](#Employee-Benefits-Summary) |   |   |
| [Verzoek om een rekeningafschrift](#Request-for-Account-Statement) |   |   |
| [Veiligheidsinspectieformulier](#Safety-Inspection) |   |   |
| [Kwaliteitscontrole](#Quality-Control-Inspection) |   |   |
| [Aankoopaanvraag](#Purchase-Request) |  |  |

## Voorbeeldthema&#39;s {#Sample-Themes}

Met referentiemonsteringsthema&#39;s kunnen auteurs stijlen voor formulieren gebruiken, definiëren en aanpassen, zodat auteurs met zelfs een basiskennis van CSS het thema naar behoefte kunnen aanpassen.

**Hoe krijg je deze thema&#39;s?**
U krijgt deze thema&#39;s door de volgende stappen hieronder te gebruiken voor **AEM as a Cloud Service** milieu:

1. [Adaptieve Core-componenten van formulieren inschakelen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html)
1. [Implementeer een AEM Archetype 45-project in uw omgeving](https://github.com/adobe/aem-project-archetype)


Wanneer u een AEM archetype implementeert, kunt u alleen de OOTB-thema&#39;s in uw formulieren gebruiken. Als u de thema&#39;s naar wens wilt aanpassen, [Gebruik de front-end pijpleiding](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html) de thema&#39;s te implementeren.

>[!NOTE]
>
> * De thema&#39;s zijn niet beschikbaar voor **AEM 6,5** milieu.

<!--

1. **AEM 6.5**

    1. [Enable Adaptive Form Core Components](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/enable-adaptive-forms-core-components.html)
    1. [Deploy an AEM Archetype 45 project to your environment](https://github.com/adobe/aem-project-archetype)


    When you deploy an AEM Archetype, you can only use the OOTB themes in your forms, To customize the themes as per your requirements, [Use the front-end pipeline](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.html) to deploy the themes.

-->


<!--

### Deploying an AEM Archetype 45 project to your environment {#using-archetype-to-deploy-themes}

You can get these themes by deploying an [AEM Archetype 45](https://github.com/adobe/aem-project-archetype) to your **AEM Forms as a Cloud Service** or **AEM 6.5** Forms environment.

### Enable core components and use front-end pipeline to deploy themes {#use-front-end-pipeline-to-deploy-themes}

1. To get these themes on **Forms as a Cloud Service** environment, [enable Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html) and use the [front-end pipeline](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html) to deploy these themes.
    
1. To get these themes on **AEM 6.5 Forms** environment, [enable Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/enable-adaptive-forms-core-components.html) and use the [Package Manager](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.html) to deploy these themes.

[Learn to use and customize themes in AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html). 

[Learn to use and customize themes in AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components.html).

-->

De **uit de doos** [Adaptieve Core-componenten van formulieren](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html) de thema &#39; s zijn :

![OOTB-thema&#39;s](/help/adaptive-forms/assets/archetype-45-themes-1.png)

### Canvas {#Canvas}

Canvas-thema is het standaardthema voor formulieren en benadrukt het gebruik van basiskleuren, transparantie en platte pictogrammen. In de onderstaande schermafbeelding kunt u zien hoe het thema Canvas eruitziet.

![Canvasthema](/help/adaptive-forms/assets/Safety-Inspection-Theme-Canvas.png)

### WKND {#WKND}

Het WKND-thema belichaamt een levendig, verbeeldend en boeiend ontwerp om uw formulieren een stijlvol uiterlijk te geven. Het thema is gebaseerd op de vormgeving en opmaak van [WKND-site](https://wknd.site/us/en.html) de website voor reizen en avontuur is gebaseerd op [Adobe Experience Manager Core-componenten](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html).

![WKND-thema](/help/adaptive-forms/assets/Safety-Inspection-Form-Theme.png)


### Easel {#Easel}

Met het thema Easel kunt u een aantrekkelijk en eenvoudig in te stellen formulier maken dat is aangepast aan de eenvoud en gebruiksvriendelijkheid. Het eenvoudige thema is gebaseerd op het concept waarin kunstenaars een draagbare standaard gebruiken om een canvas te ondersteunen terwijl ze aan hun schilderijen werken.

![Easel-thema](/help/adaptive-forms/assets/Safety-Inspection-Theme-Easel.png)

### FSI (Financiële diensten en verzekeringen) {#FSI}

In het FSI-thema wordt de nadruk gelegd op het geven van een schone, praktische look aan uw formulier. De lichte blauwe kleurtoon wordt toegepast op het formulier wanneer u het FSI-thema toepast, zoals u kunt zien in de afbeelding.

![FSI-thema](/help/adaptive-forms/assets/fsi-theme-new1.png)


### Gezondheidszorg {#Healthcare}

Het thema Gezondheid maakt gebruik van rijke, verdorvene tonen om elementen zoals lusjes, panelen, tekstvakjes, en knopen binnen uw vorm te benadrukken.

![Thema gezondheidszorg](/help/adaptive-forms/assets/healthcare-new-theme.png)


## Voorbeeldsjablonen {#Sample-templates}

Sjablonen definiëren de initiële formulierstructuur, inhoud en handelingen die in het formulier moeten worden herhaald of gebruiken een vergelijkbare sjabloonstructuur als het formulier, zoals Goedkeuring, Voordelen, Inschrijvingsformulier en nog veel meer.

**Hoe krijg je deze sjablonen?**
U kunt deze malplaatjes krijgen door op te stellen [AEM Archetype 45](https://github.com/adobe/aem-project-archetype) aan uw **AEM Forms as a Cloud Service** milieu of **AEM 6,5 Forms** milieu.

<!--

>[!NOTE]
>
> * If you have [enabled core components and used front-end pipeline to deploy themes](#use-front-end-pipeline-to-deploy-themes), you need not to deploy an AEM Archetype.
> * You can find list of all OOTB templates when you create a form.

-->


De **uit de doos** [Adaptieve Core-componenten van formulieren](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html) sjablonen zijn:

![Referentiesjablonen](/help/adaptive-forms/assets/reference-templates-core-components.png)

<!--

### Basic {#Basic}

A basic template helps you quickly create an enrollment experience form. You can also use it to preview the functionality of [Adaptive Forms Core Components](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html). It provides a wizard layout for section-by-section presentation of data.

![Basic Template](/help/adaptive-forms/assets/Basic-template-desktop-view.png)

-->

### Leeg {#Blank}

Een lege canvassjabloon wordt gebruikt om een adaptieve formulierstructuur, inhoud en helemaal nieuwe regels te maken. Er zijn geen formuliercomponenten vooraf opgenomen in de lege sjabloon.

![Lege sjabloon](/help/adaptive-forms/assets/Blank-temp-desktop-view.png)

### Contact opnemen {#Contact-Us}

Met de formuliersjabloon Contact opnemen wordt een formulier gemaakt waarmee bezoekers van de website en formulierbeheerders gemakkelijker kunnen communiceren. Gebruikers kunnen via het formulier query&#39;s, feedback of ondersteuningsverzoeken verzenden.

![Contactpersonensjabloon](/help/adaptive-forms/assets/Contact-us-desktop-view.png)

### Update contactgegevens {#Contact-Details-Update}

Auteurs van de updatesjabloon voor contactgegevens kunnen een formulier maken voor het bijwerken van adres- en contactgegevens van klanten. Het formulier helpt klanten ook bij het bijwerken van persoonlijke informatie met betrekking tot abonnementen of voordelen, zodat u een naadloze communicatie en ononderbroken toegang tot de services of voordelen kunt garanderen.

![Contact-details-update](/help/adaptive-forms/assets/Contact-details-update.png)

### Goedkeuringsformulier {#Consent-Form}

Het toestemmingsformulier wordt gebruikt om een formulier te maken voor de aanschaf van een juridisch document van deelnemers die deelnemen aan een specifieke activiteit, een onderzoeksstudie, een medische procedure of een situatie waarin hun persoonlijke informatie of rechten betrokken kunnen zijn. Het formulier zorgt voor transparantie, beschermt de rechten van de deelnemer en geeft een duidelijk inzicht in wat het individu ermee instemt.

![Goedkeuringsformulier](/help/adaptive-forms/assets/Consent-form-desktop-view.png)

### Aanvraag voor logservice {#Log-Service-Request}

De de dienstverzoekmalplaatje van het logboek helpt tot een vorm leiden die logboek-specifieke het registreren diensten van een dienstverlener vraagt. Het formulier fungeert als een formeel verzoek om een ticket te maken voor gebeurtenissen, activiteiten of gegevenslogboeken voor het controleren of bijhouden van de status.

![Log Service Request Template](/help/adaptive-forms/assets/Log-service-request-desktop-view.png)


### Feedback geven {#Give-Feedback}

Met een feedbackformuliersjabloon kunt u een formulier samenstellen om een andere persoon of een ander team constructieve feedback te geven. Het formulier helpt ervoor te zorgen dat die feedback duidelijk, specifiek en actioneerbaar is en open communicatie en verbetering bevordert.

![Feedbacksjabloon geven](/help/adaptive-forms/assets/Give-feedback-desktop-view.png)


### Inschrijving voordelen {#Benefits-Enrollment}

Het inschrijvingsformuliersjabloon wordt gebruikt om een formulier te maken voor het verzamelen van essentiële informatie van hun werknemers over hun voorkeursvoordelen en dekkingsopties. Het gaat doorgaans vergezeld van de jaarlijkse periode waarin uitkeringen worden ingeschreven.

![Voordelen van inschrijfsjabloon](/help/adaptive-forms/assets/Benefits-enrollment-form-template.png)


### Overzicht personeelsbeloningen {#Employee-Benefits-Summary}

Samenvattingsformuliersjabloon voor personeelsbeloningen wordt gebruikt om een formulier te maken voor het verzamelen van essentiële details over de prestaties van een individu. Het helpt om dekking snel en nauwkeurig te evalueren, die een uitvoerig overzicht voor efficiënte hulp en steun verstrekken.
![Overzicht personeelsbeloningen](/help/adaptive-forms/assets/Employee-benefits-summary.png)


### Verzoek om accountverklaring {#Request-for-Account-Statement}

Een verzoek om de malplaatjes van de rekeningsverklaring van de rekening helpt om een vorm tot stand te brengen die het proces om een nauwkeurige en bijgewerkte verklaring van klanten in werking te stellen. Het overzicht bevat een gedetailleerd overzicht van financiële transacties, activiteiten of andere relevante informatie over klanten die dit formulier gebruiken.

![Verzoek om een rekeningverklaring](/help/adaptive-forms/assets/Request-for-account-statment.png)

### Veiligheidscontrole {#Safety-Inspection}

Met het sjabloon van het formulier voor veiligheidscontroles kunt u een formulier maken om gegevens in te voeren voor een veilige werkomgeving. Door regelmatige inspecties uit te voeren met behulp van dit formulier kunnen mogelijke gevaren worden geïdentificeerd. Het formulier heeft betrekking op diverse aspecten, zoals nooduitgangen, brandveiligheid, elektrische veiligheid, gevaarlijke materialen, persoonlijke beschermingsmiddelen, ergonomie van het werkstation voor de veiligheid en het welzijn van werknemers, bezoekers en klanten.

![Veiligheidscontroleformulier](/help/adaptive-forms/assets/Safety-inspection-form.png)

### Kwaliteitscontrole {#Quality-Control-Inspection}

Met het voorbeeldformulier voor kwaliteitscontrole kunt u een formulier maken voor het beoordelen en documenteren van de visuele weergave, afmetingen, functionaliteit, documentatie, testresultaten en algemene kwaliteit van een product of item. Het helpt gebreken, afwijkingen, en correctieve acties identificeren noodzakelijk om naleving van kwaliteitsnormen te verzekeren.

![Kwaliteitscontrole](/help/adaptive-forms/assets/Quality-Control-Inspection.png)


### Aankoopaanvraag {#Purchase-Request}

Met een formulier voor inkoopaanvragen kunt u een formulier maken waarmee het aanbestedingsproces kan worden geïnitieerd en werknemers de mogelijkheid krijgen formeel de aankoop van goederen of diensten aan te vragen die nodig zijn voor hun werk. In het formulier worden essentiële gegevens opgenomen, zoals de beschrijving van de artikelen, de hoeveelheid, de leverancier van de voorkeursleverancier (indien van toepassing), de toewijzing van het budget, de rechtvaardiging voor de aankoop, de leveringsinformatie en de vereiste goedkeuringen.

![purchase-request-form](/help/adaptive-forms/assets/Purchase-request-form.png)

## Referentieformuliergegevensmodellen {#reference-models}

Nadat u een adaptief formulier hebt gemaakt op [Kerncomponent](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html), kunt u uw formulier verbinden met de database Microsoft® Dynamics 365 en Salesforce-servers om bedrijfsworkflows mogelijk te maken. Bijvoorbeeld:

* Schrijf gegevens in Microsoft® Dynamics 365 en Salesforce over het verzenden van adaptieve formulieren.
* Schrijf gegevens in Microsoft® Dynamics 365 en Salesforce via aangepaste entiteiten die zijn gedefinieerd in het Form Data Model en vice versa.
* Vraag Microsoft® Dynamics 365 en Salesforce-server naar gegevens en vul Adaptive Forms vooraf in.
* Lees gegevens van Microsoft® Dynamics 365 en Salesforce-server.

U kunt de volgende modellen van de Gegevens van het Vorm krijgen door te installeren [Referentie-inhoudspakket](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-forms-reference-content.ui.content-2.1.0.zip):

* Microsoft® Dynamics 365
* Salesforce

Zie voor informatie over het gebruik van deze modellen [Microsoft® Dynamics 365 en Salesforce-cloudservices configureren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/configure-msdynamics-salesforce.html#configure-dynamics-cloud-service)
