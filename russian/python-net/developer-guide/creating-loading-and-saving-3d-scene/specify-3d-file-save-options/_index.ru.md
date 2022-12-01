---
title: Укажите параметры сохранения файла 3D
type: docs
weight: 40
url: /ru/python-net/specify-3d-file-save-options/
description: Существует несколько перегрузок метода Scene.Save, которые принимают объект SaveOptions. Каждый формат сохранения имеет соответствующий класс, который содержит параметры сохранения для этого формата сохранения.
---
## **Параметры сохранения файла 3D**
Существует несколько перегрузок метода [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene), которые принимают объект `SaveOptions`. Это должен быть объект класса, производного от класса `SaveOptions`. Каждый формат сохранения имеет соответствующий класс, который содержит параметры сохранения для этого формата сохранения, например, есть `ColladaSaveOptions` для формата сохранения `FileFormat.Collada`.
### **Использование опций сохранения Collada**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением файла 3D в формат Collada.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ColladaSaveOption.py" >}}
### **Использование опций сохранения Discreet3DS**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением файла 3D в формат Discreet 3DS.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.py" >}}
### **Использование опций сохранения FBX**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением файла 3D в формате FBX.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-FBXSaveOption.py" >}}

`FBXSaveOptions` также раскрывает свойство `enable_compression`, которое можно использовать для сжатия больших двоичных данных в файле FBX. Значение по умолчанию этого свойства является истинным. Ниже фрагмент кода объясняет, как вы можете работать с этим свойством при сохранении сцены.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-Save3DScene-Compression.py" >}}
### **Использование опций сохранения Obj**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением файла 3D в формат Obj.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ObjSaveOption.py" >}}
### **Использование опций сохранения STL**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением файла 3D в формат STL.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-STLSaveOption.py" >}}
### **Использование опций сохранения U3D**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формат U3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-U3DSaveOption.py" >}}
### **Использование опций сохранения glTF**
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 



В приведенном ниже коде показано, как установить параметры сохранения перед сохранением документа в формат glTF.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-glTFSaveOptions.py" >}}
### **PrettyPrint в вариантах сохранения glTF**
Вы также можете использовать свойство PrettyPrint класса GLTFSaveOptions для понятной для человека печати JSON. Код ниже показывает, как использовать эту функциональность.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.py" >}}
### **Сохранение зависимостей сцены 3D в реальной файловой системе**
Разработчикам может потребоваться сохранить все зависимости сцены 3D в реальной файловой системе. Они могут определить путь локального каталога, сохранить в объекте MemoryFileSystem или просто отказаться от зависимостей. Свойство FileSystem добавляется во все классы опций сохранения.
#### **Откажите сохранение файлов материала**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DiscardSavingMaterial.py" >}}
#### **Сохранить зависимости в локальном каталоге**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.py" >}}
#### **Сохранение зависимостей в объекте MemoryFileSystem**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.py" >}}
### **Использование опций сохранения Google Draco (.drc)**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением модели 3D в формат DRC.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DRCSaveOptions.py" >}}
### **Использование опций сохранения RVM**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением модели 3D в формат RVM.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-RVMSaveOptions.py" >}}
