---
title: Encoding 3D Mesh in the Google Draco File
type: docs
weight: 30
url: /java/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Java API has support of importing 3D model, retrieve mesh, and then encode mesh in the Google Draco file.
---

{{% alert color="primary" %}} 

Aspose.3D for Java API has support of importing 3D model, retrieve mesh, and then encode mesh in the Google Draco file. Developers can also specify the position, texture coordinates, color and normal bits as well as the compression level before encoding a mesh.

{{% /alert %}} 
## **Retrieve 3D Mesh and Encode in Google Draco File**
The encode method exposed by the `DracoFormat` class can be used to encode a 3D mesh in the Google Draco file. It takes a `Mesh` and `DracoSaveOptions` objects as parameters. With the Draco save options, developers can also specify the position, texture coordinates, color and normal bits as well as the compression level before encoding a mesh.
### **Programming Sample**
This code example retrieves Mesh of Sphere, and then encode in the Google Draco file after specifying a compression level.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-Encode3DMeshinGoogleDraco.java" >}}
