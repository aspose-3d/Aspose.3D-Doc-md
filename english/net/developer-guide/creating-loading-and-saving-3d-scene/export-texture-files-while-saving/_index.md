---
title: Export texture files while saving 3D scene
type: docs
weight: 10
url: /net/export-texture-files-while-saving-3d-scene
description: Using Aspose.3D for .NET, developers can export texture files to file system while saving 3D scene.
---

{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), When exporting a scene to files, it's often necessary to export the textures, whether embedded or external, to the same directory. Aspose.3D for .NET facilitates this process, ensuring that all textures are properly managed and stored along with the exported scene. This guide demonstrates how to achieve this.

{{% /alert %}}

To export a scene and ensure that all associated textures are saved to the same directory, follow these steps:


{{% highlight csharp %}}

Scene scene = Scene.FromFile(@"BoomBox.glb");
var opt = new ObjSaveOptions();
opt.ExportTextures = true;
scene.Save(@"D:\tmp\boombox\output.obj", opt);

{{% /highlight %}}


All `SaveOptions` objects in Aspose.3D include the `ExportTextures` property, which simplifies the process of managing textures during export. This property ensures that all textures, whether external or embedded, are saved to the specified output directory. This feature is compatible with various file formats that support texture exporting, such as FBX, 3DS, OBJ, USD, GLTF, and DAE.



Explanation

1.  Load the Scene: The scene is loaded from the input file.
1.  Configure Save Options: Set `ExportTextures` to `true`.
1.  Export the Scene: The scene is saved to the output directory with the updated texture paths.


By leveraging the `ExportTextures` property in `SaveOptions`, you can seamlessly export 3D scenes along with their textures, ensuring that all necessary assets are organized in a single directory. This feature enhances the portability and ease of use of 3D files across various platforms and applications.

## **Resources**

1. [Online Tutorial](https://products.aspose.com/3d/tutorial/)
1. [SaveOptions](https://reference.aspose.com/3d/net/aspose.threed.formats/saveoptions/)