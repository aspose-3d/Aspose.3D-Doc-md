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

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
