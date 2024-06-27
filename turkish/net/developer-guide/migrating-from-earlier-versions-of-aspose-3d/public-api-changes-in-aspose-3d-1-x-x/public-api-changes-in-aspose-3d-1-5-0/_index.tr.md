---
title: Kamu API Aspose içinde değişir. 3D 1.5.0
type: docs
weight: 20
url: /tr/net/public-api-changes-in-aspose-3d-1-5-0/
---
**Contents Summary**

- [İlkel bir ağa dönüştürün ve primitive 3D modellerinden bir sahne oluşturun](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [Vonvert a Vesh to Triangle Mesh with uustom Vetex yout aaof the Vertex](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [Split Mesh](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [Distreet3DS formatın emoemoval.](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [Adds Discreet3DS format.](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [Adds property FlipCoordinateSystem in class Aspose.ThreeD.Formats.Universal3DConfig](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 1.4.0 to 1.5.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **İlkel bir ağa dönüştürün ve primitive 3D modellerinden bir sahne oluşturun**
**Various Classes, Methods ve Properties eklenir**

- **Arayüz Aspose ekler. threed. entities. imeshconvertible.** 
-Bu arayüzü uygulayan herhangi bir sınıf, herhangi bir 3D dosya formatına ihracat yaparken ağa dönüştürülebilir.
- **Sınıf Aspose ekler. threed. entities. primitive.** 
-It, Entity sınıfından ve aynı zamanda tüm ilkel sınıflar için temel sınıftan türetilmiştir.
- **Sınıf Aspose ekler. threed. entities. box/silindir/düzlem/küre/torus.** 
-These, sahneyi basit ilkellerle tanımlamak için kullanılabilir. Developers ayrıca bunları otomatik olarak ağa dönüştürebilir.

İlkeller, kutu, küre, uçak, silindir ve torus gibi en temel ve en çok kullanılan nesnelerin birçoğunu içerir. Geliştiriciler de bunları modifikasyon amacıyla ağa dönüştürebilir. Bu yardım konuları nasıl yapılacağını göstermektedir: [Monvert the Primitive to a Mesh](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models) ve [Monvert the Primitive to a Mesh](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
###  **Vonvert a Vesh to Triangle Mesh with uustom Vetex yout aaof the Vertex**
**Various Classes, Methods ve Properties eklenir**

- **Sınıf Aspose ekler. threed. entities. trimesh/trimesh <t>** 
-Tririesh/Tririesh<T>Geliştirici, sahneyi kendi özel dosya formatlarına veya render olarak dönüştürmeyi gerektirdiğinde yararlı olan özel bellek düzenine sahip üçgen tabanlı kafesler tanımını içerir.
- **Yapı Aspose ekler. threed. yardımcı programlar. fvector2/fvector3/fvector4** 
  - These classes present vector components in the float. Only a few modern GPU supports double-precision vector, single-precision float types are more welcomed in real-time rendering world. These replacements will co-exist with the original Vector2/Vector3/Vector4 since they play different roles in Aspose.3D. Double-precision is mainly used to store model’s data because it has less accumulated error. Single-precision is mainly used in rendering or user’s own proprietary file formats conversion because it has better acceptance and performance. We introduced this set of vectors in Aspose.3D 1.5 because we added support for custom vertex layout, where the float vectors will be frequently used.
- **Adds attribute class Aspose.ThreeD.Utilities.SemanticAttribute** 
-Developer, vertex için özel yapı tanımlayabilir ve alanların anlamlılığını işaretlemek için bu özelliği kullanabilir.
- **Sınıf Aspose ekler. threed. yardımcı programlar. vertexdeclaration** 
-It, vertex'in hafıza düzenini açıklar.
- **Enum Aspose ekler. threed. yardımcı programlar. vertexfielddatype/vertexfieldsemantic** 
-These enum türleri sırasıyla vertex'in alanının veri tipini ve anlamlılığını not eder.
- **Sınıf Aspose ekler. threed. yardımcı programlar. vertexfield** 
-It, Vertex'in özel bellek düzeninde her alanı tanımlar.
- **Sınıf Aspose ekler. threed. yardımcı programlar. vertex** 
-Raw t raw ririesh/Tririesh ham vertex erişmek için kullanılabilir<T>

Geliştiriciler, herhangi bir örgü nesnesini vertex'in özel bellek düzeni ile üçgen örgüye dönüştürebilir. Grafik yazılım paketleri ve donanım cihazları üçgenler üzerinde daha verimli çalışır. Bu yardım konusu nasıl yapılacağını gösteriyor: [Vonvert a Vesh to Triangle Mesh with uustom Vetex yout aaof the Vertex](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
###  **Split Mesh**
**Various Classes, Methods ve Properties eklenir**

- **Enum Aspose ekler. threed. entities. splitmeshpolicy** 
-It, ağ bölme algoritmasında kullanılan veri politikasını belirtir, iki politikayı destekliyoruz, alt kafesler arasında veri paylaşıyoruz veya her bir alt ağ kendi verilerine sahip (Only kullanılan veriler).
- **Adds 3 SplitMesh methods to Aspose.ThreeD.Entities.PolygonModifier class** 
1. malzeme tanımı ile alt ağlara belirtilen bir düğümde shes plit meshes.
1. malzeme tanımı ile alt kafeslere verilen sahnedeki tüm örgüler.
1. verilen örgü malzeme tanımı ile alt kafeslere pliplit.
- **Adds property FlipCoordinateSystem in class Aspose.ThreeD.Formats.Universal3DConfig** 
  - It allows users to flip the coordinate system of U3D during import or export.

Geliştiriciler, bir ağı malzeme ile otomatik olarak bölmeyi gerektirebilir, böylece her ağ malzemeyi belirterek sadece bir malzeme veya bölünmüş örgü kullanır. Bu yardım konuları nasıl yapılacağını göstermektedir: [Erial plit a erial esh erial pecicithe erial aterial](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial) ve [Split All erial eshes bir cene cene er erial aterial](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
###  **Distreet3DS formatın emoemoval.**
Distreet3Dformat format yanlış büyü nedeniyle eski olarak işaretlenmiştir.
###  **Adds Discreet3DS format.**
Discreet3DS format has been introduced.
###  **Adds property FlipCoordinateSystem in class Aspose.ThreeD.Formats.Universal3DConfig**
It allows users to flip the coordinate system of U3D during import or export.
