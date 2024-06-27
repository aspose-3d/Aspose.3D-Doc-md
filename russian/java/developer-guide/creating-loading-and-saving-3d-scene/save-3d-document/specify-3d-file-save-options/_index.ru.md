---
title: Укажите параметры сохранения файла 3D
type: docs
weight: 10
url: /ru/java/specify-3d-file-save-options/
description: Существует несколько перегрузок метода Scene.save, которые принимают экземпляр SaveOptions.
---
##  **3D Параметры сохранения файла**
Существует несколько перегрузок метода Scene.save, которые принимают экземпляр SaveOptions. Это должен быть экземпляр класса, производного от класса SaveOptions. Каждый формат сохранения имеет соответствующий класс, который содержит параметры сохранения для этого формата сохранения, например, есть ColladaSaveOptions для формата сохранения FileFormat.COLLADA.
###  **Использование Collada Параметры сохранения**
Код ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате Collada.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-ColladaSaveOption.java" >}}
###  **Использование Discreet3DS Параметры сохранения**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением файла 3D в формате Discreet 3DS.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSSaveOption.java" >}}
###  **Использование параметров сохранения FBX**
В приведенном ниже коде показано, как установить параметры сохранения перед сохранением файла 3D в формате FBX.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-FBXSaveOption.java" >}}
###  **Использование OBJ Параметры сохранения**
Код ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате Obj.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJSaveOption.java" >}}
###  **Использование STL Параметры сохранения**
Код ниже показывает, как установить параметры сохранения перед сохранением файла 3D в формате STL.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLSaveOption.java" >}}
###  **Использование параметров сохранения U3D**
Код ниже показывает, как установить параметры сохранения перед сохранением документа в формате U3D.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DSaveOption.java" >}}
###  **Использование параметров сохранения glTF**
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 



Код ниже показывает, как установить параметры сохранения перед сохранением документа в формате glTF.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFSaveOption.java" >}}
###  **PrettyPrint в glTF Параметры сохранения**
Вы также можете использовать метод setPrettyPrint класса GLTFSaveOptions для печати JSON, понятной для человека. Код ниже показывает, как использовать эту функциональность.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-prettyPrintInGltfSaveOption.java" >}}
###  **Сохранение зависимостей сцены 3D в реальной файловой системе**
Разработчикам может потребоваться сохранить все зависимости сцены 3D в реальной файловой системе. Они могут определить путь к локальной директории, сохранить в объекте `MemoryFileSystem` или просто отказаться от зависимостей. Свойство FileSystem добавляется во все классы параметров сохранения.
####  **Откажите сохранение файлов материала**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DiscardSavingMaterial.java" >}}
####  **Сохранить зависимости в локальном каталоге**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInLocalDirectory.java" >}}
####  **Сохранить зависимости в экземпляр MemoryFileSystem**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInMemoryFileSystem.java" >}}
###  **Использование параметров сохранения Google Draco (.DRC)**
Код ниже показывает, как установить параметры сохранения перед сохранением модели 3D в формате DRC.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DRCSaveOption.java" >}}
###  **Использование RVM Параметры сохранения**
Код ниже показывает, как установить параметры сохранения перед сохранением модели 3D в формате RVM.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-RVMSaveOptions.java" >}}
