---
title: Create 3D Mesh ve Scene
type: docs
weight: 40
url: /tr/java/create-3d-mesh-and-scene/
description: A Mesh, bir dizi kontrol noktası ve gerektiğinde birçok n taraflı poligonlar tarafından tanımlanır. Tonun makalesi nasıl tanımlanacağını açıklıyor.
---
## **Create a 3D Cube Mesh**
A `Mesh`, bir kontrol noktası seti ve gerektiğinde birçok n taraflı poligonlar tarafından tanımlanır. Tonun makalesi `Mesh` nasıl tanımlanacağını açıklıyor.

In sipariş `Mesh` yüzey oluşturmak için, aşağıdaki gibi kontrol noktaları ve çokgenler tanımlamak gerekir:

- [Define Control ints oints](/3d/tr/java/create-3d-mesh-and-scene-html/)
- [PolygonBuilder lass lass ile Preate olyolygons](/3d/tr/java/create-3d-mesh-and-scene-html/)
- [Create olyolygons](/3d/tr/java/create-3d-mesh-and-scene-html/)

Here, küp düğümüne bir Phong malzemesi eklemek için bir örnek:
### **Define Control ints oints**
A mesh, uzayda bir kontrol noktası seti ve örgü yüzeyini tanımlamak için poligonlar ile oluşur, bir örgü oluşturmak için kontrol noktalarını tanımlamamız gerekir:

{{% alert color="primary" %}} 

To Aspose.3D tüm geometrilerin kontrol noktaları homojen koordinat kullanın, bu yüzden örnek kodda `Vector3` yerine `Vector4`.

{{% /alert %}} 

**Ex::**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-DefineControlPoints.java" >}}



### **Create olyolygons**
The kontrol noktaları renderable değildir, küpü görünür hale getirmek için, her iki tarafta poligonları tanımlamamız gerekir:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingCreatePolygons.java" >}}



### **PolygonBuilder lass lass ile Preate olyolygons**
We ayrıca PolygonBuilder sınıfı ile dikeylerle poligon tanımlayabilir:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingPolygonBuilder.java" >}}

Now bitti, örgü görünür hale getirmek için, bunun için bir düğüm hazırlamamız gerekiyor.
## **Ow ow to a riangulate a Mesh**
Triangulate mesh, oyun endüstrisi için yararlıdır, çünkü üçgen, Ghardware hardware donanım desteğinin desteklediği tek desteklenen ilkeldir (üçgen olmayan veriler, gerçek zamanlı olarak verimsiz olan sürücü seviyesinde triangulated edilir)

{{% alert color="primary" %}} 

3ds n bu sürüm biz sadece 3ds dosya ihracat, normaller/uvs ve diğer vertex elemanları tarafından gerekli olduğu için poligonlar triangulated bu prosedür sırasında kaybolur, biz gelecekte bunu uygulayabilirsiniz.

{{% /alert %}} 

In bu örnek, FBX dosyasını içe aktararak ve FBX formatında kaydederek bir Mesh triangulate.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-TriangulateMesh.java" >}}
## **Create bir 3D Cube cene cene**
Tonun konusu 3D sahnesine Mesh geometrisini nasıl ekleyeceğini gösteriyor. To örnek kod bir küp yerleştirir ve desteklenen dosya formatlarında 3D sahnesini kaydeder.
### **Create a Cube Node**
A node görünmezdir, ancak düğüme bağlı geometri işlenebilir.

{{% alert color="primary" %}} 

The Mesh sınıfı nesne kodda kullanılıyor. We can[Orada anlatılan Mesh sınıfı bir nesne oluşturun](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh).

{{% /alert %}} 

**Ex::**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateCubeScene.java" >}}

{{% alert color="primary" %}} 

NOTroot: kök düğümüne bağlı varlıklar genellikle CAD/Csoftwares softwares yazılımlarında göz ardı edilir, bu yüzden geometriyi işlemek için yeni bir düğüm oluşturmamız gerekir.

{{% /alert %}}
