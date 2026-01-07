---
title: "Läs 3D-dokument"
type: docs
weight: 30
url: "/sv/nodejs-java/read-3d-document/"
description: "Aspose.3D för Node.js via Java API har stöd för att läsa olika typer av 3D-dokument."
---

## **Lista över 3D-stödda format (import)**
Aspose.3D för Node.js via Java API har stöd för att läsa olika typer av 3D-dokument. De tillgängliga konstruktorerna för klassen `Scene` hjälper till med detta och de accepterar en giltig sökvägssträng för fil. De stödda läsbara filformaten är som följer:

1. FBX 7.5 (ASCII, Binär)
1. FBX 7.4 (ASCII, Binär)
1. FBX 7.3 (ASCII, Binär)
1. FBX 7.2 (ASCII, Binär)
1. STL (ASCII, Binär)
1. WavefrontOBJ
2. Discreet3DS
3. Universal3D
4. Collada
5. glTF
6. DXF
7. PLY (ASCII, Binär)
8. X (ASCII, Binär)
9. Draco
10. 3MF
11. RVM (Text, Binär)
12. ASE

Konstruktorerna för klassen Scene detekterar 3D-dokumentformat internt.
## **Importera 3D-dokument**
Aspose.3D för Java API har stöd för att importera olika typer av 3D-dokument för ändring, tillägg och bearbetning.
### **Läsa en 3D-scen: Programmerings exempel**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisera ett objekt av klassen Scene
var scene = new aspose.threed.Scene();

// Ladda ett befintligt 3D-dokument
scene.open( "document.obj");

{{< /highlight >}}