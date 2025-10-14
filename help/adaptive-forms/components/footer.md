---
title: Adaptieve Forms Core-component - Voettekst
description: De Adaptive Forms Footer Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: c8e7d3fe-4b82-4a80-8da2-19f6cff1e3e9
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---


# Voettekst {#footer-adaptive-forms-core-component}

Een voettekstcomponent in een adaptief formulier is een gebied dat doorgaans onder aan het formulier wordt weergegeven en dat informatie bevat zoals een copyrightkennisgeving, koppelingen naar gerelateerde bronnen of contactgegevens. Een voettekst kan aanvullende informatie bevatten, zoals de datum van de laatste update, die nuttig kan zijn voor gebruikers met toegankelijkheidsbehoeften.

{{traditional-aem}}

**Voorbeeld**

![&#x200B; voorbeeld &#x200B;](/help/adaptive-forms/assets/footer.png)

## Gebruik {#reasons-to-use-footer}

Er zijn verschillende redenen waarom het nuttig is om een voettekstcomponent in een formulier op te nemen, zoals:

- **wettelijke vereisten**: Sommige vormen kunnen worden vereist om een ontkenning, een auteursrechtbericht, of andere wettelijke informatie te omvatten. Een voettekst is een handige plaats om deze informatie op te nemen.

- **Navigatie**: Voettekst kan verbindingen aan andere belangrijke pagina&#39;s op de website, zoals een privacybeleid, termijnen van de dienst, of contactpagina verstrekken.

- **Branding**: Voettekst kan worden gebruikt om een embleem of andere brandende elementen te omvatten, die helpen de identiteit van de organisatie of website versterken.

- **Consistentie**: Voettekst verstrekt consistentie in het ontwerp en de lay-out van de vorm, die het intuïtiever en voor gebruikers gemakkelijk maken om te navigeren.

- **Extra context**: Voettekst kan extra context aan de vorm, zoals een tekst verstrekken beschrijvend de vorm of een verbinding aan verwante middelen, die tot de vorm informatief en gebruikersvriendelijker maken.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Footer Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 voor Cloud Service en Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM-compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel systeem met <br>[&#x200B; versie 2.0.4 &#x200B;](/help/adaptive-forms/version.md) en later | Compatibel met <br>[&#x200B; versie 1.1.12 &#x200B;](/help/adaptive-forms/version.md) en later maar minder dan 2.0.0. |

Voor informatie over de versies en versies van de Component van de Kern, verwijs naar het [&#128279;](/help/adaptive-forms/version.md) document van de Versies van de Componenten van de Kern 0&rbrace;.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Krijg de recentste informatie over de Aangepaste Component van de Kern van de Voettekst van Forms in de technische documentatie op [&#x200B; GitHub &#x200B;](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/footer/v1/footer). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [&#x200B; de ontwikkelaarsdocumentatie van de Componenten van de Kern &#x200B;](/help/developing/overview.md).


## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de voettekstervaring voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig voettekstopties definiëren voor een naadloze gebruikerservaring.

![&#x200B; Eigenschappen tabel &#x200B;](/help/adaptive-forms/assets/footer_propertiestab.png)

- **geef de doos van de Dialoog** uit
Het dialoogvenster Bewerken bevat standaardgereedschappen voor tekstopmaak waarmee de gebruiker tekst voor de voettekst kan maken.

- **Vet** - deze optie past vette het formatteren op geselecteerde teksten of versleten toe   formatteer tekst ingegaan na de curseur. `Ctrl+B` is een sneltoets.

- **Cursief** - deze optie past cursief het formatteren op geselecteerde teksten toe of   Tekst die na de cursor is ingevoerd cursief maken. `Ctrl+I` is een sneltoets.

![&#x200B; Opties van de Opsommingstekens &#x200B;](/help/adaptive-forms/assets/footer_bullet.png)


- **Opsommingsteken**

   - **pictogram van het Bullet** - het formatteert de geselecteerde tekst als bulleted lijst of begint de toevoeging van een bulleted lijst na de curseur. Tik of klik nogmaals op de knop Opsommingsteken of voer twee regeleinden in om een lijst met opsommingstekens te beëindigen.

   - **Genummerd lijstpictogram** - het formatteert de geselecteerde tekst als genummerde lijst of begint de toevoeging van een genummerde lijst na de curseur. Tik of klik nogmaals op de knop Genummerd om een genummerde lijst te beëindigen of voer twee regeleinden in.

   - **Uitspringen pictogram** - het vermindert het inkepingsniveau van de geselecteerde tekst of de tekst ingegaan na de curseur. Alleen actief als de geselecteerde tekst of positie van de cursor al is ingesprongen.

   - **pictogram van de Inspringing** - het verhoogt het inkepingsniveau van de geselecteerde tekst of de tekst ingegaan na de curseur.

![&#x200B; Opties van de Hyperlink &#x200B;](/help/adaptive-forms/assets/footer_link.png)

- **Hyperlink**

   - **Weg** - ga de weg in
      1. Kies een pad in AEM in het dialoogvenster Selectie openen.
      1. Als de koppeling zich niet in AEM bevindt, voert u de absolute URL in.
      1. Niet-absolute paden worden geïnterpreteerd als relatief ten opzichte van AEM.

   - **Alternatieve tekst** - ga alternatieve beschrijvende tekst voor de verbinding in.

   - **Doel** - Uitgezochte verbindingsgedrag
      - Doel
      - Zelfde tabblad
      - Nieuw tabblad
      - Bovenliggend frame
      - Bovenste frame

   - **ontkoppel pictogram** - deze optie verwijdert een verbinding die reeds op de geselecteerde tekst wordt toegepast. Deze optie is alleen actief als de koppeling al is geselecteerd.

   - **het formaatpictogram van de Paragraaf** - deze optie staat u toe om paragraaf het formatteren op de geselecteerde tekst toe te passen. Het helpt u ook om de tekst op te maken die na de curseur wordt opgenomen. Hiermee wordt het kopniveau van de titel gedefinieerd.

- **identiteitskaart**: Deze optie staat toe om het unieke herkenningsteken van de component in HTML en in de Laag van Gegevens te controleren.

   - Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. Deze kan worden gevonden door de resulterende pagina te inspecteren.
   - Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   - Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=nl-NL)

-->

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}
