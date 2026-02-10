---
title: 在 C# 中加载 3D 场景时CancellationToken
linktitle: 加载 3D 场景时CancellationToken
type: docs
weight: 80
url: /zh/net/cancellationtoken-while-loading-a-3d-scene/
description: 您可以使用CancellationTokenSource取消保存/打开任务在任何时候你需要与 C# 3D 文件操作和转换 API。
---
##  **加载 3D 场景时CancellationToken**
所有打开/保存方法都将有一个带有默认值的额外cancellationToken参数，因此使用这些方法的代码不需要修改即可编译。

您可以随时使用 `CancellationTokenSource` 取消保存/打开任务，如 C# 代码示例所示，其中包含 C# 3D 文件格式操作 API:

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
