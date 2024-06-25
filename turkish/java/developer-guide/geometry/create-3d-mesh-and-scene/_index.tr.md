---
title: 3D mesh ve sahne oluştur
type: docs
weight: 40
url: /tr/java/create-3d-mesh-and-scene/
description: A Mesh, bir dizi kontrol noktası ve gerektiğinde birçok n taraflı poligonlar tarafından tanımlanır. Tonun makalesi nasıl tanımlanacağını açıklıyor.
---
##  **3D küp mesh oluşturun**
A `Mesh` is defined by a set of control points and the many n-sided polygons as needed. This article explains how to define a `Mesh`.

`Mesh` yüzeyi oluşturmak için, kontrol noktalarını ve poligonları aşağıdaki gibi tanımlamamız gerekir:

- [Define Control ints oints](/3d/tr/java/create-3d-mesh-and-scene-html/)
- [PolygonBuilder sınıfı ile poligonlar oluşturun](/3d/tr/java/create-3d-mesh-and-scene-html/)
- [Create olyolygons](/3d/tr/java/create-3d-mesh-and-scene-html/)

Here, küp düğümüne bir Phong malzemesi eklemek için bir örnek:
###  **Define Control ints oints**
A mesh, uzayda bir kontrol noktası seti ve örgü yüzeyini tanımlamak için poligonlar ile oluşur, bir örgü oluşturmak için kontrol noktalarını tanımlamamız gerekir:

{{% alert color="primary" %}} 

The control points of all geometries in Aspose.3D use homogeneous coordinate, so it’s `Vector4` instead of `Vector3` in the example code.

{{% /alert %}} 

**Ex::**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-DefineControlPoints.java" >}}



###  **Create olyolygons**
The kontrol noktaları renderable değildir, küpü görünür hale getirmek için, her iki tarafta poligonları tanımlamamız gerekir:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingCreatePolygons.java" >}}



###  **PolygonBuilder sınıfı ile poligonlar oluşturun**
Ayrıca, PolygonBuilder sınıfı ile poligon tanımlayabiliriz:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateMeshUsingPolygonBuilder.java" >}}

Now bitti, örgü görünür hale getirmek için, bunun için bir düğüm hazırlamamız gerekiyor.
##  **Ow ow to a riangulate a Mesh**
Triangulate mesh, oyun endüstrisi için yararlıdır, çünkü üçgen, Ghardware hardware donanım desteğinin desteklediği tek desteklenen ilkeldir (üçgen olmayan veriler, gerçek zamanlı olarak verimsiz olan sürücü seviyesinde triangulated edilir)

{{% alert color="primary" %}} 

3ds n bu sürüm biz sadece 3ds dosya ihracat, normaller/uvs ve diğer vertex elemanları tarafından gerekli olduğu için poligonlar triangulated bu prosedür sırasında kaybolur, biz gelecekte bunu uygulayabilirsiniz.

{{% /alert %}} 

In this example, we triangulate a Mesh by importing FBX file and saved it in FBX format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-TriangulateMesh.java" >}}
##  **3D küp sahne oluştur**
Bu konu, 3D sahnesine örgü geometrisinin nasıl ekleneceğini gösteriyor. Örnek kod bir küp yerleştirir ve desteklenen dosya formatlarında 3D görüntüsünü kaydeder.
###  **Create a Cube Node**
A node görünmezdir, ancak düğüme bağlı geometri işlenebilir.

{{% alert color="primary" %}} 

The Mesh class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene#Create3DMeshandScene-Createa3DCubeMesh).

{{% /alert %}} 

**Ex::**

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-CreateCubeScene.java" >}}

{{% alert color="primary" %}} 

Not: kök düğümüne bağlı varlıklar genellikle CAD/cam yazılımlarında göz ardı edilir, bu yüzden geometriyi işlemek için yeni bir düğüm oluşturmamız gerekir.

{{% /alert %}}
