---
title: Adaptieve Forms Core-component - Voettekst
description: De Adaptive Forms Footer Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
exl-id: c8e7d3fe-4b82-4a80-8da2-19f6cff1e3e9
source-git-commit: 7888cfa0f1358ce8018fc1e3cc3b19eb66a82b9d
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Voettekst {#footer-adaptive-forms-core-component}

Een voettekstcomponent in een adaptief formulier is een gebied dat doorgaans onder aan het formulier wordt weergegeven en dat informatie bevat zoals een copyrightkennisgeving, koppelingen naar gerelateerde bronnen of contactgegevens. Een voettekst kan aanvullende informatie bevatten, zoals de datum van de laatste update, die nuttig kan zijn voor gebruikers met toegankelijkheidsbehoeften.

**Voorbeeld**

![](/help/adaptive-forms/assets/footer.png)

## Gebruik {#reasons-to-use-footer}

Er zijn verschillende redenen waarom het nuttig is om een voettekstcomponent in een formulier op te nemen, zoals:

* **Wettelijke vereisten**: Sommige formulieren moeten mogelijk een disclaimer, copyrightvermelding of andere juridische informatie bevatten. Een voettekst is een handige plaats om deze informatie op te nemen.

* **Navigatie**: Een voettekst kan koppelingen bevatten naar andere belangrijke pagina&#39;s op de website, zoals een privacybeleid, servicevoorwaarden of contactpagina.

* **Branding**: Een voettekst kan worden gebruikt om een logo of andere brandingelementen op te nemen, waardoor de identiteit van de organisatie of website wordt versterkt.

* **Consistentie**: Een voettekst biedt consistentie in het ontwerp en de indeling van het formulier, waardoor het intuïtiever wordt en gebruikers gemakkelijk door het formulier kunnen navigeren.

* **Aanvullende context**: Een voettekst kan een extra context voor het formulier bieden, zoals een tekst die het formulier beschrijft of een koppeling naar gerelateerde bronnen, waardoor het formulier informatiever en gebruiksvriendelijker wordt.

## Versie en compatibiliteit {#version-and-compatibility}

De Adaptive Forms Accordion Core Component is in februari 2023 uitgebracht als onderdeel van Core Components 2.0.4 for Cloud Service and Core Components 1.1.12 voor AEM 6.5.16.0 Forms of hoger. Hier volgt een tabel met alle ondersteunde versies, AEM compatibiliteit en koppelingen naar de bijbehorende documentatie:

| Componentversie | AEM as a Cloud Service | AEM 6.5.16.0 Forms of hoger |
|---|---|---|
| v1 | Compatibel met<br>[versie 2.0.4](/help/adaptive-forms/version.md) en hoger | Compatibel met<br>[release 1.1.12](/help/adaptive-forms/version.md) en later, maar minder dan 2.0.0. |

Raadpleeg voor meer informatie over versies en releases van de Core Component de [Core Components-versies](/help/adaptive-forms/version.md) document.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Technische details {#technical-details}

Lees de nieuwste informatie over de Adaptive Forms Footer Core Component in de technische documentatie over [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/footer/v1/footer). Raadpleeg de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).


## Dialoogvenster configureren {#configure-dialog}

Met het dialoogvenster Configureren kunt u de voettekstervaring voor bezoekers eenvoudig aanpassen. U kunt ook eenvoudig voettekstopties definiëren voor een naadloze gebruikerservaring.

![Eigenschappen, tabblad](/help/adaptive-forms/assets/footer_propertiestab.png)

* **Dialoogvenster Bewerken**
Het dialoogvenster Bewerken bevat standaardgereedschappen voor tekstopmaak waarmee de gebruiker tekst voor de voettekst kan maken.

* **Vet** - Met deze optie past u vette opmaak toe op geselecteerde tekst of opgemaakte tekst die na de cursor wordt ingevoerd. `Ctrl+B` is een sneltoets.

* **Cursief** - Met deze optie wordt cursieve opmaak toegepast op geselecteerde tekst of cursieve tekst die na de cursor wordt ingevoerd. `Ctrl+I` is een sneltoets.

![Opties voor opsommingstekens](/help/adaptive-forms/assets/footer_bullet.png)


* **Opsommingsteken**

   * **Pictogram opsommingsteken** - De geselecteerde tekst wordt opgemaakt als een lijst met opsommingstekens of er wordt begonnen met het invoegen van een lijst met opsommingstekens na de cursor. Tik of klik nogmaals op de knop Opsommingsteken of voer twee regeleinden in om een lijst met opsommingstekens te beëindigen.

   * **Pictogram Genummerde lijst** - De geselecteerde tekst wordt opgemaakt als een genummerde lijst of er wordt begonnen met het invoegen van een genummerde lijst na de cursor. Tik of klik nogmaals op de knop Genummerd om een genummerde lijst te beëindigen of voer twee regeleinden in.

   * **Pictogram Uitspringen** - Hiermee verlaagt u het inspringingsniveau van de geselecteerde tekst of tekst die u na de cursor invoert. Alleen actief als de geselecteerde tekst of positie van de cursor al is ingesprongen.

   * **Pictogram Inspringen** - Hiermee verhoogt u het inspringingsniveau van de geselecteerde tekst of tekst die u na de cursor invoert.

![Hyperlinkopties](/help/adaptive-forms/assets/footer_link.png)

* **Hyperlink**

   * **Pad** - Voer het pad in
      1. Kies in het dialoogvenster Selectie openen een pad in AEM.
      1. Als de koppeling zich niet binnen AEM bevindt, voert u de absolute URL in.
      1. Niet-absolute paden worden geïnterpreteerd als relatief ten opzichte van AEM.

   * **Alternatieve tekst** - Voer alternatieve beschrijvende tekst in voor de koppeling.

   * **Doel** - Koppelingsgedrag selecteren
      * Doel
      * Zelfde tabblad
      * Nieuw tabblad
      * Bovenliggend frame
      * Bovenste frame

   * **Pictogram Ontkoppelen** - Met deze optie verwijdert u een koppeling die al op de geselecteerde tekst is toegepast. Deze optie is alleen actief als de koppeling al is geselecteerd.

   * **Pictogram Alineaopmaak** - Met deze optie kunt u alineaopmaak toepassen op de geselecteerde tekst. Het helpt u ook om de tekst op te maken die na de curseur wordt opgenomen. Hiermee wordt het kopniveau van de titel gedefinieerd.

* **ID**: Met deze optie kunt u de unieke id van de component bepalen in de HTML en in de gegevenslaag.

   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. Deze kan worden gevonden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

## Verwante artikelen {#related-article}

* [Een adaptief formulier maken in AEM Sites Page of Experience Fragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

* [Een zelfstandig adaptief formulier maken](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)
