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

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "AssetInformation-InformationToScene-AddAssetInformationToScene.py" >}}
##  **Voltear sistema de coordenadas en formatos 3D**
Aspose.3D for Python via .NET API permite a los usuarios voltear el sistema de coordenadas en los formatos OBJ, 3DS, STL y U3D.

{{% alert color="primary" %}} 

Para importar un archivo 3ds y guardarlo en formato OBJ, la clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) se está utilizando en el código.

{{% /alert %}} 

En este ejemplo, volteamos el sistema de coordenadas al importar el archivo 3ds y lo guardamos en formato OBJ sin materiales.
