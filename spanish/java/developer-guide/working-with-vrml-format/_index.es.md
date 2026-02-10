---
title: Trabajar con formato VRML
type: docs
weight: 90
url: /es/java/working-with-vrml-format/
description: Aspose.3D for Java permite trabajar con VRML versión 1,0. El formato de archivo VRML se ha agregado a la clase FileFormat. Aspose.3D puede detectar automáticamente el formato VRML, por lo que FileFormat generalmente se ignora en el método Open.
---
#  **Formato de archivo abierto VRML**
Aspose.3D for Java permite trabajar con VRML versión 1,0. El formato de archivo `VRML` se ha agregado a la clase `FileFormat`. Aspose.3D puede detectar automáticamente el formato `VRML`, por lo que `FileFormat` generalmente se ignora en el método Open. El siguiente fragmento de código muestra cómo abrir el archivo VRML formato.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// initialize a scene
Scene scene = new Scene();
// open Virtual Reality Modeling Language (VRML) file format
scene.open( MyDir + "test.wrl");
// work with VRML file format...

{{< /highlight >}}
