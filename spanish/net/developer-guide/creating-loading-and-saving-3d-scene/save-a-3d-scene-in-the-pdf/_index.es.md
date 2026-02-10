---
title: Guardar una escena 3D en PDF en C#
linktitle: Guardar una escena 3D en el PDF
type: docs
weight: 60
url: /es/net/save-a-3d-scene-in-the-pdf/
description: La clase Scene de Aspose.3D API representa una escena 3D. Los desarrolladores pueden construir una escena 3D añadiendo cámara, luz, polígonos y varias otras entidades. Ahora también pueden guardar una escena 3D en el formato de archivo PDF.
---
##  **Descripción general**

Este artículo explica cómo puede convertir un archivo 3D al formato PDF usando C# .NET 3D manipulación y conversión de archivos API, primero necesita [Cargar el archivo 3D en el objeto Scene](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/) y luego guardarlo en el formato PDF. Cubre una amplia gama de temas, por ejemplo.

- Convierte 3D a PDF en C#
- Convierte FBX a PDF en C#
- Convierte STL a PDF en C#
- Convierte U3D a PDF en C#
- Convierte OBJ a PDF en C#

{{% alert color="primary" %}} 

La clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) de la Aspose.3D API representa una escena 3D. Los desarrolladores pueden construir una escena 3D agregando Cámara, Luz, polígonos y varias otras entidades. Ahora también pueden guardar una escena 3D en el formato de archivo PDF.

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for .NET escribe directamente la información sobre el API y el número de versión en los documentos de salida. Por ejemplo, al representar un dibujo a PDF, Aspose.3D for .NET rellena el campo `Application` con el valor 'Aspose.3D' y `PDF Producer` campo con valor, e.g 'Aspose.3D 17,9'.

Tenga en cuenta que no puede indicar a Aspose.3D for .NET API que cambie o quite esta información de los documentos de salida.

{{% /alert %}} 
##  **Cree un 3D PDF con un cilindro y renderizado en modo de ilustración sombreada con CAD Iluminación optimizada**
El método Save de la clase `Scene` permite guardar una escena 3D en el formato PDF. Los desarrolladores pueden cargar cualquier archivo compatible con 3D o construir una nueva escena 3D, pueden guardar una escena 3D en el formato PDF como se muestra en este ejemplo de código C#:

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
