---
title: Mit Point Cloud arbeiten
type: docs
weight: 150
url: /de/net/working-with-pointcloud/
description: Aspose.3D for .NET ermöglicht das direkte Decodieren eines Netzes aus einer Draco-Datei, ohne eine Szene mit der Decode-Methode der DracoFormat-Klasse zu erstellen.
---
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.7 oder höher unterstützt.

{{% /alert %}} 
#  **Netz entschlüsseln**
Aspose.3D for .NET ermöglicht das direkte Decodieren eines Netzes aus einer Draco-Datei, ohne eine Szene mit der [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/decode/methods/1)-Methode der [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)-Klasse zu erstellen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-DecodeMesh-1.cs" >}}
#  **Maschen kodieren**
Aspose.3D for .NET ermöglicht die direkte Codierung eines Kugel netzes in eine Draco-Datei, ohne eine Szene mit der [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2)-Methode der [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)-Klasse zu erstellen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeMesh-1.cs" >}}
#  **Kugel als Point Cloud codieren**
Aspose.3D for .NET ermöglicht das Codieren eines Kugel netzes in Draco-Datei als Punktwolke mit der [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2)-Methode der [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeSphereAsPointCloud-1.cs" >}}
#  **Encodieren Sie Mesh auf PLY**
Aspose.3D for .NET ermöglicht die direkte Codierung eines Netzes in PLY-Datei, ohne eine Szene mit der [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1)-Methode der [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat)-Klasse zu erstellen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeMeshToPly-1.cs" >}}
#  **Dekodieren Sie Mesh von PLY**
Aspose.3D for .NET ermöglicht das Decodieren einer Mesh-/Punktwolke aus einer PLY-Datei mit der [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/decode/methods/1)-Methode der [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeMeshToPly-1.cs" >}}
#  **Als Point Cloud nach PLY exportieren**
Aspose.3D for .NET ermöglicht den Export einer Szene nach PLY als Point Cloud mithilfe der [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1)-Methode der [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-ExportToPlyAsPointCloud-1.cs" >}}
#  **3D Szene als Point Cloud exportieren**
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.8 oder höher unterstützt.

{{% /alert %}} 

Aspose.3D for .NET ermöglicht den Export einer 3D-Szene als Point Cloud unter Verwendung der [`PointCloud`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud)-Eigenschaft der [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-Export3DSceneAsPointCloud-1.cs" >}}
