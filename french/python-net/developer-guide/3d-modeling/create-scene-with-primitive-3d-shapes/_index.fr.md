---
title: Créer une scène avec des formes primitives 3D
type: docs
weight: 10
url: /fr/python-net/create-scene-with-primitive-3d-shapes/
description: En utilisant Aspose.3D for Python via .NET, les développeurs peuvent définir une scène avec des formes primitives 3D. Toutes les primitives paramétrées seront converties en maillage automatiquement tout en sauvegardant dans n'importe quel format de fichier de sortie pris en charge.
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), les développeurs peuvent définir une scène avec des formes primitives 3D. Toutes les primitives paramétrées seront converties en maillage automatiquement tout en sauvegardant dans n'importe quel format de fichier de sortie pris en charge.

{{% /alert %}}
##  **Construire une scène à partir de formes primitives 3D**
La modélisation est le processus de création pure et Aspose.3D API supporte la création d'une scène avec des formes primitives 3D.
###  **Échantillon de programmation**
Cet exemple de code crée une scène avec des formes primitives 3D et enregistre dans le fichier FBX.

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Box, Cylinder

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
#  Initialize a Scene object
scene = Scene()
#  Create a Box model
scene.root_node.create_child_node("box", Box())
#  Create a Cylinder model
scene.root_node.create_child_node("cylinder", Cylinder())
#  Save drawing in the FBX format
output = "out"  + "test.fbx"
scene.save(output, FileFormat.FBX7500ASCII)

{{< /highlight >}}
