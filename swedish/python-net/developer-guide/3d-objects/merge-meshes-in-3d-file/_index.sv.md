---
title: Sammanfoga maskor i 3D- filen
type: docs
weight: 90
url: /sv/python-net/merge-meshes-in-3d-file/
description: Utvecklare kan slå ihop flera maskor till en enda giltig mask. De kan omvandla alla maskor i en 3D scen, en nod eller en uppsättning noder till ett enda nät. För att uppnå detta, det finns tre MergeMesh medlemmar i Aspose.ThreeD.Enheter.PolygonModifier klass.
---
## **Sammanfoga maskor till en enda giltig mesh**
Utvecklare kan slå ihop flera maskor till en enda giltig mask. De kan omvandla alla maskor i en 3D scen, en nod eller en uppsättning noder till ett enda nät. För att uppnå detta finns det flera `merge_mesh` medlemmar i klassen `aspose.threed.entities.PolygonModifier`.

Kodprovet nedan sammanfogar alla maskor i en scen i ett enda giltigt maskor.

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
