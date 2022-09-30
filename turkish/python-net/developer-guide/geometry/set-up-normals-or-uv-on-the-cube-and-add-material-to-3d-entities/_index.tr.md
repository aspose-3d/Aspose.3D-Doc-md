---
title: Cet up normals veya CV on Cube ve Add erial aterial to 3D Entities
type: docs
weight: 20
url: /tr/python-net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: HAspose.3D yılında bir ağ üzerinde normaller veya uv verileri oluşturmak için.
---
{{% alert color="primary" %}}

Python via .NET için Aspose.3D geometrik şekillerde normalleri ve UV yönetmek için sunuyor. A mesh, her verteksin temel özelliklerini depolar, uzaydaki konumu ve normal, orijinal yüzeye dik bir vektör. To normal sayıları gölgelendirmek için önemlidir. The normalleri birim vektörleri olmalıdır. Most mesh biçimleri ayrıca, ağın farklı poligonlarına uygulamak için 2 boyutlu bir doku haritasının hangi kısmının uygulanacağını göstermek için "açılmamış" ağının ayrı bir 2d temsili olan UV koordinatlarını da destekler.

{{% /alert %}} {{% alert color="primary" %}}

The `Mesh` sınıf nesnesi kodda kullanılıyor. We can[Orada anlatıldığı gibi `Mesh` sınıfı bir nesne oluşturun](/3d/tr/python-net/create-3d-mesh-and-scene/)Ve daha sonra Mesh geometrisine noktası[Creating bir 3D cene cene](/3d/tr/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Create Normal ctors ectors**
To aydınlatma üzerinde iyi bir görsel görünüme sahip, daha iyi bir ayrıntıya sahip olmak için her vertex için normaller bilgilerini belirtmemiz gerekiyor, ayrıca normal ve dağınık haritayı da kullanabiliriz (gölge/speküler haritasını kullanabileceğinizden emin olun)-piksel başına normal/renk. Normal veya vertex rengi gibi verper-vertex bilgileri `VertexElement` ile elde edilir. In Aspose.3D, vertex için normalleri tanımlamak için bir örnek olan puan/çokgen vertex/çokgen/kenar kontrol etmek için ekstra bilgileri haritalayabiliriz:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupNormalsOnCube-SetupNormalsOnCube.py" >}}

The 8 normal vektör, 8 kontrol noktasına doğrudan eşleştirilir, bir sonraki örnekte, biraz daha karmaşık bir senaryo göstereceğiz.
## **Create UV ordinoordinates**
Here, sadece 4 UV koordinatlarını tanımladık, ancak endeksleri kullanarak 24 poligon dikeyine (poligon başına 6 yüz * 4 vertex) uyguladık.
The Aspose.3D 5 haritalama modu sağlar:

- `CONTROL_POINT`-her veri geometrinin kontrol noktasına eşleştirilir.
- `POLYGON_VERTEX`-veriler poligon'un vertex'ine eşleştirilmiştir.
- `POLYGON`-veriler çokgen ile eşleştirilir.
- `EDGE`-veriler kenara eşleştirilir.
- `ALL_SAME`-bir veri tüm geometriye eşleştirildi.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupUVOnCube-SetupUVOnCube.py" >}}
## **Add Materials 3D Objects**
Python via .NET için Aspose.3D, geliştiricilerin doğru gölgeleme ve vurgular için gölgeleme algoritmasını kullanmasına izin verir. The Phong, düğümün etkisini maskelemek için kullanabileceğimiz birkaç harita girişine sahiptir. Hycally cally ased dering en. (PBR) nesnelerin bazı fiziksel özelliklerini dikkate alır, bu tür bir yaklaşım gerçek dünyada olduğu gibi malzemelerin görünümünü sağlar.
### **Cube için Texture ile Phong erial aterial**
Uhen Ucoordinates koordinatları kullanıma hazır, malzeme kullanarak örgü yüzeyine bir doku uygulayabiliriz. Only vertex rengi, yüzey detaylarını tarif edemez, bu da kullanılan malzemelerdir. Here, küp düğümüne bir Phong malzemesi eklemek için bir örnek:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MaterialToCube-AddMaterialToCube.py" >}}

We dağınık doku haritalama ve parlaklık parametresi ile speküler bir renk belirledi.
### **Hyhycally hysically Based dering en( (PBR) erial aterial to a Box**
PBgame oyun motoru görselleri için önemli bir rol oynar, ışık ile yüzey arasındaki etkileşimlerin verimli ve gerçekçi bir şekilde oluşturulması ile yansıyan ışığın parlaklığı ve saçılması zayıflatılır. Developers, bir sahnede 3D nesnelerine 07R malzeme uygulamak için Aspose.3D API kullanabilir. Tkod örneği, bir Box nesnesinin nasıl oluşturulacağını gösterir ve daha sonra PBmaterial malzemesini uygular.

**.NET, C#**

```py
import aspose.threed as a3d
# initialize a scene

scene = a3d.Scene()

# initialize PBR material object

mat = a3d.shading.PbrMaterial()

# an almost metal material

mat.metallic_factor = 0.9

# material surface is very rough

mat.roughness_factor = 0.9;

# create a box to which the material will be applied

boxNode = scene.root_node.create_child_node("box", a3d.entities.Box())

boxNode.material = mat

# save 3d scene into STL format

scene.save("PBR_Material_Box_Out.stl", a3d.FileFormat.STLASCII)

```
