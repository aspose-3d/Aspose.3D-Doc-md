---
title: Lavorare con il formato VRML
type: docs
weight: 90
url: /it/java/working-with-vrml-format/
description: Aspose.3D for Java consente di lavorare con VRML versione 1.0. Il formato di file VRML è stato aggiunto alla classe FileFormat. Aspose.3D può rilevare automaticamente il formato VRML, quindi il FileFormat viene solitamente ignorato nel metodo Open.
---
#  **Apri il formato file VRML**
Aspose.3D for Java consente di lavorare con VRML versione 1.0. Il formato di file `VRML` è stato aggiunto alla classe `FileFormat`. Aspose.3D può rilevare automaticamente il formato `VRML`, quindi `FileFormat` viene solitamente ignorato nel metodo Open. Il seguente frammento di codice mostra come aprire il formato di file VRML.

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
