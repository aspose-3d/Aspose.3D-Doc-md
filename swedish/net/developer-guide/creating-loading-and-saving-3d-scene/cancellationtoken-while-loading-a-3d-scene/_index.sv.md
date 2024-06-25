---
title: AvbokningToken vid laddning av en 3D i C#
linktitle: AvbokningToken vid laddning av en 3D-scen
type: docs
weight: 80
url: /sv/net/cancellationtoken-while-loading-a-3d-scene/
description: Du kan använda AvbokningTokenSource för att avbryta spara/öppna aktiviteten när som helst du behöver med C# 3D filmanipulering och konvertering. API.
---
##  **AvbokningToken vid laddning av en 3D-scen**
Alla öppna / spara metoder kommer att ha en extra avbokningTokenparameter med ett standardvärde, så koder som använde dessa metoder behöver inte ändra för att kompilera.

Du kan använda `CancellationTokenSource` för att avbryta spara/öppna aktiviteten när som helst du behöver, som visas i detta C# kodexempel med C# 3D filformatmanipulering API:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
