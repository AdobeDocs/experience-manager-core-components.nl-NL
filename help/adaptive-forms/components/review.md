---
title: Adaptive Forms Core Component - Revisiecomponent
description: De Adaptive Forms Review Core-component gebruiken of aanpassen.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
source-git-commit: 04a685cfa2616839f4fec715847bf0821808bd59
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---


# Revisiecomponent

Met de Revisiecomponent in Adaptive Forms kunnen gebruikers de ingevoerde gegevens controleren en verifiëren voordat ze het formulier verzenden. Het dient als een overzichtspagina, die een read-only mening van alle gebieden en hun waarden in een gestructureerd en gebruikersvriendelijk formaat verstrekt. Met deze functie kunnen gebruikers eventuele fouten of omissies opsporen en corrigeren voordat ze hun verzending voltooien. Hierdoor wordt de algehele formulierervaring verbeterd. Door op het pictogram Bewerken te klikken, kunnen ze de ingevoerde gegevens wijzigen voordat ze het formulier verzenden.

**Voorbeeld**

![ Component van het Overzicht ](/help/adaptive-forms/assets/review-component.png){width=50%, align=center}

## Gebruik

Hieronder ziet u de redenen om de revisiecomponent in een adaptieve vorm te gebruiken:

- **Verbeterde gegevensnauwkeurigheid**: De Component van het Overzicht staat gebruikers toe om alle gegevens te herzien die zij vóór voorlegging zijn ingegaan. Hierdoor wordt de kans op fouten of omissies kleiner, zodat de verzonden gegevens correct zijn.
- **Verbeterde gebruikerservaring**: De gebruikers krijgen een duidelijke, georganiseerde samenvatting van alle informatie die zij hebben ingevuld, vandaar die hen vertrouwen geven dat de vorm volledig en nauwkeurig vóór definitieve voorlegging is, verbeterend de algemene ervaring.
- **de opsporing en de correctie van de Fout**: Het verstrekt capaciteit om informatie op het paneel of gebiedsniveau uit te geven staat gebruikers toe om fouten te verbeteren zonder terug door veelvoudige lusjes te navigeren. Het klikken van **geeft** pictogram naast een paneel of een gebied uit maakt het gemakkelijk terug te gaan en om het even welke kwesties te bevestigen.
- **Verhoogd gebruikersvertrouwen**: De gebruikers kunnen de ingegane gegevens herzien, die hen verzekeren dat de informatie die zij voorleggen correct is, wat tot minder voorleggingsfouten en groter vertrouwen in de functionaliteit van de vorm leidt.
- **verhindert onopzettelijke voorlegging**: De gebruikers klikken vaak **voorleggen** zonder alle details te herzien. De **component van het Overzicht** geeft hen een definitieve kans om hun gegevens te verifiëren, die de waarschijnlijkheid van onopzettelijke voorlegging verminderen.


## Technische details {#technical-details}

Krijg de recentste informatie over de AanpassingsComponent van de Kern van de Controle van Forms in de technische documentatie over [ GitHub ](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). Voor meer bij het ontwikkelen van de Componenten van de Kern, controleer de [ de ontwikkelaarsdocumentatie van de Componenten van de Kern ](/help/developing/overview.md).

## Dialoogvenster configureren {#configure-dialog}

U kunt de ervaring voor bezoekers gemakkelijk aanpassen met het dialoogvenster Configureren voor een naadloze gebruikerservaring.

![ Vorm Dialoog ](/help/adaptive-forms/assets/review-component-configure-dialog.png)

- **Naam** - u kunt een vormcomponent gemakkelijk met zijn unieke naam zowel in de vorm als in de regelredacteur identificeren, maar de naam moet geen ruimten of speciale karakters bevatten.

- **Titel** - met zijn Titel, kunt u een component in een vorm gemakkelijk identificeren en door gebrek, verschijnt de titel bovenop de component. Als u geen titel toevoegt, wordt de naam van de component weergegeven in plaats van de titeltekst.
- **Verberg Titel** - selecteer de optie om de Titel van de component te verbergen.
- **laat geef wijzeacties voor** toe - **laat de Acties van de Wijze voor** opties toe gebruikers toe om de ingegaan informatie te wijzigen. Gebruikers kunnen de informatie op veldniveau of paneelniveau bewerken.
   - Wanneer de gebruikers de **optie van het Gebied** selecteren, kunnen zij individuele vormgebieden tijdens de overzicht uitgeven.
   - Wanneer de gebruikers de **optie van het Comité** selecteren, kunnen zij alle gebieden binnen een specifieke sectie (paneel) uitgeven.
   - Wanneer de gebruikers het **Gebied en van het Comité** optie selecteren, kunnen zij het uitgeven pictogram naast een gebied klikken om specifieke informatie te wijzigen of naast een paneel om alle gebieden binnen dat paneel uit te geven.
   - Wanneer de gebruikers **niets** selecteren optie, kunnen zij om het even welk gebied of paneel binnen de volledige vorm uitgeven.

  Door gebrek, wordt de **1} optie van het Comité {geselecteerd.**

- **de Panelen van de Verbinding** - de **optie van de Vensters van de Verbinding** staat gebruikers toe om de panelen voor overzicht te selecteren. Wanneer deelvensters zijn gekoppeld, kunnen gebruikers de ingevoerde informatie van de geselecteerde deelvensters controleren en deze wijzigen voordat ze de gegevens verzenden.

## Usecase

Neem een voorbeeld van de Vorm van de Toepassing van de a **Lening** die uit vier lusjes bestaat, waar elk lusje specifieke informatie over de gebruiker verzamelt:

- **Persoonlijke Details**: Verzamelt de fundamentele persoonlijke details van de gebruiker, zoals naam, geboortedatum, contactinformatie, en adres.

- **Details van de Lening**: Verzamelt informatie met betrekking tot de lening, met inbegrip van het type van lening, gewenst bedrag, terugbetalingsperiode, en automatisch berekende gebieden zoals rente en maandelijkse EMI.

- **Extra Documenten**: Staat de gebruiker toe om vereiste documenten, zoals het bewijs van identiteitskaart, adresproef, en inkomensbewijs te uploaden. Het omvat ook een vakje van de verklaringsverklaring om overeenstemming met de termijnen te bevestigen.

- **Overzicht en legt Vorm** voor: Eigenschappen een Component van het Overzicht die alle input van de vorige lusjes samenvatten. Gebruikers kunnen hun gegevens controleren en bewerken voordat ze het formulier verzenden. Dit lusje omvat ook **voorlegt** knoop om de toepassing voor te leggen.

De video toont hieronder aan hoe te om de **component van het Overzicht** te vormen zodat het de gebruiker van de flexibiliteit voorziet om informatie uit te geven:

## Verwante artikelen {#related-articles}

{{more-like-this}}

## Zie ook {#see-also}

{{see-also}}

