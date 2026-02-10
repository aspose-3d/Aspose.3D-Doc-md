---
title: Save a 3D Scene in the PDF in C#
linktitle: Save a 3D Scene in the PDF
type: docs
weight: 60
url: /net/save-a-3d-scene-in-the-pdf/
description: The Scene class of the Aspose.3D API represents a 3D scene. Developers can build a 3D scene by adding Camera, Light, polygons and various other entities. They can also now save a 3D scene in the PDF file format.
---

## **Overview**

This article explains how you can convert 3D file to PDF format using C# .NET 3D file manipulation and conversion API, first you need to [load 3D file into Scene object](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/) and then save it into PDF format. It covers wide range of topics e.g.

- Convert 3D to PDF in C#
- Convert FBX to PDF in C#
- Convert STL to PDF in C#
- Convert U3D to PDF in C#
- Convert OBJ to PDF in C#

{{% alert color="primary" %}} 

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class of the Aspose.3D API represents a 3D scene. Developers can build a 3D scene by adding Camera, Light, polygons and various other entities. They can also now save a 3D scene in the PDF file format.

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for .NET directly writes the information about the API and Version Number in output documents. For example, upon rendering a Drawing to PDF, Aspose.3D for .NET populates `Application` field with value 'Aspose.3D' and `PDF Producer` field with value, e.g 'Aspose.3D 17.9'.

Please note that you cannot instruct Aspose.3D for .NET API to change or remove this information from output Documents.

{{% /alert %}} 
## **Create a 3D PDF with a Cylinder, and Rendered in Shaded Illustration Mode with CAD Optimized Lighting**
The Save method of the `Scene` class allows to save a 3D scene in the PDF format. Developers may load any 3D supported file or build a new 3D scene, they can save a 3D scene in the PDF format as shown in this C# code example:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Create a new scene
            Scene scene = new Scene();
            // Create a cylinder child node
            scene.RootNode.CreateChildNode("cylinder", new Cylinder()).Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.DarkCyan) };
            // Set rendering mode and lighting scheme
            PdfSaveOptions opt = new PdfSaveOptions();
            opt.LightingScheme = PdfLightingScheme.CAD;
            opt.RenderMode = PdfRenderMode.ShadedIllustration;
            // Save in the PDF format
            scene.Save("output_out.pdf", opt);

{{< /highlight >}}
