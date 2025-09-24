---
title: Aspose.3D Dokumentobjektmodell (DOM)
type: docs
weight: 20
url: "/sv/nodejs-java/aspose-3d-document-object-model"
description: "Varje 3D-scen kan bestå av valfritt antal vyer. Med Aspose.3D för nodejs-java API kan utvecklare fånga en eller flera vyer i en enda skärmdump. De kan rendera den i ett GUI-baserat nodejs-java-applikation eller en bild."
---

Aspose.3D Dokumentobjektmodell (DOM) är en kraftfull in-memory representation av en 3D-scen. Det ger utvecklare möjlighet att läsa, manipulera och modifiera innehållet och formateringen av en 3D-scen programmatiskt.

I detta avsnitt kommer vi att utforska de viktigaste klasserna i Aspose.3D DOM och deras relationer. Genom att använda dessa klasser kan du få programmatisk åtkomst till olika element i en 3D-scen.

Låt oss dyka in i de viktigaste klasserna i Aspose.3D DOM:

* **Scene**: Scene-klassen representerar roten i 3D-scenens hierarki. Den fungerar som en container för alla andra element och ger metoder för att manipulera hela scenen.
* **Node**: Noder är byggstenarna i en 3D-scen. De representerar individuella objekt eller entiteter i scenen, såsom mesh, ljus, kameror eller grupper. Noder kan transformeras, animeras och textureras.
* **Entities**: Entities-klasserna omfattar ett brett utbud av objekt och element som utgör en 3D-scen. Det inkluderar entiteter som mesh, ljus, kameror, profiler och mer. Dessa entiteter fungerar som byggstenar, vilket gör att du kan skapa komplexa scener genom att kombinera och manipulera dem programmatiskt. Entities-kategorin ger åtkomst och kontroll över dessa grundläggande element i en 3D-scen.
* **Materials**: Materials-klasserna handlar om att definiera de visuella egenskaperna hos objekt i en 3D-scen. Det ger verktyg för att programmatiskt skapa, modifiera och styra material, vilket bestämmer hur ljus interagerar med ytor. Genom att justera egenskaper som färg, textur, transparens och reflektion kan du uppnå olika visuella effekter och anpassa utseendet på dina 3D-modeller.
* **Animations**: Animation-klasserna fokuserar på att skapa och styra rörelse och transformationer i en 3D-scen. Det gör att du programmatiskt kan definiera och manipulera animationer, vilket gör att objekt kan röra sig, rotera, skala eller ändra egenskaper över tid. Med denna kategori kan du ge dynamiska och interaktiva element till dina 3D-scener.

Genom att använda Aspose.3D DOM-klasserna som nämnts ovan kan du programmatiskt interagera med och manipulera innehållet och strukturen i en 3D-scen. Detta ger flexibilitet och kontroll när du arbetar med 3D-modeller i dina applikationer.


## Scenstruktur

När Aspose.3D läser en 3D-fil i minnet genereras objekt av olika typer för att representera de olika elementen i 3D-scenen.

Scenstrukturen i Aspose.3D följer kompositdesignmönstret, vilket erbjuder flexibilitet och organisation:

* Noder fungerar som containrar som kan innehålla andra noder, vilket möjliggör gruppering av olika objekt i scenen.
* Varje nod kan ha sin egen transformation, som också tillämpas på dess barnnoder.
* Alla spatiala entitetstyper i Aspose.3D måste placeras under en Node-instans. Detta säkerställer att objekt som mesh, ljus, kameror och andra element är organiserade i scenens hierarki.
* Noder kan innehålla flera material, och förhållandet mellan polygoner och material som är fästa vid en nod hanteras med hjälp av `VertexElementMaterial`-konceptet i Mesh-objektet.

![Scen hierarki](scene.png)

## Spatiala Entiteter
Alla spatiala entiteter i Aspose.3D ärver från `Entity`-klassen, vilket fungerar som grundläggande byggstenar för att konstruera virtuella miljöer. Aspose.3D kategoriserar dessa entiteter i flera huvudkategorier, var och en med sitt eget specifika syfte och funktionalitet.

![Entiteter](entity.png)

* **Primitive**: `Primitive`-klassen fungerar som basklass för alla proceduriella 3D-geometrier i Aspose.3D, såsom `Cylinder`, `Torus` och `Sphere`. Dessa geometrier kan definieras med ett minimalt antal parametrar, vilket gör det bekvämt att skapa grundläggande 3D-former.
* **Geometry**: Geometrier i Aspose.3D består vanligtvis av hörn, kanter och polygoner som definierar formen och strukturen hos ett 3D-objekt.
* **MirroredProfile**: Denna profiltyp gör att du kan spegla en befintlig profil längs Y-axeln och skapa en symmetrisk form.
* **ArbitraryProfile**: Med den godtyckliga profilimplementeringen kan du mappa en godtycklig kurva för att skapa en sluten profil.
* **Text**: Aspose.3D inkluderar förmågan att generera profiler från text med ett angivet teckensnitt.
* **Camera and light**:
* **Material types**:
* **Animation objects relationship**:
* **A scene with animations**:

En scen med animationer kan ha denna typ av struktur:

![Animations Sample](animation_relations.png)