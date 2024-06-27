---
title: Укажите параметры сохранения файла 3D
type: docs
weight: 40
url: /ru/python-net/specify-3d-file-save-options/
description: Существует несколько перегрузок метода Scene.Save, которые принимают объект SaveOptions. Каждый формат сохранения имеет соответствующий класс, который содержит параметры сохранения для этого формата сохранения.
---
##  **3D Параметры сохранения файла**
Существует несколько перегрузок методов [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene), которые принимают объект `SaveOptions`. Это должен быть объект класса, производного от класса `SaveOptions`. Каждый формат сохранения имеет соответствующий класс, который содержит параметры сохранения для этого формата сохранения, например, есть `ColladaSaveOptions` для формата сохранения `FileFormat.Collada`.
###  **Использование параметров сохранения Collada**
Код ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате Collada.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ColladaSaveOption.py" >}}
###  **Использование параметров сохранения Discreet3DS**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением файла 3D в формате Discreet 3DS.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.py" >}}
###  **Использование параметров сохранения FBX**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением файла 3D в формате FBX.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-FBXSaveOption.py" >}}

`FBXSaveOptions` также предоставляет свойство `enable_compression`, которое можно использовать для сжатия больших двоичных данных в файле FBX. Значение этого свойства по умолчанию-true. Ниже фрагмент кода объясняет, как вы можете работать с этим свойством при сохранении сцены.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-Save3DScene-Compression.py" >}}
###  **Использование опций сохранения Obj**
Код ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате Obj.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ObjSaveOption.py" >}}
###  **Использование параметров сохранения STL**
Код ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате STL.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-STLSaveOption.py" >}}
###  **Использование параметров сохранения U3D**
Код ниже показывает, как установить параметры сохранения перед сохранением документа в формате U3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-U3DSaveOption.py" >}}
###  **Использование параметров сохранения glTF**
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 



Код ниже показывает, как установить параметры сохранения перед сохранением документа в формате glTF.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-glTFSaveOptions.py" >}}
###  **PrettyPrint в glTF Параметры сохранения**
Вы также можете использовать свойство PrettyPrint класса GLTFSaveOptions для понятной для человека печати JSON. Код ниже показывает, как использовать эту функциональность.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.py" >}}
###  **Сохранение зависимостей сцены 3D в реальной файловой системе**
Разработчикам может потребоваться сохранить все зависимости сцены 3D в реальной файловой системе. Они могут определять путь к локальной директории, сохранять в объекте MemoryFileSystem или просто отбрасывать зависимости. Свойство FileSystem добавляется во все классы параметров сохранения.
####  **Откажите сохранение файлов материала**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DiscardSavingMaterial.py" >}}
####  **Сохранить зависимости в локальном каталоге**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.py" >}}
####  **Сохранение зависимостей в объекте MemoryFileSystem**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.py" >}}
###  **Использование параметров сохранения Google Draco (.drc)**
Код ниже показывает, как установить параметры сохранения перед сохранением модели 3D в формате DRC.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DRCSaveOptions.py" >}}
###  **Использование параметров сохранения RVM**
Код ниже показывает, как установить параметры сохранения перед сохранением модели 3D в формате RVM.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-RVMSaveOptions.py" >}}
