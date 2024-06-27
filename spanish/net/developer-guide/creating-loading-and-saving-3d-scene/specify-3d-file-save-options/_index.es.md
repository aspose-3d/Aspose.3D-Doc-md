---
title: Especificar las opciones de guardado de archivos 3D en C#
linktitle: Especificar las opciones de guardado de archivos 3D
type: docs
weight: 40
url: /es/net/specify-3d-file-save-options/
description: Hay varias sobrecargas del método Scene.Save que aceptan un objeto SaveOptions. Cada formato de guardado tiene una clase correspondiente que contiene opciones de guardado para ese formato de guardado.
---
##  **Descripción general**

Este artículo explica cómo puede guardar archivos 3D en diferentes formatos [Después de cargarlos en objeto Escena](https://docs.aspose.com/3d/net/specify-3d-file-load-options/) usando C#. Al cargar y guardar, puede realizar varias conversiones diferentes, p.

- Convertir FBX a X en C#
- Convierte GLTF a OBJ en C#
- Convertir OBJ a X en C#
- Convierte STL a OBJ en C#
- Convierte RVM a 3DS en C#

##  **3D Opciones para guardar archivos**
Hay varias sobrecargas de método [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene) que aceptan un objeto SaveOptions. Debe ser un objeto de una clase derivada de la clase `SaveOptions`. Cada formato de guardado tiene una clase correspondiente que contiene las opciones de guardado para ese formato de guardado, por ejemplo, hay `ColladaSaveOptions` para el formato de guardado `FileFormat.Collada`.
###  **Uso de las opciones de guardado Collada**
El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en el formato Collada.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ColladaSaveOption.cs" >}}
###  **Uso de las opciones de guardado Discreet3DS**
El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en un formato Discreet 3DS.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.cs" >}}
###  **Uso de las opciones de guardado FBX**
El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en un formato FBX.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-FBXSaveOption.cs" >}}

`FBXSaveOptions` también expone la propiedad `EnableCompression` que se puede usar para comprimir datos binarios grandes en el archivo FBX. El valor predeterminado de esta propiedad es true. A continuación, el fragmento de código explica cómo puede trabajar con esta propiedad mientras guarda una escena.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Compression.cs" >}}
###  **Uso de las opciones de Obj Save**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en un formato Obj.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ObjSaveOption.cs" >}}
###  **Uso de las opciones de guardado STL**
El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en el formato STL.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-STLSaveOption.cs" >}}
###  **Uso de las opciones de guardado U3D**
El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un documento en formato U3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-U3DSaveOption.cs" >}}
###  **Uso de las opciones de guardado glTF**
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,8 o superior.

{{% /alert %}} 



El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un documento en formato glTF.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-glTFSaveOptions.cs" >}}
###  **PrettyPrint en glTF Guardar opciones**
También puede utilizar la propiedad PrettyPrint de la clase GLTFSaveOptions para la impresión JSON comprensible para el ser humano. El siguiente código muestra cómo usar esta funcionalidad.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.cs" >}}
###  **Guardar dependencias de una escena 3D en el sistema de archivos real**
Los desarrolladores pueden requerir guardar todas las dependencias de escena 3D en el sistema de archivos real. Pueden definir la ruta de un directorio local, guardar en el objeto `MemoryFileSystem` o simplemente descartar dependencias. La propiedad `FileSystem` se agrega en las clases de opción all save.
####  **Descarte guardar los archivos de material**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DiscardSavingMaterial.cs" >}}
####  **Guardar dependencias en el directorio local**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.cs" >}}
####  **Guardar dependencias en el objeto MemoryFileSystem**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.cs" >}}
###  **Uso de las opciones de guardado Google Draco (.drc)**
El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un modelo 3D en formato DRC.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DRCSaveOptions.cs" >}}
###  **Uso de las opciones de guardado RVM**
El siguiente código C# muestra cómo configurar las opciones de guardado antes de guardar un modelo 3D en formato RVM.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-RVMSaveOptions.cs" >}}
