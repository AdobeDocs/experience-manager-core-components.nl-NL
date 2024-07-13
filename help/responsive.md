---
title: Responsief ontwerp van de kerncomponenten
description: Leer over het ontvankelijke ontwerp van de Componenten van de Kern en hoe het uw project kan beïnvloeden.
role: Architect, Developer, Admin, User
exl-id: c0eff174-6803-4b44-aeb1-eae3bc8a36ea
source-git-commit: 5f49fb45869d1721e16a787a2c6ff927b6ad49fe
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Responsief ontwerp van de kerncomponenten {#responsive-design}

Alle Core Components zijn ontworpen om volledig te reageren, zodat u over alle apparaten probleemloos kunt genieten. Het is belangrijk om op te merken dat sommige geavanceerde componenten, zoals [ Carousel, ](/help/components/carousel.md) [ Lusjes, ](/help/components/tabs.md) en [ Componenten van de Accordeon, ](/help/components/accordion.md) specifieke overweging binnen de context van het het uitvoeren project kunnen vereisen om ontvankelijkheid in alle voorwaarden te handhaven.

Gezien de diverse manieren kunnen deze componenten ontvankelijk gedrag vertonen, en in het engagement van de Adobe om de Componenten van de Kern lichtgewicht uit-van-de-doos te houden, wordt de verantwoordelijkheid voor het uitvoeren van gedetailleerde responsieve aspecten opzettelijk aan het project overgelaten.

Op nauwe schermen kan de component Tabs zich bijvoorbeeld aanpassen door brede tabbladen op nieuwe regels te splitsen, door verticaal schuiven toe te staan, door tabbladen in vervolgkeuzelijsten te transformeren of door een accordeonstijl aan te nemen. Wegens het potentiële effect op prestaties dat het uitvoeren van al die gedragingen zou veroorzaken, zijn [ clientlibs ](/help/developing/including-clientlibs.md#provided) voorgenomen als uitgangspunt voor implementoren eerder dan een exhaustieve oplossing.
