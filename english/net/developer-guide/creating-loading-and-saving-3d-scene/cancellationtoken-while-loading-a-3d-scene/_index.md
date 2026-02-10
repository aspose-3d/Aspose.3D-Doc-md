---
title: CancellationToken while loading a 3D scene in C#
linktitle: CancellationToken while loading a 3D scene
type: docs
weight: 80
url: /net/cancellationtoken-while-loading-a-3d-scene/
description: You can use the CancellationTokenSource to cancel the save/open task at any time you need with C# 3D file manipulation and conversion API.
---

## **CancellationToken while loading a 3D scene**
All open/save methods will have an extra cancellationToken parameter with a default value, so codes that used these methods don't need to modify to compile.

You can use the `CancellationTokenSource` to cancel the save/open task at any time you need, as shown in this C# code example with C# 3D file formats manipulation API:

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
