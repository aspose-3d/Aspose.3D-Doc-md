---
title: Codificación de la malla 3D en el archivo Google Draco
type: docs
weight: 30
url: /es/java/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Java API tiene soporte para importar el modelo 3D, recuperar la malla y luego codificar la malla en el archivo Google Draco.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API tiene soporte para importar el modelo 3D, recuperar la malla y luego codificar la malla en el archivo Google Draco. Los desarrolladores también pueden especificar la posición, las coordenadas de textura, el color y los bits normales, así como el nivel de compresión antes de codificar una malla.

{{% /alert %}} 
##  **Recuperar malla 3D y codificar en archivo Google Draco**
El método de codificación expuesto por la clase `DracoFormat` se puede usar para codificar una malla 3D en el archivo Google Draco. Toma un objeto `Mesh` y `DracoSaveOptions` como parámetros. Con las opciones Draco save, los desarrolladores también pueden especificar la posición, las coordenadas de textura, el color y los bits normales, así como el nivel de compresión antes de codificar una malla.
###  **Muestra de programación**
Este ejemplo de código recupera Mesh of Sphere y, a continuación, codifica en el archivo Google Draco después de especificar un nivel de compresión.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Create a sphere
Sphere sphere = new Sphere();
// Encode the sphere to Google Draco raw data using optimal compression level.
DracoSaveOptions opt = new DracoSaveOptions();
opt.setCompressionLevel(DracoCompressionLevel.OPTIMAL);
byte[] b = FileFormat.DRACO.encode(sphere.toMesh(), opt);
// Save the raw bytes to file
Files.write(Paths.get(MyDir, "SphereMeshtoDRC_Out.drc"), b);
{{< /highlight >}}
