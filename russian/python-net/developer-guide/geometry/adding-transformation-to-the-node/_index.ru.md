---
title: Добавление преобразования к узлу
type: docs
weight: 30
url: /ru/python-net/adding-transformation-to-the-node/
description: TSR (преобразование/масштабирование/вращение) чаще всего используются в сценарии 3D, мы предоставили класс Transform для доступа к ним в Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET предлагает вращать объекты в пространстве 3D. Существует три способа определения вращения объекта в пространстве 3D: углы Эйлер, Quaternion и Custom Matrix, все они поддерживаются классом [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform).

{{% /alert %}}

TSR (трансляция/масштабирование/ротация) чаще всего используются в сценарии 3D, мы предоставили класс `Transform` для доступа к ним в Aspose.3D. Аффинные преобразования включают:

- Перевод
- Масштабирование
- Вращение
- Отображение сдвига
- Отжать картографирование

{{% alert color="primary" %}}

В коде используется объект класса [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh). Мы можем [Создать объект класса `Mesh`, как там рассказано](/3d/ru/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Вращать от Quaternion**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.py" >}}
##  **Поворот от углов Эйлера**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.py" >}}
##  **Пользовательская матрица трансформации**
Мы также можем использовать Matrix напрямую:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.py" >}}
