---
title: Укажите 3D Параметры сохранения файла в C#
linktitle: Укажите параметры сохранения файла 3D
type: docs
weight: 40
url: /ru/net/specify-3d-file-save-options/
description: Существует несколько перегрузок метода Scene.Save, которые принимают объект SaveOptions. Каждый формат сохранения имеет соответствующий класс, который содержит параметры сохранения для этого формата сохранения.
---
##  **Обзор**

В этой статье объясняется, как сохранить файлы 3D в разных форматах [После загрузки их в объекте Scene](https://docs.aspose.com/3d/net/specify-3d-file-load-options/), используя C#. Загрузив и сохранив, вы можете выполнить ряд различных преобразований, например

- Конвертировать FBX в X в C#
- Конвертировать GLTF в OBJ в C#
- Конвертировать OBJ в X в C#
- Конвертировать STL в OBJ в C#
- Конвертировать RVM в 3DS в C#

##  **3D Параметры сохранения файла**
Существует несколько перегрузок метода [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene), которые принимают объект SaveOptions. Это должен быть объект класса, производного от класса `SaveOptions`. Каждый формат сохранения имеет соответствующий класс, который содержит параметры сохранения для этого формата сохранения, например, есть `ColladaSaveOptions` для формата сохранения `FileFormat.Collada`.
###  **Использование параметров сохранения Collada**
Код C# ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате Collada.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ColladaSaveOption.cs" >}}
###  **Использование параметров сохранения Discreet3DS**
Код C# ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате Discreet 3DS.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.cs" >}}
###  **Использование параметров сохранения FBX**
Код C# ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате FBX.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-FBXSaveOption.cs" >}}

`FBXSaveOptions` также предоставляет свойство `EnableCompression`, которое можно использовать для сжатия больших двоичных данных в файле FBX. Значение этого свойства по умолчанию-true. Ниже фрагмент кода объясняет, как вы можете работать с этим свойством при сохранении сцены.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Compression.cs" >}}
###  **Использование опций сохранения Obj**
Код ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате Obj.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ObjSaveOption.cs" >}}
###  **Использование параметров сохранения STL**
Код C# ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате STL.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-STLSaveOption.cs" >}}
###  **Использование параметров сохранения U3D**
Код C# ниже показывает, как установить параметры сохранения перед сохранением документа в формате U3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-U3DSaveOption.cs" >}}
###  **Использование параметров сохранения glTF**
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 



Код C# ниже показывает, как установить параметры сохранения перед сохранением документа в формате glTF.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-glTFSaveOptions.cs" >}}
###  **PrettyPrint в glTF Параметры сохранения**
Вы также можете использовать свойство PrettyPrint класса GLTFSaveOptions для понятной для человека печати JSON. Код ниже показывает, как использовать эту функциональность.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.cs" >}}
###  **Сохранение зависимостей сцены 3D в реальной файловой системе**
Разработчикам может потребоваться сохранить все зависимости сцены 3D в реальной файловой системе. Они могут определить путь к локальной директории, сохранить в объекте `MemoryFileSystem` или просто отказаться от зависимостей. Свойство `FileSystem` добавляется во все классы опций сохранения.
####  **Откажите сохранение файлов материала**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DiscardSavingMaterial.cs" >}}
####  **Сохранить зависимости в локальном каталоге**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.cs" >}}
####  **Сохранение зависимостей в объекте MemoryFileSystem**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.cs" >}}
###  **Использование параметров сохранения Google Draco (.drc)**
Код C# ниже показывает, как установить параметры сохранения перед сохранением модели 3D в формате DRC.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DRCSaveOptions.cs" >}}
###  **Использование параметров сохранения RVM**
Код C# ниже показывает, как установить параметры сохранения перед сохранением модели 3D в формате RVM.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-RVMSaveOptions.cs" >}}
