---
title: Tonvert Mesh to Triangle Mesh ve Mrimitive Shape to Mesh
type: docs
weight: 30
url: /tr/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Python via .NET API için Aspose.3D, geliştiricilerin herhangi bir örgü nesnesini, vertex'in özel bellek düzeni ile üçgen örgüye dönüştürmelerine izin verir. Vo Vertex'in özel bellek düzeni, kod örneklerinde VertexDeclaration sınıfı tarafından Struct veya dynamically kullanılarak tanımlanır.
---
## **Vonvert a Vesh to Triangle Mesh with uustom Vetex yout aaof the Vertex**
[Python via .NET için Aspose.3D](https://products.aspose.com/3d/python-net/)API, geliştiricilerin herhangi bir örgü nesnesini vertex'in özel bellek düzeni ile üçgen ağa dönüştürmelerine izin verir. Vo Vertex'in özel bellek düzeni, kod örneklerinde 07truct veya dinamik olarak [`VertexDeclaration`](http://www.aspose.com/api/net/3d/aspose.threed.utilities/vertexdeclaration) sınıfı kullanılarak tanımlanır.

{{% alert color="primary" %}}

Tonun yardım konusu, kodu kapsamlı ve kısa tutmak için kutudan ve küreden kafesler oluşturur. Developers, bu yardım konusu olarak manuel olarak bir örgü oluşturabilir:[Create a 3D Cube Mesh](/3d/tr/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

These örnekleri nasıl olduğunu gösterir:

- [Convert a verphere to verriangle Mesh vertex özel bellek düzeni ile (Struct olarak tanımlanmıştır)](/3d/tr/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convert bir Box Triangle Mesh vertex özel bellek düzeni ile (Vertextexeclaration sınıfı tarafından tanımlanmıştır)](/3d/tr/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
### **Convert Mesh**
Developers, örgüyü üçgen örgüye dönüştürebilir, çünkü herhangi bir karmaşık (yüzey) yapı bir grup üçgen olarak temsil edilebilir. The üçgen en atomik geometridir. Talmost neredeyse her şey için temel olarak kullanılır.
### **Bir Triangle Mesh Access ces ertices**
Developers, hafızadaki dikeylerin birleştirilmeden önce Indices, gerçek dikenlere, dikeylere ve toplam bayt değerlerine erişebilir.

Below örneği, özel bellek düzeni ile üçgen ağa bir Sphere dönüştürür.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout.py" >}}




Below örneği, bir Box'u özel bellek düzeni ile üçgen ağa dönüştürür.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.py" >}}
## **Convert 'Mrimitive' a 'Mesh'**
Python via .NET için Aspose.3D sing sing, geliştiriciler herhangi bir ilkel nesneyi bir ağa dönüştürebilirler. Primitives, kutu, küre, uçak, silindir ve torus gibi en temel ve en çok kullanılan nesnelerin birçoğunu içerir.

{{% alert color="primary" %}}

Bir arayüz uygulayan Any sınıfı 07eshesheshonvertible 3D dosya formatına ihracat yaparken ağa dönüştürülebilir.

{{% /alert %}}
### **Convert a 'Sphere' to 'eshesh'**
A sphere, spor toplarından uzaydaki gezegenlere kadar her yerde görünen üç boyutlu alanda mükemmel bir yuvarlak geometrik nesnedir. Let, bir örgü oluşturmak için Sphere İlkel kullanıyor.
To kod örneği aşağıda bir Sphere örgü dönüştürür.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertSpherePrimitivetoMesh-ConvertSpherePrimitivetoMesh.py" >}}
### **Convert a 'Box' to 'eshesh'**
A Box, içeriğin taşınması için genellikle depolama olarak veya geçici kullanım için kalıcı kullanım için çeşitli kaplar ve prizler açıklar. Let, bir örgü oluşturmak için Box İlkel kullanıyor. The kod örneği aşağıda bir Box ağa dönüştürür.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertBoxPrimitivetoMesh-ConvertBoxPrimitivetoMesh.py" >}}
### **Convert a 'Plane' to 'eshesh'**
A plane kalınlığı olmadan sonsuz uzanır. An bir uçağın örneği bir koordinat düzlemidir. Lets bir örgü oluşturmak için Plane İlkel kullanın. The kod örneği aşağıda bir Plane'i ağa dönüştürür.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertPlanePrimitivetoMesh-ConvertPlanePrimitivetoMesh.py" >}}
### **Convert a 'Cylinder' to 'Mesh'**
A silindir, en temel eğrisel geometrik şekillerden biridir, verilen düz bir çizgiden, silindirin ekseninden sabit bir mesafede noktalar tarafından oluşturulan yüzey. It birçok yerde, örneğin bir evin önünde veya bir araba tahrik mili olarak bir sütun olarak kullanılabilir. Lets, bir örgü oluşturmak için Cylinder ilkelini kullanır. To kod örneği aşağıda bir Cylinder ağa dönüştürür.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertCylinderPrimitivetoMesh-ConvertCylinderPrimitivetoMesh.py" >}}
### **Convert a 'Torus' to 'eshesh'**
A torus, daire ile bir eksen koplanar hakkında üç boyutlu bir alanda bir daire döndürerek oluşan bir devrim yüzeyidir. If devrimin ekseni çembere dokunmaz, yüzeyin halka şekli vardır ve devrim torusuna denir. Let, bir örgü oluşturmak için Torus ilkelini kullanıyor. The kod örneği aşağıda bir Torus'u ağa dönüştürür.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertTorusPrimitivetoMesh-ConvertTorusPrimitivetoMesh.py" >}}
