---
title: Lavorare con il formato VRML
type: docs
weight: 90
url: /it/nodejs-java/working-with-vrml-format/
description: Aspose.3D for Node.js via Java consente di lavorare con VRML versione 1.0. Il formato di file VRML è stato aggiunto alla classe FileFormat. Aspose.3D può rilevare automaticamente il formato VRML, quindi il FileFormat viene solitamente ignorato nel metodo Open.
---
#  **Apri il formato file VRML**
Aspose.3D for Node.js via Java consente di lavorare con VRML versione 1.0. Il formato di file `VRML` è stato aggiunto alla classe `FileFormat`. Aspose.3D può rilevare automaticamente il formato `VRML`, quindi `FileFormat` viene solitamente ignorato nel metodo Open. Il seguente frammento di codice mostra come aprire il formato di file VRML.

{{< highlight "java" >}}

// initialize a scene
var scene = new aspose.threed.Scene();

// open Virtual Reality Modeling Language (VRML) file format
scene.open( "test.wrl");

{{< /highlight >}}
