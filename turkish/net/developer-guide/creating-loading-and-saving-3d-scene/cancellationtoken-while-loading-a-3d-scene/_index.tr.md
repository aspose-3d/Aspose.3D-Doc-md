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

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
