---
title: Adaptieve Forms Core-component - Formuliercontainer
description: Voeg een adaptief formulier toe aan een webpagina.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
exl-id: 1e413ef3-7a6f-41fc-825d-dbe09ebaffe9
source-git-commit: e843ccf5c030cd4f1015e3290347b5799828537a
workflow-type: tm+mt
source-wordcount: '869'
ht-degree: 0%

---

# Google reCPATCHA {#google-recaptcha}

CAPTCHA (Complete Automated Public Turing test to tell Computers and Humans Apart) is een programma dat vaak wordt gebruikt bij online transacties om onderscheid te maken tussen mensen en geautomatiseerde programma&#39;s of bots. Het stelt een uitdaging en evalueert de reactie van de gebruiker om te bepalen of het een mens of bot is die met de site communiceert. Het verhindert de gebruiker om te werk te gaan als de test ontbreekt en de hulp maakt online transacties veilig door bots te houden spam of kwaadwillige doeleinden posten.

AEM Forms as a Cloud Service ondersteunt Google reCAPTCHA v2 in Adaptive Forms. U kunt het gebruiken om een CAPTCHA-uitdaging aan te geven bij het verzenden van formulieren

## Gebruik {#reasons-to-use-google-recaptcha}

- **Spam en Bot Preventie**: Één van de primaire redenen om reCAPTCHA te gebruiken moet spamvoorlegging en kwaadwillige bots verhinderen uw vorm te overstromen. De geavanceerde algoritmen van reCAPTCHA kunnen geautomatiseerde pogingen om het formulier te verzenden ontdekken, zodat alleen legitieme gebruikers ermee kunnen werken.

- **Verbeterde Veiligheid**: Door reCAPTCHA uit te voeren, voegt u een extra laag van veiligheid aan uw adaptieve vorm toe. Dit helpt gevoelige informatie beschermen en kwaadwillige gebruikers verhinderen kwetsbaarheid te exploiteren.

- **Ervaring van de Gebruiker**: Terwijl CAPTCHAs soms als ongemak kan worden gezien, betekent de adaptieve benadering van reCAPTCHA dat de meeste gebruikers met een gestroomlijnde, gebruikersvriendelijke ervaring worden voorgesteld die minimale interactie vereist. Dit kan helpen een positieve gebruikerservaring te behouden terwijl het afschrikken van bots.

- **Aanpassingsvermogen**: reCAPTCHA&#39;s adaptieve mechanisme analyseert gebruikersgedrag en interactie om te bepalen of zij menselijk of niet zijn. Dit betekent dat het niveau van de uitdaging die de gebruiker wordt aangeboden kan variëren afhankelijk van de waarschijnlijkheid dat hij een bot is. Dit aanpassingsvermogen vermindert de wrijving voor echte gebruikers terwijl het handhaven van sterke veiligheid.

- **Verminderde Handmatige Moderatie**: Door het aantal spambijdragen en allebei-geproduceerde inhoud beduidend te verminderen, kan reCAPTCHA tijd en middelen besparen die anders aan handmatiging en schoonmaakbeurt zouden worden uitgegeven.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Google reCAPTCHA Core Component is in augustus 2023 uitgebracht als onderdeel van de Core Components &#39;version&#39;. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:


|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | — |
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/versions.md) en later | Compatibel | Compatibel |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het ](/help/versions.md) document van de Versies van de Componenten van de Kern 0}.[

## Technische details {#technical-details}

Krijg de recentste informatie over de Adaptieve Component van de Kern van Forms Google reCAPTCHA in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u uw Google reCAPTCHA-ervaring eenvoudig aanpassen voor bezoekers. U kunt eenvoudig Google reCAPTCHA-opties definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

- **Naam** - u kunt een vormcomponent gemakkelijk met zijn unieke naam zowel in de vorm als in de regelredacteur identificeren, maar de naam moet geen ruimten of speciale karakters bevatten.

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bovenop de component. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

- **Verberg Titel** - selecteer de optie om de Titel van de component te verbergen.

- **Configuratie** -

- **Type** -

- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gegevens van de uitgeschakelde component worden niet verzonden De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

- **read-only** - selecteer de optie om de component niet-editable te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tabblad Validatie {#validation-tab}

- **Bericht van de Fout** - Deze optie staat u toe om een bericht in te gaan dat wordt getoond als **Vereiste** checkbox wordt gecontroleerd en het vormgebied wordt verlaten leeg.

## Zie ook {#see-also}

- [ creeer een AEM Aangepaste Vorm ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)
- [ voeg een AEM Aangepaste Vorm aan de pagina van AEM Sites toe ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)
- [ pas thema&#39;s op een AEM Aangepaste Vorm ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html) toe
- [Componenten toevoegen aan een AEM adaptief formulier](/help/adaptive-forms/introduction.md#adaptive-forms-core-components-components)
- [ Gebruik reCAPTCHA in een AEM Aangepaste Vorm ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms.html)
- [ produceer PDF versie (DoR) van een AEM Aanpassings Vorm ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components.html)
- [ vertaal een AEM AanpassingsVorm ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-aem-translation-workflow-to-localize-adaptive-forms-core-components.html)
- [ laat Adobe Analytics voor een Aangepast Vorm toe om vormgebruik te volgen ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/services/enable-adobe-analytics-adaptive-form-using-experience-cloud-setup-automation.html)
- [ verbind Aangepast Vorm met Microsoft SharePoint ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#create-sharepoint-configuration)
- [ Verbind Aangepast Vorm aan de Macht van Microsoft ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#microsoft-power-automate)
- [ verbind Aangepast Vorm met Microsoft OneDrive ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#submit-to-onedrive)
- [ Verbind Aangepast Vorm met de Opslag van Microsoft Azure Blob ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#submit-to-azure-blob-storage)
- [ verbind Aangepast Vorm met Salesforce ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/oauth2-client-credentials-flow-for-server-to-server-integration.html)
- [ Gebruik Adobe Sign in een AEM Aangepaste Vorm ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/use-adobe-sign/working-with-adobe-sign.html)
- [ voeg een nieuwe scène voor een Aangepaste Vorm ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/supporting-new-language-localization-core-components.html) toe
- [ verzendt de Adaptieve gegevens van de Vorm naar een gegevensbestand ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/data-integration.html)
- [ verzendt de Adaptieve gegevens van de Vorm naar een REST eindpunt ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#submit-to-rest-endpoint)
- [ verzendt de Adaptieve gegevens van de Vorm naar AEM Werkschema ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components.html#invoke-an-aem-workflow)
- [ Portaal van Forms van het gebruik om AEM Aangepaste Forms op een AEM website ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-forms-portal.html) op te nemen

