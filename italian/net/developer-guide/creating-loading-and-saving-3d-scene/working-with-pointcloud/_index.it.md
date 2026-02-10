---
title: Lavorare con PointCloud
type: docs
weight: 150
url: /it/net/working-with-pointcloud/
description: Aspose.3D for .NET consente di decodificare direttamente una mesh da un file Draco senza creare una scena utilizzando il metodo Decode della classe DracoFormat.
---
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.7 o maggiore.

{{% /alert %}} 
#  **Decodificare la maglia**
Aspose.3D for .NET consente di decodificare direttamente una mesh da un file Draco senza creare una scena utilizzando il metodo [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/decode/methods/1) della classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var pointCloud = (PointCloud)FileFormat.Draco.Decode("point_cloud_no_qp.drc");

{{< /highlight >}}
#  **Code Mesh**
Aspose.3D for .NET consente di codificare direttamente una mesh a sfera in un file Draco senza creare una scena utilizzando il metodo [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) della classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.Draco.Encode(new Sphere(), "sphere.drc");

{{< /highlight >}}
#  **Codificare sfera come PointCloud**
Aspose.3D for .NET consente di codificare una mesh sfera in file Draco come nuvola di punti utilizzando il metodo [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) della classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.Draco.Encode(new Sphere(), "sphere.drc", new DracoSaveOptions() { PointCloud = true });

{{< /highlight >}}
#  **Codificare la maglia fino a PLY**
Aspose.3D for .NET consente di codificare direttamente un file mesh in PLY senza creare una scena utilizzando il metodo [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) della classe [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
#  **Decodificare mesh a partire da PLY**
Aspose.3D for .NET consente di decodificare una nuvola mesh/point da un file PLY utilizzando il metodo [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/decode/methods/1) della classe [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
#  **Esporta a PLY come PointCloud**
Aspose.3D for .NET consente di esportare una scena a PLY come PointCloud utilizzando il metodo [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) della classe [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply", new PlySaveOptions() { PointCloud = true });


{{< /highlight >}}
#  **Esporta 3D scena come Point Cloud**
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.8 o maggiore.

{{% /alert %}} 

Aspose.3D for .NET consente di esportare una scena 3D come PointCloud utilizzando la proprietà [`PointCloud`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) della classe [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). Il seguente frammento di codice mostra come utilizzare questa funzionalità:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var scene = new Scene(new Sphere());
scene.Save("Export3DSceneAsPointCloud.obj", new ObjSaveOptions() { PointCloud = true });

{{< /highlight >}}
