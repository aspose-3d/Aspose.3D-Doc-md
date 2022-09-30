---
title: Installation
type: docs
weight: 40
url: /fr/python-net/installation/
---
## **Configuration requise**

Tout d'abord, vous devez vérifier et confirmer que les spécifications de la machine répondent[Exigences du système](/3d/fr/python-net/system-requirements/).

## **Installation Aspose.3D pour Python via .NET**
`pip` est le moyen le plus simple de télécharger et d'installer[Aspose.3D pour Python via .NET](https://pypi.org/project/aspose-3d/).

Pour installer Aspose.3D, exécutez cette commande: pip installer aspose-3d

## **Utilisation de Aspose.3D pour Python via .NET**

Une fois que vous avez fini d'installer le module, vous pouvez utiliser Aspose.3D à partir de votre code python de cette façon:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

