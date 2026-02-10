---
title: Agregar un sistema de coordenadas de información de activos y voltear en formatos 3D
type: docs
weight: 10
url: /es/python-net/add-an-asset-information-and-flip-coordinate-system-in-3d-formats/
description: Los metadatos son información estructurada que describe, explica, localiza o facilita la recuperación, el uso o la gestión de un recurso de información. Aspose.3D for Python via .NET API permite a los desarrolladores definir metadatos para la escena.
---
##  **Agregar información de activos a la escena 3D**
Los metadatos son información estructurada que describe, explica, localiza o facilita la recuperación, el uso o la gestión de un recurso de información. Aspose.3D for Python via .NET API permite a los desarrolladores definir metadatos para la escena.
###  **Definir metadatos para la escena**
3D muestra producir cantidades masivas de metadatos e información de imagen. Los metadatos son un activo y parte del programa.

1. Inicialice una escena 3D usando la clase `Scene`.
1. Establecer el nombre de la aplicación/herramienta.
1. Establezca el nombre del proveedor de la aplicación/herramienta.
1. Establecer unidad de medición.
1. Establezca el factor de escala de la unidad de medición.
1. Guarde la escena 3D en el formato de archivo compatible.

En este ejemplo, asumimos que la escena es creada por una herramienta CAD llamada “Egypt” y está diseñada por “Manualdesk”:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize a 3D scene
scene = Scene()
#  Set application/tool name
scene.asset_info.application_name = "Egypt"
#  Set application/tool vendor name
scene.asset_info.application_vendor = "Manualdesk"
#  We use ancient egyption measurement unit Pole
scene.asset_info.unit_name = "pole"
#  One Pole equals to 60cm
scene.asset_info.unit_scale_factor = 0.6
#  The saved file
output = "out"  + "InformationToScene.fbx"
#  Save scene to 3D supported file formats
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
##  **Voltear sistema de coordenadas en formatos 3D**
Aspose.3D for Python via .NET API permite a los usuarios voltear el sistema de coordenadas en los formatos OBJ, 3DS, STL y U3D.

{{% alert color="primary" %}} 

Para importar un archivo 3ds y guardarlo en formato OBJ, la clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) se está utilizando en el código.

{{% /alert %}} 

En este ejemplo, volteamos el sistema de coordenadas al importar el archivo 3ds y lo guardamos en formato OBJ sin materiales.
