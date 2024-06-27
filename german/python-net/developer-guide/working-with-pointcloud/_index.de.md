---
title: Mit Point Cloud arbeiten
type: docs
weight: 150
url: /de/python-net/working-with-pointcloud/
description: Aspose.3D for Python via .NET ermöglicht das direkte Decodieren eines Netzes aus einer Draco-Datei, ohne eine Szene mit der Decode-Methode der DracoFormat-Klasse zu erstellen.
---
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.7 oder höher unterstützt.

{{% /alert %}} 
#  **Netz entschlüsseln**
Aspose.3D for Python via .NET ermöglicht das direkte Decodieren eines Netzes aus einer Draco-Datei, ohne eine Szene mit der [`decode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/decode/methods/1)-Methode der [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)-Klasse zu erstellen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-DecodeMesh-1.py" >}}
#  **Maschen kodieren**
Aspose.3D for Python via .NET ermöglicht die direkte Codierung eines Kugel netzes in eine Draco-Datei, ohne eine Szene mit der [`encode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/encode/methods/2)-Methode der [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)-Klasse zu erstellen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMesh-1.py" >}}
#  **Kugel als Point Cloud codieren**
Aspose.3D for Python via .NET ermöglicht die Codierung eines Kugel netzes in eine Draco-Datei als Punktwolke mithilfe der [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.dracoformat/encode/methods/2)-Methode der [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeSphereAsPointCloud-1.py" >}}
#  **Encodieren Sie Mesh auf PLY**
Aspose.3D for Python via .NET ermöglicht die direkte Codierung eines Netzes in eine PLY-Datei, ohne eine Szene mit der [Kodieren](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1)-Methode der [Ply Format](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat)-Klasse zu erstellen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
#  **Dekodieren Sie Mesh von PLY**
Aspose.3D for Python via .NET ermöglicht das Decodieren einer Mesh/Point Cloud aus einer PLY-Datei mit der [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1)-Methode der [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
#  **Als Point Cloud nach PLY exportieren**
Aspose.3D for Python via .NET ermöglicht den Export einer Szene nach PLY als Point Cloud mit der [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1)-Methode der [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-ExportToPlyAsPointCloud-1.py" >}}
#  **3D Szene als Point Cloud exportieren**
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.8 oder höher unterstützt.

{{% /alert %}} 

Aspose.3D for Python via .NET ermöglicht den Export einer 3D-Szene als Point Cloud mit der [`point_cloud`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud)-Eigenschaft der [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-Export3DSceneAsPointCloud-1.py" >}}
