---
title: Especificar 3D Opciones de guardado de archivos
type: docs
weight: 10
url: /es/java/specify-3d-file-save-options/
description: Hay varias sobrecargas del método Scene.save que aceptan una instancia de SaveOptions.
---
## **3D Opciones de guardado de archivos**
Hay varias sobrecargas del método Scene.save que aceptan una instancia de SaveOptions. Debe ser una instancia de una clase derivada de la clase SaveOptions. Cada formato de guardado tiene una clase correspondiente que contiene opciones de guardado para ese formato de guardado; por ejemplo, está ColladaSaveOptions para el formato de guardado FileFormat.COLLADA.
### **Uso de Collada Opciones de Guardar**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en formato Collada.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-ColladaSaveOption.java" >}}
### **Uso de Discreet3DS Opciones de Guardar**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en un formato Discreet 3DS.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSSaveOption.java" >}}
### **Uso de las opciones de Guardar FBX**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D a un formato FBX.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-FBXSaveOption.java" >}}
### **Uso de OBJ Opciones de Guardar**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en un formato Obj.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJSaveOption.java" >}}
### **Uso de STL Opciones de Guardar**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D al formato STL.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLSaveOption.java" >}}
### **Uso de las opciones de Guardar U3D**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato U3D.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DSaveOption.java" >}}
### **Uso de las opciones de Guardar glTF**
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,8 o superior.

{{% /alert %}} 



El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato glTF.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFSaveOption.java" >}}
### **PrettyPrint en glTF Opciones de guardado**
También puede usar el método setPrettyPrint de la clase GLTFSaveOptions para la impresión JSON comprensible para el ser humano. El siguiente código muestra cómo usar esta funcionalidad.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-prettyPrintInGltfSaveOption.java" >}}
### **Guardar dependencias de una escena 3D en el sistema de archivos reales**
Los desarrolladores pueden requerir guardar todas las dependencias de la escena 3D en el sistema de archivos real. Pueden definir la ruta de un directorio local, guardar en el objeto `MemoryFileSystem` o simplemente descartar las dependencias. La propiedad FileSystem se agrega en todas las clases de opción de guardar.
#### **Descarte guardar los archivos de material**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DiscardSavingMaterial.java" >}}
#### **Guardar dependencias en el directorio local**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInLocalDirectory.java" >}}
#### **Guardar dependencias en la instancia de MemoryFileSystem**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInMemoryFileSystem.java" >}}
### **Uso de las opciones de guardado Google Draco (.DRC)**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un modelo 3D a formato DRC.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DRCSaveOption.java" >}}
### **Uso de RVM Opciones de Guardar**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un modelo 3D a formato RVM.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-RVMSaveOptions.java" >}}
