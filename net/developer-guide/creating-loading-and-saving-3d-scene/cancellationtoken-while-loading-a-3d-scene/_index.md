---
title: CancellationToken while loading a 3D scene
type: docs
weight: 80
url: /net/cancellationtoken-while-loading-a-3d-scene/
---

# **CancellationToken while loading a 3D scene**
All open/save methods will have an extra cancellationToken parameter with a default value, so codes that used these methods don't need to modify to compile.

You can use the CancellationTokenSource to cancel the save/open task at any time you need, as shown in this code example:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
