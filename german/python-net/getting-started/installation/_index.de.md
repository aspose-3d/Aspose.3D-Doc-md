---
title: Installation
type: docs
weight: 40
url: /de/python-net/installation/
---
##  **Systema forderungen**

Zuerst müssen Sie überprüfen und bestätigen, dass die Spezifikationen der Maschine die [Systema forderungen](/3d/de/python-net/system-requirements/) erfüllen.

##  **Installation von Aspose.3D for Python via .NET**
`pip` ist der einfachste Weg, [Aspose.3D for Python via .NET](https://pypi.org/project/aspose-3d/) herunter zuladen und zu installieren.

Um Aspose.3D zu installieren, führen Sie den folgenden Befehl aus: pip install aspose-3d

##  **Verwenden von Aspose.3D for Python via .NET**

Sobald Sie mit der Installation des Moduls fertig sind, können Sie Aspose.3D aus Ihrem Python-Code folgender maßen verwenden:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

