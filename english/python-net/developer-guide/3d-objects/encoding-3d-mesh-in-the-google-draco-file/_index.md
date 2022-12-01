---
title: Encoding 3D Mesh in the Google Draco File
type: docs
weight: 60
url: /python-net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Python via .NET API allows developers to import a 3D model, and then encode meshes in the Google Draco files. Developers can also specify the position, texture coordinates, color and normal bits as well as the compression level before encoding a mesh.
---

{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API allows developers to [import a 3D model](/3d/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), and then encode meshes in the Google Draco files. Developers can also specify the position, texture coordinates, color and normal bits as well as the compression level before encoding a mesh.

{{% /alert %}}
## **Retrieve a 3D Mesh and Encode in Google Draco File**
The `encode` method exposed by the [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) class can be used to encode a 3d mesh in the Google Draco file. It takes a [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) and [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) objects as parameters. Using the Draco save options, developers can also specify the position, texture coordinates, color and normal bits as well as the compression level before encoding a mesh.
### **Programming Sample**
This code example retrieves a Mesh of Sphere, and then encode in the Google Draco file after specifying a compression level.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.py" >}}
