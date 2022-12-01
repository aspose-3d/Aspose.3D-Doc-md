---
title: Установка
type: docs
weight: 40
url: /ru/python-net/installation/
---
## **Системные Требования**

Во-первых, вы должны проверить и подтвердить, что спецификации машины соответствуют[Требования к системе](/3d/ru/python-net/system-requirements/).

## **Установка Aspose.3D для Python via .NET**
`pip`-это самый простой способ скачать и установить[Aspose.3D для Python via .NET](https://pypi.org/project/aspose-3d/).

Чтобы установить Aspose.3D, запустите эту команду: pip install aspose-3d

## **Использование Aspose.3D для Python via .NET**

Как только вы закончите установку модуля, вы можете использовать Aspose.3D из вашего кода Python следующим образом:

```py
import aspose.threed as a3d

scene = a3d.Scene()
scene.root_node.create_child_node(a3d.entities.Cylinder())
scene.save("Cylinder.fbx", a3d.FileFormat.FBX7400ASCII)
```

