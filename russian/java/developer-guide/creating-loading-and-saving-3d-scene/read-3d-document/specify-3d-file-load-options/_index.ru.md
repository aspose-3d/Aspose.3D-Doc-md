---
title: Укажите параметры нагрузки на файл 3D
type: docs
weight: 10
url: /ru/java/specify-3d-file-load-options/
description: Существует несколько перегрузок метода Scene.open или перегрузок конструктора класса Scene, которые принимают экземпляр LoadOptions.
---
## **3D Варианты нагрузки файла**
Существует несколько перегрузок метода Scene.open или перегрузок конструктора класса Scene, которые принимают экземпляр LoadOptions. Это должен быть экземпляр класса, производного от класса LoadOptions. Каждый формат загрузки имеет соответствующий класс, который содержит параметры загрузки для этого формата загрузки, например, есть ColladaSaveOptions для формата сохранения FileFormat.COLLADA.
### **Использование сдерженных вариантов нагрузки 3DS**
В приведенном ниже коде показано, как установить параметры загрузки перед загрузкой файла Discreet 3DS.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSLoadOption.java" >}}
### **Использование опций нагрузки Obj**
В приведенном ниже коде показано, как установить параметры загрузки перед загрузкой файла 3D Obj.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJLoadOption.java" >}}
### **Использование вариантов нагрузки STL**
В приведенном ниже коде показано, как установить параметры загрузки перед загрузкой файла STL.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLLoadOption.java" >}}
### **Использование вариантов нагрузки U3D**
Код ниже показывает, как установить параметры загрузки перед загрузкой файла U3D.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DLoadOption.java" >}}
### **Использование вариантов нагрузки glTF**
Код ниже показывает, как установить параметры загрузки перед загрузкой файла glTF.
#### **Переверните координату текстуры V/T**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFLoadOptions.java" >}}
### **Использование опций нагрузки Ply**
Код ниже показывает, как установить параметры загрузки перед загрузкой модели PLY.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-PLYLoadOption.java" >}}
### **Использование вариантов нагрузки DirectX X**
В приведенном ниже коде показано, как установить параметры загрузки перед загрузкой файла DirectX X.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-XLoadOption.java" >}}
### **Используйте параметры нагрузки FBX**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-LoadOptions-FBXLoadOptions.java" >}}
