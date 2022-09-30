---
title: Geteiltes Netz
type: docs
weight: 10
url: /de/java/split-mesh/
description: Aspose.3D for Java API unterstützt alle Maschen einer Szene in mehrere Unternetze pro Material. Die SplitMesh-Methode teilt kein Netz der Szene, wenn ihr ein einzelnes Material zugewiesen wurde. Sie kann unter Verwendung von Aspose.3D for Java API erreicht werden.
---
## **Teilen Sie alle Maschen der Szene pro Material**
Aspose.3D for Java API unterstützt alle Maschen einer Szene in mehrere Unternetze pro Material. Die SplitMesh-Methode teilt kein Netz der Szene, wenn ihr ein einzelnes Material zugewiesen wurde. Sie kann unter Verwendung von Aspose.3D for Java API erreicht werden.

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum gibt die Daten richtlinie an, die im Mesh-Splitting-Algorithmus verwendet wird. Es unterstützt zwei Richtlinien, Daten zwischen Subnetz teilen oder jedes Sub-Mesh hat seine eigenen Daten (nur verwendete Daten).

{{% /alert %}} 

Das folgende Code beispiel teilt alle Maschen einer Szene pro Material auf. Jedes Teil netz teilt die gleichen direkten Daten und unter scheidet sich nur in Indizes.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitAllMeshesofScenebyMaterial.java" >}}
## **Teilen Sie ein Netz, indem Sie das Material angeben**
Aspose.3D for Java API unterstützt die Aufteilung eines Netzes durch manuelle Angabe des Materials. Die Split-Mesh-Option erstellt separate Objekte und jedes Sub-Mesh verwendet nur ein Material.
### **Geteiltes Netz der Box**
Dieses Hilfe thema erstellt ein Netz der Box, um den Code umfassend und kurz zu halten. Entwickler können ein Netz manuell konstruieren, wie in diesem Hilfe thema erzählt:[Erstellen Sie ein 3D Cube Mesh](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). Darüber hinaus besteht eine Box aus 6 Ebenen und jede Ebene wird zu einem Teilnetz. Das folgende Code beispiel teilt ein primitives Netz, indem Material manuell angegeben wird.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitMeshbyMaterial.java" >}}
