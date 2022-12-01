---
title: CancellationToken во время загрузки сцены 3D в C#
linktitle: CancellationToken во время загрузки сцены 3D
type: docs
weight: 80
url: /ru/net/cancellationtoken-while-loading-a-3d-scene/
description: Вы можете использовать CancellationTokenSource для отмены задачи сохранения/открытия в любое время, которое вам нужно, с помощью C# 3D манипуляции с файлом и преобразования API.
---
## **CancellationToken во время загрузки сцены 3D**
Все методы открытия/сохранения будут иметь дополнительный параметр cancellationToken со значением по умолчанию, поэтому коды, которые использовали эти методы, не нужно изменять для компиляции.

Вы можете использовать `CancellationTokenSource`, чтобы отменить задачу сохранения/открытия в любое время, как показано в этом примере кода C# с C# 3D манипулирование форматами файлов API:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
