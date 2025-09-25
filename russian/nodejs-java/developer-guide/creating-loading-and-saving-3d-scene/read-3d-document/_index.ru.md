---
title: Прочитать 3D документ
type: docs
weight: 30
url: "/ru/nodejs-java/read-3d-document/"
description: "Aspose.3D для Node.js через Java API поддерживает чтение различных типов 3D-документов."
---

## **Список поддерживаемых 3D форматов (импорт)**
Aspose.3D для Node.js через Java API поддерживает чтение различных типов 3D документов. Доступные конструкторы класса `Scene` помогают в этом и принимают строку допустимого пути к файлу. Поддерживаемые форматы файлов для чтения следующие:

1. FBX 7.5 (ASCII, Binary)
1. FBX 7.4 (ASCII, Binary)
1. FBX 7.3 (ASCII, Binary)
1. FBX 7.2 (ASCII, Binary)
1. STL (ASCII, Binary)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, Binary)
1. X (ASCII, Binary)
1. Draco
1. 3MF
1. RVM (Text, Binary)
1. ASE

Конструкторы класса Scene определяют формат 3D документа внутренне.
## **Импорт 3D документа**
Aspose.3D для Java API поддерживает импорт различных типов 3D документов для целей модификации, добавления и обработки.
### **Чтение 3D сцены: Примеры программирования**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Инициализация объекта класса Scene
var scene = new aspose.threed.Scene();

// Загрузка существующего 3D документа
scene.open( "document.obj");

{{< /highlight >}}