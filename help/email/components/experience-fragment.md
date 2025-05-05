---
title: E-mailervaringsfragmentcomponent
description: Met de E-mailervaringsfragmentcomponent kan de auteur van de inhoud een Experience-fragmentvariatie in de inhoud plaatsen en een gelokaliseerde inhoudsstructuur ondersteunen.
role: Architect, Developer, Admin, User
exl-id: 861c1fd1-6d6d-426c-a338-a558326fe16e
source-git-commit: 91969e4956bef1a511b8d588d5290a7999bf86ec
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---


# E-mailervaringsfragmentcomponent {#email-experience-fragment-component}

Met de E-mailervaringsfragmentcomponent kan de auteur van de inhoud een Experience-fragmentvariatie in de inhoud plaatsen en een gelokaliseerde inhoudsstructuur ondersteunen.

## Gebruik {#usage}

Met de E-mailervaringsfragmentcomponent kan de auteur van de inhoud bestaande Experience-fragmentvariaties selecteren en deze in de inhoud plaatsen. Een ervaringsfragment is een groep inhoud die zowel inhoud als lay-out bevat en die via kanalen opnieuw kan worden gebruikt.

* De eigenschappen van de component kunnen in [ worden bepaald vormen dialoog ](#configure-dialog).
* De gebreken voor de component wanneer het toevoegen van het aan inhoud kunnen in de [ ontwerpdialoog ](#design-dialog) worden bepaald.

De component E-mailervaringsfragment ondersteunt een gelokaliseerde sitestructuur.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de E-mailervaringsfragmentcomponent is v1, die in oktober 2022 is geïntroduceerd met release X van de e-mailkerncomponenten en in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel | - | - |

Voor meer informatie over de versies en de versies van de Component van de Kern E-mailE-mail van de Component, zie het document [ Versies van de Componenten van de Kern.](/help/email/versions.md)

## Ondersteuning voor gelokaliseerde sitestructuur {#localized-site-structure}

De E-mailervaringsfragmentcomponent is aangepast aan gelokaliseerde inhoudsstructuren en geeft het juiste ervaringsfragment weer op basis van de lokalisatie van de inhoud. Hiervoor moet het ervaringsfragment aan de volgende voorwaarden voldoen.

* De component van het Fragment van de Ervaring E-mail wordt toegevoegd aan a [ paginamalplaatje.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/templates.html?lang=nl-NL)
* Die sjabloon wordt gebruikt om een nieuwe inhoudspagina te maken die deel uitmaakt van een gelokaliseerde structuur onder `/content/<site>` .
* Het ervaringsfragment waarnaar op een inhoudspagina wordt verwezen, maakt deel uit van een gelokaliseerde Experience-fragmentstructuur onder `/content/experience-fragments` die dezelfde patronen volgt als de onderstaande site `/content/<site>` , inclusief het gebruik van dezelfde componentnamen.

In dit geval, zal het fragment met de zelfde localisatie ([ taal, blauwdruk, of levende exemplaar ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/reusing-content/msm-and-translation.html?lang=nl-NL)) zoals de huidige pagina als deel van het malplaatje worden teruggegeven.

Dit gedrag is beperkt tot E-mailervaringsfragmentcomponenten die aan sjablonen zijn toegevoegd. De Componenten van het Fragment van de ervaring die aan individuele inhoudspagina&#39;s worden toegevoegd zullen de nauwkeurige die Uitvoeringen van het Fragment van de Ervaring teruggeven binnen de component worden gevormd.

* Voor een voorbeeld van hoe de localisatieeigenschappen van de Component van het Fragment van de Ervaring werken, zie [ de sectie hieronder ](#example).
* Voor een voorbeeld van hoe de localisatieeigenschappen van de Componenten van de Kern samenwerken, zie de [ Eigenschappen van de Localisatie van de pagina van de Componenten van de Kern ](/help/get-started/localization.md).

### Voorbeeld {#example}

Laten we zeggen dat uw inhoud er ongeveer als volgt uitziet:

```
/content
+-- experience-fragments
   \-- wknd
      +-- language-masters
      +-- us
         +-- en
            +-- footerTextXf
            \-- headerTextXf
         \-- es
            +-- footerTextXf
            \-- headerTextXf
      \-- ch
         +-- de
            +-- footerTextXf
            \-- headerTextXf
         +-- fr
            +-- footerTextXf
            \-- headerTextXf
         \-- it
            +-- footerTextXf
            \-- headerTextXf
+-- wknd
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

De structuur onder `/content/experience-fragments/wknd` spiegelt de structuur van `/content/wknd` .

Als de E-mailervaringsfragmentcomponent `/content/experience-fragments/wknd/us/en/footerTextXf` in dit geval op een sjabloon wordt geplaatst, geven de gelokaliseerde pagina&#39;s die op die sjabloon zijn gebaseerd automatisch het gelokaliseerde ervaringsfragment weer dat overeenkomt met de gelokaliseerde inhoudspagina.

Als u dus naar een inhoudspagina navigeert onder `/content/wknd/ch/de` die dezelfde sjabloon gebruikt, wordt `/content/experience-fragments/wknd/ch/de/footerTextXf` weergegeven in plaats van `/content/experience-fragments/wknd/us/en/footerTextXf` .

### Fallback {#fallback}

De E-mailervaringsfragmentcomponent probeert een overeenkomende gelokaliseerde component in de volgende volgorde te vinden.

1. Eerst wordt geprobeerd een taalhoofdmap te vinden.
1. Als deze niet wordt gevonden, wordt geprobeerd een blauwdruk te vinden.
1. Als deze niet wordt gevonden, wordt geprobeerd een live kopie te zoeken.
1. Als niet gevonden, blijft het aan het Fragment van de Ervaring in de component worden gevormd in gebreke.

## Technische details {#technical-details}

Lees de recentste [ technische documentatie over de Component van het Fragment van de Ervaring ](https://www.adobe.com/go/aem_cmp_xf_v1).

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden.](/help/developing/overview.md)

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud de variant van het ervaringsfragment selecteren die in de inhoud moet worden gerenderd.

![ E-mailE-mail de bewerkingsdialoog van de Component van het Fragment van de Ervaring ](/help/email/assets/email-experience-fragment-edit.png)

Gebruik de **Open Dialoog van de Selectie** knoop om de componentenselecteur te openen om te kiezen welke de componentenvariatie van het Fragment van de Ervaring aan de inhoudspagina toe te voegen.

Als u de Component van het Fragment van de Ervaring E-mail aan een malplaatje toevoegt, zal het automatisch gelokaliseerd zijn op voorwaarde dat de Fragmenten van de Ervaring worden gelokaliseerd, zodat wat op de pagina wordt teruggegeven van de component kan variëren u uitdrukkelijk selecteert. [ zie het voorbeeld hierboven ](#example) voor meer informatie.

U kunt ook een **identiteitskaart** bepalen. Met deze optie kunt u de unieke id van de component in het HTML-bestand bepalen.

* Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende inhoud te inspecteren.
* Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
* Het wijzigen van de id kan gevolgen hebben voor CSS.

### Tabblad Stijlen {#styles-tab-edit}

De component van het Fragment van de Ervaring E-mail steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling)

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in de [ ontwerpdialoog ](#design-dialog) worden gevormd opdat het lusje beschikbaar is.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de E-mailervaringsfragmentcomponent gebruikt en de standaardinstellingen die zijn ingesteld bij het plaatsen van de E-mailervaringsfragmentcomponent.

### Tabblad Stijlen {#styles-tab}

De component van het Fragment van de Ervaring E-mail steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling)
