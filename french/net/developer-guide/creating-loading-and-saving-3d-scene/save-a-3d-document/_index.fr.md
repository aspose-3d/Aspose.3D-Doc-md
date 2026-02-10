---
title: Enregistrer un document 3D dans différents formats 3D en utilisant C#
linktitle: Enregistrer un document 3D
type: docs
weight: 20
url: /fr/net/save-a-3d-document/
description: La classe Scene de la Aspose.3D API représente un document 3D et les développeurs peuvent enregistrer son objet dans n'importe quel format de fichier pris en charge.
---
##  **Aperçu**
L'article explique comment vous pouvez enregistrer un document 3D dans différents formats en utilisant la bibliothèque de traitement de documents C# 3D, y compris

- Enregistrer un document 3D au format FBX en utilisant C# - AutoDesk
- Enregistrez un document 3D au format DAE en utilisant C# - Collada
- Enregistrer un document 3D au format 3DS en utilisant C# -Discret 3D Studio
- Enregistrez un document 3D au format DRC en utilisant C# - Google Draco

{{% alert color="primary" %}} 

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) de Aspose.3D API représente un document 3D et les développeurs peuvent enregistrer son objet dans n'importe quel format de fichier pris en charge. Pour enregistrer une scène 3D, utilisez simplement la méthode [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save), elle accepte un nom de fichier avec un chemin complet ou un objet de flux de fichiers. Aspose.3D API offre un autre paramètre `FileFormat` pour spécifier le format du fichier de sortie.

{{% /alert %}} 

##  **Enregistrer une scène 3D dans les formats 3D pris en charge**

L'exemple de code C# ci-dessous montre comment enregistrer une scène ou un document 3D dans un flux dans divers formats 3D pris en charge.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
// Load a 3D document into Aspose.3D
Scene scene = new Scene();

// Open an existing 3D scene
scene.Open("document.fbx");

// Save Scene to a stream
MemoryStream dstStream = new MemoryStream();
scene.Save(dstStream, FileFormat.FBX7500ASCII);
            
// Save Scene to a local path
scene.Save("output_out.fbx");

{{< /highlight >}}
