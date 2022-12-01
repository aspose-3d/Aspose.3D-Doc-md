---
title: Генерировать нормальные данные для всех сеток модели 3D
type: docs
weight: 40
url: /ru/java/generate-normal-data-for-all-meshes-of-3d-model/
description: Aspose.3D for Java API имеет поддержку генерации нормальных данных для всех сеток модели 3D (без нормальных данных).
---
{{% alert color="primary" %}} 

Aspose.3D for Java API имеет поддержку генерации нормальных данных для всех сеток модели 3D (без нормальных данных).

{{% /alert %}} 
## **Генерировать нормальные данные для всех сеток модели 3DS**
Метод generateNormal, открытый классом `PolygonModifier`, может использоваться для генерации нормальных данных для всех сеток в файле 3DS. Если элемент VertexElementSmoothingGroup был определен в сетке, сгенерированные нормальные данные будут сглажены VertexmentElementSmoothingGroup.
### **Образец программирования**
Этот пример кода загружает файл 3DS, посещает все узлы и создает нормальные данные для всех сеток.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-GenerateDataForMeshes.java" >}}
