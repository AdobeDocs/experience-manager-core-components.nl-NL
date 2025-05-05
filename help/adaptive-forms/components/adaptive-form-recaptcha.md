---
title: Adaptive Forms Core Component - Google reCAPTCHA
description: Verbeter de formulierbeveiliging met de Google reCAPTCHA-service zonder moeite met AEM Forms. Eigenschappen van Adaptief Form reCaptcha uitleggen
role: Architect, Developer, Admin, User
exl-id: 2d986b90-e596-4e8f-9a32-0ebced5461c8
source-git-commit: b97687e7f7437af57e2a8b9f442d4e0c8322a3d2
workflow-type: tm+mt
source-wordcount: '1325'
ht-degree: 0%

---

# Adaptief formulier reCAPTCHA {#google-recaptcha}

CAPTCHA (Complete Automated Public Turing Test to tell Computers and Humans Apart) is een programma dat veel wordt gebruikt bij online transacties om onderscheid te maken tussen mensen en geautomatiseerde programma&#39;s of bots. Het stelt een uitdaging en evalueert de reactie van de gebruiker om te bepalen of het een mens of bot is die met de site communiceert. Het verhindert de gebruiker om te werk te gaan als de test ontbreekt en de hulp maakt online transacties veilig door bots te houden spam of kwaadwillige doeleinden posten.

AEM Forms as a Cloud Service ondersteunt Google reCAPTCHA v2 in Adaptive Forms. U kunt het gebruiken om een CAPTCHA-uitdaging aan te geven bij het verzenden van formulieren

## Gebruik {#reasons-to-use-google-recaptcha}


- **Spam en Bot Preventie**: Één van de primaire redenen om reCAPTCHA te gebruiken moet spamvoorlegging en kwaadwillige bots verhinderen uw vorm te overstromen. De geavanceerde algoritmen van reCAPTCHA kunnen geautomatiseerde pogingen om het formulier te verzenden ontdekken, zodat alleen legitieme gebruikers ermee kunnen werken.

- **Verbeterde Veiligheid**: Door reCAPTCHA uit te voeren, voegt u een extra laag van veiligheid aan uw adaptieve vorm toe. Dit helpt gevoelige informatie beschermen en kwaadwillige gebruikers verhinderen kwetsbaarheid te exploiteren.

- **Ervaring van de Gebruiker**: Terwijl CAPTCHAs soms als ongemak kan worden gezien, betekent de adaptieve benadering van reCAPTCHA dat de meeste gebruikers met een gestroomlijnde, gebruikersvriendelijke ervaring worden voorgesteld die minimale interactie vereist. Dit kan helpen een positieve gebruikerservaring te behouden terwijl het afschrikken van bots.

- **Aanpassingsvermogen**: reCAPTCHA&#39;s adaptieve mechanisme analyseert gebruikersgedrag en interactie om te bepalen of zij menselijk of niet zijn. Dit betekent dat het niveau van de uitdaging die de gebruiker wordt aangeboden kan variëren afhankelijk van de waarschijnlijkheid dat hij een bot is. Dit aanpassingsvermogen vermindert de wrijving voor echte gebruikers terwijl het handhaven van sterke veiligheid.

- **Verminderde Handmatige Moderatie**: Door het aantal spambijdragen en allebei-geproduceerde inhoud beduidend te verminderen, kan reCAPTCHA tijd en middelen besparen die anders aan handmatiging en schoonmaakbeurt zouden worden uitgegeven.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Google reCAPTCHA Core Component is in augustus 2023 uitgebracht als onderdeel van de Core Components &#39;version&#39;. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:


| Componentversie | AEM as a Cloud Service |
|--- |--- |
| v1 | Compatibel systeem met <br>[ versie 2.0.4 ](/help/versions.md) en later | Compatibel | Compatibel |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het [&#128279;](/help/versions.md) document van de Versies van de Componenten van de Kern 0&rbrace;.

## Technische details {#technical-details}

Krijg de recentste informatie over de Adaptieve Component van de Kern van Forms Google reCAPTCHA in de technische documentatie op [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u uw Google reCAPTCHA-ervaring eenvoudig aanpassen voor bezoekers. U kunt eenvoudig Google reCAPTCHA-opties definiëren voor een naadloze gebruikerservaring.

### Tabblad Standaard {#basic-tab}

![ BasisLusje ](/help/adaptive-forms/assets/recaptcha-basictab.png)

- **Naam** - u kunt een vormcomponent gemakkelijk met zijn unieke naam zowel in de vorm als in de regelredacteur identificeren, maar de naam moet geen ruimten of speciale karakters bevatten.

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bovenop de component. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.

- **staat RTF voor Titel** toe - Deze eigenschappen laat gebruikers toe om gewone teksttitels te formatteren, die eigenschappen zoals vette, cursieve, onderstreepte tekst, diverse doopvonten, doopvontgrootte, kleuren, en extra optie opnemen om visuele presentatie en aanpassing te verbeteren. Deze functie biedt meer flexibiliteit en creatieve controle bij het opvallen van titels in documenten, websites of toepassingen.\
  Als u het selectievakje **RTF-tekst toestaan voor titel inschakelt, worden opmaakopties zichtbaar om de titel van de component op te maken. Om tot alle beschikbare het formatteren opties toegang te hebben, kunt u op het ![ pictogram Volledig scherm ](/help/adaptive-forms/assets/fullscreen-icon.png) tabel klikken.

  ![&#128279;](/help/adaptive-forms/assets/richtext-support-title.png) de rijke tekststeun van 0&rbrace;

- **Verberg Titel** - selecteer de optie om de Titel van de component te verbergen.
- **Teken als Niet-gebonden Element van de Vorm**: Selecteer de optie om een vormgebied te vormen niet verbonden aan om het even welk schema. Met deze optie kunt u gegevens opslaan zonder de gegevensbron bij te werken. Het laat u ook toe om gegevens op een douanemethode, los van standaardgegevensbestandintegratie te behandelen.
- **de montages van de Configuratie**: Selecteer de configuratiecontainer die de wolkenconfiguratie bevat die AEM Forms met de dienst reCAPTCHA door Google verbindt.

  >[!NOTE]
  >
  > Verwijs naar het [ Gebruik Google reCAPTCHA in een AEM Aangepaste Vorm die op het artikel van de Componenten van de Kern &lbrace;wordt gebaseerd om te leren hoe te om Google reCAPTCHA voor uw milieu tot stand te brengen en te vormen.](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

- **Type**: Kies deze optie om de grootte voor reCAPTCHA te selecteren.
   - **Normaal**: Verwijst naar de norm, grotere versie van de reCAPTCHA widget, die voor gebruikers beter zichtbaar en gemakkelijker kan zijn om met, vooral op apparaten met grotere schermen in wisselwerking te staan.
   - **Compact**: Verwijs naar een kleinere versie van de reCAPTCHA widget. Deze optie is geschikt voor situaties waarin ruimte beperkt is, zoals op mobiele apparaten of in strakke lay-outs op webpagina&#39;s.

- **de Component van de Huid** - selecteer de optie om de component van de vorm te verbergen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel. Dit is handig wanneer u informatie wilt opslaan die niet hoeft te worden bekeken of rechtstreeks door de gebruiker hoeft te worden gewijzigd.

- **maak Component** onbruikbaar - selecteer de optie om de component onbruikbaar te maken. De uitgeschakelde component is niet actief of bewerkbaar voor de eindgebruiker. De gegevens van de uitgeschakelde component worden niet verzonden De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

- **read-only** - selecteer de optie om de component niet-editable te maken. De gebruiker kan de waarde van het veld zien, maar kan deze niet wijzigen. De component blijft toegankelijk voor andere doeleinden, zoals het gebruiken voor berekeningen in de Redacteur van de Regel.

### Tabblad Validatie {#validation-tab}

![ het Lusje van de Bevestiging ](/help/adaptive-forms/assets/recaptcha-validationtab.png)

- **Bericht van de Fout** - Deze optie staat u toe om een bericht in te gaan dat wordt getoond als **Vereiste** checkbox wordt gecontroleerd en het vormgebied wordt verlaten leeg.

- **Bericht van de Bevestiging van het Manuscript** - Deze optie staat u toe om een bericht in te gaan dat moet worden getoond als de manuscriptbevestiging ontbreekt.

## Ontwerpdialoogvenster {#design-dialog}

Het dialoogvenster Ontwerpen wordt gebruikt om CSS-stijlen voor de component reCAPTCHA te definiëren en te beheren.

### Tabblad Stijlen {#styles-design-tab}

De Adaptieve Component van de Kern van Forms reCAPTCHA steunt het AEM [ Systeem van de Stijl ](/help/get-started/authoring.md#component-styling).

![ Dialoog van het Ontwerp ](/help/adaptive-forms/assets/checkbox-style.png)

- **StandaardCSS Klassen**: U kunt een standaardCSS klasse voor de Adaptieve Component van de Kern van Forms reCAPTCHA verstrekken.

- **Toegestane Stijlen**: U kunt stijlen bepalen door een naam en de CSS klasse te verstrekken die de stijl vertegenwoordigt. U kunt bijvoorbeeld een stijl met de naam &quot;vetgedrukte tekst&quot; maken en de CSS-klasse &quot;font-weight: bold&quot; opgeven. U kunt deze stijlen gebruiken of toepassen op een adaptief formulier in de Adaptieve Forms-editor. Om een stijl, in de Aanpassingsredacteur van Forms toe te passen, selecteer de component u de stijl op wilt toepassen, aan de eigenschappendialoog navigeren, en de gewenste stijl van de **drop-down lijst van Stijlen** selecteren. Als u de stijlen moet bijwerken of wijzigen, gaat u terug naar het dialoogvenster Ontwerpen, werkt u de stijlen op het tabblad Stijlen bij en slaat u de wijzigingen op.

### Aangepaste eigenschappen

![ de Dialoog van Eigenschappen van de Douane ](/help/adaptive-forms/assets/checkbox-customproperties.png)

Met aangepaste eigenschappen kunt u aangepaste kenmerken (sleutelwaardeparen) aan een Adaptief kernonderdeel van een formulier koppelen met behulp van de formuliersjabloon. De aangepaste eigenschappen worden weergegeven in de sectie Eigenschappen van de koploze uitvoering van de component. Hiermee kunt u dynamisch formuliergedrag maken dat wordt aangepast op basis van de waarden van aangepaste kenmerken. Ontwikkelaars kunnen bijvoorbeeld verschillende uitvoeringen van een Forms-component zonder koptekst ontwerpen voor mobiele apparaten, desktops of webplatforms, waardoor de gebruikerservaring op een groot aantal apparaten aanzienlijk wordt verbeterd.
- **Naam van de Groep**: U kunt een naam verstrekken om de groep van het douanebezit te identificeren. U kunt meerdere groepen met aangepaste eigenschappen toevoegen, verwijderen of opnieuw rangschikken. Nadat u de aangepaste groep eigenschappen hebt toegevoegd, kunt u de volgende opties zien:

   - **zeer belangrijk-Waarde paren**: U kunt veelvoudige namen van het douanebezit en douanebezitswaarden toevoegen door **te klikken voegt** knoop voor elke groep van het douanebezit toe.

   - **Schrapping**: Tik of klik om de naam van het douanebezit en de waarde van het douanebezit te schrappen.

   - **herschikt**: Tik of klik en sleep om de naam van het douanebezit en de waarde van het douanebezit te herschikken.


## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
