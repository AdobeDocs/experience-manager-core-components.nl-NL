---
title: Component E-mailinhoudsfragment
description: Met de component E-mailinhoudsfragment kunt u een inhoudsfragment in uw inhoud weergeven.
role: Architect, Developer, Admin, User
exl-id: 9bc6b730-0d2a-4e5b-891c-d2f67f600bcc
source-git-commit: 3abc29e0c186a84f079d5938b8b716f4c7378d65
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 1%

---


# Component E-mailinhoudsfragment {#email-content-fragment-component}

Met de component E-mailinhoudsfragment kunt u een [inhoudsfragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) in uw inhoud.

## Gebruik {#usage}

Met de component E-mailinhoudsfragment kunt u een [inhoudsfragment](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) in uw e-mailinhoud. Inhoudsfragmenten zijn gestructureerde inhoud met meerdere kanalen die centraal kan worden ontworpen en eenvoudig opnieuw kan worden gebruikt.

* Het fragment en de bijbehorende eigenschappen kunnen worden geselecteerd in het dialoogvenster [configureren, dialoogvenster.](#configure-dialog)
* De typen bronnen voor het verwerken van bepaalde afbeeldingen en rasters kunnen worden gedefinieerd in het dialoogvenster [ontwerpdialoogvenster.](#design-dialog)
* Met de optie Bewerken opent u het geselecteerde fragment in het dialoogvenster [editor voor inhoudsfragmenten,](#edit-dialog) aangepast voor gebruik met de e-mailkerncomponenten.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de E-mailcomponent Content Fragment is v1, die in oktober 2022 is geïntroduceerd met release X van de Email Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatibel | - |

Raadpleeg het document voor meer informatie over versies en releases van e-mail Core Component [Core Components-versies e-mailen.](/help/email/versions.md)

## Technische details {#technical-details}

De meest recente technische documentatie over de E-mailcomponent Inhoudsfragment [kan op GitHub worden gevonden.](https://adobe.com/go/aem_cmp_tech_email_cf_v1)

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [De ontwikkelaarsdocumentatie van de Componenten van de kern.](/help/developing/overview.md)

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster configureren kan de auteur van de inhoud definiëren welk inhoudsfragment en de elementen van dat fragment moeten worden opgenomen.

### Tabblad Eigenschappen {#properties-tab}

![Component E-mailinhoudsfragment](/help/email/assets/email-content-fragment-edit-properties.png)

* **Inhoudsfragment**

   * Pad naar het gewenste inhoudsfragment
   * De **Dialoogvenster Selectie** kan worden gebruikt om het fragment te zoeken

* **Weergavemodus**
   * **Element voor één tekst** - Schakelt de selectie van één tekstelement met meerdere regels in en schakelt de opties voor alineacontrole in
* **Variatie** - Welke variatie van het inhoudfragment moet worden gebruikt (standaard ingesteld op **Master**)

* **ID** - Met deze optie kunt u de unieke id van de component in de HTML bepalen.
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende inhoud te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor CSS.

### Tabblad Alinealijn {#paragraph-control-tab}

![Component E-mailinhoudsfragment](/help/assets/content-fragment-edit-paragraph.png)

* **Alinea&#39;s** - Selectie van alle alinea&#39;s of een bereik toestaan
   * **Alles** - Alle alinea&#39;s weergeven
   * **Bereik**
      * Bereiken opgeven voor alinea&#39;s die moeten worden weergegeven, gescheiden door een puntkomma
      * Bijvoorbeeld `1;3-5;7;9-*` de eerste, de derde tot en met de vijfde, de zevende en de negende alinea
* **Koptekst verwerken als eigen alinea&#39;s**

## Dialoogvenster Bewerken {#edit-dialog}

Wanneer u de component E-mailinhoudfragmentatie hebt gebruikt om een inhoudsfragment te configureren, wordt bij het selecteren van de component in de inhoudseditor een **Bewerken** optie.

![Werkbalk van de component E-mailinhoudsfragment](/help/email/assets/email-content-fragment-edit-toolbar.png)

Tikken of klikken op de knop **Bewerken** opent de inhoudfragment-editor. De inhoudfragmenteditor is uitgebreid en bevat nu knoppen voor de **Adobe Campaign-variabele selecteren** om Adobe Campaign-variabelen in te voegen in uw inhoudsfragmenten.

![Inhoudsfragmenteditor voor e-mail](/help/email/assets/email-content-fragment-editor.png)

Zie het document voor meer informatie over het bewerken en ontwerpen van inhoudsfragmenten [Fragmentinhoud ontwerpen.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments-variations.html)

## Ontwerpdialoogvenster {#design-dialog}

Wanneer een component E-mailcontentfragment wordt geconfigureerd met een inhoudsfragment, wordt op de werkbalk een knop weergegeven waarmee de editor voor het inhoudsfragment wordt geopend wanneer u dit selecteert in de inhoudseditor.


### Hoofdtabblad {#main-tab}

![Het dialoogvenster Ontwerpen van de component E-mailinhoudsfragment](/help/email/assets/email-content-fragment-design.png)

* **Intern responsief raster**

   * Het Sling-brontype dat wordt gebruikt voor het interne responsieve raster

### Tabblad Stijlen {#styles-tab}

De E-mailervaringsfragmentcomponent ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling)
