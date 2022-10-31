---
title: Afbeeldingscomponent
description: De component Core Component Image is een adaptieve afbeeldingscomponent.
role: Architect, Developer, Admin, User
exl-id: c5e57f4b-139f-40e7-8d79-be9a74360b63
source-git-commit: f0971db66cbbf8221c12cedf108eee3bca8a527a
workflow-type: tm+mt
source-wordcount: '1678'
ht-degree: 0%

---

# Afbeeldingscomponent{#image-component}

De component Core Component Image is een adaptieve afbeeldingscomponent.

## Gebruik {#usage}

De component Afbeelding biedt een adaptieve selectie van afbeeldingen en een responsief gedrag bij het laden van de pagina voor de bezoeker van de pagina en bij het eenvoudig plaatsen van de afbeelding voor de auteur van de inhoud.

De breedte van de afbeelding en aanvullende instellingen kunnen door de sjabloonauteur worden gedefinieerd in het dialoogvenster [ontwerpdialoogvenster](#design-dialog). De inhoudeditor kan elementen uploaden of selecteren in het dialoogvenster [configureren, dialoogvenster.](#configure-dialog)

## Versie en compatibiliteit {#version-and-compatibility}

De huidige versie van de Image Component is v3, die in februari 2022 is geïntroduceerd met versie 2.18.0 van de Core Components, en die in dit document wordt beschreven.

In de volgende tabel staan alle ondersteunde versies van de component, de AEM versies waarmee de versies van de component compatibel zijn en koppelingen naar documentatie voor vorige versies.

| Componentversie | AEM 6,4 | AEM 6,5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v3 | - | Compatibel | Compatibel |
| [v2](v2/image.md) | Compatibel | Compatibel | Compatibel |
| [v1](v1/image-v1.md) | Compatibel | Compatibel | Compatibel |

Raadpleeg het document voor meer informatie over versies en releases van de Core Component [Core Components-versies](/help/versions.md).

## Responsieve functies {#responsive-features}

De component Image wordt geleverd met robuuste responsieve functies die direct uit de verpakking zijn te vinden. Op het niveau van het paginasjabloon [ontwerpdialoogvenster](#design-dialog) kan worden gebruikt om de standaardbreedten van het afbeeldingselement te definiëren. De component van het Beeld zal dan automatisch de correcte breedte aan vertoning afhankelijk van de grootte van het browser venster laden. Wanneer het formaat van het venster wordt gewijzigd, laadt de component Image dynamisch de juiste afbeeldingsgrootte. Componentontwikkelaars hoeven zich geen zorgen te maken over het definiëren van aangepaste mediaquery&#39;s, aangezien de component Image al is geoptimaliseerd om uw inhoud te laden.

Bovendien ondersteunt de component Afbeelding lui laden om het laden van het eigenlijke afbeeldingselement uit te stellen totdat het element zichtbaar is in de browser, waardoor de reacties op uw pagina&#39;s sneller worden.

>[!TIP]
>
>De component Image wordt standaard geactiveerd door de adaptieve afbeeldingsserver. Zie het document [Adaptieve afbeeldingsserver](#adaptive-image-servlet) voor meer informatie over hoe het werkt.

## Dynamic Media-ondersteuning {#dynamic-media}

De afbeeldingscomponent (vanaf [release 2.13.0](/help/versions.md)) ondersteunt [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html#dynamicmedia) activa. [Indien ingeschakeld,](#design-dialog) Met deze functies kunt u Dynamic Media-afbeeldingselementen toevoegen met een eenvoudige sleepfunctie of via de middelenbrowser, net als met andere afbeeldingen. Daarnaast worden ook afbeeldingsaanpassingen, voorinstellingen voor afbeeldingen en slimme gewassen ondersteund.

Uw webervaringen die zijn gemaakt met Core Components kunnen beschikken over uitgebreide, op Sensei gebaseerde, robuuste, krachtige Dynamic Media Image-mogelijkheden voor meerdere platforms.

## SVG-ondersteuning {#svg-support}

Schaalbare vectorafbeeldingen (SVG) worden ondersteund door de afbeeldingscomponent.

* De belemmering-en-daling van SVG activa van DAM en het uploaden van een SVG dossier van een lokaal dossiersysteem worden allebei gesteund.
* Het oorspronkelijke SVG-bestand wordt gestreamd (transformaties worden overgeslagen).
* Voor een SVG-afbeelding worden de &quot;slimme afbeeldingen&quot; en de &quot;slimme formaten&quot; ingesteld op een lege array in het afbeeldingsmodel.

### Beveiliging {#security}

Om veiligheidsredenen wordt de originele SVG nooit direct geroepen door de Redacteur van het Beeld. Het wordt doorgeroepen `<img src=“path-to-component”>`. Hierdoor wordt voorkomen dat de browser scripts uitvoert die in het SVG-bestand zijn ingesloten.

>[!NOTE]
>
>Voor SVG-ondersteuning is release 2.1.0 van de Core Components of hoger vereist, samen met [servicepack 2](https://experienceleague.adobe.com/docs/experience-manager-64/release-notes/sp-release-notes.html) voor AEM 6.4 of hoger [functies voor afbeeldingseditor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/image-editor.html) binnen AEM.

## Uitvoer van voorbeeldcomponent {#sample-component-output}

Als u de afbeeldingscomponent wilt ervaren en voorbeelden wilt zien van de configuratieopties en van de HTML- en JSON-uitvoer, gaat u naar de [Componentbibliotheek](https://adobe.com/go/aem_cmp_library_image).

### Technische details {#technical-details}

De meest recente technische documentatie over de Image Component [kan op GitHub worden gevonden](https://adobe.com/go/aem_cmp_tech_image_v3).

Meer informatie over het ontwikkelen van kerncomponenten vindt u in de [Documentatie voor ontwikkelaars van kerncomponenten](/help/developing/overview.md).

De component Image ondersteunt [schema.org-microgegevens](https://schema.org).

## Dialoogvenster configureren {#configure-dialog}

De component image biedt een dialoogvenster voor configureren waarin de afbeelding zelf wordt gedefinieerd, samen met de beschrijving en basiseigenschappen.

### Tabblad Element {#asset-tab}

![Tabblad Element van het dialoogvenster Configureren van Image Component](/help/assets/image-configure-asset.png)

* **Weergegeven afbeelding overnemen van pagina** - Deze optie gebruikt de optie [weergegeven afbeelding van de gekoppelde pagina](page.md) of de weergegeven afbeelding van de huidige pagina als de afbeelding niet is gekoppeld.

* **Alternatieve tekst voor toegankelijkheid** - In dit veld kunt u een beschrijving van de afbeelding definiëren voor visueel gehandicapte gebruikers.

   * **Alternatieve tekst van pagina overnemen** - Bij deze optie wordt de alternatieve beschrijving van de waarde van het gekoppelde element van de optie `dc:description` metagegevens in DAM of van de huidige pagina als er geen element is gekoppeld.

* **Afbeeldingselement**
   * Middelen uit het deelvenster [middelenbrowser](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) of tik op **doorbladeren** uploaden vanuit een lokaal bestandssysteem.
   * Tik of klik op **Wissen** om de selectie van de geselecteerde afbeelding op te heffen.
   * Tik of klik op **Bewerken** tot [de uitvoeringen van het actief beheren](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) in de middeleneditor.

* **Geen alternatieve tekst bieden** - Deze optie markeert dat de afbeelding wordt genegeerd door ondersteunende hulpmiddelen, zoals schermlezers, wanneer de afbeelding zuiver decoratief is of anderszins geen aanvullende informatie naar de pagina overbrengt.

### Tabblad Metagegevens {#metadata-tab}

![Tabblad Metagegevens van het dialoogvenster Configureren van Image Component](/help/assets/image-configure-metadata.png)

* **Type voorinstelling** - Hiermee worden de typen voorinstellingen voor afbeeldingen gedefinieerd die beschikbaar zijn. **Voorinstelling afbeelding** of **Slim uitsnijden** en is alleen beschikbaar wanneer [Dynamic Media-functies](#dynamic-meida) zijn ingeschakeld.
   * **Voorinstelling afbeelding** - Wanneer **Type voorinstelling** van **Voorinstelling afbeelding** is geselecteerd, de vervolgkeuzelijst **Voorinstelling afbeelding** is beschikbaar, zodat u kunt kiezen uit de beschikbare Dynamic Media-voorinstellingen. Dit is alleen beschikbaar als er voorinstellingen zijn gedefinieerd voor het geselecteerde element.
   * **Slim uitsnijden** - Wanneer **Type voorinstelling** van **Slim uitsnijden** is geselecteerd in de vervolgkeuzelijst **Vertoning** is beschikbaar, zodat u kunt kiezen uit de beschikbare uitvoeringen van het geselecteerde element. Dit is alleen beschikbaar als uitvoeringen zijn gedefinieerd voor het geselecteerde element.
   * **Afbeeldingsaanpassingen** - U kunt hier aanvullende opdrachten voor Dynamic Media-beeldserving definiëren door `&`, ongeacht welke **Type voorinstelling** is geselecteerd.
* **Bijschrift** - Aanvullende informatie over de afbeelding, die standaard onder de afbeelding wordt weergegeven.
   * **Bijschrift ophalen van DAM** - Als deze optie is ingeschakeld, wordt de bijschrifttekst van de afbeelding gevuld met de waarde van de optie `dc:title` metagegevens in DAM.
   * **Bijschrift weergeven als pop-up** - Als deze optie is ingeschakeld, wordt het bijschrift niet weergegeven onder de afbeelding, maar als een pop-up die door sommige browsers wordt weergegeven wanneer de muisaanwijzer op de afbeelding wordt geplaatst.
* **Koppeling** - Koppel de afbeelding aan een andere bron.
   * In het dialoogvenster Selecteren kunt u een koppeling maken naar een andere AEM.
   * Als u geen koppeling naar een AEM maakt, voert u de absolute URL in. Niet-absolute URL&#39;s worden geïnterpreteerd als relatief ten opzichte van AEM.
   * **Koppeling openen op nieuw tabblad** - Met deze optie opent u de koppeling in een nieuw browservenster.
* **ID** - Met deze optie kunt u de unieke id van de component in de HTML en in de [Gegevenslaag](/help/developing/data-layer/overview.md).
   * Als deze leeg blijft, wordt automatisch een unieke id voor u gegenereerd. U kunt deze vinden door de resulterende pagina te inspecteren.
   * Als een id is opgegeven, is het de verantwoordelijkheid van de auteur om ervoor te zorgen dat deze uniek is.
   * Het wijzigen van de id kan gevolgen hebben voor het bijhouden van CSS-, JS- en gegevenslagen.

>[!TIP]
>
>**Slim uitsnijden** en **Voorinstelling afbeelding** zijn opties die elkaar uitsluiten. Als een auteur een voorinstelling voor een afbeelding moet gebruiken in combinatie met een uitvoering voor slim uitsnijden, moet de auteur de opdracht **Afbeeldingsaanpassingen** om handmatig voorinstellingen toe te voegen.

### Tabblad Stijlen {#styles-tab-edit}

![Het tabblad Stijlen van het dialoogvenster Afbeeldingscomponent bewerken](/help/assets/image-configure-styles.png)

De component Image ondersteunt de AEM [Stijlsysteem.](/help/get-started/authoring.md#component-styling).

Gebruik de vervolgkeuzelijst om de stijlen te selecteren die u op de component wilt toepassen. Selecties in het dialoogvenster Bewerken hebben hetzelfde effect als de selecties op de werkbalk van de component.

De stijlen moeten voor deze component in worden gevormd [ontwerpdialoogvenster](#design-dialog) zodat het vervolgkeuzemenu beschikbaar is.

## Ontwerpdialoogvenster {#design-dialog}

### Hoofdtabblad {#main-tab}

![Het hoofdtabblad van het dialoogvenster Ontwerp van de afbeeldingscomponent](/help/assets/image-design-main.png)

* **DM-functies inschakelen** - Indien ingeschakeld, [Dynamic Media-functies](#dynamic-media) zijn beschikbaar.
   * Deze optie wordt alleen weergegeven als Dynamic Media is ingeschakeld in de omgeving.
* **Geoptimaliseerde webafbeeldingen inschakelen** - Indien ingeschakeld, [de webgeoptimaliseerde service voor het leveren van afbeeldingen](/help/developing/web-optimized-image-delivery.md) Hiermee worden afbeeldingen in de WebP-indeling geleverd. De afbeeldingen worden gemiddeld met 25% verkleind.
   * Deze optie is alleen beschikbaar in AEMaaCS.
   * Als deze optie niet is ingeschakeld of als de service voor het leveren van afbeeldingen voor het web niet beschikbaar is, [Adaptieve afbeeldingsserver](/help/developing/adaptive-image-servlet.md) wordt gebruikt.
* **Lazy load uitschakelen** - Als deze optie is ingeschakeld, worden alle afbeeldingen vooraf geladen zonder dat dit wordt vertraagd.
* **Afbeelding is decoratief** - Definieer of de optie Decoratieve afbeelding automatisch wordt ingeschakeld wanneer u de afbeeldingscomponent aan een pagina toevoegt.
* **Alternatieve tekst ophalen van DAM**- Definieer of de optie voor het ophalen van de alternatieve tekst van de DAM automatisch is ingeschakeld wanneer u de afbeeldingscomponent aan een pagina toevoegt.
* **Bijschrift ophalen van DAM** - Bepaal als de optie om de titel van DAM terug te winnen automatisch wordt toegelaten wanneer het toevoegen van de beeldcomponent aan een pagina.
* **Bijschrift weergeven als pop-up** - Definieer of de optie voor het weergeven van het bijschrift als pop-up automatisch is ingeschakeld wanneer u de afbeeldingscomponent aan een pagina toevoegt.
* **Breedte wijzigen** - Deze waarde wordt gebruikt voor het vergroten of verkleinen van de breedte van de basisafbeeldingen die DAM-elementen zijn.
   * De hoogte-breedteverhouding van de afbeeldingen blijft behouden.
   * Als de waarde groter is dan de werkelijke breedte van de afbeelding, heeft deze waarde geen effect.
   * Deze waarde heeft geen effect op SVG-afbeeldingen.

U kunt een lijst van breedten in pixel voor het beeld bepalen en de component zal automatisch de meest aangewezen breedte laden die op browser grootte wordt gebaseerd. Dit is een belangrijk onderdeel van het [responsieve functies](#responsive-features) van de afbeeldingscomponent.

* **Breedten** - Definieert een lijst met breedten in pixels voor de afbeelding en de component laadt automatisch de meest geschikte breedte op basis van de browsergrootte.
   * Tik of klik op de knop **Toevoegen** om een andere grootte toe te voegen.
      * Gebruik de grepen om de volgorde van de formaten te wijzigen.
      * Gebruik de **Verwijderen** pictogram om een breedte te verwijderen.
   * Het laden van afbeeldingen wordt standaard uitgesteld totdat ze zichtbaar worden.
      * Selecteer de optie **Lazy load uitschakelen** om de afbeeldingen te laden wanneer de pagina wordt geladen.
* **JPEG-kwaliteit** - De kwaliteitsfactor (als percentage van 0 en 100) voor getransformeerde (bijv. geschaalde of bijgesneden) JPEG-afbeeldingen.

>[!TIP]
>
>Zie het document [Adaptieve afbeeldingsserver](/help/developing/adaptive-image-servlet.md) voor tips voor het optimaliseren van de selectie van uitvoeringen door uw breedten zorgvuldig te definiëren.

### Tabblad Stijlen {#styles-tab}

De component Image ondersteunt de AEM [Stijlsysteem](/help/get-started/authoring.md#component-styling).

## Gegevenslaag Adobe-client {#data-layer}

De component Image ondersteunt de [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)
