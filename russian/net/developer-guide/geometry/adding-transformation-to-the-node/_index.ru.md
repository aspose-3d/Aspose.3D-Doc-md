---
title: Добавление преобразования к узлу
type: docs
weight: 30
url: /ru/net/adding-transformation-to-the-node/
description: TSR (перевод/масштабирование/вращение) чаще всего используются в сценарии 3D, мы предоставили класс Transform для доступа к ним в Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET предлагает вращать объекты в пространстве 3D. Есть три способа определить вращение объекта в пространстве 3D: углы Эйлера, кватернион и пользовательская матрица, все они поддерживаются классом [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform).

{{% /alert %}}

TSR (перевод/масштабирование/вращение) чаще всего используются в сценарии 3D, мы предоставили класс `Transform` для доступа к ним в Aspose.3D. Аффинные преобразования включают:

- Перевод
- Масштабирование
- Вращение
- Отображение сдвига
- Отжать картографирование

{{% alert color="primary" %}}

Объект класса [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) используется в коде. Мы можем[Создать объект класса Mesh, как там рассказано](/3d/ru/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Вращать от Quaternion**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.cs" >}}
## **Поворот от углов Эйлера**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.cs" >}}
## **Пользовательская матрица трансформации**
Мы также можем использовать Matrix напрямую:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.cs" >}}
