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

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
