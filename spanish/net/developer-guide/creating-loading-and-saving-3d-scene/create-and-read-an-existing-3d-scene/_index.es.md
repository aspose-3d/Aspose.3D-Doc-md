---
title: Crear y leer una escena 3D existente
type: docs
weight: 10
url: /es/net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API admite la creación de las nuevas escenas 3D desde cero y luego guardadas en cualquier formato de archivo compatible. Los desarrolladores también pueden cargar una escena 3D existente para la modificación, la adición o el procesamiento.
---
##  **Descripción general**
El artículo explica los siguientes temas utilizando la biblioteca de manipulación de formatos de archivo C# 3D.
- Crear una escena 3D vacía en C# desde cero
- Leer o cargar escena 3D existente en C#
- Guardar la escena 3D en formatos 3D compatibles utilizando C#
- Trabajar con propiedades de escena 3D en C#

##  **Crear una escena 3D vacía y guardar en los formatos de archivo 3D compatibles**
Aspose.3D API admite la creación de las nuevas escenas 3D desde cero y luego guardadas en cualquier formato de archivo compatible. Los desarrolladores también pueden cargar una escena 3D existente para la modificación, la adición o el procesamiento.

###  **Creación de un documento de escena 3D**
Siga estos pasos en C# para crear un documento de escena 3D utilizando las API Aspose.3D:

1. Cree una instancia de la clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) que represente un documento de escena 3D.
1. Genere un documento 3D Scene llamando al método [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) del objeto de clase Scene.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CreateEmpty3DDocument-CreateEmpty3DDocument.cs" >}}

##  **Leyendo una escena de 3D**
Con Aspose.3D API, los desarrolladores pueden cargar todos los documentos 3D compatibles. Los constructores disponibles de la clase `Scene` permiten hacerlo y aceptan una cadena de ruta de archivo válida. Los formatos de archivo legibles admitidos son los siguientes:

1. FBX 7,5 (ASCII, binario)
1. FBX 7,4 (ASCII, binario)
1. FBX 7,3 (ASCII, binario)
1. FBX 7,2 (ASCII, binario)
1. FBX 6,1 (ASCII, binario)
1. STL (ASCII, binario)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF (ASCII, binario)
1. Maya (ASCII, Binario)
1. OpenUSD (USD, USDZ)
1. Licuadora
1. DXF
1. PLY (ASCII, binario)
1. X (ASCII... Binary)
1. Draco
1. 3MF
1. RVM (Texto, binario)
1. ASE

Los constructores de la clase `Scene` detectan internamente el formato de documento 3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ReadExistingScene-ReadExistingScene.cs" >}}

##  **Trabajar con propiedades de escena 3D**
Aspose.3D API le permite leer las propiedades de la escena 3D utilizando los nodos secundarios de la escena. El siguiente ejemplo de código C# muestra el uso de esta característica.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DScene-ThreeDProperties-ThreeDProperties.cs" >}}
