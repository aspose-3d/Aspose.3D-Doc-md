---
title: C# yılında 3D sahnesini yüklerken CancellationToken
linktitle: 3D sahnesini yüklerken CancellationToken
type: docs
weight: 80
url: /tr/net/cancellationtoken-while-loading-a-3d-scene/
description: You, C# 3D dosya manipülasyonu ve dönüşüm API ile ihtiyacınız olan her zaman kaydetme/açık görevi iptal etmek için CancellationTokenSource kullanabilir.
---
## **3D sahnesini yüklerken CancellationToken**
All açık/kaydetme yöntemleri, varsayılan bir değere sahip ekstra bir iptal işlemine sahip olacaktır, böylece bu yöntemleri kullanan kodların derlemek için değiştirilmesine gerek yoktur.

You, C# kod örneğinde C# 3D dosya biçimleri manipülasyonu 076481 481 ile gösterildiği gibi, istediğiniz zaman kaydetme/açık görevi iptal etmek için `CancellationTokenSource` kullanabilirsiniz:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
