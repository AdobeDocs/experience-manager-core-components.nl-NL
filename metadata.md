---
product: Adobe Experience Manager
description: Documentatie voor de Adobe Experience Manager Core-componenten
git-repo: https://git.corp.adobe.com/AdobeDocs/experience-manager-core-components.nl-NL
index: y
solution-title: Meer informatie en ondersteuning voor AEM
solution-hub-url: https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/home.html
getting-started-title: Aan de slag met ontwikkelen voor AEM
getting-started-url: https://docs.adobe.com/content/help/en/experience-manager-cloud-service/core-concepts/home.html
tutorials-title: AEM Tutorials
tutorials-url: https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/overview.html
translation-type: tm+mt
source-git-commit: f109463f1942349c300600acf6b94f268e8aa60e
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 16%

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

Aanvullende informatie over de metagegevens vindt u in de [interne handleiding voor het schrijven van programmacode.](https://docs.adobe.com/help/en/collaborative-doc-instructions/collaboration-guide/markdown/metadata.html#solution-metadata)
