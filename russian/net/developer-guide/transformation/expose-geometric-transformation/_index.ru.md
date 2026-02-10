---
title: Выяснить геометрическую трансформацию
type: docs
weight: 80
url: /ru/net/expose-geometric-transformation/
description: Aspose.3D for .NET позволяет выставить геометрическое преобразование сцены 3D. Вы можете оценить глобальное преобразование с помощью метода EvaluateGlobalTransform.
---
##  **Выяснить геометрическую трансформацию**
Aspose.3D for .NET позволяет выставить геометрическое преобразование сцены 3D. Вы можете оценить глобальную трансформацию, используя метод `EvaluateGlobalTransform`. Следующий фрагмент кода показывает, как раскрыть геометрическое преобразование.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize node 
var n = new Node();
// Get Geometric Translation
n.Transform.GeometricTranslation = new Vector3(10, 0, 0);
// The first Console.WriteLine will output the transform matrix that includes the geometric transformation 
// while the second one will not.
Console.WriteLine(n.EvaluateGlobalTransform(true));
Console.WriteLine(n.EvaluateGlobalTransform(false));

{{< /highlight >}}
