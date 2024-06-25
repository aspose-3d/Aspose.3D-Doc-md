---
title: Tonvert Mesh to Triangle Mesh ve Mrimitive Shape to Mesh
type: docs
weight: 30
url: /tr/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for .NET API, geliştiricilerin herhangi bir örgü nesnesini, vertex'in özel bellek düzeni ile üçgen ağa dönüştürmelerine izin verir. Vertex'in özel bellek düzeni, kod örneklerinde vertexdeclaration sınıfı tarafından yapısı veya dinamik olarak tanımlanır.
---
##  **Vonvert a Vesh to Triangle Mesh with uustom Vetex yout aaof the Vertex**
[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API allows developers to convert any mesh object to triangle mesh with custom memory layout of the vertex. The custom memory layout of the Vertex is defined using the Struct or dynamically by [`VertexDeclaration`](https://reference.aspose.com/3d/net/aspose.threed.utilities/vertexdeclaration/) class in the code examples.

{{% alert color="primary" %}}

Bu yardım konusu, kodu kapsamlı ve kısa tutmak için kutudan ve küreden kafesler oluşturur. Geliştiriciler, bu yardım konusu hakkında manuel olarak bir ağ oluşturabilirler: [3D küp mesh oluşturun](/3d/tr/net/create-3d-mesh-and-scene/).

{{% /alert %}}

These örnekleri nasıl olduğunu gösterir:

- [Convert a verphere to verriangle Mesh vertex özel bellek düzeni ile (Struct olarak tanımlanmıştır)](/3d/tr/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convert bir Box Triangle Mesh vertex özel bellek düzeni ile (Vertextexeclaration sınıfı tarafından tanımlanmıştır)](/3d/tr/net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
###  **Convert Mesh**
Developers, örgüyü üçgen örgüye dönüştürebilir, çünkü herhangi bir karmaşık (yüzey) yapı bir grup üçgen olarak temsil edilebilir. The üçgen en atomik geometridir. Talmost neredeyse her şey için temel olarak kullanılır.
###  **Bir Triangle Mesh Access ces ertices**
Developers, hafızadaki dikeylerin birleştirilmeden önce Indices, gerçek dikenlere, dikeylere ve toplam bayt değerlerine erişebilir.

Below örneği, özel bellek düzeni ile üçgen ağa bir Sphere dönüştürür.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout.cs" >}}




Below örneği, bir Box'u özel bellek düzeni ile üçgen ağa dönüştürür.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.cs" >}}
##  **Monvert the Primitive to a Mesh**
Using Aspose.3D for .NET, developers can convert any primitive object to a mesh. Primitives include many of the most basic and most used objects like box, sphere, plane, cylinder, and torus.

{{% alert color="primary" %}}

Bir arayüz uygulayan herhangi bir sınıf `IMeshConvertible` herhangi bir 3D dosya formatına ihracat yaparken ağa dönüştürülebilir.

{{% /alert %}}
###  **Monvert a Sphere to Mesh**
A sphere, spor toplarından uzaydaki gezegenlere kadar her yerde görünen üç boyutlu alanda mükemmel bir yuvarlak geometrik nesnedir. Let, bir örgü oluşturmak için Sphere İlkel kullanıyor.
To kod örneği aşağıda bir Sphere örgü dönüştürür.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertSpherePrimitivetoMesh-ConvertSpherePrimitivetoMesh.cs" >}}
###  **Monvert a Box to Mesh**
A Box, içeriğin taşınması için genellikle depolama olarak veya geçici kullanım için kalıcı kullanım için çeşitli kaplar ve prizler açıklar. Let, bir örgü oluşturmak için Box İlkel kullanıyor. The kod örneği aşağıda bir Box ağa dönüştürür.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertBoxPrimitivetoMesh-ConvertBoxPrimitivetoMesh.cs" >}}
###  **Monvert a Mlane to Mesh**
A plane extends infinitely without thickness. An example of a plane is a coordinate plane. Lets use the `Plane` primitive to create a mesh. The code example below converts a `Plane` to `Mesh`.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertPlanePrimitivetoMesh-ConvertPlanePrimitivetoMesh.cs" >}}
###  **Monvert a Cylinder to Mesh**
A silindir, en temel eğrisel geometrik şekillerden biridir, verilen düz bir çizgiden, silindirin ekseninden sabit bir mesafede noktalar tarafından oluşturulan yüzey. It birçok yerde, örneğin bir evin önünde veya bir araba tahrik mili olarak bir sütun olarak kullanılabilir. Lets, bir örgü oluşturmak için Cylinder ilkelini kullanır. To kod örneği aşağıda bir Cylinder ağa dönüştürür.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertCylinderPrimitivetoMesh-ConvertCylinderPrimitivetoMesh.cs" >}}
###  **Monvert a Torus to Mesh**
A torus, daire ile bir eksen koplanar hakkında üç boyutlu bir alanda bir daire döndürerek oluşan bir devrim yüzeyidir. If devrimin ekseni çembere dokunmaz, yüzeyin halka şekli vardır ve devrim torusuna denir. Let, bir örgü oluşturmak için Torus ilkelini kullanıyor. The kod örneği aşağıda bir Torus'u ağa dönüştürür.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-ConvertTorusPrimitivetoMesh-ConvertTorusPrimitivetoMesh.cs" >}}
