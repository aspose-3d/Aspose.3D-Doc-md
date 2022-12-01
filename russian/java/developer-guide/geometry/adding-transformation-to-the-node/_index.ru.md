---
title: Добавление преобразования к узлу
type: docs
weight: 10
url: /ru/java/adding-transformation-to-the-node/
description: "Aspose.3D for Java API имеет поддержку вращения объектов в пространстве 3D. Есть три способа определить вращение объекта в пространстве 3D: углы Эйлера, кватернион и пользовательская матрица, все они поддерживаются классом Transform."
---
{{% alert color="primary" %}} 

Aspose.3D for Java API имеет поддержку вращения объектов в пространстве 3D. Есть три способа определить вращение объекта в пространстве 3D: углы Эйлера, Quaternion и Custom Matrix, все они поддерживаются классом `Transform`.

{{% /alert %}} 

TSR (перевод/масштабирование/вращение) чаще всего используются в сценарии 3D, мы предоставили класс `Transform` для доступа к ним в Aspose.3D Аффинные преобразования включают:

- Перевод
- Масштабирование
- Вращение
- Отображение сдвига
- Отжать картографирование

{{% alert color="primary" %}} 

Объект класса `Mesh` используется в коде. Мы можем[Создать объект класса Mesh, как там рассказано](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
## **Вращать от Quaternion**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByQuaternion.java" >}}
## **Поворот от углов Эйлера**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByEulerAngles.java" >}}
## **Пользовательская матрица трансформации**
Мы также можем использовать Matrix напрямую:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByTransformationMatrix.java" >}}
