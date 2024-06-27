---
title: Skapa och läsa en existerande 3D Scene
type: docs
weight: 10
url: /sv/python-net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API stöder skapandet av nya 3D scener från skrängen och sparas sedan i något filformat som stöds. Utvecklare kan också ladda en befintlig 3D scen för ändring, tillägg eller bearbetning.
---
##  **Skapa ett tomt 3D och spara i stödda 3D filformat**
Aspose.3D API stöder skapandet av nya 3D scener från skrängen och sparas sedan i något filformat som stöds. Utvecklare kan också ladda en befintlig 3D scen för ändring, tillägg eller bearbetning.
###  **Skapa ett dokument i 3D @ info: whatsthis**
Följ dessa steg för att skapa ett 3D Scene-dokument med Aspose.3D-programmen:

1. Skapa en instans av klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) som representerar ett 3D scenedokument.
1. Skapa ett 3D Scene-dokument genom att ringa [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)-metoden för Scene-objektet.
####  **Skapa ett 3D Scene-dokument: Programmeringsprovning**


{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}
##  **Läs en 3D Scene**
Using Aspose.3D API, developers can load all the supported 3D documents. The available constructors of the **Scene**Klassen tillåter att göra det och de accepterar en giltig filsökvägssträng. De läsbara filformat som stöds är följande:

1. FBX 7.7 (ASCII, Binära)
1. FBX 7.6 (ASCII, Binär)
1. FBX 7.5 (ASCII, Binära)
1. FBX 7.4 (ASCII, Binära)
1. FBX 7.3 (ASCII, Binära)
1. FBX 7.2 (ASCII, Binära)
1. STL (ASCII, binär)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, binär)
1. X (ASCII, binära)
1. XYZ
1. Draco
1. 3MF
1. RVM (Text, binärt)
1. ASE
1. USDZ
1. USD

Constructors of the `Scene` class detect 3D document format internally.
###  **Läs en 3D Scene: Programmeringsprovning**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
