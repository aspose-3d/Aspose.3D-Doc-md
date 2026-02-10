---
title: CancellationToken durante il caricamento di una scena 3D in C#
linktitle: CancellationToken durante il caricamento di una scena 3D
type: docs
weight: 80
url: /it/net/cancellationtoken-while-loading-a-3d-scene/
description: È possibile utilizzare CancellationTokenSource per annullare l'attività di salvataggio/apertura in qualsiasi momento necessario con C# 3D manipolazione di file e conversione API.
---
##  **CancellationToken durante il caricamento di una scena 3D**
Tutti i metodi di open/save avranno un parametro di cancellazione extra Token con un valore predefinito, quindi i codici che hanno utilizzato questi metodi non devono essere modificati per essere compilati.

Puoi utilizzare `CancellationTokenSource` per annullare l'attività di salvataggio/apertura in qualsiasi momento, come mostrato in questo esempio di codice C# con C# 3D formati di file manipolare API:

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
