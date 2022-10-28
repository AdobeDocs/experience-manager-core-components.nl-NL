---
title: E-mailervaringsfragmentcomponent
description: Met de E-mailervaringsfragmentcomponent kan de auteur van de inhoud een Experience-fragmentvariatie in de inhoud plaatsen en een gelokaliseerde inhoudsstructuur ondersteunen.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 0%

---


# E-mailervaringsfragmentcomponent {#email-experience-fragment-component}

Met de E-mailervaringsfragmentcomponent kan de auteur van de inhoud een Experience-fragmentvariatie in de inhoud plaatsen en een gelokaliseerde inhoudsstructuur ondersteunen.

## Gebruik {#usage}

Met de E-mailervaringsfragmentcomponent kan de auteur van de inhoud bestaande Experience-fragmentvariaties selecteren en deze in de inhoud plaatsen. Een ervaringsfragment is een groep inhoud die zowel inhoud als lay-out bevat en die via kanalen opnieuw kan worden gebruikt.

* De eigenschappen van de component kunnen worden gedefinieerd in het dialoogvenster [dialoogvenster configureren](#configure-dialog).
* De standaardwaarden voor de component wanneer deze aan inhoud wordt toegevoegd, kunnen worden gedefinieerd in het dialoogvenster [ontwerpdialoogvenster](#design-dialog).

De component E-mailervaringsfragment ondersteunt een gelokaliseerde sitestructuur.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de E-mailervaringsfragmentcomponent is v1, die in oktober 2022 is geïntroduceerd met release X van de e-mailkerncomponenten en in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over de versies en releases van de e-mailCore-component [Core Components-versies e-mailen.](/help/email/versions.md)

## Ondersteuning voor gelokaliseerde sitestructuur {#localized-site-structure}

De E-mailervaringsfragmentcomponent is aangepast aan gelokaliseerde inhoudsstructuren en geeft het juiste ervaringsfragment weer op basis van de lokalisatie van de inhoud. Hiervoor moet het ervaringsfragment aan de volgende voorwaarden voldoen.

* De E-mailervaringsfragmentcomponent wordt toegevoegd aan een [paginasjabloon.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/templates.html)
* Die sjabloon wordt gebruikt om een nieuwe inhoudspagina te maken die deel uitmaakt van een onderstaande gelokaliseerde structuur `/content/<site>`.
* Het ervaringsfragment waarnaar op een inhoudspagina wordt verwezen, maakt deel uit van een onderstaande gelokaliseerde fragmentstructuur van de Experience `/content/experience-fragments` die dezelfde patronen volgt als de onderstaande site `/content/<site>` inclusief het gebruik van dezelfde componentnamen.

In dit geval is het fragment met dezelfde lokalisatie ([taal, blauwdruk of live kopie](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/reusing-content/msm-and-translation.html)) als de huidige pagina wordt weergegeven als onderdeel van de sjabloon.

Dit gedrag is beperkt tot E-mailervaringsfragmentcomponenten die aan sjablonen zijn toegevoegd. De Componenten van het Fragment van de ervaring die aan individuele inhoudspagina&#39;s worden toegevoegd zullen de nauwkeurige die Uitvoeringen van het Fragment van de Ervaring teruggeven binnen de component worden gevormd.

* Voor een voorbeeld van hoe de lokalisatiefuncties van de Component van het Fragment van de Ervaring werken, zie [het onderstaande gedeelte](#example).
* Voor een voorbeeld van hoe de lokalisatiefuncties van de Core Components samenwerken, raadpleegt u de [Localisatiefuncties van de pagina Core Components](/help/get-started/localization.md).

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

U ziet dat de onderstaande structuur `/content/experience-fragments/wknd` spiegelt de structuur van `/content/wknd`.

In dit geval geldt dat als de E-mail de component Fragment aantreft `/content/experience-fragments/wknd/us/en/footerTextXf` op een sjabloon wordt geplaatst, geven de gelokaliseerde pagina&#39;s die op die sjabloon zijn gebaseerd automatisch het gelokaliseerde ervaringsfragment weer dat overeenkomt met de gelokaliseerde inhoudspagina.

Dus als u naar een inhoudspagina onder navigeert `/content/wknd/ch/de` die dezelfde sjabloon gebruiken, `/content/experience-fragments/wknd/ch/de/footerTextXf` wordt weergegeven in plaats van `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Fallback {#fallback}

De E-mailervaringsfragmentcomponent probeert een overeenkomende gelokaliseerde component in de volgende volgorde te vinden.

1. Eerst wordt geprobeerd een taalhoofdmap te vinden.
1. Als deze niet wordt gevonden, wordt geprobeerd een blauwdruk te vinden.
1. Als deze niet wordt gevonden, wordt geprobeerd een live kopie te zoeken.
1. Als niet gevonden, blijft het aan het Fragment van de Ervaring in de component worden gevormd in gebreke.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de E-mailervaringsfragmentcomponent wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek.](https://adobe.com/go/aem_cmp_library_email_xf)

## Technische details {#technical-details}

De meest recente technische documentatie over de component Experience Fragment [kan op GitHub worden gevonden.](https://adobe.com/go/aem_cmp_email_tech_xf_v1)

Meer informatie over de ontwikkeling van de kerncomponenten vindt u in de [De ontwikkelaarsdocumentatie van de Componenten van de kern.](/help/developing/overview.md)

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster Configureren kan de auteur van de inhoud de variant van het ervaringsfragment selecteren die in de inhoud moet worden gerenderd.

![Dialoogvenster voor bewerken van E-mailervaringsfragmentcomponent](/help/email/assets/email-experience-fragment-edit.png)

Gebruik de **Dialoogvenster Selectie openen** om de componentkiezer te openen en aan te geven welke variatie in de fragmentcomponent moet worden toegevoegd aan de inhoudspagina.

Als u de Component van het Fragment van de Ervaring E-mail aan een malplaatje toevoegt, zal het automatisch gelokaliseerd zijn op voorwaarde dat de Fragmenten van de Ervaring worden gelokaliseerd, zodat wat op de pagina wordt teruggegeven van de component kan variëren u uitdrukkelijk selecteert. [Zie het bovenstaande voorbeeld](#example) voor meer informatie .

U kunt ook een **ID**. Met deze optie kunt u de unieke id van de component in het HTML-bestand bepalen.

* Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende inhoud te inspecteren.
* Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
* Het wijzigen van de id kan gevolgen hebben voor CSS.

### Tabblad Stijlen {#styles-tab-edit}

De E-mailervaringsfragmentcomponent ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling)

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in worden gevormd [ontwerpdialoogvenster](#design-dialog) zodat het tabblad beschikbaar is.

## Ontwerpdialoogvenster {#design-dialog}

In het ontwerpdialoogvenster kan de sjabloonauteur de opties definiëren die beschikbaar zijn voor de auteur van de inhoud die de E-mailervaringsfragmentcomponent gebruikt en de standaardinstellingen die zijn ingesteld bij het plaatsen van de E-mailervaringsfragmentcomponent.

### Tabblad Stijlen {#styles-tab}

De E-mailervaringsfragmentcomponent ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling)
