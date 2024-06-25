---
title: دمج الشبكات في ملف 3D
type: docs
weight: 90
url: /ar/python-net/merge-meshes-in-3d-file/
description: يمكن للمطورين دمج شبكات متعددة في شبكة واحدة صالحة. قد يحولون جميع شبكات مشهد 3D أو عقدة أو مجموعة من العقد إلى شبكة واحدة. لتحقيق ذلك ، يوجد ثلاثة أعضاء من MergeMesh في فئة Aspose.ThreeD.Entities.PolygonModifier.
---
##  **Merge ينسجم في واحد صالح Msh**
يمكن للمطورين دمج شبكات متعددة في شبكة واحدة صالحة. قد يحولون جميع شبكات مشهد 3D أو عقدة أو مجموعة من العقد إلى شبكة واحدة. لتحقيق ذلك ، هناك العديد من أعضاء `merge_mesh` في فئة `aspose.threed.entities.PolygonModifier`.

Tانه رمز عينة أدناه دمج جميع تنسجم المشهد في شبكة صالحة واحدة.

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
