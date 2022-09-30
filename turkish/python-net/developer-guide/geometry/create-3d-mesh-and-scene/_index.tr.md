---
title: Create 3D Mesh ve Scene
type: docs
weight: 10
url: /tr/python-net/create-3d-mesh-and-scene/
description: A Mesh, bir dizi kontrol noktası ve gerektiğinde birçok n taraflı poligonlar tarafından tanımlanır. Tonun makalesi nasıl tanımlanacağını açıklıyor.
---
## **Create a 3D Cube Mesh**
A [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh), bir kontrol noktası seti ve gerektiğinde birçok n taraflı poligonlar tarafından tanımlanır. Tonun makalesi nasıl tanımlanacağını açıklıyor.

Bir Mesh yüzeyi oluşturmak için In siparişi, aşağıdaki gibi kontrol noktalarını ve poligonları tanımlamamız gerekiyor:

- [Define Control ints oints](/3d/tr/python-net/create-3d-mesh-and-scene/)
- [PolygonBuilder lass lass ile Preate olyolygons](/3d/tr/python-net/create-3d-mesh-and-scene/)
- [Create olyolygons](/3d/tr/python-net/create-3d-mesh-and-scene/)

Here, küp düğümüne bir Phong malzemesi eklemek için bir örnek:
### **Define Control ints oints**
A mesh, uzayda bir kontrol noktası seti ve örgü yüzeyini tanımlamak için poligonlar ile oluşur, bir örgü oluşturmak için kontrol noktalarını tanımlamamız gerekir:

{{% alert color="primary" %}}

To Aspose.3D tüm geometrilerin kontrol noktaları homojen koordinat kullanın, bu yüzden örnek kodda `Vector3` yerine `Vector4`.

{{% /alert %}}

**Ex::**

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-DefineControlPoints.py" >}}


### **Create olyolygons**
The kontrol noktaları renderable değildir, küpü görünür hale getirmek için, her iki tarafta poligonları tanımlamamız gerekir:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-CreateMeshUsingCreatePolygons.py" >}}


### **PolygonBuilder lass lass ile Preate olyolygons**
We ayrıca `PolygonBuilder` sınıfı ile dikeylerle poligon tanımlayabilir:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-Common-CreateMeshUsingPolygonBuilder.py" >}}

Now bitti, örgü görünür hale getirmek için, bunun için bir düğüm hazırlamamız gerekiyor.
## **Ow ow to a riangulate a Mesh**
Triangulate mesh, oyun endüstrisi için yararlıdır, çünkü üçgen, Ghardware hardware donanım desteğinin desteklediği tek desteklenen ilkeldir (üçgen olmayan veriler, gerçek zamanlı olarak verimsiz olan sürücü seviyesinde triangulated edilir)

{{% alert color="primary" %}}

3ds n bu sürüm biz sadece 3ds dosya ihracat, normaller/uvs ve diğer vertex elemanları tarafından gerekli olduğu için poligonlar triangulated bu prosedür sırasında kaybolur, biz gelecekte bunu uygulayabilirsiniz.

{{% /alert %}}

In bu örnek, FBX dosyasını içe aktararak ve FBX formatında kaydederek bir Mesh triangulate.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TriangulateMesh-TriangulateMesh.py" >}}
## **Create bir 3D Cube cene cene**
Tonun konusu 3D sahnesine Mesh geometrisini nasıl ekleyeceğini gösteriyor. To örnek kod bir küp yerleştirir ve desteklenen dosya formatlarında 3D sahnesini kaydeder.
### **Create a Cube Node**
A node görünmezdir, ancak düğüme bağlı geometri işlenebilir.

{{% alert color="primary" %}}

The Mesh sınıfı nesne kodda kullanılıyor. We can[Orada anlatıldığı gibi `Mesh` sınıfı bir nesne oluşturun](https://docs.aspose.com/3d/python-net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Example**

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-CubeScene-CreateCubeScene.py" >}}

{{% alert color="primary" %}}

NOTroot: kök düğümüne bağlı varlıklar genellikle CAD/Csoftwares softwares yazılımlarında göz ardı edilir, bu yüzden geometriyi işlemek için yeni bir düğüm oluşturmamız gerekir.

{{% /alert %}}
