---
title: Geteiltes Netz
type: docs
weight: 100
url: /de/python-net/split-mesh/
description: Entwickler müssen möglicher weise alle Maschen einer Szene in mehrere Unter netze pro Material aufteilen. Die SplitMesh-Methode teilt kein Netz der Szene auf, wenn ihr ein einzelnes Material zugewiesen wurde. Entwickler können dies jetzt erreichen, indem sie Aspose.3D for Python via .NET API verwenden.
---
##  **Alle Maschen einer Szene pro Material aufteilen**
Entwickler müssen möglicher weise alle Maschen einer Szene in mehrere Unter netze pro Material aufteilen. Die `split_mesh`-Methode teilt kein Netz der Szene auf, wenn ihr ein einzelnes Material zugewiesen wurde. Entwickler können dies jetzt erreichen, indem sie [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API verwenden.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum gibt die Daten richtlinie an, die im Mesh-Splitting-Algorithmus verwendet wird. Es unterstützt zwei Richtlinien, Daten zwischen Subnetz teilen oder jedes Sub-Mesh hat seine eigenen Daten (nur verwendete Daten).

{{% /alert %}}

Das folgende Code beispiel teilt alle Maschen einer Szene pro Material auf. Jedes Teil netz teilt die gleichen direkten Daten und unter scheidet sich nur in Indizes.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.py" >}}
##  **Teilen Sie ein Netz, indem Sie das Material angeben**
Mit Aspose.3D for Python via .NET API können Entwickler ein Netz aufteilen, indem sie das Material manuell angeben. Die Split-Mesh-Option erstellt separate Objekte und jedes Sub-Mesh verwendet nur ein Material.
###  **Teilen Sie das Netz der Box**
Dieses Hilfe thema erstellt ein Netz der Box, um den Code umfassend und kurz zu halten. Entwickler können ein Netz manuell erstellen, wie in diesem Hilfe thema beschrieben: [Erstellen Sie ein 3D Cube Mesh](/3d/de/python-net/create-3d-mesh-and-scene/). Darüber hinaus besteht eine Box aus 6 Ebenen und jede Ebene wird zu einem Teilnetz. Das folgende Code beispiel teilt ein primitives Netz, indem das Material manuell angegeben wird.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.py" >}}
