---
title: Public API Changes Aspose.3D 1.5.0
type: docs
weight: 20
url: /tr/net/public-api-changes-in-aspose-3d-1-5-0/
---
**Contents Summary**

- [Monvert Mrimitive bir Mesh ve Create bir 07cene gelen 07rimitive 3D ododels](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [Vonvert a Vesh to Triangle Mesh with uustom Vetex yout aaof the Vertex](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [Split Mesh](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [Distreet3DS formatın emoemoval.](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [Dds dds Discreet3DS formatı.](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [Dds dds mülkiyet sınıfı Aspose.ThreeD sınıfında liplipCoordinatestem ystem. Formats. Universal3Dononfig](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

This belgesi, 1.4.0 sürümünden 1.5.0 'a kadar Aspose.3D API 'teki değişiklikleri, modül/uygulama geliştiricilerine ilgi duyulabilir. It sadece yeni ve güncellenmiş kamu yöntemlerini değil, aynı zamanda Aspose.3D 'deki sahnelerin arkasındaki davranıştaki herhangi bir değişikliğin açıklamasını da içerir.

{{% /alert %}} 
### **Monvert Mrimitive bir Mesh ve Create bir 07cene gelen 07rimitive 3D ododels**
**Various Classes, Methods ve Properties eklenir**

- **Dds dds arayüzü Aspose.ThreeD.Entities. Ieshesheshonver..** 
-Bu arayüzü uygulayan Any sınıfı, herhangi bir 3D dosya formatına ihracat yaparken ağa dönüştürülebilir.
- **Dds dds sınıf Aspose.ThreeD.Entities.Primitive.** 
-It, Entity sınıfından ve aynı zamanda tüm ilkel sınıflar için temel sınıftan türetilmiştir.
- **Dds dds sınıf Aspose.ThreeD.Entities. ox ox/Cylinder/Plane/Sphere/Torus.** 
-These, sahneyi basit ilkellerle tanımlamak için kullanılabilir. Developers ayrıca bunları otomatik olarak ağa dönüştürebilir.

Primitives, kutu, küre, uçak, silindir ve torus gibi en temel ve en çok kullanılan nesnelerin birçoğunu içerir. Developers, bunları modifikasyon amaçları için ağa dönüştürebilir. These yardımcı konular nasıl yapılacağını gösterir:[Monvert the Primitive to a Mesh](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models)Ve[Monvert the Primitive to a Mesh](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
### **Vonvert a Vesh to Triangle Mesh with uustom Vetex yout aaof the Vertex**
**Various Classes, Methods ve Properties eklenir**

- **Dds dds sınıf Aspose.ThreeD.Entities. Tririesh/Tririesh <T>** 
-Tririesh/Tririesh<T>Geliştirici, sahneyi kendi özel dosya formatlarına veya render olarak dönüştürmeyi gerektirdiğinde yararlı olan özel bellek düzenine sahip üçgen tabanlı kafesler tanımını içerir.
- **Dds dds yapısı Aspose.ThreeD. lities tilities.FVector2/Fecector3/Fecector4** 
-These sınıfları şamandırada vektör bileşenleri sunar. Only birkaç modern GPdouble çift hassas vektör destekler, tek hassasiyetli şamandıra türleri gerçek zamanlı işleme dünyasında daha memnuniyetle karşılanmaktadır. These değiştirmeleri, Aspose.3D 'te farklı roller oynadıklarından orijinal Vector2/Vector3/Vector4 ile birlikte olacaktır. Double-hassasiyet, daha az birikmiş hataya sahip olduğu için modelin verilerini saklamak için kullanılır. Single-hassasiyet esas olarak daha iyi kabul ve performansa sahip olduğu için render veya kullanıcının kendi özel dosya biçimleri dönüşümünde kullanılır. We, Aspose.3D 1.5 yılında bu vektör setini tanıttı, çünkü şamandıra vektörlerinin sık sık kullanılacağı özel vertex düzeni için destek ekledik.
- **Dds dds öznitelik sınıfı Aspose.ThreeD. Uti.. emanemantictttribute** 
-Developer, vertex için özel yapı tanımlayabilir ve alanların anlamlılığını işaretlemek için bu özelliği kullanabilir.
- **Dds dds sınıf Aspose.ThreeD.Utilities.VertexDeclaration** 
-It, vertex'in hafıza düzenini açıklar.
- **Dds dds enum Aspose.ThreeD. lities tilities.VertexFieldDataType/VertexFieldSemantic** 
-These enum türleri sırasıyla vertex'in alanının veri tipini ve anlamlılığını not eder.
- **Dds dds sınıf Aspose.ThreeD. lities tilities.VertexField** 
-It, Vertex'in özel bellek düzeninde her alanı tanımlar.
- **Dds dds sınıf Aspose.ThreeD. lities tilities.Vertex** 
-Raw t raw ririesh/Tririesh ham vertex erişmek için kullanılabilir<T>

Developers, herhangi bir örgü nesnesini, vertex'in özel hafıza düzeni ile üçgen ağa dönüştürebilir. To grafik yazılım paketleri ve donanım cihazları üçgenler üzerinde daha verimli çalışır. Tonun yardım konusu nasıl yapılacağını gösteriyor:[Vonvert a Vesh to Triangle Mesh with uustom Vetex yout aaof the Vertex](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
### **Split Mesh**
**Various Classes, Methods ve Properties eklenir**

- **Dds dds enum Aspose.ThreeD.Entities. pliplitMesholiolicy** 
-It, ağ bölme algoritmasında kullanılan veri politikasını belirtir, iki politikayı destekliyoruz, alt kafesler arasında veri paylaşıyoruz veya her bir alt ağ kendi verilerine sahip (Only kullanılan veriler).
- **Dds dds 3 Spliteesh yöntemleri Aspose.ThreeD.Entities. olyolygongonodifier sınıfı** 
1. malzeme tanımı ile alt ağlara belirtilen bir düğümde shes plit meshes.
1. malzeme tanımı ile alt kafeslere verilen sahnedeki tüm örgüler.
1. verilen örgü malzeme tanımı ile alt kafeslere pliplit.
- **Dds dds mülkiyet sınıfı Aspose.ThreeD sınıfında liplipCoordinatestem ystem. Formats. Universal3Dononfig** 
-It, kullanıcıların ithalat veya ihracat sırasında U3D koordinat sistemini çevirmelerine izin verir.

Developers, bir ağın malzemeye otomatik olarak bölünmesini gerektirebilir, böylece her bir örgü malzemeyi belirterek sadece bir malzeme veya bölünmüş örgü kullanır. These yardımcı konular nasıl yapılacağını gösterir:[Erial plit a erial esh erial pecicithe erial aterial](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial)Ve[Split All erial eshes bir cene cene er erial aterial](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
### **Distreet3DS formatın emoemoval.**
Distreet3Dformat format yanlış büyü nedeniyle eski olarak işaretlenmiştir.
### **Dds dds Discreet3DS formatı.**
Discreet3DS formatı tanıtıldı.
### **Dds dds mülkiyet sınıfı Aspose.ThreeD sınıfında liplipCoordinatestem ystem. Formats. Universal3Dononfig**
It, kullanıcıların ithalat veya ihracat sırasında U3D koordinat sistemini çevirmelerine izin verir.
