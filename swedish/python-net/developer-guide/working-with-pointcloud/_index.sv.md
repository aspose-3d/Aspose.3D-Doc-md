---
title: Arbeta med PointCloudName
type: docs
weight: 150
url: /sv/python-net/working-with-pointcloud/
description: Aspose.3D for Python via .NET tillåter avkodning av en mesh från en Draco-fil direkt utan att skapa en scen med Dra- avkodningsmetoden Koformat klass.
---
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.7 eller större.

{{% /alert %}} 
#  **Avkoda mask**
Aspose.3D for Python via .NET tillåter avkodning av en mesh från en Draco-fil direkt utan att bygga en scen med [`decode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/decode/methods/1)-metoden för [`decode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/decode/methods/1) [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-DecodeMesh-1.py" >}}
#  **Koda mesh**
Aspose.3D for Python via .NET tillåter kodning av en sfärsmask till en Draco-fil direkt utan att skapa en scen med [`encode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/encode/methods/2) metod för [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMesh-1.py" >}}
#  **Koda sfären som PointCloudName**
Aspose.3D for Python via .NET allows encoding a sphere mesh to Draco file as a point cloud using the [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.dracoformat/encode/methods/2) method of [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) class. The following code snippet shows how to use this functionality:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeSphereAsPointCloud-1.py" >}}
#  **Koda mesh till PLY.**
Aspose.3D for Python via .NET allows encoding a mesh to PLY file directly without building a scene using the [Encode](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) method of [PlyFormat ](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat)class. The following code snippet shows how to use this functionality:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
#  **Avkoda mesh från PLY.**
Aspose.3D for Python via .NET tillåter avkodning av ett mesh/punktmoln från en PLY-fil med [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1)-metoden för [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat) klassens .. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
#  **Exportera till PLY som PointCloud?**
Aspose.3D for Python via .NET tillåter att exportera en scen till PLY som PointCloud med [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1)-metoden i [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat)-klassen. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-ExportToPlyAsPointCloud-1.py" >}}
#  **Exportera 3D Scene som punktmoln**
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 

Aspose.3D for Python via .NET tillåter att en 3D scen exporteras som PointCloud med egendom [`point_cloud`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) i klassen [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). Följande kodsnutt visar hur denna funktionalitet ska användas:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-Export3DSceneAsPointCloud-1.py" >}}
