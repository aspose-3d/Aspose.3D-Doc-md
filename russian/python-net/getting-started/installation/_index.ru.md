---
title: Installation
type: docs
weight: 40
url: /ru/python-net/installation/
---
##  **Системные требования**

Во-первых, вы должны проверить и подтвердить, что технические характеристики машины соответствуют [Требования к системе](/3d/ru/python-net/system-requirements/).

##  **Установка Aspose.3D for Python via .NET**
`pip`-самый простой способ загрузить и установить [Aspose.3D for Python via .NET](https://pypi.org/project/aspose-3d/).

Чтобы установить Aspose.3D, выполните эту команду: pip install aspose-3d

##  **Использование Aspose.3D for Python via .NET**

Как только вы закончите установку модуля, вы можете использовать Aspose.3D из вашего кода python следующим образом:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

