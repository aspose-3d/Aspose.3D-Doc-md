---
title: Skapa och läsa en existerande 3D Scene
type: docs
weight: 10
url: /sv/net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API stöder skapandet av nya 3D scener från skrängen och sparas sedan i något filformat som stöds. Utvecklare kan också ladda en befintlig 3D scen för ändring, tillägg eller bearbetning.
---
##  **Översikt**
The article explains the following topics using C# 3D file formats manipulation library.
- Skapa en tom 3D Scene i C# från början.
- Läs eller ladda existerande 3D Scene i C#
- Spara 3D i format som stöds med 3D med C#
- Arbeta med 3D Scenegenskaper i C#

##  **Skapa ett tomt 3D och spara i stödda 3D filformat**
Aspose.3D API stöder skapandet av nya 3D scener från skrängen och sparas sedan i något filformat som stöds. Utvecklare kan också ladda en befintlig 3D scen för ändring, tillägg eller bearbetning.

###  **Skapa ett dokument i 3D @ info: whatsthis**
Följ dessa steg i C# för att skapa ett 3D-dokument med Aspose. 3D API:

1. Skapa en instans av klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) som representerar ett 3D scenedokument.
1. Skapa ett 3D Scene-dokument genom att ringa [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)-metoden för Scene-objektet.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CreateEmpty3DDocument-CreateEmpty3DDocument.cs" >}}

##  **Läs en 3D Scene**
Using Aspose.3D API, developers can load all the supported 3D documents. The available constructors of the `Scene` class allow to do so and they accept a valid file path string. The supported readable file formats are as follows:

1. FBX 7.5 (ASCII, Binära)
1. FBX 7.4 (ASCII, Binära)
1. FBX 7.3 (ASCII, Binära)
1. FBX 7.2 (ASCII, Binära)
1. FBX 6.1 (ASCII, binär)
1. STL (ASCII, binär)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF (ASCII, binär)
1. Maya (ASCII, binära)
1. OpenUSD (USD, USDZ)
1. BlenderName
1. DXF
1. PLY (ASCII, binär)
1. X (ASCII, binära)
1. Draco
1. 3MF
1. RVM (Text, binärt)
1. ASE

Constructors of the `Scene` class detect 3D document format internally.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ReadExistingScene-ReadExistingScene.cs" >}}

##  **Arbetar med 3D Scenegenskaper**
Aspose.3D API låter dig läsa 3D Scenegenskaper med hjälp av scenens barnnoder. Följande C# kodprov visar hur denna funktion används.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DScene-ThreeDProperties-ThreeDProperties.cs" >}}
