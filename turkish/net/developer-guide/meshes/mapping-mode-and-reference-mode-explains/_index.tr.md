---
title: Mappingmode ve referencemode açıklar
type: docs
weight: 10
url: /tr/net/mapping-mode-and-reference-mode-explains
description: Aspose.3D for .NET kullanarak, geliştiriciler çeşitli vertex veri öğeleri ile mesh tanımlayabilir, burada shes'in bileşenine verileri nasıl eşleştireceğimizi ve verileri nasıl canlandıracağımızı açıklıyoruz.
---
{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers can define meshes with various vertex data elements, including normals, colors, and weights. Aspose.3D offers two mechanisms to optimize data reuse: `MappingMode` and `ReferenceMode`. These mechanisms are designed to minimize the memory footprint of meshes, particularly in advanced formats like FBX and USD. MappingMode allows for efficient mapping of vertex data to mesh components, while ReferenceMode facilitates the referencing of vertex element data across multiple mesh components. Together, these features enhance performance and memory efficiency, making Aspose.3D a powerful tool for handling complex 3D models in .NET applications.

{{% /alert %}}



###  `MappingMode` açıklıyor

 `MappingMode` determines how the element data is mapped to the surface of the geometry in Aspose.3D for .NET. It provides various ways to define this mapping:

1. **Controltroloint**Her bir veri öğesi geometrinin kontrol noktasına eşleştirilir. Bu mod, geometrinin şeklini tanımlayan her kontrol noktasının belirli bir veri elemanıyla ilişkili olmasını sağlar.
1. **Olyolygongonertex**Veriler bir çokgenin verteksine eşleştirilmiştir. Bir kontrol noktasının çoklu çokgenler tarafından paylaşıldığı durumlarda, kontrol noktasının her örneği, farklı poligonlarda göründüğü gibi, kendi ayrı verilerine sahip olacaktır. Bu, paylaşılan kontrol noktalarının bile farklı poligonlar için dikenler olarak hizmet verdiklerinde benzersiz verilere sahip olmasını sağlar.
1. **Polygon**Veriler tüm çokgen ile eşleştirilir. Bu, bir çokgenin tüm dikenlerinin aynı veri elemanını paylaştığı anlamına gelir. Bu mod, poligon içindeki tutarlılığı sağlayarak, tüm poligon yüzeyinde tek tip verilerin uygulanması gerektiğinde kullanışlıdır.
1. **Edge**Veriler geometrinin kenarlarına eşleştirilir. Bir kenarın her uç noktası aynı verileri paylaşır ve farklı kenarlar için farklı verilere izin verirken kenarlara düzgün veri uygulamanın bir yolunu sağlar. Bu, kırışık değerleri veya kenar tabanlı özellikler gibi kenarlara özgü özellikleri tanımlamak için özellikle yararlı olabilir.
1. **Allllame**Tek bir veri elemanı geometrinin tüm yüzeyine eşleştirilir. Verilerin kontrol noktaları, çokgen dikenleri veya kenar uç noktaları olarak yorumlanmasına bakılmaksızın, aynı veri değeri tüm elementler boyunca eşit olarak uygulanır. Bu mod, tüm geometri boyunca sabit bir değerin korunması gereken senaryolar için idealdir ve tüm 3D modelinde tek tip bir özellik sağlar.




###  `ReferenceMode` açıklıyor
 `ReferenceMode` verileri endekslerle yeniden kullanıp kullanamayacağını tanımlar, `ReferenceMode` için üç politika vardır:

1.**Doğrudan**, data is directly referenced, and stored in `VertexElement`'s `Data` property.
1.**Indextodirect**Veriler indeks ile başvurulur, daha sonra `VertexElement` veri listesinde dizine erişilir.
1.**Dizin**, data is only referenced by index, now only the `VertexElementMaterial` use this reference mode, this is similar to `IndexToDirect` but the differences is the materials are defined under the `Node`'s property `Materials`, not in the `VertexElementMaterial`, all `VertexElement` only works with primitive data.



Örneğin, bir küpün tanımı göz önüne alındığında:

{{< highlight "csharp" >}}
var cube = new Mesh();
Vector4[] controlPoints = new Vector4[]
{
    new Vector4( -5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 0.0, 5.0, 1.0),
    new Vector4( 5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 10.0, 5.0, 1.0),
    new Vector4( -5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 0.0, -5.0, 1.0),
    new Vector4( 5.0, 10.0, -5.0, 1.0),
    new Vector4( -5.0, 10.0, -5.0, 1.0)
};
cube.ControlPoints.AddRange(controlPoints);

// Front face (Z+)
cube.CreatePolygon(new int[] { 0, 1, 2, 3 });
// Right side (X+)
cube.CreatePolygon(new int[] { 1, 5, 6, 2 });
// Back face (Z-)
cube.CreatePolygon(new int[] { 5, 4, 7, 6 });
// Left side (X-)
cube.CreatePolygon(new int[] { 4, 0, 3, 7 });
// Bottom face (Y-)
cube.CreatePolygon(new int[] { 0, 4, 5, 1 });
// Top face (Y+)
cube.CreatePolygon(new int[] { 3, 2, 6, 7 });

var vertexColor = (VertexElementVertexColor) cube.CreateElement(VertexElementType.VertexColor);
vertexColor.MappingMode = MappingMode.ControlPoint;
var red = new Vector4(1, 0, 0, 1);
var green = new Vector4(0, 1, 0, 1);
var blue = new Vector4(0, 0, 1, 1);
var white = new Vector4(1, 1, 1, 1);

{{< /highlight >}}

Kontrol noktaları 0 ve 1, yeşil kontrol noktaları 2 ve 3, mavi kontrol noktaları 4 ve 5 ve beyaz kontrol noktaları 6 ve 7 için kırmızı atamak istiyorsanız, aşağıdaki yaklaşımla bunu elde edebilirsiniz:

{{< highlight "csharp" >}}
vertexColor.ReferenceMode = ReferenceMode.Direct;
vertexColor.Data.Add(red); // 0
vertexColor.Data.Add(red); // 1
vertexColor.Data.Add(green); // 2
vertexColor.Data.Add(green); // 3
vertexColor.Data.Add(blue); // 4
vertexColor.Data.Add(blue); // 5
vertexColor.Data.Add(white); // 6
vertexColor.Data.Add(white); // 7
{{< /highlight >}}

Noktaları verimli bir şekilde kontrol etmek ve bellek tüketimini azaltmak için renkler atamak için renkleri referans almak için endeksleri kullanabilirsiniz. Renkleri ayrı ayrı tanımlayarak ve bunları endekslerle referans alarak, yedekliliği en aza indirebilirsiniz. İşte bunu nasıl başarabilirsiniz:

İlk olarak, benzersiz renkler için vector4 tipinde 4 renk tanımlayın ve daha sonra bu renkleri her kontrol noktasına atamak için 8 endeksli bir dizi kullanın:

{{< highlight "csharp" >}}
vertexColor.ReferenceMode = ReferenceMode.IndexToDirect;
vertexColor.Data.Add(red);
vertexColor.Data.Add(green);
vertexColor.Data.Add(blue);
vertexColor.Data.Add(white);

vertexColor.SetIndices(new int[] { 0, 0, 1, 1, 2, 2, 3, 3 });
{{< /highlight >}}

Bu yaklaşımda:

1. Benzersiz renkleri tanımlayın: vector4 örnekleri olarak sadece 4 renk tanımlanır (kırmızı, yeşil, mavi, beyaz).
1. Bir renk dizin dizisi oluşturun: her kontrol noktası için bu 4 rengi referans etmek için 8 endeksli bir dizi kullanılır.
1. Indices kullanarak harita renkleri: renkleri endekslerle referans alarak, her bir renk bir kez saklandığı ve çoklu kontrol noktalarında yeniden kullanıldığı için bellek tüketimini azaltırsınız.

Bu yöntem, yedekli veri depolama alanını düşürerek bellek kullanımını optimize eder ve 3D modelinizi daha verimli hale getirir.