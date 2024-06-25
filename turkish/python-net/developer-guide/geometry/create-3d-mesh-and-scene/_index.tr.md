---
title: 3D mesh ve sahne oluştur
type: docs
weight: 10
url: /tr/python-net/create-3d-mesh-and-scene/
description: A Mesh, bir dizi kontrol noktası ve gerektiğinde birçok n taraflı poligonlar tarafından tanımlanır. Tonun makalesi nasıl tanımlanacağını açıklıyor.
---
##  **3D küp mesh oluşturun**
Bir [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh), bir dizi kontrol noktası ve gerektiğinde birçok n taraflı poligonlar tarafından tanımlanır. Bu makale bir ağın nasıl tanımlanacağını açıklar.

Bir Mesh yüzeyi oluşturmak için In siparişi, aşağıdaki gibi kontrol noktalarını ve poligonları tanımlamamız gerekiyor:

- [Define Control ints oints](/3d/tr/python-net/create-3d-mesh-and-scene/)
- [PolygonBuilder sınıfı ile poligonlar oluşturun](/3d/tr/python-net/create-3d-mesh-and-scene/)
- [Create olyolygons](/3d/tr/python-net/create-3d-mesh-and-scene/)

Here, küp düğümüne bir Phong malzemesi eklemek için bir örnek:
###  **Define Control ints oints**
A mesh, uzayda bir kontrol noktası seti ve örgü yüzeyini tanımlamak için poligonlar ile oluşur, bir örgü oluşturmak için kontrol noktalarını tanımlamamız gerekir:

{{% alert color="primary" %}}

The control points of all geometries in Aspose.3D use homogeneous coordinate, so it’s `Vector4` instead of `Vector3` in the example code.

{{% /alert %}}

**Ex::**

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-DefineControlPoints.py" >}}


###  **Create olyolygons**
The kontrol noktaları renderable değildir, küpü görünür hale getirmek için, her iki tarafta poligonları tanımlamamız gerekir:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-CreateMeshUsingCreatePolygons.py" >}}


###  **PolygonBuilder sınıfı ile poligonlar oluşturun**
Ayrıca, `PolygonBuilder` sınıfı ile poligon tanımlayabiliriz:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-CreateMeshUsingPolygonBuilder.py" >}}

Now bitti, örgü görünür hale getirmek için, bunun için bir düğüm hazırlamamız gerekiyor.
##  **Ow ow to a riangulate a Mesh**
Triangulate mesh, oyun endüstrisi için yararlıdır, çünkü üçgen, Ghardware hardware donanım desteğinin desteklediği tek desteklenen ilkeldir (üçgen olmayan veriler, gerçek zamanlı olarak verimsiz olan sürücü seviyesinde triangulated edilir)

{{% alert color="primary" %}}

3ds n bu sürüm biz sadece 3ds dosya ihracat, normaller/uvs ve diğer vertex elemanları tarafından gerekli olduğu için poligonlar triangulated bu prosedür sırasında kaybolur, biz gelecekte bunu uygulayabilirsiniz.

{{% /alert %}}

In this example, we triangulate a Mesh by importing FBX file and saved it in FBX format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TriangulateMesh-TriangulateMesh.py" >}}
##  **3D küp sahne oluştur**
Bu konu, 3D sahnesine örgü geometrisinin nasıl ekleneceğini gösteriyor. Örnek kod bir küp yerleştirir ve desteklenen dosya formatlarında 3D görüntüsünü kaydeder.
###  **Create a Cube Node**
A node görünmezdir, ancak düğüme bağlı geometri işlenebilir.

{{% alert color="primary" %}}

The Mesh class object is being used in the code. We can [create a `Mesh` class object as narrated there](https://docs.aspose.com/3d/python-net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Example**

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-CubeScene-CreateCubeScene.py" >}}

{{% alert color="primary" %}}

Not: kök düğümüne bağlı varlıklar genellikle CAD/cam yazılımlarında göz ardı edilir, bu yüzden geometriyi işlemek için yeni bir düğüm oluşturmamız gerekir.

{{% /alert %}}
