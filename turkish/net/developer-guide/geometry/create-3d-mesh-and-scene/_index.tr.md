---
title: Create 3D Mesh ve Scene
type: docs
weight: 10
url: /tr/net/create-3d-mesh-and-scene/
description: A Mesh, bir dizi kontrol noktası ve gerektiğinde birçok n taraflı poligonlar tarafından tanımlanır. Tonun makalesi nasıl tanımlanacağını açıklıyor.
---
## **Create a 3D Cube Mesh**
A [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh), bir kontrol noktası seti ve gerektiğinde birçok n taraflı poligonlar tarafından tanımlanır. Tonun makalesi `Mesh` nasıl tanımlanacağını açıklıyor.

In sipariş `Mesh` yüzey oluşturmak için, aşağıdaki gibi kontrol noktaları ve çokgenler tanımlamak gerekir:

- [Define Control ints oints](/3d/tr/net/create-3d-mesh-and-scene/)
- [PolygonBuilder lass lass ile Preate olyolygons](/3d/tr/net/create-3d-mesh-and-scene/)
- [Create olyolygons](/3d/tr/net/create-3d-mesh-and-scene/)

Here, küp düğümüne bir Phong malzemesi eklemek için bir örnek:
### **Define Control ints oints**
A mesh, uzayda bir kontrol noktası seti ve örgü yüzeyini tanımlamak için poligonlar ile oluşur, bir örgü oluşturmak için kontrol noktalarını tanımlamamız gerekir:

{{% alert color="primary" %}}

07o Aspose.3D tüm geometrilerin kontrol noktaları homojen koordinat kullanın, bu yüzden örnek kodda Vector3 yerine `Vector4`.

{{% /alert %}}

**Ex::**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-Common-DefineControlPoints.cs" >}}


### **Create olyolygons**
The kontrol noktaları renderable değildir, küpü görünür hale getirmek için, her iki tarafta poligonları tanımlamamız gerekir:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-Common-CreateMeshUsingCreatePolygons.cs" >}}


### **PolygonBuilder lass lass ile Preate olyolygons**
We ayrıca `PolygonBuilder` sınıfı ile dikeylerle poligon tanımlayabilir:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-Common-CreateMeshUsingPolygonBuilder.cs" >}}

Now bitti, örgü görünür hale getirmek için, bunun için bir düğüm hazırlamamız gerekiyor.
## **Ow ow to a riangulate a Mesh**
Triangulate mesh, oyun endüstrisi için yararlıdır, çünkü üçgen, Ghardware hardware donanım desteğinin desteklediği tek desteklenen ilkeldir (üçgen olmayan veriler, gerçek zamanlı olarak verimsiz olan sürücü seviyesinde triangulated edilir)

{{% alert color="primary" %}}

3ds n bu sürüm biz sadece 3ds dosya ihracat, normaller/uvs ve diğer vertex elemanları tarafından gerekli olduğu için poligonlar triangulated bu prosedür sırasında kaybolur, biz gelecekte bunu uygulayabilirsiniz.

{{% /alert %}}

In bu örnek, FBX dosyasını içe aktararak ve FBX formatında kaydederek bir Mesh triangulate.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TriangulateMesh-TriangulateMesh.cs" >}}
## **Create bir 3D Cube cene cene**
Tonun konusu 3D sahnesine Mesh geometrisini nasıl ekleyeceğini gösteriyor. To örnek kod bir küp yerleştirir ve desteklenen dosya formatlarında 3D sahnesini kaydeder.
### **Create a Cube Node**
A node görünmezdir, ancak düğüme bağlı geometri işlenebilir.

{{% alert color="primary" %}}

The `Mesh` sınıf nesnesi kodda kullanılıyor. We can[Orada anlatılan Mesh sınıfı bir nesne oluşturun](https://docs.aspose.com/3d/net/create-3d-mesh-and-scene/#create-a-3d-cube-mesh).

{{% /alert %}}

**Example**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-CubeScene-CreateCubeScene.cs" >}}

{{% alert color="primary" %}}

NOTroot: kök düğümüne bağlı varlıklar genellikle CAD/Csoftwares softwares yazılımlarında göz ardı edilir, bu yüzden geometriyi işlemek için yeni bir düğüm oluşturmamız gerekir.

{{% /alert %}}
