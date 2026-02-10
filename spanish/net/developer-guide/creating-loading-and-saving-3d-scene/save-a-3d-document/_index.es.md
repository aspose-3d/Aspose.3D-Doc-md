---
title: Guardar un documento 3D en diferentes formatos 3D utilizando C#
linktitle: Guardar un documento 3D
type: docs
weight: 20
url: /es/net/save-a-3d-document/
description: La clase Scene de Aspose.3D API representa un documento 3D y los desarrolladores pueden guardar su objeto en cualquier formato de archivo compatible.
---
##  **Descripción general**
El artículo explica cómo puede guardar el documento 3D en varios formatos usando la biblioteca de procesamiento de documentos C# 3D, incluyendo

- Guardar un documento 3D en formato FBX con C# - AutoDesk
- Guardar un documento 3D en formato DAE usando C# - Collada
- Guardar un documento 3D en formato 3DS usando C# - Discreet 3D Studio
- Guardar un documento 3D en formato DRC usando C# - Google Draco

{{% alert color="primary" %}} 

La clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) de Aspose.3D API representa un documento 3D y los desarrolladores pueden guardar su objeto en cualquier formato de archivo compatible. Para guardar una escena 3D, simplemente use el método [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save), acepta un nombre de archivo con ruta completa o un objeto de flujo de archivo. Aspose.3D API ofrece otro parámetro `FileFormat` para especificar el formato del archivo de salida.

{{% /alert %}} 

##  **Guardar una escena 3D en formatos 3D compatibles**

El ejemplo de código C# a continuación muestra cómo guardar una escena o documento 3D en una secuencia en varios formatos 3D compatibles.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
// Load a 3D document into Aspose.3D
Scene scene = new Scene();

// Open an existing 3D scene
scene.Open("document.fbx");

// Save Scene to a stream
MemoryStream dstStream = new MemoryStream();
scene.Save(dstStream, FileFormat.FBX7500ASCII);
            
// Save Scene to a local path
scene.Save("output_out.fbx");

{{< /highlight >}}
