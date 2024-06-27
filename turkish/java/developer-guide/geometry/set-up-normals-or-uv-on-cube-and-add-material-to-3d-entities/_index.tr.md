---
title: Set up normals or UV on Cube and Add Material to 3D Entities
type: docs
weight: 60
url: /tr/java/set-up-normals-or-uv-on-cube-and-add-material-to-3d-entities/
description: Aspose.3D for Java geometrik şekillerdeki normalleri ve uv'yi yönetmeyi teklif eder. Bir ağ, her vertex için temel özellikleri, uzayda pozisyonu ve normal, orijinal yüzeye dik bir vektör olarak bilinir. Normal, sayıları gölgelendirmek için önemlidir ve bir birim vektör olmalıdır. Çoğu örgü biçimi, ağın farklı poligonlarına uygulamak için 2 boyutlu bir doku haritasının hangi kısmının uygulanacağını göstermek için "açılmamış" ağının ayrı bir 2d gösterimi olan bir uv koordinatlarını da destekler.
---
{{% alert color="primary" %}}

Aspose.3D for Java geometrik şekillerdeki normalleri ve uv'yi yönetmeyi teklif eder. Bir ağ, her vertex için temel özellikleri, uzayda pozisyonu ve normal, orijinal yüzeye dik bir vektör olarak bilinir. Normal, sayıları gölgelendirmek için önemlidir ve bir birim vektör olmalıdır. Çoğu örgü biçimi, ağın farklı poligonlarına uygulamak için 2 boyutlu bir doku haritasının hangi kısmının uygulanacağını göstermek için "açılmamış" ağının ayrı bir 2d gösterimi olan bir uv koordinatlarını da destekler.

{{% /alert %}} {{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated here](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) and then point node to the Mesh geometry by creating a 3D Scene.

{{% /alert %}}
##  **Create Normal ctors ectors**
Aydınlatma konusunda iyi bir görsel görünüme sahip olmak için, her vertex için normaller bilgilerini belirtmemiz gerekiyor. Daha iyi ayrıntılara sahip olmak için, piksel başına normal/renk gerçekleştirmek için normal ve dağınık harita (gölge/speküler harita kullanın) kullanabiliriz. Vertexelement tarafından normal veya vertex rengi gibi bir vertex bilgisi elde edilir. Aspose.3D vertex/polygon/edge noktalarını kontrol etmek için ekstra bilgileri haritalayabiliriz, vertex için normalleri tanımlamak için bir örnek:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupNormalsOnCube.java" >}}


The 8 normal vektör, 8 kontrol noktasına doğrudan eşleştirilir, bir sonraki örnekte, biraz daha karmaşık bir senaryo göstereceğiz.
##  **Create UV ordinoordinates**
Here, sadece 4 UV koordinatlarını tanımladık, ancak endeksleri kullanarak 24 poligon dikeyine (poligon başına 6 yüz * 4 vertex) uyguladık.
Aspose.3D 5 haritalama modu sağlar:

- **Controltroloint**-Her veri geometrinin kontrol noktasına eşleştirilir.
- **Olyolygongonertex**-Veriler poligon'un vertex'ine eşleştirildi.
- **Polygon**-Veriler çokgen ile eşleştirilir.
- **Edge**-Veriler kenara çıkarıldı.
- **Allllame**-Tüm geometriye bir veri eşleştirildi.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupUVOnCube.java" >}}
##  **Add Materials to 3D Objects**
Aspose.3D for Java, geliştiricilerin doğru gölgeleme ve vurgular için gölgeleme algoritmasını kullanmasına izin verir. Phong, düğümün etkisini maskelemek için kullanabileceğimiz birkaç harita girişine sahiptir. Fiziksel olarak dayalı render (pbr) nesnelerin bazı fiziksel özelliklerini dikkate alır, bu tür bir yaklaşım gerçek dünyada olduğu gibi malzemelerin görünümünü sağlar.
###  **Cube için Texture ile Phong erial aterial**
Uhen Ucoordinates koordinatları kullanıma hazır, malzeme kullanarak örgü yüzeyine bir doku uygulayabiliriz. Only vertex rengi, yüzey detaylarını tarif edemez, bu da kullanılan malzemelerdir. Here, küp düğümüne bir Phong malzemesi eklemek için bir örnek:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddMaterialToCube.java" >}}


We dağınık doku haritalama ve parlaklık parametresi ile speküler bir renk belirledi.
###  **Hyhycally hysically Based dering en( (PBR) erial aterial to a Box**
PBR plays a key role for the game engine visuals, with its efficient and realistic rendering of interactions between light and surface via attenuation of the brightness and scattering of reflected light. Developers can use Aspose.3D API to apply PBR material to 3D objects in a scene. This code example demonstrates to how to create a Box object, and then apply the PBR material.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ApplyPBRMaterialToBox.java" >}}
