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

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            CancellationTokenSource cts = new CancellationTokenSource();
            Scene scene = new Scene();
            cts.CancelAfter(1000);
            try
            {
                scene.Open("document.fbx" , cts.Token);
                Console.WriteLine("Import is done within 1000ms");
            }
            catch (ImportException e)
            {
                if (e.InnerException is OperationCanceledException)
                {
                    Console.WriteLine("It takes too long time to import, import has been canceled.");
                }
            }

{{< /highlight >}}
