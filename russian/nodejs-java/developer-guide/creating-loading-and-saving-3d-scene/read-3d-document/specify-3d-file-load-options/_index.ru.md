---
title: "Укажите параметры загрузки 3D-файлов"
type: docs
weight: 10
url: "/ru/nodejs-java/specify-3d-file-load-options/"
description: Существует несколько перегрузок метода Scene.open или перегрузок конструктора класса Scene, которые принимают экземпляр LoadOptions.
---

## **3D File Load Options**
Существуют различные перегрузки метода Scene.open или перегрузки конструктора класса Scene, которые принимают экземпляр LoadOptions. Это должен быть экземпляр класса, производного от класса LoadOptions. Для каждого формата загрузки существует соответствующий класс, содержащий параметры загрузки для этого формата загрузки, например, ColladaSaveOptions для формата сохранения FileFormat.COLLADA.
### **Использование параметров загрузки Discreet 3DS**
В приведенном ниже коде показано, как установить параметры загрузки перед загрузкой файла Discreet 3DS.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

var loadOpts = new aspose.threed.Discreet3dsLoadOptions();

// Устанавливает, использовать ли преобразование, определенное в первой кадра анимационной дорожки.
loadOpts.setApplyAnimationTransform(true);

// Переворачивает систему координат
loadOpts.setFlipCoordinateSystem(true);

// Предпочитать использование гамма-корректированной цветовой информации, если файл 3ds предоставляет как оригинальный цвет, так и гамма-корректированный цвет.
loadOpts.setGammaCorrectedColor(true);

{{< /highlight >}}

### **Использование параметров загрузки Obj**
В приведенном ниже коде показано, как установить параметры загрузки перед загрузкой 3D-файла Obj.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

var loadObjOpts  = new aspose.threed.ObjLoadOptions();

// Импортировать материалы из внешнего файла библиотеки материалов
loadObjOpts.setEnableMaterials(true);

// Переворачивает систему координат.
loadObjOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Использование параметров загрузки STL**
В приведенном ниже коде показано, как установить параметры загрузки перед загрузкой файла STL.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Инициализировать объект
var loadSTLOpts   = new aspose.threed.StlLoadOptions();

// Переворачивает систему координат.
loadSTLOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Использование параметров загрузки U3D**
В приведенном ниже коде показано, как установить параметры загрузки перед загрузкой файла U3D.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Инициализировать объект
var loadU3DOpts = new aspose.threed.U3dLoadOptions();

// Переворачивает систему координат.
loadU3DOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Использование параметров загрузки glTF**
В приведенном ниже коде показано, как установить параметры загрузки перед загрузкой файла glTF.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Установить параметры загрузки
var loadOpt = new aspose.threed.GltfLoadOptions();

// Значение по умолчанию равно true, обычно его не нужно изменять. Aspose.3D автоматически переворачивает текстурные координаты V/T при загрузке и сохранении.
loadOpt.setFlipTexCoordV(true);

{{< /highlight >}}

### **Использование параметров загрузки Ply**
В приведенном ниже коде показано, как установить параметры загрузки перед загрузкой модели PLY.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// инициализировать объект класса Scene
var scene = new aspose.threed.Scene();

// инициализировать объект
var loadPLYOpts  = new aspose.threed.PlyLoadOptions();

// Переворачивает систему координат.
loadPLYOpts.setFlipCoordinateSystem(true);

// загрузить 3D-модель Ply
scene.open("vase-v2.ply", loadPLYOpts);

{{< /highlight >}}

### **Использование параметров загрузки DirectX X**
В приведенном ниже коде показано, как установить параметры загрузки перед загрузкой файла DirectX X.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// инициализировать объект класса Scene
var scene = new aspose.threed.Scene();

// инициализировать объект
var loadXOpts = new aspose.threed.XLoadOptions(aspose.threed.FileContentType.ASCII);

// переворачивает систему координат.
loadXOpts.setFlipCoordinateSystem(true);

// загрузить 3D-файл X
scene.open("warrior.x", loadXOpts);

{{< /highlight >}}

### **Использование параметров загрузки FBX**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

//Это выведет все свойства, определенные в GlobalSettings в файле FBX.
var opt = new aspose.threed.FbxLoadOptions();

opt.setKeepBuiltinGlobalSettings(true);

{{< /highlight >}}