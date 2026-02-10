---
title: 3D belgesini kaydedin
type: docs
weight: 20
url: /tr/python-net/save-a-3d-document/
description: Aspose.3D API sahne sınıfı, 3D belgesini temsil eder ve geliştiriciler nesnesini herhangi bir desteklenen dosya biçiminde kaydedebilir.
---
{{% alert color="primary" %}} 

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class of the Aspose.3D API represents a 3D document and developers can save its object in any supported file format. To save a 3D Scene, simply use the [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) method, it accepts a file name with complete path or a file stream object. Aspose.3D API offers another `FileFormat` parameter to specify output file format.

{{% /alert %}} 
##  **3D sahnesini kaydet**


The kod örneği aşağıda bir belgenin bir akışa nasıl kaydedileceğini gösterir.

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
