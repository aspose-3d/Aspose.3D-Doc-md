---
title: 在C#中加载3D场景时取消令牌
linktitle: 加载3D场景时取消令牌
type: docs
weight: 80
url: /zh/net/cancellationtoken-while-loading-a-3d-scene/
description: 您可以使用CancellationTokenSource在C# 3D文件操作和转换API的任何时候取消保存/打开任务。
---
## **加载3D场景时取消令牌**
所有打开/保存方法都将有一个带有默认值的额外cancellationToken参数，因此使用这些方法的代码不需要修改即可编译。

您可以使用`CancellationTokenSource`在需要的任何时候取消保存/打开任务，如C# 3D文件格式操作API的C#代码示例所示:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
