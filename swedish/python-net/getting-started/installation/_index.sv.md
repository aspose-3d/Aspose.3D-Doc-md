---
title: Anläggning
type: docs
weight: 40
url: /sv/python-net/installation/
---
## **Systemkrav**

Först måste du kontrollera och bekräfta att maskinens specifikationer uppfylle[Systemkrav](/3d/sv/python-net/system-requirements/).

## **Installera Aspose.3D för Python via .NET**
`pip` är det enklaste sättet att ladda ner och installerar[Aspose.3D för Python via .NET](https://pypi.org/project/aspose-3d/).

För att installera Aspose.3D, kör det här kommandot: pip install aspose-3d

## **Använda Aspose.3D för Python via .NET**

När du har avslutat installationen av modulen, kan du använda Aspose.3D från din python-kod på det här sättet:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

