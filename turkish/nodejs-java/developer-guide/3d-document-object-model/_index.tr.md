---
title: Aspose.3D Belge Nesne Modeli (DOM)
type: docs
weight: 20
url: "/tr/nodejs-java/aspose-3d-document-object-model"
description: "Her 3B boyutsal sahne, herhangi sayıda pencere elemanından oluşabilir. Aspose.3D for nodejs-java API'si ile geliştiriciler, tek bir ekran görüntüsünde bir veya daha fazla pencere elemanını yakalayabilirler. Bunları GUI tabanlı nodejs-java uygulamalarında veya bir resimde işleyebilirler."
---

Aspose.3D Belge Nesne Modeli (DOM), 3B sahnesinin güçlü bir bellek içi gösterimidir. Geliştiricilere 3B sahnesinin içeriğini ve biçimlendirmesini programlı olarak okuma, değiştirme ve düzenleme yeteneği sağlar.

Bu bölümde, Aspose.3D DOM'unun temel sınıflarını ve bunların ilişkilerini inceleyeceğiz. Bu sınıfları kullanarak, 3B sahnesindeki çeşitli öğelere programlı erişim sağlayabilirsiniz.

Aspose.3D DOM'unun ana sınıflarına bakalım:

* **Sahne**: Sahne sınıfı, 3B sahne hiyerarşisinin kökünü temsil eder. Diğer tüm öğeler için bir kapsayıcı görevi görür ve sahneyi manipüle etmek için yöntemler sağlar.
* **Düğüm**: Düğümler, 3B sahnesinin yapı taşlarıdır. Sahnedeki bireysel nesneleri veya varlıkları, örneğin örgüleri, ışıkları, kameraları veya grupları temsil eder. Düğümler dönüştürülebilir, canlandırılabilir ve dokulandırılabilir.
* **Varlıklar**: Varlıklar sınıfı, 3B sahnesini oluşturan geniş bir nesne ve öğe yelpazesini kapsar. Örgüler, ışıklar, kameralar, profiller ve daha fazlası gibi varlıkları içerir. Bu varlıklar yapı taşları görevi görür, bunları programlı olarak birleştirerek ve değiştirerek karmaşık sahneler oluşturmanıza olanak tanır. Varlıklar kategorisi, 3B sahnesinin temel öğelerine erişim ve kontrol sağlar.
* **Malzemeler**: Malzemeler sınıfı, 3B sahnesindeki nesnelerin görsel özelliklerini tanımlamaya odaklanır. Programlı olarak malzeme oluşturmak, değiştirmek ve kontrol etmek için araçlar sağlar; bunlar yüzeylerin ışıkla nasıl etkileşimini belirler. Renk, doku, şeffaflık ve yansıma gibi özellikleri ayarlayarak çeşitli görsel efektler elde edebilir ve 3B modellerinizin görünümünü özelleştirebilirsiniz.
* **Animasyonlar**: Animasyonlar sınıfı, 3B sahnesi içindeki hareket ve dönüşümleri oluşturmaya ve kontrol etmeye odaklanır. Programlı olarak animasyonları tanımlamanıza ve manipüle etmenize olanak tanıyarak nesnelerin zaman içinde hareket etmesini, dönmesini, ölçeklenmesini veya özelliklerini değiştirmesini sağlar. Bu kategori ile 3B sahnelerinize dinamik ve etkileşimli öğeler ekleyebilirsiniz.

Yukarıda bahsedilen Aspose.3D DOM sınıflarını kullanarak, 3B sahnesinin içeriği ve yapısı ile programlı olarak etkileşim kurabilir ve onu değiştirebilirsiniz. Bu, uygulamalarınızdaki 3B modellerle çalışırken esneklik ve kontrol sağlar.

## Sahne yapısı

Aspose.3D, bir 3B dosyayı belleğe okuduğunda, 3B sahnesindeki farklı öğeleri temsil etmek için çeşitli türlerde nesneler oluşturur.

Aspose.3D içindeki sahne yapısı, esneklik ve organizasyon sunan kompozit tasarım desenini izler:

* Düğümler, sahne içindeki farklı nesnelerin gruplandırılmasına olanak tanıyan diğer düğümleri barındırabilen kapsayıcılar görevi görür.
* Her düğümün kendi dönüşümü olabilir ve bu dönüşüm aynı zamanda alt düğümlerine de uygulanır.
* Aspose.3D içindeki tüm uzamsal varlık türleri bir Düğüm örneğinin altında yer almalıdır. Bu, örgüleri, ışıkları, kameraları ve diğer öğeleri sahne hiyerarşisi içinde düzenler.
* Düğümler birden fazla malzemeyi içerebilir ve bir düğüme ekli çokgenler ve malzemeler arasındaki ilişki, Örgü nesnesi içindeki `VertexElementMaterial` kavramı kullanılarak ele alınır.

![Sahne hiyerarşisi](scene.png)

## Uzamsal Varlıklar
Aspose.3D içindeki tüm uzamsal varlıklar, sanal ortamlar oluşturmak için temel yapı taşları görevi gören `Entity` sınıfından türetilir. Aspose.3D, bu varlıkları kendi özel amaç ve işlevselliğine sahip çeşitli ana kategorilere ayırır.

![Varlıklar](entity.png)

* **İlkelli**: `Primitive` sınıfı, Aspose.3D içindeki tüm işlemsel 3B geometriler için temel sınıf görevi görür, örneğin `Silindir`, `Torus` ve `Küre`. Bu geometriler, minimum bir parametre seti kullanılarak tanımlanabilir, bu da temel 3B şekiller oluşturmayı kolaylaştırır.
* **Geometri**: Aspose.3D'deki Geometri, 3B ortamda kapalı şekiller veya konturlar oluşturmak için kullanılabilecek 2B profiller sunar. Bu profiller, daha sonra 3B geometrilere dönüştürülebilecek karmaşık 2B yapılar oluşturmak için kullanılabilir.
* **ArbitraryProfile**: Keyfi profil uygulaması ile, bir eğriyi haritalandırarak kapalı bir profil oluşturabilirsiniz. Bu, bir eğri tanımlayarak ve bunu daha fazla manipülasyon için kapalı bir profile dönüştürerek özel şekiller tasarlamak için esneklik sunar.
* **Metin**: Aspose.3D, belirtilen bir yazı tipi kullanarak metinden profiller oluşturma yeteneği içerir. Bu özellik, harflerin, sayıların veya diğer metin içeriğinin şekillerinde profiller oluşturmanıza olanak tanıyarak 3B modellerinize kişiselleştirme veya markalaşma öğesi ekler.

![2B profil türleri](profiles.png)

## Kamera ve ışık türleri

![Kamera ve ışık](frustums.png)

## Malzeme türleri

Aspose.3D, Lambert malzemesi, Phong malzemesi, PBR malzemesi, PBR özel malzemesi ve gölge malzemesi (yalnızca FBX dosyalarında kullanılabilir) dahil olmak üzere çeşitli malzeme türlerini destekler.

Aspose.3D'deki her malzeme, 3B sahne içindeki görünümünü ve davranışını tanımlen özelliklere sahip olabilir. Bu malzemeler, görsel özelliklerini geliştirmek için doku örneklerine bağlanabilir.

Aspose.3D'deki dokular, belirli bir malzeme özelliğine ilişkilidir. Doku türü, görüntü kaynağı ve doku örnekleyici için parametre tanımlarını birleştirir. Dokuları kullanarak, 3B modellerinizin yüzeylerine ayrıntılı desenler, renkler ve diğer görsel efektler uygulayabilirsiniz.

Çeşitli malzeme türlerine ve dokuları bağlama desteği ile Aspose.3D, 3B sahneleriniz için görsel olarak çekici ve gerçekçi malzemeler oluşturmak için esneklik sunar.

![Malzeme türleri](materials.png)

## Animasyon nesneleri ilişkisi
Aspose.3D veri düzeyi animasyon desteği sağlar ve hesaplama desteği şu anda geliştirilmektedir.

Aspose.3D'de bir sahne birden fazla `AnimationClip` nesnesi içerebilir. Her animasyon klipi birden fazla animasyon düğümü içerebilir. Animasyon düğümü, alt animasyon düğümleriyle hiyerarşik yapılar oluşturmaya olanak tanıyan kompozit tasarım desenini izler.

Animasyon düğümleri, hedeflenen nesnenin canlandırılacak özelliklerini tanımlayan bağlama noktalarıyla ilişkilendirilebilir. Vektörler, birçok varlık özelliğinde yaygın olarak kullanılan veri türleridir. Bu nedenle, bağlama noktaları, vektörün bağımsız kanallarını güncellemek için farklı animasyon kanallarına sahip olabilir. Her kanal, değerin zaman içinde nasıl animasyonlandırılacağını tanımlayan bir anahtar kare dizisi içerir.

Bu sistem, bir sahnedeki nesneleri animasyonlandırmak için esnek bir çerçeve sağlar. Animasyon klipleri, düğümleri, bağlama noktalarını ve kanalları tanımlayarak, 3B sahnenizdeki varlıkların çeşitli özelliklerini etkileyen karmaşık ve dinamik animasyonlar oluşturabilirsiniz.

Aspose.3D şu anda veri düzeyi animasyonunu desteklerken, hesaplama desteğinin genişletilmesi odak noktasıdır, bu da çerçeve içinde animasyonları oluşturma ve manipüle etme yeteneklerini artıracaktır.

![Animasyonlar](animations.png)

Bir sahne, bu tür bir yapıya sahip olabilir:

![Animasyonlar Örneği](animation_relations.png)