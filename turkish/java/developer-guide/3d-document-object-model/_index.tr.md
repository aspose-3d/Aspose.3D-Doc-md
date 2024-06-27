---
title: Aspose.3D belge nesne modeli (dom)
type: docs
weight: 20
url: /tr/java/aspose-3d-document-object-model
description: Each 3D scene can comprise of any number of viewports. Using Aspose.3D for Java API, developers can capture one or more viewports in a single screenshot. They may render it in the GUI based Java application or an image.
---
The Aspose.3D Document Object Model (DOM) is a powerful in-memory representation of a 3D scene. It provides developers with the ability to read, manipulate, and modify the content and formatting of a 3D scene programmatically.

In this section, we will explore the key classes of the Aspose.3D DOM and their relationships. By utilizing these classes, you can gain programmatic access to various elements within a 3D scene.

Aspose.3D dom'un ana sınıflarına geçelim:

* **Sahne**: The Scene class represents the root of the 3D scene hierarchy. It serves as the container for all other elements and provides methods to manipulate the overall scene.
* **Düğüm**: Nodes are the building blocks of a 3D scene. They represent individual objects or entities within the scene, such as meshes, lights, cameras, or groups. Nodes can be transformed, animated, and textured.
* **Varlıklar**: Varlıklar sınıfları, 3D sahnesini oluşturan çok çeşitli nesneleri ve öğeleri kapsar. Kafesler, ışıklar, kameralar, profiller ve daha fazlası gibi varlıkları içerir. Bu varlıklar, bunları programlı olarak birleştirerek ve manipüle ederek karmaşık sahneler oluşturmanıza izin veren yapı taşları olarak hizmet vermektedir. Varlıklar kategorisi, 3D sahnesinin bu temel unsurları üzerinde erişim ve kontrol sağlar.
* **Malzemeler**: Malzeme sınıfları, nesnelerin görsel özelliklerini 3D sahnesinde tanımlamak etrafında döner. Işığın yüzeylerle nasıl etkilediğini belirleyen, programlı olarak oluşturmak, değiştirmek ve kontrol etmek için araçlar sağlar. Renk, doku, şeffaflık ve yansıma gibi özellikleri ayarlayarak, çeşitli görsel efektler elde edebilir ve 3D modellerinizin görünümünü özelleştirebilirsiniz.
* **Animasyonlar**: The Animation classes focuses on creating and controlling movement and transformations within a 3D scene. It allows you to programmatically define and manipulate animations, enabling objects to move, rotate, scale, or change properties over time. With this category, you can bring dynamic and interactive elements to your 3D scenes.

By utilizing the Aspose.3D DOM classes mentioned above, you can programmatically interact with and manipulate the content and structure of a 3D scene. This provides flexibility and control when working with 3D models in your applications.


## Sahne yapısı

When Aspose.3D reads a 3D file into memory, it generates objects of various types to represent the different elements within the 3D scene.


Sahne yapısı Aspose.3D esneklik ve organizasyon sunan kompozit tasarım desenini takip eder:

 * Düğüm, diğer düğümleri tutabilen kaplar olarak hizmet eder ve sahne içinde farklı nesnelerin gruplanmasına izin verir.
 * Her düğüm, çocuk düğümlerine de uygulanabilen kendi dönüşümüne sahip olabilir.
 * Tüm mekansal varlık türleri Aspose.3D bir düğüm örneğinin altına yerleştirilmelidir. Bu, kafes, ışık, kamera ve diğer öğeler gibi nesnelerin sahne hiyerarşisinde düzenlenmesini sağlar.
 * Düğümler birden fazla malzeme içerebilir ve bir düğüme bağlı poligonlar ve malzemeler arasındaki ilişki, örgü nesnesindeki `VertexElementMaterial` kavramı kullanılarak ele alınır.


! [Sahne hiyerarşi](scene.png)


## Mekansal varlıklar
Tüm mekansal varlıklar Aspose içinde. 3D sanal ortamlar oluşturmak için temel yapı taşları olarak hizmet veren `Entity` sınıfından devralır. Aspose.3D, bu varlıkları kendi özel amacı ve işlevselliği ile birkaç ana kategoriye ayırır.

! [Varlıklar](entity.png)

* **İlkel** The `Primitive` class serves as the base class for all procedural 3D geometries within Aspose.3D, such as `Cylinder`, `Torus`, and `Sphere`. These geometries can be defined using a minimal set of parameters, making it convenient to create basic 3D shapes.
* **Eoeometri**: Geometriler Aspose.3D genellikle 3D nesnesinin şeklini ve yapısını tanımlayan dikenlerden, kenarlardan ve poligonlardan oluşur. Bu kategori, 3D sahnesinde çeşitli nesneleri temsil etmek için kullanılan çok çeşitli karmaşık geometrileri kapsamaktadır.
* **Profil**: İlkellere benzer profiller, x-y düzleminde 2d kapalı kontür tanımlayın. Karşılık gelen 3D geometrileri oluşturmak için ekstrüde edilebilen 2d şekiller oluşturmanın bir yolunu sağlarlar. Profiller genellikle daha karmaşık 3D nesneler oluşturmak için bir başlangıç noktası olarak kullanılır.
* **Curve**: Unlike profiles, curves can be open or unconnected. They are utilized to define spatial paths in 3D. Curves provide a means to create flexible and customizable paths that objects can follow within a 3D environment.
* **Ekstrüzyon**: Extrusions are a procedural technique employed to construct 3D geometries using profiles and curves. By applying extrusion to a profile or a curve, a 3D shape can be generated by extending the profile or curve along a specified direction. This approach enables the creation of more complex and dynamic geometries.
* **Frustum**: Frustum kategorisi ışıklar ve kameralar gibi nesneleri içerir. Frustums görüntüleme hacmini ve bakış açısını 3D sahnesinde tanımlar. Kameralar sahnenin görünür kısmını belirlemek için meyveleri kullanırken, ışıklar sahneyi aydınlattıkları bölgeyi tanımlamak için meyveleri kullanır.

These major entity categories in Aspose.3D encompass a variety of entities that play essential roles in constructing and representing virtual environments, providing a versatile toolkit for creating and manipulating 3D scenes.


### Geometri türleri

! [Geometri türleri](geometries.png)

Aspose.3D birçok geometri türü içerir:


* `Mesh` yazma aracı dostu poligon mesh.
* `PointCloud` nokta bulutu.
* `NurbsSurface` üniform olmayan rasyonel b-spline yüzeyleri.
* Bir dizi kontrol noktası ve karıştırma fonksiyonu ile tanımlanan `Patch` yüzey.
* `TriMesh` API dostu üçgen tabanlı ağ oluşturur.


Bunların en önemlisi `Mesh` ve `TriMesh`, farklılıklar tabloda:

|Feature| `Mesh` | `TriMesh` |
| ---     |---     |---        |
|Üçgen olmayan çokgen|Evet|Hayır|
|Değiştirmek kolay|Evet|Hayır|
|Veri indeksi yeniden kullanım|Evet|Hayır|
|Cpu önbellek dostu|Hayır|Evet|
|API dostu|Hayır|Evet|
|Sabit bellek düzeni|Hayır|Evet|

Classes derived from `Geometry` is designed for modify and content creation while the `TriMesh` is designed for rendering.

A `Geometry` consists of control points and `VertexElement` which defined extra data for control point/edge/polygon/polygon vertex, `Geometry` can contains zero or more `VertexElement`, concrete `Geometry` sub classes implemented different methods for modeling and representing 3D geometries.


! [Geometri türleri](mesh.png)


Bir vertex elemanını manuel olarak oluşturabilir ve bunun için veri atayabilirsiniz. Aşağıdaki kod örneği bunu nasıl yapacağını gösterir:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-SetupNormalsOnCube.java" >}}

### İlkel geometri türleri


Aspose.3D provides a set of predefined primitive geometry types that follow specific rules and algorithms to generate 3D models. These primitive types simplify the process of creating 3D geometries compared to using more complex Geometry types.

Mevcut önceden tanımlanmış ilkel tipler Aspose.3D şunları içerir:

*  `Box`: İlkel kutu, genişlikleri, yüksekliği ve derinliği ile tanımlanan dikdörtgen küp şeklinde şekiller oluşturmanıza izin verir.
* Silindir: silindir İlkel ile, yarıçapı ve yüksekliği belirterek silindirik şekiller oluşturabilirsiniz. Bu, tüpler veya sütunlar gibi nesneler oluşturmak için kullanışlıdır.
*  `Dish`: çanak primitive, kaseler veya uydu yemekleri gibi nesneleri temsil etmek için yaygın olarak kullanılan çanak şeklindeki geometrilerin yaratılmasını sağlar.
*  `Plane`: The plane primitive generates flat surfaces defined by their width and length. It is frequently used as a foundation or ground plane in 3D scenes.
*  `Pyramid`: piramit İlkel ile, taban boyutu ve yüksekliği ile karakterize piramit şeklindeki geometriler oluşturabilirsiniz. Bu, binalar veya piramitler gibi nesneleri inşa etmek için yararlıdır.
*  `Torus`: torus primitive, ana ve küçük daireler için belirtilen radii ile çörek şeklindeki geometriler oluşturmanıza izin verir. Halkaları veya lastikleri andıran nesneler oluşturmak için uygundur.
*  `RectangularTorus`: dikdörtgen torus primitive dairesel olanlar yerine dikdörtgen kesitli torus benzeri geometriler üretir. Benzersiz şekiller oluşturmak için ek esneklik sağlar.
*  `Sphere`: küre İlkel, belirtilen yarıçapa göre mükemmel yuvarlak geometriler üretir. Bu, gezegen veya top gibi nesneler oluşturmak için yararlıdır.

Bu önceden tanımlanmış ilkel türleri Aspose olarak kullanarak. 3D, kolayca geniş bir temel 3D geometrileri oluşturabilirsiniz. Bu, modelleme sürecini basitleştirir ve 3D sahnelerinizde nesneleri hızlı bir şekilde şekillendirmenizi ve monte etmenizi sağlar.

! [İlkel geometri türleri](primitives.png)

Aşağıdaki kod örneği, belirtilen yarıçaplı bir küre nasıl oluşturulacağını gösterir:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-objects-WorkingWithSphereRadius-WorkingWithSphereRadius.java" >}}


### Ekstrüzyon türleri

Ekstrüzyon, çeşitli karmaşık 3D nesneleri oluşturmak için kullanılabilir, 3D nesnesini oluşturmak için bir eğri boyunca 2d profilini genişletmeyi içeren 3D modellemesinde temel bir yöntemdir.

Aspose.3D 3 ekstrüzyon türü sağladık:

* `LinearExtrusion` lineer ekstrüzyon, giriş olarak 2d bir profil alır ve 3. boyuttaki şekli uzatır.
* `RevolvedAreaSolid` bu sınıf, bir eksen hakkında bir profil tarafından sağlanan bir kesiti döndürerek sağlam bir modeli temsil eder.
* `SweptAreaSolid` bu sınıf, 2d profil kesitinin alanı taramasına izin veren kapsamlı bir temsil şeması ile sağlam bir modeli temsil eder.


! [Sions yonlar](extrusions.png)

Aşağıdaki kod örneği, bir metin profilinden doğrusal bir ekstrüzyon nasıl oluşturulacağını gösterir:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-LinearExtrusion-Text.java" >}}


### Eğri türleri

Aspose.3D, bir eğri, birden fazla eğri segmentinden oluşan çizgiler, nurler eğrileri veya kompozit eğriler gibi çeşitli formları alabilen bir veya daha fazla uzamsal yolu temsil eder. Eğriler, dinamik ve karmaşık 3D şekilleri oluşturmak için ekstrüzyon tipleri ile birlikte yaygın olarak kullanılır.

Eğriler, nesnelerin pürüzsüz ve hassas hareketler sağlayan, 3D ortamında takip ettiği karmaşık yolları tanımlamak için kullanılabilir. Farklı eğri tiplerini kullanarak ve bunları birlikte oluşturarak, 3D modelleriniz için çok yönlü ve özelleştirilebilir mekansal yollar elde edebilirsiniz.

Moreover, certain file formats supported by Aspose.3D also provide the capability to import and export curve data. This allows you to seamlessly integrate curves created in external applications or share curves generated within Aspose.3D with other software.


! [Eğri türleri](curves.png)

## Profil türleri

Aspose.3D offers a range of 2D profiles that can be utilized to create closed shapes or contours within a 3D environment. These profiles enable the creation of intricate 2D structures that can be further extruded or manipulated into 3D geometries. Here are some notable profile implementations in Aspose.3D:

* `ParameterizedProfile`: Aspose.3D standart şekillerle profil sunan birkaç uygulama sağlar. Bu önceden tanımlanmış profiller, daireler, dikdörtgenler ve çokgenler gibi yaygın olarak kullanılan şekillerin hızlı bir şekilde oluşturulmasına izin verir.

* `MirroredProfile`: bu profil tipi, y ekseni boyunca mevcut bir profili yansıtmanıza ve simetrik bir şekil oluşturmanıza izin verir. Dengeli ve görsel olarak çekici profiller oluşturmak için uygun bir yol sağlar.

* `ArbitraryProfile`: keyfi profil uygulamasıyla, kapalı bir profil oluşturmak için keyfi bir eğri eşleştirebilirsiniz. Bu, bir eğri tanımlayarak ve daha fazla manipülasyon için kapalı bir profile dönüştürerek özel şekiller tasarlamada esneklik sunar.

* `Text`: Aspose.3D, belirtilen yazı tipini kullanarak metinden profil üretme yeteneğini içerir. Bu özellik, harf, sayı veya başka bir metin içeriği şeklinde profil oluşturmanıza, 3D modellerinize kişiselleştirme veya markalaşma unsuru eklemenize izin verir.

! [2d profil tipleri](profiles.png)

### Kamera ve ışık türleri

! [Kamera ve ışık](frustums.png)

## Malzeme türleri

Aspose.3D, lambert malzeme, phong malzeme, pbr malzeme, pbr speküler malzeme ve gölgelendirici malzeme (sadece FBX dosyalarında mevcuttur) dahil olmak üzere çeşitli malzeme türleri için destek sağlar.

Her bir malzeme Aspose.3D, görünümünü ve davranışını 3D sahnesinde tanımlayan farklı özelliklere ve özelliklere sahip olabilir. Bu malzemeler doku örneklerine bağlanabilir, görsel özelliklerini geliştirebilir.

Dokular Aspose.3D belirli bir malzeme özelliği ile ilişkilidir. Doku tipi, görüntü kaynağı ve doku örnekleyicisi için parametre tanımlarını birleştirir. Dokuları kullanarak, 3D modellerinizin yüzeylerine detaylı desenler, renkler ve diğer görsel efektler uygulayabilirsiniz.

Bir dizi malzeme türü desteği ve dokuları bağlama yeteneği ile Aspose.3D, 3D sahneleriniz için görsel olarak çekici ve gerçekçi malzemeler oluşturmada esneklik sunar.

! [Malzeme türleri](materials.png)

Aşağıdaki kod örneği, bir pbr malzemesinin geometriye nasıl uygulanacağını gösterir:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ApplyPBRMaterialToBox.java" >}}

## Animasyon nesneleri ilişkisi
Aspose.3D veri seviyesi animasyon desteği sağlar ve hesaplama desteği şu anda geliştirilmektedir.

Aspose.3D, bir sahne birden fazla animationclip nesnesini içerebilir. Her animasyon klipsi birden fazla animasyon düğümünden oluşabilir. Animasyon düğümü, alt animasyon düğümleriyle hiyerarşik yapıların oluşturulmasına izin veren kompozit tasarım desenini takip eder.

Animasyon düğümleri, animasyonlu olacak hedef nesnenin özelliklerini tanımlayan bağlama noktaları ile ilişkili olabilir. Vektörler, birçok varlık özelliklerinde yaygın olarak kullanılan veri tipleridir. Bu nedenle, bağlama noktaları, vektörün belirli kanallarını bağımsız olarak güncellemek için farklı animasyon kanallarına sahip olabilir. Her kanal, değerin zamanla nasıl canlandırıldığını tanımlayan bir anahtar çerçeve dizisi içerir.

Bu sistem, bir sahne içindeki nesneleri canlandırmak için esnek bir çerçeve sağlar. Animasyon kliplerini, düğümleri, bağlantı noktalarını ve kanalları tanımlayarak, 3D sahnesindeki varlıkların çeşitli özelliklerini etkileyen karmaşık ve dinamik animasyonlar oluşturabilirsiniz.

Aspose.3D şu anda veri seviyesi animasyonunu desteklerken, devam eden geliştirme, çerçeve içinde animasyonlar oluşturma ve manipüle etme yeteneklerini geliştirecek hesaplama desteğini genişletmeye odaklanmıştır.

! [Animasyonlar](animations.png)


Animasyonlu bir sahne bu tür bir yapıya sahip olabilir:


! [Animasyonlar örnek](animation_relations.png)