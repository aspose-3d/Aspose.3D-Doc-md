---
title: Read 3D document
type: docs
weight: 30
url: /nodejs-java/read-3d-document/
description: Aspose.3D for Node.js via Java API has support of reading various type of 3D documents.
---

## **List of 3D supported formats (import)**
Aspose.3D for Node.js via Java API has support of reading various type of 3D documents. The available constructors of the `Scene` class helps to do so and they accept a valid file path string. The supported readable file formats are as follows:

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

The constructors of Scene class detect 3D document format internally.
## **Import 3D document**
Aspose.3D for Java API has support of importing various types of 3D document for the modification, addition and processing purposes.
### **Reading a 3D Scene: Programming Samples**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialize a Scene class object
var scene = new aspose.threed.Scene();

// Load an existing 3D document
scene.open( "document.obj");

{{< /highlight >}}

