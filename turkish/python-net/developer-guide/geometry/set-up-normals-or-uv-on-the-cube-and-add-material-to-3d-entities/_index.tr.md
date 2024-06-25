---
title: Set up normals or UV on the Cube and Add Material to 3D Entities
type: docs
weight: 20
url: /tr/python-net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: Aspose içinde bir ağ üzerinde normaller veya uv verileri nasıl oluşturulur. 3D.
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET geometrik şekillerde normalleri ve uv'yi yönetmeyi teklif eder. Bir ağ, her bir verteksin temel özelliklerini depolar, uzayda konumu ve normal, orijinal yüzeye dik bir vektör. Normal, sayıları gölgelendirmek için önemlidir. Normaller birim vektörleri olmalıdır. Çoğu örgü biçimi, ağın farklı poligonlarına uygulamak için 2 boyutlu bir doku haritasının hangi kısmının uygulanacağını göstermek için "açılmamış" ağının ayrı bir 2d gösterimi olan bir uv koordinatlarını da destekler.

{{% /alert %}} {{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a `Mesh` class object as narrated there](/3d/python-net/create-3d-mesh-and-scene/) and then point node to the Mesh geometry by [Creating a 3D Scene](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Create Normal ctors ectors**
Aydınlatma konusunda iyi bir görsel görünüme sahip olmak için, her vertex için normaller bilgilerini belirtmemiz, daha iyi bir ayrıntıya sahip olmamız gerekiyor, ayrıca normal ve dağınık haritayı da kullanabiliriz (gölge/speküler haritasını kullanabileceğinizden emin olun)-piksel başına normal/renk. Normal veya vertex rengi gibi bir vertex bilgisi `VertexElement` ile elde edilir. Aspose.3D vertex/polygon/edge noktalarını kontrol etmek için ekstra bilgileri haritalayabiliriz, vertex için normalleri tanımlamak için bir örnek:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupNormalsOnCube-SetupNormalsOnCube.py" >}}

The 8 normal vektör, 8 kontrol noktasına doğrudan eşleştirilir, bir sonraki örnekte, biraz daha karmaşık bir senaryo göstereceğiz.
##  **Create UV ordinoordinates**
Here, sadece 4 UV koordinatlarını tanımladık, ancak endeksleri kullanarak 24 poligon dikeyine (poligon başına 6 yüz * 4 vertex) uyguladık.
Aspose.3D 5 haritalama modu sağlar:

- `CONTROL_POINT` -her veri geometrinin kontrol noktasına eşleştirilir.
- `POLYGON_VERTEX` -veriler poligon'un vertex'ine eşleştirildi.
- `POLYGON` -veriler çokgen ile eşleştirilir.
- `EDGE` -veriler kenara yazılmıştır.
- `ALL_SAME` -tüm geometriye bir veri eşleştirildi.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupUVOnCube-SetupUVOnCube.py" >}}
##  **Add Materials to 3D Objects**
Aspose.3D for Python via .NET, geliştiricilerin doğru gölgeleme ve vurgular için gölgeleme algoritmasını kullanmasına izin verir. Phong, düğümün etkisini maskelemek için kullanabileceğimiz birkaç harita girişine sahiptir. Fiziksel olarak dayalı render (pbr) nesnelerin bazı fiziksel özelliklerini dikkate alır, bu tür bir yaklaşım gerçek dünyada olduğu gibi malzemelerin görünümünü sağlar.
###  **Cube için Texture ile Phong erial aterial**
Uhen Ucoordinates koordinatları kullanıma hazır, malzeme kullanarak örgü yüzeyine bir doku uygulayabiliriz. Only vertex rengi, yüzey detaylarını tarif edemez, bu da kullanılan malzemelerdir. Here, küp düğümüne bir Phong malzemesi eklemek için bir örnek:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MaterialToCube-AddMaterialToCube.py" >}}

We dağınık doku haritalama ve parlaklık parametresi ile speküler bir renk belirledi.
###  **Hyhycally hysically Based dering en( (PBR) erial aterial to a Box**
PBR plays a key role for the game engine visuals, with its efficient and realistic rendering of interactions between light and surface via attenuation of the brightness and scattering of reflected light. Developers can use Aspose.3D API to apply PBR material to 3D objects in a scene. This code example demonstrates to how to create a Box object, and then apply the PBR material.

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
