---
title: 3D sahnesini C# olarak yüklerken iptal etme
linktitle: 3D sahnesini yüklerken iptal etme
type: docs
weight: 80
url: /tr/net/cancellationtoken-while-loading-a-3d-scene/
description: C# 3D dosya manipülasyonu ve dönüşüm API ile ihtiyacınız olan herhangi bir zamanda kaydetme/açık görevi iptal etmek için iptal edilen kaynağı kullanabilirsiniz.
---
##  **3D sahnesini yüklerken iptal etme**
All açık/kaydetme yöntemleri, varsayılan bir değere sahip ekstra bir iptal işlemine sahip olacaktır, böylece bu yöntemleri kullanan kodların derlemek için değiştirilmesine gerek yoktur.

Bu C# kod örneğinde C# 3D dosya biçimleri manipülasyonu API ile gösterildiği gibi, istediğiniz zaman kaydetme/açık görevi iptal etmek için `CancellationTokenSource` kullanabilirsiniz:

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
