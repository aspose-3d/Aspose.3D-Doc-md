---
title: Trabajar con formato VRML
type: docs
weight: 90
url: /es/nodejs-java/working-with-vrml-format/
description: Aspose.3D for Node.js via Java permite trabajar con VRML versión 1,0. El formato de archivo VRML se ha agregado a la clase FileFormat. Aspose.3D puede detectar automáticamente el formato VRML, por lo que FileFormat generalmente se ignora en el método Open.
---
#  **Formato de archivo abierto VRML**
Aspose.3D for Node.js via Java permite trabajar con VRML versión 1,0. Se ha agregado el formato de archivo `VRML` a la clase `FileFormat`. Aspose.3D puede detectar automáticamente el formato `VRML`, por lo que el `FileFormat` generalmente se ignora en el método Open. El siguiente fragmento de código muestra cómo abrir el formato de archivo VRML.

{{< highlight "java" >}}

// initialize a scene
var scene = new aspose.threed.Scene();

// open Virtual Reality Modeling Language (VRML) file format
scene.open( "test.wrl");

{{< /highlight >}}
