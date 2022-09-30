---
title: Укажите параметры сохранения файла 3D
type: docs
weight: 10
url: /ru/java/specify-3d-file-save-options/
description: Существует несколько перегрузок метода Scene.save, которые принимают экземпляр SaveOptions.
---
## **Параметры сохранения файла 3D**
Существует несколько перегрузок метода Scene.save, которые принимают экземпляр SaveOptions. Это должен быть экземпляр класса, производного от класса SaveOptions. Каждый формат сохранения имеет соответствующий класс, который содержит параметры сохранения для этого формата сохранения, например, есть ColladaSaveOptions для формата сохранения FileFormat.COLLADA.
### **Использование опций сохранения Collada**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением файла 3D в формате Collada.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-ColladaSaveOption.java" >}}
### **Использование опций сохранения Discreet3DS**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением файла 3D в формат Discreet 3DS.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSSaveOption.java" >}}
### **Использование опций сохранения FBX**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением файла 3D в формате FBX.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-FBXSaveOption.java" >}}
### **Использование опций сохранения OBJ**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением файла 3D в формат Obj.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJSaveOption.java" >}}
### **Использование опций сохранения STL**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением файла 3D в формат STL.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLSaveOption.java" >}}
### **Использование опций сохранения U3D**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формат U3D.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DSaveOption.java" >}}
### **Использование опций сохранения glTF**
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 



В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формат glTF.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFSaveOption.java" >}}
### **PrettyPrint в вариантах сохранения glTF**
Вы также можете использовать метод setPrettyPrint класса GLTFSaveOptions для печати JSON, понятной для человека. Код ниже показывает, как использовать эту функциональность.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-prettyPrintInGltfSaveOption.java" >}}
### **Сохранение зависимостей сцены 3D в реальной файловой системе**
Разработчики могут потребовать сохранить все зависимости сцены 3D в реальной файловой системе. Они могут определить путь локального каталога, сохранить в объекте `MemoryFileSystem` или просто отказаться от зависимостей. Свойство FileSystem добавляется во все классы опций сохранения.
#### **Откажите сохранение файлов материала**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DiscardSavingMaterial.java" >}}
#### **Сохранить зависимости в локальном каталоге**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInLocalDirectory.java" >}}
#### **Сохранить зависимости в экземпляр MemoryFileSystem**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInMemoryFileSystem.java" >}}
### **Использование вариантов сохранения Google Draco (.DRC)**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением модели 3D в формат DRC.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DRCSaveOption.java" >}}
### **Использование опций сохранения RVM**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением модели 3D в формат RVM.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-RVMSaveOptions.java" >}}
