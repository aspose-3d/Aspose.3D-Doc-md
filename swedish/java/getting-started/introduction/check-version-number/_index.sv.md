---
title: Kontrollera versionsnummer
type: docs
weight: 80
url: /sv/java/check-version-number/
---
{{% alert color="primary" %}}

I vissa fall kanske du undrar vilken version av produkten du har. Ofta bygger vi nya rättelser (bug fixeringar för de användarscenarier som de pekar ut) och lägger ut dem i forum mot deras behov brådskande. Versionsnumret består av större versionsnummer, mindre versionsnummer och hotfix versionsnummer. Alla definierade komponenter måste vara heltal större än eller lika med 0 Formatet för versionsnumret är följande:

Major.minor.hotfix kan vi öka en del med 1 och göra en ny version. Normalt ökar vi den sista delen med 1 och bygger en ny fix för att lägga upp det i forum för användarna.

Det här dokumentet beskriver några sätt att kontrollera vilken version av komponenten som är installerad på systemet.

{{% /alert %}}

##  **Kontrollera versionsnummer manuellt**

För att ta reda på vilken version av Aspose.3D du använder manuellt:

1. Om du har Java version/fix (Aspose. 3D for Java), kan du dra upp Aspose. 3D biblioteksfil, öppna MANIFEST-filen med anteckningsblock och sök i strängen i. e... "Specification-Version: " att kontrollera dess värde.
1. Klicka på fliken Version (eller detaljer) för att kontrollera versionsnummer.

