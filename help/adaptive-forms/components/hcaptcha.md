---
title: Captcha in AEM Adaptive Forms
description: Verbeter de formulierbeveiliging met hCaptcha&reg; service zonder problemen. Stap-voor-stap gids binnen!
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
source-git-commit: 08d44e4db42594fb5aaf33d7d42df6fe19c70f59
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---

# component Captcha{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> Dit onderdeel valt onder het programma Vroege adoptie. U kunt vanaf uw officiële e-mailadres naar aem-forms-ea@adobe.com schrijven om deel te nemen aan het programma voor vroege adoptie en toegang tot de functie te vragen. </span>

De service Captcha® beschermt uw formulieren tegen bots, spam en automatisch misbruik. Er wordt een widget selectievakje ingesteld en de reactie van de gebruiker geëvalueerd om te bepalen of het een mens of bot is die met het formulier communiceert. Het verhindert de gebruiker om te werk te gaan als de test ontbreekt en de hulp maakt online transacties veilig door bots te houden spam of kwaadwillige activiteiten posten.

![hCaptcha®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

## Gebruik {#usage}

Er zijn verschillende redenen waarom het nuttig is om een hCaptcha-uitdaging op te nemen in een formulierverzendingsproces, namelijk:

- **Botpreventie**: Het zorgt ervoor dat het formulier wordt ingediend door een mens, waardoor spam en automatisch verzonden materiaal wordt verminderd.

- **Beveiliging**: Het voegt een extra laag van veiligheid toe, die de legitimiteit van elke vormvoorlegging verifieert en tegen kwaadwillige aanvallen beschermt.

- **Gegevensintegriteit**: Door meerdere of frauduleuze inzendingen te voorkomen, helpt het de integriteit en nauwkeurigheid van de via het formulier verzamelde gegevens te handhaven.

- **Gebruikersverificatie**: Hiermee wordt de identiteit gecontroleerd van de gebruiker die het formulier verzendt, zodat alleen geverifieerde gebruikers gevoelige transacties kunnen voltooien.

- **Laadbeheer**: Het helpt serverbelasting te beheren door de snelheid van formulierverzendingen te bepalen en systeemoverbelasting tijdens hoge-verkeersperioden te voorkomen.

## Technische details {#technical-details}

Voor de meest recente informatie over de component hCaptcha raadpleegt u de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

Geef de eigenschappen van de component Captcha op met de opdracht [dialoogvenster configureren](#configure-dialog). Het dialoogvenster voor configureren maakt deel uit van de kerncomponenten die zijn ontwikkeld om het ontwerpen van de formulieren eenvoudig te maken en een efficiënte manier te bieden om complexe formulieren te maken.

## Versie en compatibiliteit {#version-and-compatibility}


De Adaptive Forms hCaptcha Component wordt in mei 2024 vrijgegeven als onderdeel van de [Core Components 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491). Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | — |
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/adaptive-forms/version.md) document.

## Dialoogvenster configureren {#configure-dialog}

U kunt eigenschappen van uw component hCaptcha met zijn gemakkelijk aanpassen vormt Dialoog die BasisLusje en het Lusje van de Bevestiging voor het aanpassen van diverse eigenschappen heeft.

### Tabblad Standaard {#basic-tab}

- **[!UICONTROL Name]:** Als u de naam voor de component Captcha opgeeft, kunt u een formuliercomponent gemakkelijk identificeren met de unieke naam in zowel het formulier als de regeleditor.
- **[!UICONTROL Title]:** Geef de titel van de component Captcha op.
- **[!UICONTROL Configuration Settings]:** Selecteer een cloudconfiguratie die is geconfigureerd voor hCaptcha®.
- **Grootte captcha:** U kunt de weergavegrootte van het dialoogvenster Captcha®-uitdaging selecteren. Gebruik de **[!UICONTROL Compact]** als u een klein formaat en de **[!UICONTROL Normal]** optie om een relatief groot hCaptcha®-uitdagingsdialoogvenster weer te geven.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![Het tabblad Basis van Captcha](/help/adaptive-forms/assets/hcaptcha-basic.png)

### Tabblad Validatie {#validation-tab}

- **[!UICONTROL Validation Message]:** Geef een validatiebericht op voor uw Captcha-validatie bij het verzenden van het formulier.
- **[!UICONTROL Script Validation Message]** - Gebruik deze optie om een prompt bericht in te voeren als de scriptvalidatie mislukt.

  ![Tab voor hCaptcha-validatie](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**Captcha® is a registered trademark of Intution Machines, Inc.**

**Meer weten** over andere **Captcha-componenten** en hun diensten, zoals:

- [Captcha gebruiken in een adaptief formulier voor kerncomponenten](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hCaptcha-core-components)

- [Gebruik hCaptcha in een Aangepaste Vorm voor de Componenten van de Stichting](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [De Draaibare CAPTCHA van het gebruik in een AanpassingsVorm voor de Componenten van de Stichting](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [Google reCAPTCHA gebruiken in een adaptieve vorm voor Foundation Components](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}