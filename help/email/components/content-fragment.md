---
title: Component E-mailinhoudsfragment
description: Met de component E-mailinhoudsfragment kunt u een inhoudsfragment in uw inhoud weergeven.
role: Architect, Developer, Admin, User
exl-id: 9bc6b730-0d2a-4e5b-891c-d2f67f600bcc
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---


# Component E-mailinhoudsfragment {#email-content-fragment-component}

De component van het Fragment van de Inhoud E-mail staat voor de vertoning van a [ inhoudsfragment ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) in uw inhoud toe.

## Gebruik {#usage}

De component van het Fragment van de Inhoud E-mail staat voor de opneming van a [ inhoudsfragment ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) in uw e-mailinhoud toe. Inhoudsfragmenten zijn gestructureerde inhoud met meerdere kanalen die centraal kan worden ontworpen en eenvoudig opnieuw kan worden gebruikt.

* Het fragment en zijn eigenschappen kunnen in [ worden geselecteerd vormen dialoog.](#configure-dialog)
* De types van middel om bepaalde beelden en netten te behandelen kunnen in de [ ontwerpdialoog worden bepaald.](#design-dialog)
* De uitgeven optie opent het geselecteerde fragment binnen de [ redacteur van het inhoudsfragment, ](#edit-dialog) die voor gebruik met de Componenten van de Kern E-mail wordt aangepast.

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de E-mailcomponent Content Fragment is v1, die in oktober 2022 is geïntroduceerd met release X van de Email Core Components, en die in dit document wordt beschreven.

In de volgende tabel worden alle ondersteunde versies van de component, de AEM-versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor eerdere versies weergegeven.

| Componentversie | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatibel | Compatibel | - |

Voor meer informatie over de versies en versies van de Component van de Kern E-mailE-mail van de Component, zie de Versies van de Componenten van de Document [ E-mailKern.](/help/email/versions.md)

## Technische details {#technical-details}

De recentste technische documentatie over de Component van het Fragment van de E-mailInhoud [ kan op GitHub worden gevonden.](https://adobe.com/go/aem_cmp_tech_email_cf_v1)

De verdere details over het ontwikkelen van de Componenten van de Kern kunnen in de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern worden gevonden.](/help/developing/overview.md)

## Dialoogvenster configureren {#configure-dialog}

In het dialoogvenster configureren kan de auteur van de inhoud definiëren welk inhoudsfragment en de elementen van dat fragment moeten worden opgenomen.

### Tabblad Eigenschappen {#properties-tab}

![ Component van het Fragment van de Inhoud E-mail ](/help/email/assets/email-content-fragment-edit-properties.png)

* **het Fragment van de Inhoud**

   * Pad naar het gewenste inhoudsfragment
   * De **Dialoog van de Selectie** kan worden gebruikt om van het fragment de plaats te bepalen

* **Wijze van de Vertoning**
   * **Enig Element van de Tekst** - laat selectie van één multiline tekstelement toe en laat paragraafcontroleopties toe
* **Variatie** - welke variatie van het inhoudsfragment om te gebruiken (gebreken aan **Hoofd**)

* **identiteitskaart** - Deze optie staat het controleren van het unieke herkenningsteken van de component in HTML toe.
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende inhoud te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor CSS.

### Tabblad Alinealijn {#paragraph-control-tab}

![ Component van het Fragment van de Inhoud E-mail ](/help/assets/content-fragment-edit-paragraph.png)

* **Paragraaf** - sta selectie van alle paragrafen of een waaier toe
   * **allen** - toon alle paragrafen
   * **Waaier**
      * Bereiken opgeven voor alinea&#39;s die moeten worden weergegeven, gescheiden door een puntkomma
      * `1;3-5;7;9-*` neemt bijvoorbeeld de eerste, de derde tot de vijfde, de zevende en de negende alinea op
* **de rubriek van het Handvat als hun eigen paragrafen**

## Dialoogvenster Bewerken {#edit-dialog}

Zodra u de Component van het Fragment van de Inhoud E-mail hebt gebruikt om een inhoudsfragment te vormen, wanneer u de component in de inhoudsredacteur selecteert, toont het een **geeft** optie uit.

![ Toolbar van de Component van het Fragment van de Inhoud E-mail ](/help/email/assets/email-content-fragment-edit-toolbar.png)

Tapping of het klikken van **geeft** knoop uit opent de redacteur van het inhoudsfragment. De redacteur van het inhoudsfragment is uitgebreid om knopen voor de **Uitgezochte Variabele van Adobe Campaign** te omvatten om de variabelen van Adobe Campaign in uw inhoudsfragmenten op te nemen.

![ de fragmentredacteur van de Inhoud voor e-mail ](/help/email/assets/email-content-fragment-editor.png)

Voor meer informatie over het uitgeven en het ontwerpen van inhoudsfragmenten, zie het document [ Authoring Inhoud van het Fragment.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments-variations.html)

## Ontwerpdialoogvenster {#design-dialog}

Wanneer een component E-mailcontentfragment wordt geconfigureerd met een inhoudsfragment, wordt op de werkbalk een knop weergegeven waarmee de editor voor het inhoudsfragment wordt geopend wanneer u dit selecteert in de inhoudseditor.


### Hoofdtabblad {#main-tab}

![ dialoog van het Ontwerp van de Component van het Fragment van de Inhoud E-mail ](/help/email/assets/email-content-fragment-design.png)

* **Intern ontvankelijk net**

   * Het Sling-brontype dat wordt gebruikt voor het interne responsieve raster

### Tabblad Stijlen {#styles-tab}

De component van het Fragment van de Ervaring E-mail steunt het Systeem van de Stijl van AEM [.](/help/get-started/authoring.md#component-styling)
