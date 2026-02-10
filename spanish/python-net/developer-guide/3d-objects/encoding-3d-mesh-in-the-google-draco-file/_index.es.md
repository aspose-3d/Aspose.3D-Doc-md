---
title: Codificación de la malla 3D en el archivo Google Draco
type: docs
weight: 60
url: /es/python-net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Python via .NET API permite a los desarrolladores importar un modelo 3D y luego codificar mallas en los archivos Google Draco. Los desarrolladores también pueden especificar la posición, las coordenadas de textura, el color y los bits normales, así como el nivel de compresión antes de codificar una malla.
---
{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API permite a los desarrolladores [Importar un modelo 3D](/3d/es/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), y luego codificar las mallas en los archivos Google Draco. Los desarrolladores también pueden especificar la posición, las coordenadas de textura, el color y los bits normales, así como el nivel de compresión antes de codificar una malla.

{{% /alert %}}
##  **Recuperar una malla 3D y codificar en un archivo Google Draco**
El método `encode` expuesto por la clase [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) se puede usar para codificar una malla 3d en el archivo Google Draco. Toma un objeto [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) y [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) como parámetros. Usando las opciones de guardado Draco, los desarrolladores también pueden especificar la posición, las coordenadas de la textura, el color y los bits normales, así como el nivel de compresión antes de codificar una malla.
###  **Muestra de programación**
Este ejemplo de código recupera una malla de esfera y, a continuación, codifica en el archivo Google Draco después de especificar un nivel de compresión.

{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import DracoCompressionLevel, DracoSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a sphere
sphere = Sphere()
options = DracoSaveOptions()
options.compression_level = DracoCompressionLevel.OPTIMAL
#  Encode the sphere to Google Draco raw data using optimal compression level.
b = FileFormat.DRACO.encode(sphere.to_mesh(), options)
#  Save the raw bytes to file
with open("out"  + "SphereMeshtoDRC_Out.drc", "wb") as f:
    f.write(b)

{{< /highlight >}}
