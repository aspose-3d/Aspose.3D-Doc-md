﻿---
title: Добавить иерархию узлов и поделиться геометрическими данными сетки среди нескольких узлов сцены 3D
type: docs
weight: 40
url: /ru/python-net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D для Python via .NET предлагает построить иерархию узлов. Узел-это основной строительный блок сцены. Иерархия узлов определяет логическую структуру сцены и предоставляет видимый контент путем прикрепления к узлам геометрии, освещения и камер.
---
## **Добавить иерархию узлов в документе сцены 3D**
Aspose.3D для Python via .NET предлагает построить иерархию узлов. Узел-это основной строительный блок сцены. Иерархия узлов определяет логическую структуру сцены и предоставляет видимый контент путем прикрепления к узлам геометрии, освещения и камер.
### **Пример графов сцены**
Образец иерархии сцен выглядит так:

![Todo: изображение_Альт_Текст](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

В Aspose.3D каждый экземпляр `Node` может иметь несколько дочерних узлов, в этом примере мы создали узел с двумя узлами куба, если мы повернем корневой узел, все дочерние узлы также будут затронуты:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-NodeHierarchy-AddNodeHierarchy.py" >}}
## **Поделитесь данными геометрии Mesh между несколькими узлами**
Чтобы уменьшить потребности в памяти, один экземпляр класса [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) может быть привязан к различным экземплярам класса [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node). Представьте, что вам нужна система, в которой все кубики 3D казались неотличимыми, однако вам требовалось их большое количество. Вы можете сэкономить память, сделав один объект Mesh, когда система запускается. В этот момент каждый раз, когда вам требуется другая форма, вы делаете еще один объект Node, а затем указываете этот узел на одну сетку. Это называется instancing. Aspose.3D для Python via .NET API позволяет делать instancing.
### **Пример установки**
В таких играх, как RTS (стратегия в реальном времени), мы всегда можем видеть несколько NPC (Non-Player Character) с одной и той же моделью 3D, возможно, в разных цветах, механизм рендеринга обычно имеет одинаковые данные геометрии сетки для разных NPC, этот метод называется Instancing.

{{% alert color="primary" %}}

Объект класса `Mesh` используется в коде. Мы можем[Создать объект класса `Mesh`, как там рассказано](/3d/ru/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Демонстрация кода примера:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MeshGeometryData-ShareMeshGeometryData.py" >}}

В этом примере мы создали 3 кубических узла, которые имеют одну и ту же сетку, каждый из них имеет разный материал с разными цветами.
