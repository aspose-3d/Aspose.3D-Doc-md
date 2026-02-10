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



{{< highlight "python" >}}
from aspose import pycore
from aspose.threed import FileFormat
from aspose.threed.entities import PointCloud

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
pointCloud = pycore.cast(PointCloud, FileFormat.DRACO.decode("data-dir"  + "point_cloud_no_qp.drc"))

{{< /highlight >}}
#  **Encode Mesh**
Aspose.3D for Python via .NET permet d'encoder directement un maillage de sphère dans un fichier Draco sans construire de scène en utilisant la méthode [`encode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/encode/methods/2) de la classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.DRACO.encode(Sphere(), "data-dir"  + "sphere.drc")

{{< /highlight >}}
#  **Encoder la sphère en tant que PointCloud**
Aspose.3D for Python via .NET permet d'encoder un maillage de sphère dans un fichier Draco comme un nuage de points en utilisant la méthode [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.dracoformat/encode/methods/2) de la classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import DracoSaveOptions

options = DracoSaveOptions()
options.point_cloud = true 
#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.DRACO.encode(Sphere(), "data-dir"  + "sphere.drc", options)

{{< /highlight >}}
#  **Encoder le maillage à PLY**
Aspose.3D for Python via .NET permet d'encoder directement un maillage vers un fichier PLY sans construire de scène en utilisant la méthode [Encode](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) de la classe [PlyFormat](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "sphere.ply")

{{< /highlight >}}
#  **Décoder le maillage à partir de PLY**
Aspose.3D for Python via .NET permet de décoder un maillage/nuage de points à partir d'un fichier PLY en utilisant la méthode [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1) de la classe [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "sphere.ply")

{{< /highlight >}}
#  **Exporter vers PLY en tant que PointCloud**
Aspose.3D for Python via .NET permet d'exporter une scène vers PLY en tant que PointCloud en utilisant la méthode [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) de la classe [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import PlySaveOptions

options = PlySaveOptions()
options.point_cloud = true 
#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.encode(Sphere(), "data-dir"  + "sphere.ply", options)

{{< /highlight >}}
#  **Exporter 3D Scène sous forme de nuage de points**
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.8 ou supérieure.

{{% /alert %}} 

Aspose.3D for Python via .NET permet d'exporter une scène 3D en tant que PointCloud en utilisant la propriété [`point_cloud`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) de la classe [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). L'extrait de code suivant montre comment utiliser cette fonctionnalité:

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Sphere
from aspose.threed.formats import ObjSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
scene = Scene(Sphere())
options = ObjSaveOptions()
options.point_cloud = true 
scene.save("data-dir"  + "Export3DSceneAsPointCloud.obj", options)

{{< /highlight >}}
