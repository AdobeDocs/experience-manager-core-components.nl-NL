---
product: adobe experience manager
solution: Experience Manager, Experience Manager Sites
type: Documentation
description: Documentatie voor de Adobe Experience Manager Core-componenten
git-repo: https://github.com/AdobeDocs/experience-manager-core-components.nl-NL
index: y
recommendations: noDisplay
source-git-commit: 55e5ef9271b07d8fffc7b396c890af1637309ff3
workflow-type: tm+mt
source-wordcount: '101'
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
* `index: y`
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
* `index: n` (alleen voor vorige versies van componenten)

Aanvullende informatie over de metagegevens vindt u in het gedeelte [interne ontwerphandleiding.](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/authoring/features/metadata.html#solution)
