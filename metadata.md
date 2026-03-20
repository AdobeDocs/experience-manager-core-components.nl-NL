---
product: adobe experience manager
solution: Experience Manager, Experience Manager Sites
type: Documentation
description: Documentatie voor de Adobe Experience Manager Core-componenten
git-repo: https://github.com/AdobeDocs/experience-manager-core-components.nl-NL
index: true
recommendations: noDisplay
source-git-commit: 7ba1374bd64686c2e7ac44398d77fb187ff60949
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# Metagegevens voor intern gebruik

De meta-gegevens in het GitHub auteurssysteem zijn hiërarchisch en worden bepaald de volgende stijgende niveaus van precedent.

1. metadata.md
1. ToC
1. Artikel

De metagegevens die zijn gedefinieerd in het bestand metadata.md, worden toegepast op de volledige repo, maar kunnen worden overschreven op de ToC- en artikelniveaus. Als de metagegevens worden genegeerd, moet dat op het laagst mogelijke niveau gebeuren.

De meta-gegevens in ervaring-manager-core-components.en repo is het vereiste minimum.

metadata.md

* `product`
* `git-repo`
* `index: true`
* `solution-title`
* `solution-hub-url`
* `getting-started-title`
* `getting-started-url`
* `tutorials-title`
* `tutorials-url`

ToCs

* `sub-product`
* `user-guide-title`

Artikel

* `title`
* `description`
* `index: false` (alleen voor vorige versies van componenten)

De extra informatie over de meta-gegevens kan in de [&#x200B; interne auteursgids worden gevonden.](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/authoring/features/metadata.html#solution)
