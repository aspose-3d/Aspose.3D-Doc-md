---
title: Guardar un documento 3D
type: docs
weight: 20
url: /es/python-net/save-a-3d-document/
description: La clase Scene de Aspose.3D API representa un documento 3D y los desarrolladores pueden guardar su objeto en cualquier formato de archivo compatible.
---
{{% alert color="primary" %}} 

La clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) de Aspose.3D API representa un documento 3D y los desarrolladores pueden guardar su objeto en cualquier formato de archivo compatible. Para guardar una escena 3D, simplemente use el método [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save), acepta un nombre de archivo con ruta completa o un objeto de flujo de archivo. Aspose.3D API ofrece otro parámetro `FileFormat` para especificar el formato del archivo de salida.

{{% /alert %}} 
##  **Guardar una escena 3D**


El siguiente ejemplo de código muestra cómo guardar un documento en una secuencia.

{{< highlight "python" >}}
import aspose.threed as a3d
import io
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
# Load a 3D document into Aspose.3D
scene = a3d.Scene.from_file("document.fbx")

# Save Scene to a stream
dstStream = io.BytesIO()
scene.save(dstStream, a3d.FileFormat.FBX7500ASCII);

{{< /highlight >}}
