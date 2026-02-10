---
title: Crear un documento 3D vacío
type: docs
weight: 20
url: /es/java/create-an-empty-3d-document/
description: Aspose.3D for Java API tiene soporte para crear una escena 3D desde cero y luego guardar en el formato 3D compatible.
---
##  **Cree una escena 3D vacía y guárdela en formato 3D compatible**
Aspose.3D for Java API tiene soporte para crear una escena 3D desde cero y luego guardar en el formato 3D compatible.
###  **Creación de una escena 3D vacía**
Siga estos pasos para crear una escena 3D con Aspose.3D for Java API:

1. Crear una instancia de la**Escena**Que representa la escena 3D.
1. Genere el documento 3D llamando al**Guardar**Método de la**Escena**Instancia de clase.
####  **Creación de una escena 3D vacía: Muestras de programación**
{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "document.fbx";
// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}




