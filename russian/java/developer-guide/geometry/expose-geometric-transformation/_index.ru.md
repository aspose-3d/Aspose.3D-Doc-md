---
title: Выяснить геометрическую трансформацию
type: docs
weight: 50
url: /ru/java/expose-geometric-transformation/
description: Aspose.3D for Java позволяет выставить геометрическое преобразование сцены 3D. Вы можете оценить глобальное преобразование с помощью метода evalivateGlobalTransform.
---
#  **Выяснить геометрическую трансформацию**
Aspose.3D for Java позволяет выставить геометрическое преобразование сцены 3D. Вы можете оценить глобальную трансформацию, используя метод `evaluateGlobalTransform`. Следующий фрагмент кода показывает, как раскрыть геометрическое преобразование.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Initialize node
Node n = new Node();
// Get Geometric Translation
n.getTransform().setGeometricTranslation(new Vector3(10, 0, 0));
// The first Console.WriteLine will output the transform matrix that includes the geometric transformation
// while the second one will not.
System.out.println(n.evaluateGlobalTransform(true));
System.out.println(n.evaluateGlobalTransform(false));

{{< /highlight >}}
