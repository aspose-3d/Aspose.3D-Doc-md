---
title: Passen Sie die Umwandlung von Nicht-PBR-Materialien an, bevor Sie die Szenen 3D in das Format GLTF 2.0 speichern
type: docs
weight: 70
url: /de/python-net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Die Szene klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können bereits eine 3D-Szene erstellen, indem sie verschiedene Entitäten hinzufügen. GLTF 2.0 unterstützt nur PBR-Materialien (Physically Based Rendering), Aspose.3D API wandelt Nicht-PBR-Materialien intern in PBR-Materialien um, bevor es in GLTF 2.0 exportiert.
---
{{% alert color="primary" %}} 

Die [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klasse der Aspose.3D API repräsentiert eine 3D-Szene. Entwickler können bereits eine 3D-Szene erstellen, indem sie verschiedene Entitäten hinzufügen. GLTF 2.0 unterstützt nur PBR-Materialien (Physically Based Rendering), Aspose.3D API wandelt Nicht-PBR-Materialien intern in PBR-Materialien um, bevor sie in GLTF 2.0 exportiert (die Materialien in der Szene bleiben während des Exports unverändert), und die Entwickler können benutzer definierte Konvertierungs funktion bereitstellen das Standard verhalten außer Kraft setzen.

{{% /alert %}} 
## **Nicht-PBR-zu-PBR-Material umwandlung**
Dieses Code beispiel zeigt, wie Material in PBR-Material umgewandelt wird, und speichert dann die 3D-Szene im Format GLTF:

**C#**

```py

import aspose.threed as a3d

# initialize a new 3D scene

s = a3d.Scene()

box = a3d.Box()

mat = a3d.shading.PhongMaterial()
mat.diffuse_color = Vector3(1, 0, 1)

s.root_node.create_child_node("box1", box).material = mat

opt = a3d.formats.GLTFSaveOptions(FileFormat.GLTF2);

# save in GLTF 2.0 format

s.save("test.gltf", opt);

```
