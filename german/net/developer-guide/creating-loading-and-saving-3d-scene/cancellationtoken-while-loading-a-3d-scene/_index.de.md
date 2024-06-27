---
title: Cancel lation Token beim Laden einer 3D-Szene in C#
linktitle: Cancel lation Token beim Laden einer 3D-Szene
type: docs
weight: 80
url: /de/net/cancellationtoken-while-loading-a-3d-scene/
description: Sie können die Cancel lation Token Source verwenden, um die Aufgabe Speichern/Öffnen jederzeit mit C# 3D Datei manipulation und Konvertierung API abzubrechen.
---
##  **Cancel lation Token beim Laden einer 3D-Szene**
Alle Open/Save-Methoden verfügen über einen zusätzlichen Cancel lation Token-Parameter mit einem Standardwert, sodass Codes, die diese Methoden verwendet haben, zum Kompilieren nicht geändert werden müssen.

Sie können die `CancellationTokenSource` verwenden, um die Speichern/Öffnen-Aufgabe jederzeit abzubrechen, wie in diesem C#-Code beispiel mit C# 3D Datei-Formate Manipulation API gezeigt:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CancellationToken-CancellationTokenSource.cs" >}}
