---
title: Captcha in AEM Adaptive Forms
description: Verbeter de formulierbeveiliging met hCaptcha&reg; service zonder problemen. Stap-voor-stap gids binnen!
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
source-git-commit: 9a691fc2aa656f5a96d8cd4b6285e6bd473cdaa4
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---

# component Captcha{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> Deze functie valt onder het programma Vroege adopter. U kunt vanaf uw officiële e-mailadres naar aem-forms-ea@adobe.com schrijven om deel te nemen aan het programma voor vroege adoptie en toegang tot de functie te vragen. </span>

De service Captcha® beschermt uw formulieren tegen bots, spam en automatisch misbruik. Er wordt een widget selectievakje ingesteld en de reactie van de gebruiker geëvalueerd om te bepalen of het een mens of bot is die met het formulier communiceert. Het verhindert de gebruiker om te werk te gaan als de test ontbreekt en de hulp maakt online transacties veilig door bots te houden spam of kwaadwillige activiteiten posten.

![ hCaptcha® ](/help/adaptive-forms/assets/hCaptcha-challenge.png)

## Gebruik {#usage}

Er zijn verschillende redenen waarom het nuttig is om een hCaptcha-uitdaging op te nemen in een formulierverzendingsproces, namelijk:

- **Bot Preventie**: Het zorgt ervoor dat de vorm door een mens wordt voorgelegd, verminderend spam en geautomatiseerde voorlegging.

- **Veiligheid**: Het voegt een extra laag van veiligheid toe, die de legitimiteit van elke vormvoorlegging verifieert en tegen kwaadwillige aanvallen beschermt.

- **Integriteit van Gegevens**: Door veelvoudige of frauduleuze voorlegging te verhinderen, helpt het om de integriteit en de nauwkeurigheid van de gegevens te handhaven die door de vorm worden verzameld.

- **Verificatie van de Gebruiker**: Het verifieert de identiteit van de gebruiker die de vorm voorlegt, die ervoor zorgt dat slechts de voor authentiek verklaarde gebruikers gevoelige transacties kunnen voltooien.

- **Beheer van de Lading**: Het helpt serverlading beheren door het tarief van vormverzendingen te controleren, systeemoverbelasting tijdens hoog-verkeersperiodes verhinderen.

## Technische details {#technical-details}

Krijg de recentste informatie over de component hCaptcha in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

Specificeer de eigenschappen van de Component hCaptcha door [ te gebruiken vormen dialoog ](#configure-dialog). Het dialoogvenster voor configureren maakt deel uit van de kerncomponenten die zijn ontwikkeld om het ontwerpen van de formulieren eenvoudig te maken en een efficiënte manier te bieden om complexe formulieren te maken.

## Versie en compatibiliteit {#version-and-compatibility}


De adaptieve component van Forms hCaptcha wordt vrijgegeven in Mei 2024 als deel van [ Componenten 3.0.20 van de Kern ](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491). Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

|  |  |
|---|---|
| Componentversie | AEM as a Cloud Service |
| — | — |
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/adaptive-forms/version.md) en later | Compatibel | Compatibel |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het [&#128279;](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0&rbrace;.

## Dialoogvenster configureren {#configure-dialog}

U kunt eigenschappen van uw component hCaptcha met zijn gemakkelijk aanpassen vormt Dialoog die BasisLusje en het Lusje van de Bevestiging voor het aanpassen van diverse eigenschappen heeft.

### Tabblad Standaard {#basic-tab}

- **[!UICONTROL Name]:** specificeer de naam voor uw component hCaptcha, kunt u een vormcomponent gemakkelijk met zijn unieke naam zowel in de vorm als in de regelredacteur identificeren.
- **[!UICONTROL Title]:** specificeer de titel van uw component hCaptcha.
- **[!UICONTROL Configuration Settings]:** selecteer een Configuratie van de Wolk die voor hCaptcha® wordt gevormd.
- **Grootte Captcha:** U kunt de vertoningsgrootte van de de uitdagingsdialoogdoos selecteren hCaptcha®. Gebruik de **[!UICONTROL Compact]** optie om een kleine grootte en **[!UICONTROL Normal]** optie te tonen om een vrij groot de uitdagingsdialoog van hCaptcha® te tonen.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![ hCaptcha BasisLusje ](/help/adaptive-forms/assets/hcaptcha-basic.png)

### Tabblad Validatie {#validation-tab}

- **[!UICONTROL Validation Message]:** Geef een validatiebericht op voor uw Captcha-validatie bij het verzenden van het formulier.
- **[!UICONTROL Script Validation Message]** - Gebruik deze optie om een prompt bericht in te voeren als de scriptvalidatie mislukt.

  ![ hCaptcha het Lusje van de Bevestiging ](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**hCaptcha® is een geregistreerd handelsmerk van de Machines van de Intusie, Inc.**

**weet meer** over andere **Componenten Captcha** en hun diensten, zoals:

- [ Gebruik hCaptcha in een Aangepaste Vorm voor de Componenten van de Kern ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hcaptcha-core-components)

- [ Gebruik hCaptcha in een Aangepaste Vorm voor de Componenten van de Stichting ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [ Van het gebruiks Turnstile CAPTCHA in een Aanpassende Vorm voor de Componenten van de Stichting ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [ Google reCAPTCHA van het Gebruik in een AanpassingsVorm voor de Componenten van de Stichting ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
