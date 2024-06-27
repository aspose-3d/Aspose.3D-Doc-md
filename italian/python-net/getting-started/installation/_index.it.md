---
title: Installation
type: docs
weight: 40
url: /it/python-net/installation/
---
##  **Requisiti di sistema**

Innanzitutto, devi controllare e confermare che le specifiche della macchina soddisfano [Requisiti di sistema](/3d/it/python-net/system-requirements/).

##  **Installazione di Aspose.3D for Python via .NET**
`pip` è il modo più semplice per scaricare e installare [Aspose.3D for Python via .NET](https://pypi.org/project/aspose-3d/).

Per installare Aspose.3D, esegui questo comando: aspose-3d di installazione pip

##  **Utilizzo di Aspose.3D for Python via .NET**

Una volta completata l'installazione del modulo, puoi utilizzare Aspose.3D dal tuo codice python in questo modo:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

