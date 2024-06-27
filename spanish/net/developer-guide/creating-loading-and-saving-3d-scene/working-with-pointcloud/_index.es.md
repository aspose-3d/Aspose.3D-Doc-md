---
title: Trabajar con PointCloud
type: docs
weight: 150
url: /es/net/working-with-pointcloud/
description: Aspose.3D for .NET permite decodificar una malla desde un archivo Draco directamente sin construir una escena usando el método Decode de la clase DracoFormat.
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,7 o superior.

{{% /alert %}} 
#  **Decodificar malla**
Aspose.3D for .NET permite decodificar una malla de un archivo Draco directamente sin construir una escena usando el método [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/decode/methods/1) de la clase [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-DecodeMesh-1.cs" >}}
#  **Codificar malla**
Aspose.3D for .NET permite codificar una malla de esfera en un archivo Draco directamente sin construir una escena usando el método [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) de la clase [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeMesh-1.cs" >}}
#  **Codificar Esfera como PointCloud**
Aspose.3D for .NET permite codificar una malla de esfera en un archivo Draco como una nube de puntos utilizando el método [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) de la clase [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeSphereAsPointCloud-1.cs" >}}
#  **Encode Mesh a PLY**
Aspose.3D for .NET permite codificar una malla en un archivo PLY directamente sin construir una escena usando el método [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) de la clase [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeMeshToPly-1.cs" >}}
#  **Decodificar malla desde PLY**
Aspose.3D for .NET permite decodificar una malla/nube de puntos a partir de un archivo PLY usando el método [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/decode/methods/1) de la clase [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeMeshToPly-1.cs" >}}
#  **Exportar a PLY como PointCloud**
Aspose.3D for .NET permite exportar una escena a PLY como PointCloud utilizando el método [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) de la clase [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-ExportToPlyAsPointCloud-1.cs" >}}
#  **Exportar escena 3D como nube de puntos**
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,8 o superior.

{{% /alert %}} 

Aspose.3D for .NET permite exportar una escena 3D como PointCloud usando la propiedad [`PointCloud`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) de la clase [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). El siguiente fragmento de código muestra cómo utilizar esta funcionalidad:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-Export3DSceneAsPointCloud-1.cs" >}}
