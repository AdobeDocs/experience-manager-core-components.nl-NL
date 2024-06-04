---
title: Adaptive Forms Core Component - Google reCAPTCHA
description: Verbeter de formulierbeveiliging met de Google reCAPTCHA-service zonder moeite met AEM Forms. Eigenschappen van Adaptief Form reCaptcha uitleggen
role: Architect, Developer, Admin, User
source-git-commit: 4c510b8fe59f4be6e1b329ee4257ab1b780fbf22
workflow-type: tm+mt
source-wordcount: '1325'
ht-degree: 0%

---


# Adaptief formulier reCAPTCHA {#google-recaptcha}

CAPTCHA (Complete Automated Public Turing Test to tell Computers and Humans Apart) is een programma dat veel wordt gebruikt bij online transacties om onderscheid te maken tussen mensen en geautomatiseerde programma&#39;s of bots. Het stelt een uitdaging en evalueert de reactie van de gebruiker om te bepalen of het een mens of bot is die met de site communiceert. Het verhindert de gebruiker om te werk te gaan als de test ontbreekt en de hulp maakt online transacties veilig door bots te houden spam of kwaadwillige doeleinden posten.

AEM Forms as a Cloud Service ondersteunt Google reCAPTCHA v2 in Adaptive Forms. U kunt het gebruiken om een CAPTCHA-uitdaging aan te geven bij het verzenden van formulieren

## Gebruik {#reasons-to-use-google-recaptcha}


- **Spam en Bot-preventie**: Een van de belangrijkste redenen voor het gebruik van reCAPTCHA is om te voorkomen dat spam-verzendingen en kwaadaardige bots uw formulier overstromen. De geavanceerde algoritmen van reCAPTCHA kunnen geautomatiseerde pogingen om het formulier te verzenden ontdekken, zodat alleen legitieme gebruikers ermee kunnen werken.

- **Uitgebreide beveiliging**: Door reCAPTCHA te implementeren, voegt u een extra beveiligingslaag toe aan het aangepaste formulier. Dit helpt gevoelige informatie beschermen en kwaadwillige gebruikers verhinderen kwetsbaarheid te exploiteren.

- **Gebruikerservaring**: Hoewel CAPTCHA&#39;s soms als ongemak kunnen worden beschouwd, betekent de adaptieve benadering van reCAPTCHA dat de meeste gebruikers een gestroomlijnde, gebruiksvriendelijke ervaring krijgen die minimale interactie vereist. Dit kan helpen een positieve gebruikerservaring te behouden terwijl het afschrikken van bots.

- **Aanpasbaarheid**: Het adaptieve mechanisme van reCAPTCHA analyseert gebruikersgedrag en interacties om te bepalen of ze menselijk zijn of niet. Dit betekent dat het niveau van de uitdaging die de gebruiker wordt aangeboden kan variëren afhankelijk van de waarschijnlijkheid dat hij een bot is. Dit aanpassingsvermogen vermindert de wrijving voor echte gebruikers terwijl het handhaven van sterke veiligheid.

- **Beperkte handmatige modernisering**: Door het aantal spamverzendingen en beide gegenereerde inhoud aanzienlijk te verminderen, kan reCAPTCHA tijd en middelen besparen die anders zouden worden besteed aan handmatige matiging en opschoning.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Google reCAPTCHA Core Component is in augustus 2023 uitgebracht als onderdeel van de Core Components &#39;version&#39;. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:


| Componentversie | AEM as a Cloud Service |
|--- |--- |
| v1 | Compatibel met<br>[versie 2.0.4](/help/versions.md) en hoger | Compatibel | Compatibel |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Versies van kerncomponenten](/help/versions.md) document.

## Technische details {#technical-details}

Lees de nieuwste informatie over de Adaptive Forms Google reCAPTCHA Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). Voor meer informatie over het ontwikkelen van Core Components, bekijk [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u uw Google reCAPTCHA-ervaring eenvoudig aanpassen voor bezoekers. U kunt eenvoudig Google reCAPTCHA-opties definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![Tabblad Standaard](/help/adaptive-forms/assets/recaptcha-basictab.png)

- **Naam** - U kunt een formuliercomponent gemakkelijk herkennen met de unieke naam, zowel in het formulier als in de regeleditor, maar de naam mag geen spaties of speciale tekens bevatten.

- **Titel** - Met Titel kunt u een component gemakkelijk herkennen in een formulier. Standaard wordt de titel boven op de component weergegeven. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

- **RTF-tekst voor titel toestaan** - Met deze functies kunnen gebruikers gewone teksttitels opmaken en functies zoals vet, cursief, onderstreepte tekst, diverse lettertypen, tekengrootten, kleuren en extra opties opnemen om de visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Als u het selectievakje **RTF-tekst toestaan voor titel inschakelt, worden opmaakopties zichtbaar om de titel van de component op te maken. Als u toegang wilt tot alle beschikbare opmaakopties, klikt u op de knop ![Pictogram Volledig scherm](/help/adaptive-forms/assets/fullscreen-icon.png) tab.

  ![RTF-ondersteuning](/help/adaptive-forms/assets/richtext-support-title.png)

- **Titel verbergen** - Selecteer de optie om de titel van de component te verbergen.
- **Markeren als niet-gebonden formulierelement**: Selecteer de optie om een formulierveld te configureren dat niet is gekoppeld aan een schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.
- **Configuratie-instellingen**: Selecteer de configuratiecontainer die de wolkenconfiguratie bevat die AEM Forms met de reCAPTCHA dienst door Google verbindt.

  >[!NOTE]
  >
  > Zie de [Google reCAPTCHA gebruiken in een AEM adaptief formulier op basis van Core Components](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components) artikel voor het maken en configureren van Google reCAPTCHA voor uw omgeving.

- **Type**: Kies deze optie om de grootte voor reCAPTCHA te selecteren.
   - **Normaal**: Verwijst naar de standaard, grotere versie van de reCAPTCHA-widget, die voor gebruikers beter zichtbaar en gemakkelijker kan zijn om mee te werken, vooral op apparaten met grotere schermen.
   - **Compact**: Verwijst naar een kleinere versie van de reCAPTCHA-widget. Deze optie is geschikt voor situaties waarin ruimte beperkt is, zoals op mobiele apparaten of in strakke lay-outs op webpagina&#39;s.

- **Component verbergen** - Selecteer de optie om de component te verbergen voor het formulier. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

- **Component uitschakelen** - Selecteer de optie om de component uit te schakelen. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gegevens van de uitgeschakelde component worden niet verzonden De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

- **Alleen-lezen** - Selecteer de optie om de component niet-bewerkbaar te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tabblad Validatie {#validation-tab}

![Tabblad Validatie](/help/adaptive-forms/assets/recaptcha-validationtab.png)

- **Foutbericht** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de optie **Vereist** wordt ingeschakeld en wordt het formulierveld leeg gelaten.

- **Bericht voor scriptvalidatie** - Met deze optie kunt u een bericht invoeren dat wordt weergegeven als de scriptvalidatie mislukt.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component reCAPTCHA te definiëren en te beheren.

### Tabblad Stijlen {#styles-design-tab}

De Adaptive Forms reCAPTCHA Core Component ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

![Ontwerpdialoogvenster](/help/adaptive-forms/assets/checkbox-style.png)

- **Standaard CSS-klassen**: U kunt een standaard CSS-klasse opgeven voor de Adaptive Forms reCAPTCHA Core-component.

- **Toegestane stijlen**: U kunt stijlen definiëren door een naam op te geven en de CSS-klasse op te geven die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Als u een stijl wilt toepassen, selecteert u in de Adaptieve Forms-editor de component waarop u de stijl wilt toepassen, navigeert u naar het dialoogvenster Eigenschappen en selecteert u de gewenste stijl in het menu **Stijlen** vervolgkeuzelijst. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![Dialoogvenster Aangepaste eigenschappen](/help/adaptive-forms/assets/checkbox-customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.
- **Groepsnaam**: U kunt een naam opgeven om de groep met aangepaste eigenschappen te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **Belangrijke paren**: U kunt meerdere aangepaste eigenschapnamen en aangepaste eigenschapswaarden toevoegen door op de knop **Toevoegen** knop voor elke aangepaste groep eigenschappen.

   - **Verwijderen**: Tik of klik om de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap te verwijderen.

   - **Opnieuw rangschikken**: Tik of klik en sleep om de naam van de aangepaste eigenschap en de waarde van de aangepaste eigenschap opnieuw te rangschikken.


## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
