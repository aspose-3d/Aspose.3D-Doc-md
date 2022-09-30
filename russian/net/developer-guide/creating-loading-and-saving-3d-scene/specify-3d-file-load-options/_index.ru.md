---
title: Укажите параметры загрузки файла 3D в C#
linktitle: Укажите параметры нагрузки на файл 3D
type: docs
weight: 30
url: /ru/net/specify-3d-file-load-options/
description: Существует несколько перегрузок метода Scene.Open или перегрузок конструктора класса Scene, которые принимают объект LoadOptions. Каждый формат нагрузки имеет соответствующий класс, который содержит параметры загрузки для этого формата нагрузки.
---
## **Обзор**

В этой статье объясняется, как вы можете загружать различные типы файлов 3D, используя их соответствующие классы опций нагрузки в C# внутри объекта Scene, а затем вы можете[Сохранить его в различных форматах поддерживаемых файлов 3D](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). Загружая и сохраняя, вы можете выполнять количество различных преобразований, например

- Конвертировать FBX в OBJ в C#
- Конвертировать 3DS в FBX в C#
- Конвертировать U3D в OBJ в C#
- Конвертировать OBJ в 3DS в C#
- Конвертировать X в 3DS в C#

## **3D Варианты нагрузки файла**
Существует несколько перегрузок метода [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) или перегрузок конструктора класса Scene, которые принимают объект `LoadOptions`. Это должен быть объект класса, производного от класса `LoadOptions`. Каждый формат нагрузки имеет соответствующий класс, который содержит параметры загрузки для этого формата загрузки, например, есть `ColladaSaveOptions` для формата сохранения `FileFormat.Collada`.
### **Использование сдерженных вариантов нагрузки 3DS**
Код C# ниже показывает, как установить параметры загрузки перед загрузкой файла Discreet 3DS.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
### **Использование опций нагрузки Obj**
Код C# ниже показывает, как установить параметры загрузки перед загрузкой файла 3D Obj.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
### **Использование вариантов нагрузки STL**
Код C# ниже показывает, как установить параметры загрузки перед загрузкой файла STL.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
### **Использование вариантов нагрузки U3D**
Код C# ниже показывает, как установить параметры загрузки перед загрузкой файла U3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
### **Использование вариантов нагрузки glTF**
Код C# ниже показывает, как установить параметры загрузки перед загрузкой файла glTF.
#### **Переверните координату текстуры V/T**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
### **Использование опций нагрузки Ply**
Код C# ниже показывает, как установить параметры загрузки перед загрузкой модели PLY.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
### **Использование вариантов нагрузки DirectX X**
Код C# ниже показывает, как установить параметры загрузки перед загрузкой файла DirectX X.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
### **Используйте параметры нагрузки RVM**
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
### **Использование вариантов нагрузки FBX**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
