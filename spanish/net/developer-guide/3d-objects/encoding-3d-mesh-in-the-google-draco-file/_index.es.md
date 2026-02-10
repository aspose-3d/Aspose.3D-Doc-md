---
title: Codificación de la malla 3D en el archivo Google Draco
type: docs
weight: 60
url: /es/net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for .NET API permite a los desarrolladores importar un modelo 3D y luego codificar mallas en los archivos Google Draco. Los desarrolladores también pueden especificar la posición, las coordenadas de textura, el color y los bits normales, así como el nivel de compresión antes de codificar una malla.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API permite a los desarrolladores [Importar un modelo 3D](/3d/es/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), y luego codificar las mallas en los archivos Google Draco. Los desarrolladores también pueden especificar la posición, las coordenadas de textura, el color y los bits normales, así como el nivel de compresión antes de codificar una malla.

{{% /alert %}}
##  **Recuperar una malla 3D y codificar en un archivo Google Draco**
El método `Encode` expuesto por la clase [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) se puede usar para codificar una malla 3d en el archivo Google Draco. Toma un objeto [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) y [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) como parámetros. Usando las opciones de guardado Draco, los desarrolladores también pueden especificar la posición, las coordenadas de la textura, el color y los bits normales, así como el nivel de compresión antes de codificar una malla.
###  **Muestra de programación**
Este ejemplo de código recupera un `Mesh` de `Sphere` y, a continuación, codifica en el archivo Google Draco después de especificar un nivel de compresión.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
            
// Create a sphere
var sphere = new Sphere();
// Encode the sphere to Google Draco raw data using optimal compression level.
var b = FileFormat.Draco.Encode(sphere.ToMesh(), 
    new DracoSaveOptions() { CompressionLevel = DracoCompressionLevel.Optimal });
// Save the raw bytes to file
File.WriteAllBytes(RunExamples.GetOutputFilePath("SphereMeshtoDRC_Out.drc"), b);

{{< /highlight >}}
