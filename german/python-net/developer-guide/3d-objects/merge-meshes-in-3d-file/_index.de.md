---
title: Meshes in 3D-Datei zusammenführen
type: docs
weight: 90
url: /de/python-net/merge-meshes-in-3d-file/
description: Entwickler können mehrere Netze zu einem einzigen gültigen Netz zusammenführen. Sie können alle Maschen einer 3D-Szene, eines Knotens oder einer Gruppe von Knoten in ein einzelnes Netz konvertieren. Um dies zu erreichen, gibt es drei MergeMesh-Mitglieder in der Klasse Aspose.ThreeD.Entities.Polygon Modifier.
---
##  **Meshes zu einem einzigen gültigen Netz zusammenführen**
Entwickler können mehrere Netze zu einem einzigen gültigen Netz zusammenführen. Sie können alle Maschen einer 3D-Szene, eines Knotens oder einer Gruppe von Knoten in ein einzelnes Netz konvertieren. Um dies zu erreichen, gibt es mehrere `merge_mesh`-Mitglieder in der `aspose.threed.entities.PolygonModifier`-Klasse.

Im folgenden Code beispiel werden alle Maschen einer Szene in einem einzigen gültigen Netz zusammen geführt.

**Python**

```py

import aspose.threed as a3d
# load a 3D scene

scene = a3d.Scene.from_file("LAD-TOP.rvm")

# merge all meshes

mesh = a3d.PolygonModifier.merge_mesh(scene)

# encode this mesh into the PLY format

a3d.FileFormat.PLY.encode_mesh(mesh, "LAD-TOP.ply")

```
