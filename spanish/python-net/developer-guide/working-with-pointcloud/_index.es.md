---
title: Trabajar con PointCloud
type: docs
weight: 150
url: /es/python-net/working-with-pointcloud/
description: Aspose.3D for Python via .NET permite decodificar una malla desde un archivo Draco directamente sin construir una escena usando el método Decode de la clase DracoFormat.
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,7 o superior.

{{% /alert %}} 
#  **Decodificar malla**
Aspose.3D for Python via .NET permite decodificar una malla de un archivo Draco directamente sin construir una escena usando el método [`decode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/decode/methods/1) de la clase [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-DecodeMesh-1.py" >}}
#  **Codificar malla**
Aspose.3D for Python via .NET permite codificar una malla de esfera en un archivo Draco directamente sin construir una escena usando el método [`encode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/encode/methods/2) de la clase [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMesh-1.py" >}}
#  **Codificar Esfera como PointCloud**
Aspose.3D for Python via .NET permite codificar una malla de esfera en un archivo Draco como una nube de puntos utilizando el método [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.dracoformat/encode/methods/2) de la clase [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeSphereAsPointCloud-1.py" >}}
#  **Encode Mesh a PLY**
Aspose.3D for Python via .NET permite codificar una malla en un archivo PLY directamente sin construir una escena usando el método [Codificar](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) de la clase [PlyFormat](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
#  **Decodificar malla desde PLY**
Aspose.3D for Python via .NET permite decodificar una malla/nube de puntos a partir de un archivo PLY utilizando el método [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1) de la clase [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
#  **Exportar a PLY como PointCloud**
Aspose.3D for Python via .NET permite exportar una escena a PLY como PointCloud utilizando el método [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) de la clase [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-ExportToPlyAsPointCloud-1.py" >}}
#  **Exportar escena 3D como nube de puntos**
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,8 o superior.

{{% /alert %}} 

Aspose.3D for Python via .NET permite exportar una escena 3D como PointCloud usando la propiedad [`point_cloud`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) de la clase [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-Export3DSceneAsPointCloud-1.py" >}}
