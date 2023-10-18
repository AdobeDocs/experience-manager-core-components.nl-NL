---
title: Adaptieve Forms Core-component - Formuliercontainer
description: Voeg een adaptief formulier toe aan een webpagina.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
exl-id: 1e413ef3-7a6f-41fc-825d-dbe09ebaffe9
source-git-commit: 0bebc248ee2b708f7677950d90356abd5bc70a98
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 0%

---

# Google reCPATCHA {#google-recaptcha}

CAPTCHA (Complete Automated Public Turing test to tell Computers and Humans Apart) is een programma dat vaak wordt gebruikt bij online transacties om onderscheid te maken tussen mensen en geautomatiseerde programma&#39;s of bots. Het stelt een uitdaging en evalueert de reactie van de gebruiker om te bepalen of het een mens of bot is die met de site communiceert. Het verhindert de gebruiker om te werk te gaan als de test ontbreekt en de hulp maakt online transacties veilig door bots te houden spam of kwaadwillige doeleinden posten.

AEM Forms as a Cloud Service ondersteunt Google reCAPTCHA v2 in Adaptive Forms. U kunt het gebruiken om een CAPTCHA-uitdaging aan te geven bij het verzenden van formulieren

## Gebruik {#reasons-to-use-google-recaptcha}


- **Spam en Bot-preventie**: Een van de belangrijkste redenen voor het gebruik van reCAPTCHA is om te voorkomen dat spam-verzendingen en kwaadaardige bots uw formulier overstromen. De geavanceerde algoritmen van reCAPTCHA kunnen geautomatiseerde pogingen om het formulier te verzenden ontdekken, zodat alleen legitieme gebruikers ermee kunnen werken.

- **Uitgebreide beveiliging**: Door reCAPTCHA te implementeren, voegt u een extra beveiligingslaag toe aan het aangepaste formulier. Dit helpt gevoelige informatie beschermen en kwaadwillige gebruikers verhinderen kwetsbaarheid te exploiteren.

- **Gebruikerservaring**: Hoewel CAPTCHA&#39;s soms als ongemak kunnen worden beschouwd, betekent de adaptieve benadering van reCAPTCHA dat de meeste gebruikers een gestroomlijnde, gebruiksvriendelijke ervaring krijgen die minimale interactie vereist. Dit kan helpen een positieve gebruikerservaring te behouden terwijl het afschrikken van bots.

- **Aanpasbaarheid**: Het adaptieve mechanisme van reCAPTCHA analyseert gebruikersgedrag en interacties om te bepalen of ze menselijk zijn of niet. Dit betekent dat het niveau van de uitdaging die de gebruiker wordt aangeboden kan variëren afhankelijk van de waarschijnlijkheid dat hij een bot is. Dit aanpassingsvermogen vermindert de wrijving voor echte gebruikers terwijl het handhaven van sterke veiligheid.

- **Beperkte handmatige modernisering**: Door het aantal spamverzendingen en beide gegenereerde inhoud aanzienlijk te verminderen, kan reCAPTCHA tijd en middelen besparen die anders zouden worden besteed aan handmatige matiging en opschoning.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Google reCAPTCHA Core Component is in augustus 2023 uitgebracht als onderdeel van de Core Components &#39;version&#39;. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | --- |
| v1 | Compatibel met<br>[versie 2.0.4](/help/versions.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/versions.md) document.

## Technische details {#technical-details}

Lees de nieuwste informatie over de Adaptive Forms Google reCAPTCHA Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u uw Google reCAPTCHA-ervaring eenvoudig aanpassen voor bezoekers. U kunt eenvoudig Google reCAPTCHA-opties definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

- **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

- **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.

- **Configuratie** -

- **Type** -

- **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

- **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gegevens van de uitgeschakelde component worden niet verzonden De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

- **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tabblad Validatie {#validation-tab}

- **Foutbericht** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de optie **Vereist** wordt ingeschakeld en wordt het formulierveld leeg gelaten.

## Zie ook {#see-also}

- [Een adaptief formulier maken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)
- [Een adaptief formulier vertalen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)
- [PDF-versie (DoR) van een adaptief formulier genereren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components.html)
- [Een nieuwe landinstelling toevoegen voor een adaptief formulier](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components.html)
- [Aangepast formulier aansluiten op Microsoft® SharePoint,](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#create-sharepoint-configuration) [Microsoft® Power Automate,](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#microsoft-power-automate) [Microsoft® OneDrive](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#submit-to-onedrive) [of Azure Blob Storage](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#submit-to-azure-blob-storage)
- [Adaptieve formuliergegevens verzenden naar AEM Workflow of een bedrijfsprocesmanager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#invoke-an-aem-workflow)
- [Verzend Aangepaste gegevens van de Vorm naar een gegevensbestand of REST eindpunt](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#submit-to-rest-endpoint)
- [Adobe Analytics toestaan om het formuliergebruik te volgen](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/services/enable-adobe-analytics-adaptive-form-using-experience-cloud-setup-automation.html)
- [Adobe Sign gebruiken in een adaptief formulier](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/use-adobe-sign/working-with-adobe-sign.html)