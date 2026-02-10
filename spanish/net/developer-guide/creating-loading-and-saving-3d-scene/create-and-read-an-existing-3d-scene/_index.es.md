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

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.Save("document.fbx");

{{< /highlight >}}

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

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The path to the documents directory.

// Initialize a Scene class object
Scene scene = new Scene();
// Load an existing 3D document
scene.Open("document.fbx");


{{< /highlight >}}

##  **Trabajar con propiedades de escena 3D**
Aspose.3D API le permite leer las propiedades de la escena 3D utilizando los nodos secundarios de la escena. El siguiente ejemplo de código C# muestra el uso de esta característica.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Scene scene = Scene.FromFile("EmbeddedTexture.fbx");
Material material = scene.RootNode.ChildNodes[0].Material;
PropertyCollection props = material.Properties;
//List all properties using foreach
foreach (var prop in props)
{
    Console.WriteLine("{0} = {1}", prop.Name, prop.Value);
}
//or using ordinal for loop
for (int i = 0; i < props.Count; i++)
{
    var prop = props[i];
    Console.WriteLine("{0} = {1}", prop.Name, prop.Value);
}
//Get property value by name
var diffuse = props["Diffuse"];
Console.WriteLine(diffuse);
//modify property value by name
props["Diffuse"] = new Vector3(1, 0, 1);
//Get property instance by name
Property pdiffuse = props.FindProperty("Diffuse");
Console.WriteLine(pdiffuse);
//Since Property is also inherited from A3DObject
//It's possible to get the property of the property
Console.WriteLine("Property flags = {0}", pdiffuse.GetProperty("flags"));
//and some properties that only defined in FBX file:
Console.WriteLine("Label = {0}", pdiffuse.GetProperty("label"));
Console.WriteLine("Type Name = {0}", pdiffuse.GetProperty("typeName"));
//so traversal on property's property is possible
foreach (var pp in pdiffuse.Properties)
{
    Console.WriteLine("Diffuse.{0} = {1}", pp.Name, pp.Value);
}

{{< /highlight >}}
