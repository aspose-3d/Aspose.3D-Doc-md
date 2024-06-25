---
title: Especificar las opciones de carga de archivos 3D en C#
linktitle: Especificar 3D Opciones de carga de archivos
type: docs
weight: 30
url: /es/net/specify-3d-file-load-options/
description: Hay varias sobrecargas del método Scene.Open o sobrecargas del constructor de clases Scene que aceptan un objeto LoadOptions. Cada formato de carga tiene una clase correspondiente que contiene opciones de carga para ese formato de carga.
---
##  **Descripción general**

Este artículo explica cómo puede cargar diferentes tipos de archivos 3D utilizando sus respectivas clases de opción de carga en C# dentro del objeto Scene y luego puede [Guardarlo en diferentes formatos de archivo 3D compatibles](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). Al cargar y guardar, puede realizar varias conversiones diferentes, p.

- Convierte FBX a OBJ en C#
- Convierte 3DS a FBX en C#
- Convierte U3D a OBJ en C#
- Convierte OBJ a 3DS en C#
- Convertir X a 3DS en C#

##  **3D Opciones de carga de archivos**
Hay varias sobrecargas de método [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) o sobrecargas de constructor de clase Scene que aceptan un objeto `LoadOptions`. Este debe ser un objeto de una clase derivada de la clase `LoadOptions`. Cada formato de carga tiene una clase correspondiente que contiene opciones de carga para ese formato de carga, por ejemplo, hay `ColladaSaveOptions` para el formato de guardado `FileFormat.Collada`.
###  **Uso de las opciones de carga discreto 3DS**
El código C# a continuación muestra cómo establecer las opciones de carga antes de cargar un archivo Discreet 3DS.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
###  **Uso de las opciones de carga Obj**
El siguiente código C# muestra cómo establecer las opciones de carga antes de cargar un archivo 3D Obj.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
###  **Uso de las opciones de carga STL**
El siguiente código C# muestra cómo establecer las opciones de carga antes de cargar un archivo STL.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
###  **Uso de las opciones de carga U3D**
El siguiente código C# muestra cómo establecer las opciones de carga antes de cargar un archivo U3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
###  **Uso de las opciones de carga glTF**
El siguiente código C# muestra cómo establecer las opciones de carga antes de cargar un archivo glTF.
####  **Voltear la coordenadas de textura V/T**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
###  **Uso de las opciones de carga de nivel**
El siguiente código C# muestra cómo establecer las opciones de carga antes de cargar un modelo PLY.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
###  **Uso de las opciones de carga de DirectX X**
El siguiente código C# muestra cómo establecer las opciones de carga antes de cargar un archivo DirectX X.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
###  **Usar opciones de carga RVM**
**C#**

{{< highlight "java" >}}

 // set load options of RVM

Scene scene = new Scene();

var opt = new RvmLoadOptions()

{

    CylinderRadialSegments = 32,

    DishLatitudeSegments = 16,

    DishLongitudeSegments = 24,

    TorusTubularSegments = 40

};

// import RVM

scene.Open("LAD-TOP.rvm", opt);

// save in the OBJ format

scene.Save("LAD-TOP.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
###  **Uso de las opciones de carga FBX**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
