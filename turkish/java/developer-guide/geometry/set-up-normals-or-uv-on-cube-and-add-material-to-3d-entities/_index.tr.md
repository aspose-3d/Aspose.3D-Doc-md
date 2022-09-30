---
title: Normaet up normals veya UV on Cube ve Add erial aterial to 3D Entities
type: docs
weight: 60
url: /tr/java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
description: Aspose.3D for Java geometrik şekillerde normalleri ve UV yönetmek için sunuyor. A mesh, her vertex için temel özellikleri, uzayda pozisyonu ve normal, orijinal yüzeye dik bir vektör olarak bilinir. To normal sayıları gölgelendirmek için büyük ve bir birim vektör olmalıdır. Most mesh biçimleri ayrıca, ağın farklı poligonlarına uygulamak için 2 boyutlu bir doku haritasının hangi kısmının uygulanacağını göstermek için "açılmamış" ağının ayrı bir 2,5 temsili olan UV koordinatlarını da destekler.
---
{{% alert color="primary" %}}

Aspose.3D for Java geometrik şekillerde normalleri ve UV yönetmek için sunuyor. A mesh, her vertex için temel özellikleri, uzayda pozisyonu ve normal, orijinal yüzeye dik bir vektör olarak bilinir. To normal sayıları gölgelendirmek için büyük ve bir birim vektör olmalıdır. Most mesh biçimleri ayrıca, ağın farklı poligonlarına uygulamak için 2 boyutlu bir doku haritasının hangi kısmının uygulanacağını göstermek için "açılmamış" ağının ayrı bir 2,5 temsili olan UV koordinatlarını da destekler.

{{% /alert %}} {{% alert color="primary" %}}

The `Mesh` sınıf nesnesi kodda kullanılıyor. We can[Burada anlatılan Mesh sınıfı bir nesne oluşturun](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/)Ve sonra 3D Scene oluşturarak Mesh geometrisine nokta düğümü.

{{% /alert %}}
## **Create Normal ctors ectors**
In aydınlatma konusunda iyi bir görsel görünüme sahip olmak için, her vertex için normaller bilgilerini belirtmemiz gerekiyor. In daha iyi ayrıntılara sahip olmak için, piksel başına normal/renk gerçekleştirmek için normal ve dağınık harita (gölge/speküler harita kullanın) kullanabiliriz. Normal veya vertex rengi gibi verper-vertex bilgileri, Vertextexlement ile elde edilir. In Aspose.3D, vertex için normalleri tanımlamak için bir örnek olan puan/çokgen vertex/çokgen/kenar kontrol etmek için ekstra bilgileri haritalayabiliriz:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupNormalsOnCube.java" >}}


The 8 normal vektör, 8 kontrol noktasına doğrudan eşleştirilir, bir sonraki örnekte, biraz daha karmaşık bir senaryo göstereceğiz.
## **Create UV ordinoordinates**
Here, sadece 4 UV koordinatlarını tanımladık, ancak endeksleri kullanarak 24 poligon dikeyine (poligon başına 6 yüz * 4 vertex) uyguladık.
The Aspose.3D 5 haritalama modu sağlar:

- **Controltroloint**-Her veri geometrinin kontrol noktasına eşleştirilir.
- **Olyolygongonertex**-Veriler poligon'un vertex'ine eşleştirildi.
- **Polygon**-Veriler çokgen ile eşleştirilir.
- **Edge**-Veriler kenara çıkarıldı.
- **Allllame**-Tüm geometriye bir veri eşleştirildi.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupUVOnCube.java" >}}
## **Add Materials 3D Objects**
Aspose.3D for Java, geliştiricilerin doğru gölgeleme ve vurgular için gölgeleme algoritmasını kullanmasına izin verir. The Phong, düğümün etkisini maskelemek için kullanabileceğimiz birkaç harita girişine sahiptir. Hycally cally ased dering en. (PBR) nesnelerin bazı fiziksel özelliklerini dikkate alır, bu tür bir yaklaşım gerçek dünyada olduğu gibi malzemelerin görünümünü sağlar.
### **Cube için Texture ile Phong erial aterial**
Uhen Ucoordinates koordinatları kullanıma hazır, malzeme kullanarak örgü yüzeyine bir doku uygulayabiliriz. Only vertex rengi, yüzey detaylarını tarif edemez, bu da kullanılan malzemelerdir. Here, küp düğümüne bir Phong malzemesi eklemek için bir örnek:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddMaterialToCube.java" >}}


We dağınık doku haritalama ve parlaklık parametresi ile speküler bir renk belirledi.
### **Hyhycally hysically Based dering en( (PBR) erial aterial to a Box**
PBgame oyun motoru görselleri için önemli bir rol oynar, ışık ile yüzey arasındaki etkileşimlerin verimli ve gerçekçi bir şekilde oluşturulması ile yansıyan ışığın parlaklığı ve saçılması zayıflatılır. Developers, bir sahnede 3D nesnelerine 07R malzeme uygulamak için Aspose.3D API kullanabilir. Tkod örneği, bir Box nesnesinin nasıl oluşturulacağını gösterir ve daha sonra PBmaterial malzemesini uygular.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ApplyPBRMaterialToBox.java" >}}
