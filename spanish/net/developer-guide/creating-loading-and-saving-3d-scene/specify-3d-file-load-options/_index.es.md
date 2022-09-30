---
title: Especificar las opciones de carga de archivos 3D en C#
linktitle: Especificar las opciones de carga de archivos 3D
type: docs
weight: 30
url: /es/net/specify-3d-file-load-options/
description: Hay varias sobrecargas del método Scene.Open o sobrecargas del constructor de clases Scene que aceptan un objeto LoadOptions. Cada formato de carga tiene una clase correspondiente que contiene opciones de carga para ese formato de carga.
---
## **Visión de conjunto**

Este artículo explica cómo puede cargar diferentes tipos de archivos 3D utilizando sus respectivas clases de opción de carga en C# dentro del objeto Escena y luego puede[Guardarlo en diferentes formatos de archivo soportados 3D](https://docs.aspose.com/3d/net/specify-3d-file-save-options/)... Al cargar y guardar, puede realizar un número de conversiones diferentes, p. Ej.

- Convertir FBX a OBJ en C#
- Convertir 3DS a FBX en C#
- Convertir U3D a OBJ en C#
- Convertir OBJ a 3DS en C#
- Convertir X a 3DS en C#

## **3D Opciones de carga de archivos**
Hay varias sobrecargas de método [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) o sobrecargas de constructor de clase Scene que aceptan un objeto `LoadOptions`. Este debe ser un objeto de una clase derivada de la clase `LoadOptions`. Cada formato de carga tiene una clase correspondiente que contiene opciones de carga para ese formato de carga, por ejemplo, hay `ColladaSaveOptions` para el formato de guardado `FileFormat.Collada`.
### **Uso de las opciones de carga discreta 3DS**
El código C# a continuación muestra cómo establecer las opciones de carga antes de cargar un archivo Discreet 3DS.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
### **Uso de las opciones de carga Obj**
El código C# a continuación muestra cómo establecer las opciones de carga antes de cargar un archivo Obj 3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
### **Uso de las opciones de carga STL**
El código C# a continuación muestra cómo establecer las opciones de carga antes de cargar un archivo STL.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
### **Uso de las opciones de carga U3D**
El código C# a continuación muestra cómo establecer las opciones de carga antes de cargar un archivo U3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
### **Uso de las opciones de carga glTF**
El código C# a continuación muestra cómo establecer las opciones de carga antes de cargar un archivo glTF.
#### **Voltear la coordenadas de textura V/T**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
### **Uso de las opciones de carga de nivel**
El código C# a continuación muestra cómo configurar las opciones de carga antes de cargar un modelo PLY.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
### **Uso de las opciones de carga DirectX X**
El código C# a continuación muestra cómo configurar las opciones de carga antes de cargar un archivo DirectX X.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
### **Utilice las opciones de carga RVM**
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
### **Uso de opciones de carga FBX**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
