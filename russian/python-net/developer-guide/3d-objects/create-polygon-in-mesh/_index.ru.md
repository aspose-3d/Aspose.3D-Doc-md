---
title: Создать многоугольник в сетке
type: docs
weight: 40
url: /ru/python-net/create-polygon-in-mesh/
description: Aspose.3D for Python via .NET позволяет создать многоугольник в сетке. Чтобы использовать функциональность, API предлагает метод CreatePolygon класса Mesh.
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 
##  **Создать многоугольник в сетке**
Aspose.3D for Python via .NET позволяет создать многоугольник в сетке. Чтобы использовать функциональность, API предлагает метод [`create_polygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) класса [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh). Используя метод `create_polygon`, вы можете создать оптимизированный полигон [Треугольник](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) или [Квад](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1) без выделения дополнительной памяти. Следующий фрагмент кода показывает, как использовать эту функциональность.

{{< highlight "python" >}}
from aspose.threed.entities import Mesh

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
mesh = Mesh()
mesh.create_polygon([0, 1, 2 ])
mesh.create_polygon(0, 1, 2)

{{< /highlight >}}
