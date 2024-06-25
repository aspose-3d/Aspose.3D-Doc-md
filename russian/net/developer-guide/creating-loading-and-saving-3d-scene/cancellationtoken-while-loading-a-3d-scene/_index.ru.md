---
title: Токен отмены при загрузке сцены 3D в C#
linktitle: Токен отмены при загрузке сцены 3D
type: docs
weight: 80
url: /ru/net/cancellationtoken-while-loading-a-3d-scene/
description: Вы можете использовать CancellationTokenSource, чтобы отменить задачу сохранения/открытия в любое время с помощью C# 3D манипуляций с файлами и конвертации API.
---
##  **Токен отмены при загрузке сцены 3D**
Все методы открытия/сохранения будут иметь дополнительный параметр cancellationToken со значением по умолчанию, поэтому коды, которые использовали эти методы, не нужно изменять для компиляции.

Вы можете использовать `CancellationTokenSource`, чтобы отменить задачу сохранения/открытия в любое время, как показано в этом примере кода C# с манипуляцией форматами файлов C# 3D API:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
