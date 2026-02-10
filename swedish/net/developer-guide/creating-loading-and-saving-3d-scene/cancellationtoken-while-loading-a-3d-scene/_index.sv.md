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
