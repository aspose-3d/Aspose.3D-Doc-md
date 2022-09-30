---
title: Instalación
type: docs
weight: 40
url: /es/python-net/installation/
---
## **Requisitos del sistema**

Primero, debe verificar y confirmar que las especificaciones de la máquina cumplan con las[Requisitos del sistema](/3d/es/python-net/system-requirements/).

## **Instalación Aspose.3D para Python via .NET**
`pip` es la forma más fácil de descargar e instalar[Aspose.3D para Python via .NET](https://pypi.org/project/aspose-3d/).

Para instalar Aspose.3D, ejecute este comando: aspose-3d de instalación pip

## **Usando Aspose.3D para Python via .NET**

Una vez que termine de instalar el módulo, puede usar Aspose.3D desde su código python de esta manera:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

