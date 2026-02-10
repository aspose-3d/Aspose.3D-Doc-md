---
title: Travailler avec PointCloud
type: docs
weight: 150
url: /fr/net/working-with-pointcloud/
description: Aspose.3D for .NET permet de décoder un maillage à partir d'un fichier Draco directement sans construire de scène en utilisant la méthode Decode de la classe DracoFormat.
---
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.7 ou supérieure.

{{% /alert %}} 
#  **Décoder la maille**
Aspose.3D for .NET permet de décoder un maillage à partir d'un fichier Draco directement sans construire de scène en utilisant la méthode [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/decode/methods/1) de la classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var pointCloud = (PointCloud)FileFormat.Draco.Decode("point_cloud_no_qp.drc");

{{< /highlight >}}
#  **Encode Mesh**
Aspose.3D for .NET permet de coder directement un maillage de sphère dans un fichier Draco sans construire de scène en utilisant la méthode [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) de la classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.Draco.Encode(new Sphere(), "sphere.drc");

{{< /highlight >}}
#  **Encoder la sphère en tant que PointCloud**
Aspose.3D for .NET permet d'encoder un maillage de sphère dans un fichier Draco en tant que nuage de points en utilisant la méthode [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) de la classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.Draco.Encode(new Sphere(), "sphere.drc", new DracoSaveOptions() { PointCloud = true });

{{< /highlight >}}
#  **Encoder le maillage à PLY**
Aspose.3D for .NET permet d'encoder un maillage dans un fichier PLY directement sans construire de scène en utilisant la méthode [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) de la classe [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
#  **Décoder le maillage à partir de PLY**
Aspose.3D for .NET permet de décoder un maillage/nuage de points à partir d'un fichier PLY en utilisant la méthode [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/decode/methods/1) de la classe [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
#  **Exporter vers PLY en tant que PointCloud**
Aspose.3D for .NET permet d'exporter une scène vers PLY en tant que PointCloud en utilisant la méthode [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) de la classe [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply", new PlySaveOptions() { PointCloud = true });


{{< /highlight >}}
#  **Exporter 3D Scène sous forme de nuage de points**
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.8 ou supérieure.

{{% /alert %}} 

Aspose.3D for .NET permet d'exporter une scène 3D en tant que PointCloud en utilisant la propriété [`PointCloud`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) de la classe [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). L'extrait de code suivant montre comment utiliser cette fonctionnalité:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var scene = new Scene(new Sphere());
scene.Save("Export3DSceneAsPointCloud.obj", new ObjSaveOptions() { PointCloud = true });

{{< /highlight >}}
