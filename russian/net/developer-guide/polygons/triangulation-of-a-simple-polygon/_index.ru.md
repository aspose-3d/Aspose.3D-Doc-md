---
title: Триангуляция простого многоугольника
type: docs
weight: 30
url: /ru/net/triangulation-of-a-simple-polygon/
description: Используя Aspose.3D for .NET API, разработчики могут триангулировать простой многоугольник. Любой многоугольник можно разделить на треугольники. Все операции и вычисления для треугольников могут быть кусочно применены к многоугольнику.
---
{{% alert color="primary" %}}

Используя[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API разработчики могут триангулировать простой многоугольник. Любой многоугольник можно разделить на треугольники. Все операции и вычисления для треугольников могут быть кусочно применены к многоугольнику.

{{% /alert %}}
## **Триангулирование многоугольника**
Разработчики могут выбирать вершины из области многоугольника, а затем формировать треугольники, вызывая метод `Triangulate` класса [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier), каждый из форм V{1}, V{i-1}, V{i} с индексом i, идющим от 3 до n. Классы `Vertex` и `PolygonCanvas` в файле `Triangulate/PolygonCanvas.cs` под демонстрационным приложением (название: Triangulate) демонстрируют способ триангуляции многоугольника с использованием Aspose.3D API.

{{% alert color="primary" %}}

Мы подготовили демо-проект. Пожалуйста, обратитесь к[Этот URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/Demos).

{{% /alert %}}
### **Образец программирования для триангуляции**
Этот пример кода выбирает вершины из области многоугольника, а затем применяет алгоритм для создания треугольников. Вы можете скачать полный рабочий проект этого примера из[Здесь](https://github.com/aspose-3d/Aspose.3D-for-.NET/).

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TriangulationSimplePolygon-Triangulate-PolygonCanvas-TriangulationofaSimplePolygon.cs" >}}
