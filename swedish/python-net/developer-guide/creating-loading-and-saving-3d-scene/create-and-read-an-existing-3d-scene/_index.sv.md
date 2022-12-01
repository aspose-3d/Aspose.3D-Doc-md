---
title: Skapa och läsa en existerande scen 3D
type: docs
weight: 10
url: /sv/python-net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API stöder att skapa de nya 3D scener från grunden och sedan spara i någon stödde filformat. Utvecklare kan också ladda en befintlig 3D Scen för ändring, tillägg eller bearbetning.
---
## **Skapa en tom 3D scen och Spara i stödda 3D Filformat**
Aspose.3D API stöder att skapa de nya 3D scener från grunden och sedan spara i någon stödde filformat. Utvecklare kan också ladda en befintlig 3D Scen för ändring, tillägg eller bearbetning.
### **Skapa ett 3D scendokument**
Följ dessa steg för att skapa ett 3D Scen-dokument med hjälp av Aspose.3D API:er:

1. Skapa en instans av klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) som representerar en 3D scene dokument.
1. Skapa en 3D scen dokument genom att kalla [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) metoden för Scene klass objekt.
#### **Skapa ett 3D scen dokument: Programmeringprover**


{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}
## **Läser en 3D**
Med hjälp av Aspose.3D API kan utvecklare ladda alla dokument som stöds. Tillgängliga konstruktörer**Scen**Klassen tillåter att göra det och de accepterar en giltig filsökvägssträng. De läsbara filformat som stöds är följande:

1. FBX 7,7 (ASCII, binära)
1. FBX 7,6 (ASCII, binära)
1. FBX 7,5 (ASCII, binära)
1. FBX 7,4 (ASCII, binära)
1. FBX 7,3 (ASCII, binära)
1. FBX 7,2 (ASCII, binära)
1. STL (ASCII, binära)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, binära)
1. X (ASCII, binära)
1. XYZ
1. Draco
1. 3MF
1. RVM (Text, binära)
1. ASE
1. USDZ
1. USD

Konstruktörer av `Scene` klass detektera 3D dokumentformat internt.
### **Läsa en 3D scen: Programmeringprover**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
