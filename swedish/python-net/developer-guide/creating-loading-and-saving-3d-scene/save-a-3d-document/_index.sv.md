---
title: Spara ett 3D Dokument
type: docs
weight: 20
url: /sv/python-net/save-a-3d-document/
description: Scenklassen för Aspose. 3D API representerar ett 3D-dokument och utvecklare kan spara objektet i vilket filformat som stöds.
---
{{% alert color="primary" %}} 

[`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) klassen för Aspose. 3D API representerar ett 3D-dokument och utvecklare kan spara objektet i vilket filformat som stöds. För att spara en 3D scen, använd bara [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save)-metoden, det accepterar ett filnamn med fullständig sökväg eller ett filströmobjekt. Aspose.3D API erbjuder en annan parameter `FileFormat` för att ange utdatafilformat.

{{% /alert %}} 
##  **Spara en 3D Scene**


Kodprovet nedan visar hur man sparar ett dokument i en ström.

{{< highlight "python" >}}
import aspose.threed as a3d
import io
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
# Load a 3D document into Aspose.3D
scene = a3d.Scene.from_file("document.fbx")

# Save Scene to a stream
dstStream = io.BytesIO()
scene.save(dstStream, a3d.FileFormat.FBX7500ASCII);

{{< /highlight >}}
