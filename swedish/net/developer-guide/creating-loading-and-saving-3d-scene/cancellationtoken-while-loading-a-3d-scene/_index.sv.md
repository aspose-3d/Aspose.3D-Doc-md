---
title: AvbeställningToken när du laddar en 3D scen i C#
linktitle: AvbeställningToken vid inladdning av en 3D scene
type: docs
weight: 80
url: /sv/net/cancellationtoken-while-loading-a-3d-scene/
description: Du kan använda AvbrytningTokenSource för att avbryta spara/öppna uppgiften när som helst du behöver med C# 3D fil. manipulation och omvandling API.
---
## **AvbeställningToken vid inladdning av en 3D scene**
Alla öppna / spara metoder kommer att ha en extra avbokningTokenparameter med ett standardvärde, så koder som använde dessa metoder behöver inte ändra för att kompilera.

Du kan använda `CancellationTokenSource` för att avbryta spara/öppna uppgiften när du behöver, som visas i detta exempel C# kodex med C# 3D filformatmanipulering API:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
