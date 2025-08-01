---
title: E-mailtekstcomponent
description: De component E-mailtekst is een component voor tekstbewerking en -compositie met tekstopmaak die op locatie kan worden bewerkt.
role: Architect, Developer, Admin, User
exl-id: 4aa192f6-8314-40e7-8732-c6626d647986
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: tm+mt
source-wordcount: '2264'
ht-degree: 0%

---


# E-mailtekstcomponent {#email-text-component}

De component E-mailtekst is een component voor tekstbewerking en -compositie met tekstopmaak die op locatie kan worden bewerkt.

## Gebruik {#usage}

De component E-mailText biedt een robuuste teksteditor met tekstopmaak die het bewerken van tekst in een vereenvoudigde, online editor en in een volledige schermopmaak mogelijk maakt.

* Het [ geeft dialoog ](#edit-dialog) eigenschappen in-lijn uit het uitgeven met beperkte opties met volledige functionaliteit beschikbaar in het volledig scherm uitgeeft dialoog.
* Gebruikend de [ ontwerpdialoog, ](#design-dialog) tekst het formatteren opties zoals rubrieken, speciale karakters, en paragraafstijlen kunnen voor het malplaatje voor de inhoudauteur worden gevormd.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de E-mailtekstcomponent is v1, die in oktober 2022 is geïntroduceerd met release X van de Email Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel | - | - |

Voor meer informatie over de versies en de versies van de Component van de Kern, zie het document [ e-mailVersie van de Componenten van de Kern.](/help/email/versions.md)

### Technische details {#technical-details}

De recentste technische documentatie over de Component van de Tekst E-mail [ kan op GitHub ](https://adobe.com/go/aem_cmp_tech_email_text_v1) worden gevonden.

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden ](/help/developing/overview.md).

## De component E-mailtekst en de RTF-editor {#the-text-component-and-the-rich-text-editor}

De component Email Text gebruikt de AEM Rich Text Editor (RTE). RTE voorziet inhoudsauteurs van een brede waaier van functionaliteit voor het uitgeven van hun tekstinhoud. RTE is flexibel in zijn configuratie en biedt een aantal opties aan. Verdere details over hoe RTE kan worden gevormd kunnen in de artikelen [ worden gevonden vormen de Rijke Redacteur van de Tekst ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/rich-text-editor.html?lang=nl-NL) en [ vormen de Rijke stop-ins van de Redacteur van de Tekst ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html?lang=nl-NL).

De rest van dit document demonstreert de standaardconfiguratie van de component E-mailText met de uit-van-de-doos configuratie van RTE.

>[!NOTE]
>
>Slechts die opties door [ worden toegelaten UI configuraties van RTE ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html?lang=nl-NL) zijn beschikbaar in de Component van de Tekst E-mail.

## Dialoogvenster Bewerken {#edit-dialog}

![ de Edit dialoog van de Component van de Tekst ](/help/email/assets/email-text-edit.png)

### Opmaakopties {#options}

Het dialoogvenster Bewerken bevat de standaardgereedschappen voor tekstopmaak die een gebruiker zou verwachten bij het samenstellen van tekst.

#### Vet

![ Vet pictogram ](/help/assets/text-bold.png)

Wordt gebruikt om vette opmaak toe te passen op geselecteerde tekst of opgemaakte tekst die na de cursor wordt ingevoerd.

**Ctrl+B** kan als toetsenbordkortere weg worden gebruikt.

#### Cursief

![ Cursief pictogram ](/help/assets/text-italic.png)

Wordt gebruikt om cursieve opmaak toe te passen op geselecteerde tekst of om tekst die na de cursor wordt ingevoerd, cursief te maken.

**Ctrl+I** kan als toetsenbordkortere weg worden gebruikt.

#### Onderstrepen

![ onderstreepte pictogram ](/help/assets/text-underline.png)

Wordt gebruikt om onderstreepte opmaak toe te passen op geselecteerde tekst of onderstreepte tekst die na de cursor wordt ingevoerd.

**Ctrl+U** kan als toetsenbordkortere weg worden gebruikt.

#### Subscript

![ Subscript pictogram ](/help/assets/text-subscript.png)

Wordt gebruikt om geselecteerde tekst of tekst die na de cursor is ingevoerd, op te maken als een subscript.

#### Superscript

![ pictogram Superscript ](/help/assets/text-superscript.png)

Hiermee maakt u geselecteerde tekst of tekst die na de cursor is ingevoerd, op als superscript.

#### Plakken als tekst

![ Deeg als tekstpictogram ](/help/assets/text-paste-text.png)

Hiermee plakt u alle gekopieerde tekst als onbewerkte tekst zonder opmaak.

Wanneer u deze optie selecteert, wordt een venster geopend waarin de tekst als onbewerkte tekst zonder opmaak kan worden geplakt als een voorvertoning voordat deze in de tekst wordt ingevoegd. Accepteren door te tikken of op het vinkje te klikken, annuleren door te tikken of op de x te klikken.

![ Deeg als tekstvoorbeeld ](/help/assets/text-paste-text-example.png)

#### Plakken vanuit Word

![ Deeg van het pictogram van Word ](/help/assets/text-paste-word.png)

Als u deze optie selecteert, wordt een venster geopend waarin de tekst kan worden geplakt met behoud van de opmaak als voorbeeld voordat deze in de tekst wordt ingevoegd. Accepteren door te tikken of op het vinkje te klikken, annuleren door te tikken of op de x te klikken.

![ Deeg van het voorbeeld van Word ](/help/assets/text-paste-word-example.png)

#### Hyperlink

![ pictogram van de Hyperlink ](/help/assets/text-hyperlink.png)

Met deze optie kunt u de geselecteerde tekst omzetten in een hyperlink of een reeds gedefinieerde koppeling wijzigen. Met deze optie opent u een venster met aanvullende opties voor het instellen van de koppeling.

![ voorbeeld van de Hyperlink ](/help/assets/text-hyperlink-example.png)

* Het pad invoeren
   * Gebruik de **Open dialoog van de Selectie** om een weg in AEM te kiezen
   * Als de koppeling zich niet in AEM bevindt, voert u de absolute URL in
      * Niet-absolute paden worden geïnterpreteerd als relatief ten opzichte van AEM
* Alternatieve beschrijvende tekst voor de koppeling invoeren
* Koppelingsgedrag selecteren
   * Doel
   * Zelfde tabblad
   * Nieuw tabblad
   * Bovenliggend frame
   * Bovenste frame

Tik of klik op het vinkje om de koppeling toe te passen of klik op de x om te annuleren.

#### Ontkoppelen

![ pictogram van de Ontkoppeling ](/help/assets/text-unlink.png)

Gebruik deze optie om een koppeling te verwijderen die al op de geselecteerde tekst is toegepast. Deze optie is alleen actief als er al een koppeling is geselecteerd.

#### Anker {#anchor}

![ pictogram van het Anker ](/help/email/assets/anchor.png)

Gebruik deze optie om een anker in de tekst in te voegen.

#### Zoeken

![ het pictogram van de Vondst ](/help/assets/text-find.png)

Met deze optie kunt u de tekst doorzoeken op een opgegeven tekstreeks. Als u deze optie selecteert, wordt een venster geopend waarin u de zoekopties kunt opgeven.

![ vind voorbeeld ](/help/assets/text-find-example.png)

Ga de tekst in waarvoor u wilt zoeken en tikken of **Vondst** klikken om met het onderzoek te beginnen. Tik of klik op de x om te annuleren.
Als u wenst om een nauwkeurige gelijke volgens het geval te doen, selecteer de optie **Geval van de Gelijke** alvorens het onderzoek te beginnen.
Als een overeenkomst wordt gevonden, wordt deze gemarkeerd en wordt het zoekdialoogvenster gedimd weergegeven. Tik of klik opnieuw de **Vondst** knoop in de gedimde dialoog om naar het volgende voorkomen te zoeken.

![ gevonden voorbeeld van de Vondst ](/help/assets/text-find-example-found.png)

Als er geen andere exemplaren worden gevonden, wordt een bericht weergegeven en wordt de zoekopdracht opnieuw gestart vanaf het begin van de tekst.

![ vind voorbeeld niet meer voorkomen ](/help/assets/text-find-example-found-end.png)

#### Vervangen

![ vervang pictogram ](/help/assets/text-replace.png)

Gebruik deze optie om de tekst te zoeken op instanties van een opgegeven tekenreeks en de overeenkomsten te vervangen door een andere tekenreeks. Als u deze optie selecteert, wordt een venster geopend waarin u de opties voor zoeken en vervangen kunt opgeven.

![ vervangt voorbeeld ](/help/assets/text-replace-example.png)

Voer de tekst in waarnaar u wilt zoeken en de tekst waarmee u deze wilt vervangen.

* Tik of klik **Vondst** om met het onderzoek te beginnen. Klik of tik op de x om te annuleren.
* Als u wenst om een nauwkeurige gelijke volgens het geval te doen, selecteer de optie **Geval van de Gelijke** alvorens het onderzoek te beginnen.
* Selecteer **vervangen allen** om alle voorkomen van de tekst in één keer te vervangen.

Als een overeenkomst wordt gevonden, wordt deze gemarkeerd en wordt het zoekdialoogvenster gedimd weergegeven. Klik opnieuw de **Vondst** knoop in de gedimde dialoog om naar het volgende voorkomen te zoeken of **te selecteren vervang** knoop om de benadrukte, aangepaste tekst te vervangen. De **vervangt** knoop is slechts actief zodra een gelijke wordt gemaakt.

Het dialoogvenster Zoeken en vervangen wordt transparant wanneer op Zoeken wordt geklikt en wordt dekkend wanneer op Vervangen wordt geklikt. Hierdoor kan de auteur de tekst controleren die de auteur vervangt.

>[!NOTE]
>
>Wanneer u de vervangingsfunctie gebruikt, moet de te vervangen tekenreeks op hetzelfde tijdstip worden ingevoerd als de te zoeken tekenreeks. U kunt echter nog steeds op Zoeken klikken om de tekenreeks te zoeken voordat u deze vervangt. Als de vervangingstekenreeks wordt ingevoerd nadat op Zoeken is geklikt, wordt de zoekopdracht opnieuw ingesteld op het begin van de tekst.

#### Ongedaan maken

![ ongedaan maken pictogram ](/help/email/assets/undo.png)

Wordt gebruikt om de laatste bewerking in de RTF-editor ongedaan te maken.

#### Opnieuw

![ opnieuw pictogram ](/help/email/assets/redo.png)

Wordt gebruikt om een ongedaan gemaakte bewerking ongedaan te maken met het pictogram Ongedaan maken.

#### Tekst links uitlijnen

![ richt linkerpictogram ](/help/assets/text-left.png) uit

Wordt gebruikt om de tekst uit te lijnen met de linkermarge.

#### Tekst centreren

![ de tekstpictogram van het Centrum ](/help/assets/text-center.png)

Hiermee centreert u de tekst.

#### Tekst rechts uitlijnen

![ richt rechts pictogram ](/help/assets/text-right.png) uit

Wordt gebruikt om de tekst uit te lijnen met de rechtermarge.

#### Opsommingsteken

![ pictogram van het Bullet ](/help/assets/text-bullet.png)

Wordt gebruikt om de geselecteerde tekst op te maken als een lijst met opsommingstekens of om te beginnen met het invoegen van een lijst met opsommingstekens na de cursor.

Om een bulleted lijst te eindigen, onttikt of klikt opnieuw de **knoop van de Opsommingsteken** of gaat twee vervoerterugkeer in.

#### Genummerd

![ Genummerd lijstpictogram ](/help/assets/text-numbered.png)

Hiermee maakt u de geselecteerde tekst op als een genummerde lijst of begint u met het invoegen van een genummerde lijst na de cursor.

Om een genummerde lijst te beëindigen, de **Genummerde** knoop te onttikken of te klikken opnieuw of twee vervoerterugkeer in te gaan.

#### Uitspringen

![ pictogram Uitspringen ](/help/assets/text-outdent.png)

Wordt gebruikt om het inspringingsniveau te verlagen van de geselecteerde tekst of tekst die na de cursor wordt ingevoerd.

Alleen actief als de geselecteerde tekst of positie van de cursor al is ingesprongen.

#### Inspringen

![ Inspringen pictogram ](/help/assets/text-indent.png)

Wordt gebruikt om het inspringingsniveau te verhogen van de geselecteerde tekst of tekst die na de cursor wordt ingevoerd.

#### Tabel

![ pictogram van de Lijst ](/help/assets/text-table.png)

Wordt gebruikt om een tabel in de tekst in te voegen. Als u deze optie selecteert, wordt een venster geopend waarin u de details van de tabel kunt opgeven.

![ Voorbeeld van de Lijst ](/help/assets/text-table-example.png)

* **Kolommen** - het aantal kolommen van de (vereiste) lijst
* **Rijen** - het aantal rijen van de (vereiste) lijst
* **Breedte** - de breedte van de lijst
* **Hoogte** - de hoogte van de lijst
* **het opvullen van de Cel** - de ruimte rond de celinhoud
* **het uit elkaar plaatsen van de Cel** - de ruimte tussen cellen
* **Grens** - het gewicht van de grenslijnen van de lijst
   * Indien voor de koptekst van de tabel:
      * Gebruik de eerste rij
      * Gebruik de eerste kolom
      * Gebruik de eerste rij en de eerste kolom
      * Of er moet geen header worden gebruikt.
* **Titel** - de titel van de lijst

#### Afbeelding

![ pictogram van het Beeld ](/help/email/assets/image-icon.png)

Wordt gebruikt om een ingevoegde afbeelding uit te lijnen.

#### Spellingcontrole

![ het Spellingspictogram van de Controle ](/help/assets/text-spellcheck.png)

Wordt gebruikt om de spelling van de tekstinhoud te controleren. Mogelijke spelfouten worden onderstreept met gebroken, rode lijnen.

De verdere details over spellingcontrole en het aanpassen van de woordenboeken van de spellingcontrole kunnen in het document [ worden gevonden vormen de Rich Insteekmodules van de Redacteur van de Tekst ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html?lang=nl-NL).

#### Speciale tekens {#special-characters}

![ het Speciale karakterpictogram ](/help/assets/text-special-characters.png)

Wordt gebruikt om speciale tekens in te voegen in de tekst. Als u deze optie selecteert, wordt een venster geopend waarin de beschikbare tekens worden weergegeven.

![ Speciaal karaktervoorbeeld ](/help/assets/text-special-characters-example.png)

Tik op het gewenste teken of klik op het gewenste teken om het teken na de cursor in te voegen in de tekst. U kunt meerdere tekens invoegen. Tik of klik op de x om het selectievenster te sluiten.

#### Source Edit

![ Source geeft pictogram uit ](/help/assets/text-source.png)

Wordt gebruikt om de HTML-bron van de tekst weer te geven en te wijzigen.

Tik of klik **Source geeft** pictogram uit om de inhoud van de tekst van de geformatteerde mening te veranderen om ruwe HTML te bekijken. In deze modus zijn alle andere opmaakopties uitgeschakeld. Tik of klik **Source geeft** opnieuw pictogram uit om aan de geformatteerde mening terug te keren.

>[!CAUTION]
>
>Zoals altijd het geval met toegang tot ruwe HTML, moet de zorg worden uitgeoefend wanneer het gebruiken van **Source geeft** optie uit!
>
>HTML ingegaan via **Source geeft** uit wordt gescand voor XSS risico&#39;s en om het even welke manuscripten die worden opgenomen worden verwijderd en zullen niet op de resulterende pagina verschijnen. Nochtans misvormde HTML ingegaan in **Source geeft** uit kan het malplaatje voor de pagina breken die in onverwachte het formatteren of het teruggeven van de resulterende pagina onbruikbaar maken.

>[!NOTE]
>
>Omdat HTML binnenging via **Source geeft** uit wordt gescand voor XSS risico&#39;s en om het even welke manuscripten en verwijdert automatisch die gevonden, kan de daadwerkelijke inhoud voortgeduurd variëren van wat in **Source uitgeeft** was ingegaan. Om deze reden, om aangebrachte veranderingen te bewaren gebruikend **Source geeft** uit, moet u **Source eerst weggaan uitgeven** om de tekst in de normale redacteur te bekijken alvorens op te slaan.

#### Alineaopmaak

![ het formaatpictogram van de Paragraaf ](/help/assets/text-paragraph.png)

Wordt gebruikt om alineaopmaak toe te passen op de geselecteerde tekst of op tekst die na de cursor wordt ingevoegd. Als u deze optie selecteert, wordt een vervolgkeuzelijst geopend waarin de alineaopmaak wordt geselecteerd.

![ het formaatvoorbeeld van de Paragraaf ](/help/assets/text-paragraph-example.png)

#### Adobe Campaign-variabele selecteren

![ Uitgezochte Adobe Campaign veranderlijk pictogram ](/help/email/assets/select-adobe-campaign-variable-icon.png)

Opent de [ Uitgezochte Variabele van Adobe Campaign ](/help/email/campaign-variables.md) dialoog om dynamische inhoud van Adobe Campaign op te nemen.

### In-line bewerking {#in-line-editing}

De tekstcomponent kan ook online worden bewerkt. Als u online wilt bewerken, selecteert u de component E-mailtekst op de inhoudspagina.

![ Uitgezochte component van de Tekst E-mail ](/help/email/assets/email-text-select-component.png)

Dan tik of klik **uitgeven** pictogram op de toolbar die over de component omhoog springt. De toolbar verandert om beperkte tekst het formatteren opties (met inbegrip van toegang tot de **Uitgezochte Variabele van Adobe Campaign** optie) te tonen en u kunt de tekst in-lijn uitgeven.

![ In-lijn geeft voorbeeld uit ](/help/email/assets/email-text-edit-inline-example.png)

Tik of klik op het vinkje op de werkbalk om de wijzigingen op te slaan of klik op de X om de wijzigingen te verwijderen.

Vanwege ruimtebeperkingen zijn niet alle opmaakopties online beschikbaar. Schakel over naar de modus Volledig scherm om alle opties weer te geven.

### Een id instellen {#setting-id}

Met deze optie kunt u de unieke id van de component in het HTML-bestand bepalen.

* Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
* Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
* Het wijzigen van de id kan gevolgen hebben voor CSS.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur definiëren welke tekstopmaakopties beschikbaar zijn voor de auteurs van de inhoud.

### Tabblad Plugins {#plugins-tab}

Het **lusje van Insteekmodules** wordt gebruikt om diverse tekst toe te laten en onbruikbaar te maken formatterend opties beschikbaar aan de inhoudsauteurs.

### Functies {#features}

![ de dialoogeigenschappen van het Ontwerp ](/help/assets/text-design-features.png)

De volgende functies kunnen voor de component worden geactiveerd of gedeactiveerd.

* Onbewerkte tekst plakken
* Plakken van woord
* Zoeken en vervangen
* Ongedaan maken en opnieuw uitvoeren
* Spellingcontrole
* Opties voor het wijzigen van ingevoegde afbeeldingen
* HTML-bronbewerking

### Opmaak {#formatting}

![ de dialoog van het Ontwerp het formatteren ](/help/assets/text-design-formatting.png)

De volgende opmaakopties kunnen voor de component worden geactiveerd of gedeactiveerd.

* Tabel
* Lijsten (opsommingsteken, nummer, inspringing, inspringing)
* Uitlijning (links, rechts, gecentreerd)
* Vet, cursief, onderstrepen
* Koppelen (en ontkoppelen)
* Sub/superscript

### Alineastijlen {#paragraph-styles}

![ de dialoogdoos van het Ontwerp alineastijlen ](/help/assets/text-design-paragraph.png)

Alineastijlen kunnen voor de component worden geactiveerd of gedeactiveerd. Als deze optie is geactiveerd, kunnen de toegestane indelingen worden gedefinieerd.

* Tik of klik **voeg** knoop toe om een nieuwe stijl op te nemen.
* Voer de code in van de stijl en een beschrijving die worden weergegeven in het dialoogvenster Bewerken.
* Om een stijl te verwijderen, tik of klik de **knoop van de Schrapping**.
* Tik op de handgrepen of sleep deze om de volgorde van de indelingen te wijzigen.

### Speciale tekens {#configuring-special-characters}

![ de dialoog van het Ontwerp speciale karakters ](/help/assets/text-design-special-characters.png)

De optie voor het invoegen van speciale tekens kan voor de component worden geactiveerd of gedeactiveerd. Als deze optie is geactiveerd, kunnen de toegestane tekens worden gedefinieerd.

* Tik of klik **voeg** knoop toe om een nieuw karakter op te nemen.
* Voer de HTML-code in van het teken en een beschrijving die wordt weergegeven in het dialoogvenster Bewerken.
* Om een karakter te verwijderen, tik of klik de **knoop van de Schrapping**.
* Als u de volgorde van de tekens wilt wijzigen, tikt u of klikt u en sleept u de handgrepen.

## Tabblad Stijlen {#styles-tab}

De component van de Tekst E-mail steunt het de stijlsysteem van AEM [&#128279;](/help/get-started/authoring.md#component-styling).
