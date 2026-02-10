---
title: Enregistrer un document 3D
type: docs
weight: 20
url: /fr/python-net/save-a-3d-document/
description: La classe Scene de la Aspose.3D API représente un document 3D et les développeurs peuvent enregistrer son objet dans n'importe quel format de fichier pris en charge.
---
{{% alert color="primary" %}} 

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) de Aspose.3D API représente un document 3D et les développeurs peuvent enregistrer son objet dans n'importe quel format de fichier pris en charge. Pour enregistrer une scène 3D, utilisez simplement la méthode [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save), elle accepte un nom de fichier avec un chemin complet ou un objet de flux de fichiers. Aspose.3D API offre un autre paramètre `FileFormat` pour spécifier le format du fichier de sortie.

{{% /alert %}} 
##  **Enregistrer une scène 3D**


L'exemple de code ci-dessous montre comment enregistrer un document dans un flux.

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
