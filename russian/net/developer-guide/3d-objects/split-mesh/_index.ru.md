﻿---
title: Сплит Сетка
type: docs
weight: 100
url: /ru/net/split-mesh/
description: Разработчикам может потребоваться разделить все сетки сцены на несколько субсеток на материал. Метод SplitMesh не будет разделять сетку сцены, если ему был назначен один материал. Теперь разработчики могут достичь этого, используя Aspose.3D for .NET 0761234881.
---
## **Разделите все сетки сцены на материал**
Разработчикам может потребоваться разделить все сетки сцены на несколько субсеток на материал. Метод SplitMesh не будет разделять сетку сцены, если ему был назначен один материал. Теперь разработчики могут добиться этого, используя[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum определяет политику данных, используемую в алгоритме разделения сетки, он поддерживает две политики, совместно использует данные между подсетками или каждая подсетка имеет свои собственные данные (только используемые данные).

{{% /alert %}}

Образец кода ниже разделяет все сетки сцены на материал. Каждая подсетка имеет одни и те же прямые данные и различается только по индексам.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.cs" >}}
## **Разделите сетку, укажите материал**
Aspose.3D for .NET API позволяет разработчикам разделить сетку, вручную указав материал. Опция разделенная сетка создает отдельные объекты, и каждая подсетка будет использовать только один материал.
### **Разделите сетку коробки**
Эта справочная тема создает сетку коробки, чтобы код оставался исчерпывающим и коротким. Разработчики могут построить сетку вручную, как рассказано в этой теме справки:[Создайте сетку куба 3D](/3d/ru/net/create-3d-mesh-and-scene/). Кроме того, коробка состоит из 6 плоскостей, и каждая плоскость станет субсеткой. Образец кода ниже разделяет примитивную сетку, вручную указывая материал.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.cs" >}}
