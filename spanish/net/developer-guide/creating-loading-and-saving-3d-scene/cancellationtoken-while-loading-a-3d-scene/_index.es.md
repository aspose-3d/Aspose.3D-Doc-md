---
title: CancellationToken mientras carga una escena 3D en C#
linktitle: CancellationToken mientras cargaba una escena 3D
type: docs
weight: 80
url: /es/net/cancellationtoken-while-loading-a-3d-scene/
description: Puede usar CancelationTokenSource para cancelar la tarea de guardar/abrir en cualquier momento que necesite con C# 3D manipulación de archivos y conversión API.
---
## **CancellationToken mientras cargaba una escena 3D**
Todos los métodos de abrir/guardar tendrán un parámetro de cancelación adicional con un valor predeterminado, por lo que los códigos que utilizan estos métodos no necesitan modificar para compilar.

Puede usar el `CancellationTokenSource` para cancelar la tarea de guardar/abrir en cualquier momento que lo necesite, como se muestra en este ejemplo de código C# con la manipulación de formatos de archivo C# 3D:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
