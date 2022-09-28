---
title: Create and Read an Existing 3D Scene
type: docs
weight: 10
url: /net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API supports creating the new 3D scenes from the scratch and then save in any supported file format. Developers can also load an existing 3D Scene for the modification, addition or processing purposes.
---

## **Overview**
The article explains the following topics using C# 3D file formats manipulation library.
- Create an Empty 3D Scene in C# from scratch
- Read or Load Existing 3D Scene in C#
- Save the 3D Scene in Supported 3D Formats using C#
- Work with 3D Scene Properties in C#

## **Create an Empty 3D Scene and Save in Supported 3D File Formats**
Aspose.3D API supports creating the new 3D scenes from the scratch and then save in any supported file format. Developers can also load an existing 3D Scene for the modification, addition or processing purposes.

### **Creating a 3D Scene Document**
Please follow these steps in C# to create a 3D Scene document using the Aspose.3D APIs:

1. Create an instance of the [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class that represents a 3D scene document.
1. Generate a 3D Scene document by calling the [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) method of the Scene class object.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CreateEmpty3DDocument-CreateEmpty3DDocument.cs" >}}

## **Reading a 3D Scene**
Using Aspose.3D API, developers can load all the supported 3D documents. The available constructors of the `Scene` class allow to do so and they accept a valid file path string. The supported readable file formats are as follows:

1. FBX 7.5 (ASCII, Binary)
1. FBX 7.4 (ASCII, Binary)
1. FBX 7.3 (ASCII, Binary)
1. FBX 7.2 (ASCII, Binary)
1. STL (ASCII, Binary)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, Binary)
1. X (ASCII, Binary)
1. Draco
1. 3MF
1. RVM (Text, Binary)
1. ASE

Constructors of the `Scene` class detect 3D document format internally.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ReadExistingScene-ReadExistingScene.cs" >}}

## **Working with 3D Scene Properties**
Aspose.3D API lets you read 3D Scene properties using the scene's child nodes. The following C# code sample demonstrates the usage of this feature.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DScene-ThreeDProperties-ThreeDProperties.cs" >}}
