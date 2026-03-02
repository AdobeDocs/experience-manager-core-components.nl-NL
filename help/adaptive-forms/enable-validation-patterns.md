---
title: Validatiepatronen voor tekstinvoer inschakelen en gebruiken in Adobe Experience Manager Adaptive Forms
description: Leer hoe u sjabloonbeleid configureert om validatiepatronen zoals telefoonnummers, sociale-zekerheidsnummers en postcodes beschikbaar te maken en deze vervolgens te gebruiken in uw Adaptieve Forms.
hide: true
hidefromtoc: true
source-git-commit: 1ac3d987337f8279e762ab5357d32bb732dea0be
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---


# Validatiepatronen voor tekstinvoer inschakelen en gebruiken in Adobe Experience Manager Adaptive Forms

## Overzicht

In Adobe Experience Manager (Adobe Experience Manager) Forms worden specifieke validatie-indelingen (zoals burgerservicenummers, e-mailadressen of ZIP-codes) voor de componenten Tekstinvoer beheerd op het niveau Sjabloonbeleid. In deze handleiding wordt uitgelegd hoe u:

1. Open de sjablooneditor en configureer het beleid van de component Tekstinvoer om validatiepatronen beschikbaar te maken.
2. Maak een adaptief formulier en pas die validatiepatronen toe op een component Text Input.

## Vereisten

- Toegang tot een Adobe Experience Manager-instantie met Forms ingeschakeld.
- Machtigingen om sjablonen te bewerken (maken gewoonlijk deel uit van de `template-authors` -groep).
- Machtigingen voor het maken en bewerken van adaptieve Forms.

## Deel 1: Validatiepatronen inschakelen in de sjabloon

>[!VIDEO](https://video.tv.adobe.com/v/3480390/)

### Stap 1: Toegang tot de Sjabloonconsole

1. Van het scherm van het Huis van Adobe Experience Manager, klik **Hulpmiddelen** (het hamerpictogram) in linkerzijbalk.
2. Navigeer aan **Algemeen > Malplaatjes**.
3. Selecteer de map met uw projectsjablonen (bijvoorbeeld Core Components Examples).
4. Zoek de specifieke sjabloon die u wilt wijzigen (bijvoorbeeld AF Blanco) en selecteer deze.
5. Klik **uitgeven** (of open direct het malplaatje).

### Stap 2: Toegang tot de structuur van de component

1. Verzeker u in de **mening van de Structuur** (uitgezochte &quot;Structuur&quot;van de wijzendrijver in het hoogste recht indien nodig) bent.
2. Bepaal de plaats van de belangrijkste **Container van de Lay-out** of de specifieke container waar uw component van de Input van de Tekst wordt toegestaan.
3. Klik op de container om de lijst met toegestane componenten weer te geven.
4. Vind de **component van de Doos van de Tekst van de Vorm Adaptieve** in de lijst.
5. Klik het **pictogram van het Beleid** (dat door een dossier/ladersymbool wordt vertegenwoordigd) naast de componentennaam.

### Stap 3: Het beleid voor de tekstinvoercomponent configureren

1. In de beleidsredacteur, klik het **Formaten** lusje op de rechterkant van het venster.
2. Er wordt een lijst met beschikbare validatiepatronen weergegeven. Schakel de selectievakjes in voor de indelingen die u wilt inschakelen:
   - Telefoonnummer
   - Sociale verzekeringsnummer
   - Alfanumeriek e-mailen
   - Postcode

### Stap 4: Definieer en sla het beleid op

1. De schakelaar terug naar het **Beleid** lusje (of controleer de linker montages).
2. Op het **gebied van de Titel van het Beleid 0} {, ga een duidelijke naam (bijvoorbeeld, `new-textinput-default-policy`) in.**
3. Klik **Gedaan** (controleteken) pictogram in de hoogste juiste hoek om uw veranderingen te bewaren.

## Deel 2: Een formulier maken en Validatiepatronen gebruiken

Nu validatiepatronen zijn ingeschakeld in de sjabloon, kunt u een adaptief formulier maken en dit toepassen op de componenten van Tekstinvoer.

>[!VIDEO](https://video.tv.adobe.com/v/3480391/)

### Stap 1: Een adaptief formulier maken

1. Navigeer aan **Forms &amp; de interface van Documenten**.
2. Klik **creëren** knoop in de hoogste juiste hoek.
3. Selecteer **Aangepaste Vorm** van de dropdown opties.
4. Kies het malplaatje waar u de bevestigingspatronen (bijvoorbeeld, **Lege**) toeliet en **daarna** klikt.
5. Op het Add scherm van Eigenschappen:
   - Ga a **Titel** voor uw vorm (bijvoorbeeld, &quot;testPolicy&quot;) in. Het **gebied van de Naam** {automatisch-bevolkt gebaseerd op de titel.
   - Verzeker de correcte **Bibliotheek van de Cliënt van het Thema** wordt geselecteerd (bijvoorbeeld, `adaptiveform.theme.canvas3`).
6. Klik **creëren**. Er verschijnt een succesbericht.
7. Klik **uitgeven** om de vorm in de redacteur te openen.

### Stap 2: Een component Tekstinvoer toevoegen

1. In de vormredacteur, bepaal de plaats van **van Componenten** browser in linkerzijbalk.
2. Gebruik de onderzoeksbar om de **Aangepaste component van de Doos van de Tekst van de Vorm te vinden**. Als u &quot;text&quot; typt, wordt de lijst gefilterd.
3. Klik en sleep de **component van de Doos van de Tekst van de Vorm van 0} de Aanpassings op het belangrijkste canvasgebied.**

### Stap 3: Component-opmaak configureren

1. Klik op de onlangs toegevoegde **component van de Invoer van de Tekst** om het te selecteren.
2. Klik **vormen** pictogram (dat door een moersleutel wordt vertegenwoordigd) in de toolbar die boven de component verschijnt.
3. In de eigenschappendialoog, navigeer aan **Formaten** tabel.
4. Bepaal de plaats van het **Type** dropdown menu en verander de selectie in **Aantal van de Telefoon** (of een ander toegelaten formaat).

### Stap 4: Gegevensvalidatie configureren

1. Terwijl nog in de dialoog van de componentenconfiguratie, navigeer aan de **Bevestiging** tabel.
2. Bepaal de plaats van de **sectie van het Patroon van de Bevestiging**.
3. Klik het **Type** dropdown menu.
4. Selecteer **Aantal van de Telefoon** van de lijst van bevestigingspatronen. Op deze manier zorgt u ervoor dat het formulier een fout genereert als de gebruiker tekst invoert die niet overeenkomt met een geldige telefoonnummerindeling.
5. Klik **Gedaan** (controleteken) pictogram in het hoogste recht van de dialoogdoos om uw veranderingen te bewaren.

## Verificatie

Controleren of validatiepatronen correct werken:

1. Geef een voorbeeld van het formulier weer in de editor.
2. Ga testgegevens in de **component van de Input van de Tekst 0} in.**
3. Bevestig dat:
   - De ingeschakelde validatiepatronen worden weergegeven op de tabbladen Indelingen en Validatie van de component.
   - Ongeldige invoer activeert de juiste foutberichten.
   - Geldige invoer wordt zonder fouten geaccepteerd.

## Problemen oplossen

- **Uitgave:** de bevestigingspatronen verschijnen niet in de vormcomponent.
   - **Oplossing:** zorg ervoor dat het malplaatjebeleid correct werd bewaard en dat u het correcte malplaatje wanneer het creëren van de vorm gebruikt.

- **Uitgave:** Onbekwaam om tot de malplaatjeredacteur toegang te hebben.
   - **Oplossing:** verifieer dat u de noodzakelijke toestemmingen hebt om malplaatjes (lidmaatschap in de `template-authors` groep uit te geven).

- **Uitgave:** de component van de Input van de Tekst bevestigt correct input.
   - **Oplossing:** controleer de montages van het bevestigingspatroon in het lusje van de Bevestiging van de component opnieuw en zorg ervoor het correcte patroon wordt geselecteerd.

## Volgende stappen

Nadat u validatiepatronen voor tekstinvoer hebt ingeschakeld en gebruikt in uw Adobe Experience Manager Adaptive Forms:

- Aanvullende validatiepatronen configureren voor andere gegevenstypen.
- Onderzoek andere componentenbeleid om vormgedrag aan te passen.
- Stel de verwerking van formulieren en logica voor gegevensverwerking in.
