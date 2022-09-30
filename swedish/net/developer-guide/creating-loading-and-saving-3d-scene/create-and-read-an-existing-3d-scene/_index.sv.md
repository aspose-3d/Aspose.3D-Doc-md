---
title: Skapa och läsa en existerande scen 3D
type: docs
weight: 10
url: /sv/net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API stöder att skapa de nya 3D scener från grunden och sedan spara i någon stödde filformat. Utvecklare kan också ladda en befintlig 3D Scen för ändring, tillägg eller bearbetning.
---
## **Översikt**
Artikeln förklarar följande ämnen med hjälp av C# 3D filformat manipulationsbibliotek.
- Skapa en tom 3D scen i C# från grunden
- Läs eller ladda existerande 3D scen i C#
- Spara scenen 3D i stöd 3D Format med hjälp av C#
- Arbeta med 3D Scen objekt i C#

## **Skapa en tom 3D scen och Spara i stödda 3D Filformat**
Aspose.3D API stöder att skapa de nya 3D scener från grunden och sedan spara i någon stödde filformat. Utvecklare kan också ladda en befintlig 3D Scen för ändring, tillägg eller bearbetning.

### **Skapa ett 3D scendokument**
Följ dessa steg i C# för att skapa ett 3D Scen-dokument med hjälp av Aspose.3D API:

1. Skapa en instans av klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) som representerar en 3D scene dokument.
1. Skapa en 3D scen dokument genom att kalla [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) metoden för Scene klass objekt.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CreateEmpty3DDocument-CreateEmpty3DDocument.cs" >}}

## **Läser en 3D**
Med hjälp av Aspose.3D API kan utvecklare ladda alla dokument som stöds. De tillgängliga konstruktörerna i klassen `Scene` tillåter att göra det och de accepterar en giltig fil sökvägssträng. De läsbara filformat som stöds är följande:

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
1. Draco
1. 3MF
1. RVM (Text, binära)
1. ASE

Konstruktörer av `Scene` klass detektera 3D dokumentformat internt.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ReadExistingScene-ReadExistingScene.cs" >}}

## **Arbeta med 3D Scenegenskaper**
Aspose.3D API kan du läsa 3D Scenegenskaper som använder scenens barn Noder. Följande kodprov C# visar hur denna funktion används.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DScene-ThreeDProperties-ThreeDProperties.cs" >}}
