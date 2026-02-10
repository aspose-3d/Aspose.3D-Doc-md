---
title: Token de cancelación al cargar una escena 3D en C#
linktitle: CancellationToken al cargar una escena 3D
type: docs
weight: 80
url: /es/net/cancellationtoken-while-loading-a-3d-scene/
description: Puede usar CancellationTokenSource para cancelar la tarea de guardar/abrir en cualquier momento que necesite con la manipulación de archivos C# 3D y la conversión API.
---
##  **CancellationToken al cargar una escena 3D**
Todos los métodos de abrir/guardar tendrán un parámetro de cancelación adicional con un valor predeterminado, por lo que los códigos que utilizan estos métodos no necesitan modificar para compilar.

Puede usar el `CancellationTokenSource` para cancelar la tarea de guardar/abrir en cualquier momento que necesite, como se muestra en este ejemplo de código C# con C# 3D manipulación de formatos de archivo API:

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
