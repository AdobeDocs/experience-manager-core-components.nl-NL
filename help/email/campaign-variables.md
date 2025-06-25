---
title: Campagnevariabelen
description: Gebruik campagnevariabelen als plaatsaanduidingen om persoonlijke e-mailinhoud samen te stellen.
role: Architect, Developer, Admin, User
exl-id: 124ff5bf-6612-4baf-b0ff-6b1a95b455c1
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---


# Campagnevariabelen {#campaign-variables}

Gebruik campagnevariabelen om persoonlijke e-mailinhoud samen te stellen. Campagnevariabelen fungeren als plaatsaanduidingen voor Adobe Campaign-waarden die u in uw e-mailinhoud kunt invoegen. Wanneer de inhoud via Adobe Campaign wordt verzonden, worden deze variabelen vervangen door de gepersonaliseerde inhoud van de ontvanger.

## Gebruik {#usage}

Met de E-mail Core-componenten zijn campagnevariabelen gemakkelijk toegankelijk via personalisatieknoppen naast veelgebruikte tekstvelden. Als u hierop drukt, wordt een dialoogvenster weergegeven waarin u een verpersoonlijkingsveld kunt selecteren.

De lijst met beschikbare personalisatievelden is gesynchroniseerd met uw Adobe Campaign-exemplaar. De velden worden in het schema in Adobe Campaign beheerd `nms:seedMember` . Alle velden in `nms:seedMember` moeten ook aanwezig zijn in de tabel met ontvangers.

## Dialoogvenster Adobe Campaign-variabele selecteren {#dialog}

Het dialoogvenster Adobe Campaign-variabele selecteren is beschikbaar in veel bewerkingsdialoogvensters van de e-mailkerncomponenten. Om het eenvoudig te gebruiken klik op het **Uitgezochte de Variabele van Adobe Campaign** pictogram naast het toepasselijke gebied. Dit pictogram kan twee vormen aannemen.

![ knoop van Adobe Campaign ](/help/email/assets/campaign-button.png)
![ Uitgezochte Adobe Campaign veranderlijk pictogram ](/help/email/assets/select-adobe-campaign-variable-icon.png)

Het klikken van beide pictogrammen opent **Uitgezochte de Variabele van Adobe Campaign** dialoog.

![ Uitgezochte de Variabele van Adobe Campaign dialoog ](assets/select-campaign-variable-dialog.png)

Gebruik de kolomweergave om de variabele te zoeken die u wilt invoegen. Wanneer u op een knooppunt in een kolom klikt, worden de onderliggende items in een nieuwe kolom rechts van het knooppunt weergegeven. Op deze manier kunt u door de structuur van de variabele-inhoud navigeren.

Selecteer de variabele die u wilt invoegen en klik op het vinkje rechtsboven in het dialoogvenster.

![ geselecteerde Variabele van Adobe Campaign ](assets/select-campaign-variable-dialog-selected.png)

De variabele wordt vervolgens ingevoegd in het veld van het dialoogvenster Bewerken van de E-mailkerncomponent.

![ variabele van de Campagne die in wordt opgenomen uitgeeft dialoog ](assets/campaign-variable.png)

Klik op de X linksboven in het dialoogvenster om het dialoogvenster te annuleren en te sluiten.
