---
title: Installation
type: docs
weight: 40
url: /sv/python-net/installation/
---
##  **Systemkrav**

Först måste du kontrollera och bekräfta att maskinens specifikationer uppfyller [Systemkrav](/3d/sv/python-net/system-requirements/).

##  **Installerar Aspose.3D for Python via .NETe**
`pip` är det enklaste sättet att ladda ner och installera [Aspose.3D for Python via .NET](https://pypi.org/project/aspose-3d/).

För att installera Aspose.3D, kör det här kommandot: pip installera aspose-3d

##  **Använder Aspose.3D for Python via .NETe**

När du har installerat modulen, kan du använda Aspose.3D från python-koden på det här sättet:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

