---
title: Especificar las opciones de guardado de archivos 3D
type: docs
weight: 10
url: /es/java/specify-3d-file-save-options/
description: Hay varias sobrecargas del método Scene.save que aceptan una instancia de SaveOptions.
---
##  **3D Opciones para guardar archivos**
Hay varias sobrecargas del método Scene.save que aceptan una instancia de SaveOptions. Debe ser una instancia de una clase derivada de la clase SaveOptions. Cada formato de guardado tiene una clase correspondiente que contiene opciones de guardado para ese formato de guardado; por ejemplo, está ColladaSaveOptions para el formato de guardado FileFormat.COLLADA.
###  **Uso de Collada Save Options**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en formato Collada.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-ColladaSaveOption.java" >}}
###  **Uso de Discreet3DS Save Options**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en formato Discreet 3DS.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSSaveOption.java" >}}
###  **Uso de las opciones de guardado FBX**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en un formato FBX.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-FBXSaveOption.java" >}}
###  **Uso de OBJ Save Options**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en un formato Obj.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJSaveOption.java" >}}
###  **Uso de STL Save Options**
El siguiente código muestra cómo establecer las opciones de guardado antes de guardar un archivo 3D en formato STL.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLSaveOption.java" >}}
###  **Uso de las opciones de guardado U3D**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato U3D.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DSaveOption.java" >}}
###  **Uso de las opciones de guardado glTF**
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,8 o superior.

{{% /alert %}} 



El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato glTF.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFSaveOption.java" >}}
###  **PrettyPrint en glTF Guardar opciones**
También puede usar el método setPrettyPrint de la clase GLTFSaveOptions para la impresión JSON comprensible para el ser humano. El siguiente código muestra cómo usar esta funcionalidad.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-prettyPrintInGltfSaveOption.java" >}}
###  **Guardar dependencias de una escena 3D en el sistema de archivos real**
Los desarrolladores pueden necesitar guardar todas las dependencias de la escena 3D en el sistema de archivos real. Pueden definir la ruta de un directorio local, guardar en el objeto `MemoryFileSystem` o simplemente descartar dependencias. La propiedad FileSystem se agrega en las clases de opción all save.
####  **Descarte guardar los archivos de material**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DiscardSavingMaterial.java" >}}
####  **Guardar dependencias en el directorio local**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInLocalDirectory.java" >}}
####  **Guardar dependencias en la instancia de MemoryFileSystem**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInMemoryFileSystem.java" >}}
###  **Uso de las opciones de guardado Google Draco (.DRC)**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un modelo 3D en formato DRC.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DRCSaveOption.java" >}}
###  **Uso de RVM Save Options**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un modelo 3D en formato RVM.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-RVMSaveOptions.java" >}}
