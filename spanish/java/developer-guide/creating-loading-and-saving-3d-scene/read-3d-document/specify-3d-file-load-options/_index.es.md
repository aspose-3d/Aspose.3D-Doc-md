---
title: Especificar las opciones de carga de archivos 3D
type: docs
weight: 10
url: /es/java/specify-3d-file-load-options/
description: Hay varias sobrecargas de método Scene.open o sobrecargas de constructor de clase Scene que aceptan la instancia de LoadOptions.
---
## **3D Opciones de carga de archivos**
Hay varias sobrecargas de método Scene.open o sobrecargas de constructor de clase Scene que aceptan la instancia de LoadOptions. Debe ser una instancia de una clase derivada de la clase LoadOptions. Cada formato de carga tiene una clase correspondiente que contiene opciones de carga para ese formato de carga; por ejemplo, está ColladaSaveOptions para el formato de guardado FileFormat.COLLADA.
### **Uso de las opciones de carga discreta 3DS**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo Discreet 3DS.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSLoadOption.java" >}}
### **Uso de las opciones de carga Obj**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo Obj 3D.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJLoadOption.java" >}}
### **Uso de las opciones de carga STL**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo STL.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLLoadOption.java" >}}
### **Uso de las opciones de carga U3D**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo U3D.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DLoadOption.java" >}}
### **Uso de las opciones de carga glTF**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo glTF.
#### **Voltear la coordenadas de textura V/T**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFLoadOptions.java" >}}
### **Uso de las opciones de carga de nivel**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un modelo PLY.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-PLYLoadOption.java" >}}
### **Uso de las opciones de carga DirectX X**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo DirectX X.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-XLoadOption.java" >}}
### **Uso FBX Opciones de carga**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-LoadOptions-FBXLoadOptions.java" >}}
