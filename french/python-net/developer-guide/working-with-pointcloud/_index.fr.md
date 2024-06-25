---
title: Travailler avec PointCloud
type: docs
weight: 150
url: /fr/python-net/working-with-pointcloud/
description: Aspose.3D for Python via .NET permet de décoder un maillage à partir d'un fichier Draco directement sans construire une scène en utilisant la méthode Decode de la classe DracoFormat.
---
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.7 ou supérieure.

{{% /alert %}} 
#  **Décoder la maille**
Aspose.3D for Python via .NET permet de décoder un maillage à partir d'un fichier Draco directement sans construire une scène en utilisant la méthode [`decode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/decode/methods/1) de la classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-DecodeMesh-1.py" >}}
#  **Encode Mesh**
Aspose.3D for Python via .NET permet d'encoder directement un maillage de sphère dans un fichier Draco sans construire de scène en utilisant la méthode [`encode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/encode/methods/2) de la classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMesh-1.py" >}}
#  **Encoder la sphère en tant que PointCloud**
Aspose.3D for Python via .NET permet d'encoder un maillage de sphère dans un fichier Draco comme un nuage de points en utilisant la méthode [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.dracoformat/encode/methods/2) de la classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeSphereAsPointCloud-1.py" >}}
#  **Encoder le maillage à PLY**
Aspose.3D for Python via .NET permet d'encoder directement un maillage vers un fichier PLY sans construire de scène en utilisant la méthode [Encode](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) de la classe [PlyFormat](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
#  **Décoder le maillage à partir de PLY**
Aspose.3D for Python via .NET permet de décoder un maillage/nuage de points à partir d'un fichier PLY en utilisant la méthode [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1) de la classe [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
#  **Exporter vers PLY en tant que PointCloud**
Aspose.3D for Python via .NET permet d'exporter une scène vers PLY en tant que PointCloud en utilisant la méthode [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) de la classe [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-ExportToPlyAsPointCloud-1.py" >}}
#  **Exporter 3D Scène sous forme de nuage de points**
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.8 ou supérieure.

{{% /alert %}} 

Aspose.3D for Python via .NET permet d'exporter une scène 3D en tant que PointCloud en utilisant la propriété [`point_cloud`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) de la classe [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). L'extrait de code suivant montre comment utiliser cette fonctionnalité:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-Export3DSceneAsPointCloud-1.py" >}}
