---
title: Crear y leer una escena existente 3D
type: docs
weight: 10
url: /es/net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API admite la creación de las nuevas escenas 3D desde cero y luego guardar en cualquier formato de archivo compatible. Los desarrolladores también pueden cargar una escena 3D existente para fines de modificación, adición o procesamiento.
---
## **Visión de conjunto**
El artículo explica los siguientes temas utilizando la biblioteca de manipulación de formatos de archivo C# 3D.
- Crear una escena vacía 3D en C# desde cero
- Leer o cargar la escena existente 3D en C#
- Guarde la escena 3D en los formatos soportados 3D usando C#
- Trabajar con propiedades de escena 3D en C#

## **Crear una escena vacía 3D y guardar en formatos de archivo soportados 3D**
Aspose.3D API admite la creación de las nuevas escenas 3D desde cero y luego guardar en cualquier formato de archivo compatible. Los desarrolladores también pueden cargar una escena 3D existente para fines de modificación, adición o procesamiento.

### **Creación de un documento de escena 3D**
Siga estos pasos en C# para crear un documento de escena 3D usando las APIs Aspose.3D:

1. Cree una instancia de la clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) que representa un documento de escena 3D.
1. Genere un documento de escena 3D llamando al método [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) del objeto de clase Scene.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CreateEmpty3DDocument-CreateEmpty3DDocument.cs" >}}

## **Lectura de una escena 3D**
Usando Aspose.3D API, los desarrolladores pueden cargar todos los documentos 3D compatibles. Los constructores disponibles de la clase `Scene` lo permiten y aceptan una cadena de ruta de archivo válida. Los formatos de archivo legibles admitidos son los siguientes:

1. FBX 7,5 (ASCII, binario)
1. FBX 7,4 (ASCII, binario)
1. FBX 7,3 (ASCII, binario)
1. FBX 7,2 (ASCII, binario)
1. STL (ASCII, binario)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, binario)
1. X (ASCII, binario)
1. Draco
1. 3MF
1. RVM (texto, binario)
1. ASE

Los constructores de la clase `Scene` detectan internamente el formato de documento 3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ReadExistingScene-ReadExistingScene.cs" >}}

## **Trabajando con propiedades de escena 3D**
Aspose.3D API le permite leer las propiedades de la escena 3D utilizando los nodos secundarios de la escena. La siguiente muestra de código C# demuestra el uso de esta función.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DScene-ThreeDProperties-ThreeDProperties.cs" >}}
