---
title: Installation
type: docs
weight: 40
url: /de/python-net/installation/
---
## **System Anforderungen**

Zuerst müssen Sie überprüfen und bestätigen, dass die Spezifikationen der Maschine dem entsprechen[Systema forderungen](/3d/de/python-net/system-requirements/).

## **Installation Aspose.3D für Python via .NET**
`pip` ist der einfachste Weg zum Herunter laden und Installieren[Aspose.3D für Python via .NET](https://pypi.org/project/aspose-3d/).

Um Aspose.3Dzu installieren, führen Sie diesen Befehl aus: pip install aspose-3d

## **Unter Verwendung Aspose.3D für Python via .NET**

Sobald Sie mit der Installation des Moduls fertig sind, können Sie Aspose.3D aus Ihrem Python-Code folgender maßen verwenden:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

