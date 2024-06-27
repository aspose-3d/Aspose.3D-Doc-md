---
title: Geteiltes Netz
type: docs
weight: 100
url: /de/net/split-mesh/
description: Entwickler müssen möglicher weise alle Maschen einer Szene in mehrere Unter netze pro Material aufteilen. Die SplitMesh-Methode teilt kein Netz der Szene auf, wenn ihr ein einzelnes Material zugewiesen wurde. Entwickler können dies jetzt erreichen, indem sie Aspose.3D for .NET API verwenden.
---
##  **Alle Maschen einer Szene pro Material aufteilen**
Entwickler müssen möglicher weise alle Maschen einer Szene in mehrere Unter netze pro Material aufteilen. Die SplitMesh-Methode teilt kein Netz der Szene auf, wenn ihr ein einzelnes Material zugewiesen wurde. Entwickler können dies jetzt erreichen, indem sie [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API verwenden.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum gibt die Daten richtlinie an, die im Mesh-Splitting-Algorithmus verwendet wird. Es unterstützt zwei Richtlinien, Daten zwischen Subnetz teilen oder jedes Sub-Mesh hat seine eigenen Daten (nur verwendete Daten).

{{% /alert %}}

Das folgende Code beispiel teilt alle Maschen einer Szene pro Material auf. Jedes Teil netz teilt die gleichen direkten Daten und unter scheidet sich nur in Indizes.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.cs" >}}
##  **Teilen Sie ein Netz, indem Sie das Material angeben**
Aspose.3D for .NET API ermöglicht es Entwicklern, ein Netz aufzuteilen, indem sie das Material manuell angeben. Die Split-Mesh-Option erstellt separate Objekte und jedes Sub-Mesh verwendet nur ein Material.
###  **Teilen Sie das Netz der Box**
Dieses Hilfe thema erstellt ein Netz der Box, um den Code umfassend und kurz zu halten. Entwickler können ein Netz manuell erstellen, wie in diesem Hilfe thema beschrieben: [Erstellen Sie ein 3D Cube Mesh](/3d/de/net/create-3d-mesh-and-scene/). Darüber hinaus besteht eine Box aus 6 Ebenen und jede Ebene wird zu einem Teilnetz. Das folgende Code beispiel teilt ein primitives Netz, indem das Material manuell angegeben wird.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.cs" >}}
