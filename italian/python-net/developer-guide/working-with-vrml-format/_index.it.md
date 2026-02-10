---
title: Lavorare con il formato VRML
type: docs
weight: 120
url: /it/python-net/working-with-vrml-format/
description: Aspose.3D for Python via .NET consente di lavorare con VRML versione 1.0. Il formato di file VRML è stato aggiunto alla classe FileFormat. Aspose.3D può rilevare automaticamente il formato, quindi FileFormat viene solitamente ignorato nel metodo Open. Il seguente frammento di codice mostra come aprire il formato di file VRML.
---
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.4 o maggiore.

{{% /alert %}} 
#  **Apri il formato file VRML**
Aspose.3D for Python via .NET consente di lavorare con VRML versione 1.0. Il formato di file `VRML` è stato aggiunto alla classe `FileFormat`. Aspose.3D può rilevare automaticamente il formato, quindi il metodo `FileFormat` viene solitamente ignorato con `open`. Il seguente frammento di codice mostra come aprire il formato di file VRML.

{{< highlight "python" >}}
from aspose.threed import Scene

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a Scene
scene = Scene()
#  Open Virtual Reality Modeling Language (VRML) file format
scene.open("data-dir"  + "test.wrl")

{{< /highlight >}}
