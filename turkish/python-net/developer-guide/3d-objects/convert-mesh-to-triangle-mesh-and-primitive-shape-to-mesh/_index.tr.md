---
title: Tonvert Mesh to Triangle Mesh ve Mrimitive Shape to Mesh
type: docs
weight: 30
url: /tr/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for Python via .NET API, geliştiricilerin herhangi bir ağ nesnesini, vertex'in özel bellek düzeni ile üçgen ağa dönüştürmelerine izin verir. Vertex'in özel bellek düzeni, kod örneklerinde vertexdeclaration sınıfı tarafından yapısı veya dinamik olarak tanımlanır.
---
##  **Vonvert a Vesh to Triangle Mesh with uustom Vetex yout aaof the Vertex**
[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API allows developers to convert any mesh object to triangle mesh with custom memory layout of the vertex. The custom memory layout of the Vertex is defined using the Struct or dynamically by [`VertexDeclaration`](http://www.aspose.com/api/net/3d/aspose.threed.utilities/vertexdeclaration) class in the code examples.

{{% alert color="primary" %}}

Bu yardım konusu, kodu kapsamlı ve kısa tutmak için kutudan ve küreden kafesler oluşturur. Geliştiriciler, bu yardım konusu hakkında manuel olarak bir ağ oluşturabilirler: [3D küp mesh oluşturun](/3d/tr/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

These örnekleri nasıl olduğunu gösterir:

- [Convert a verphere to verriangle Mesh vertex özel bellek düzeni ile (Struct olarak tanımlanmıştır)](/3d/tr/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
- [Convert bir Box Triangle Mesh vertex özel bellek düzeni ile (Vertextexeclaration sınıfı tarafından tanımlanmıştır)](/3d/tr/python-net/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/).
###  **Convert Mesh**
Developers, örgüyü üçgen örgüye dönüştürebilir, çünkü herhangi bir karmaşık (yüzey) yapı bir grup üçgen olarak temsil edilebilir. The üçgen en atomik geometridir. Talmost neredeyse her şey için temel olarak kullanılır.
###  **Bir Triangle Mesh Access ces ertices**
Developers, hafızadaki dikeylerin birleştirilmeden önce Indices, gerçek dikenlere, dikeylere ve toplam bayt değerlerine erişebilir.

Below örneği, özel bellek düzeni ile üçgen ağa bir Sphere dönüştürür.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout-ConvertSphereMeshtoTriangleMeshCustomMemoryLayout.py" >}}




Below örneği, bir Box'u özel bellek düzeni ile üçgen ağa dönüştürür.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.py" >}}
##  **Convert 'Mrimitive' a 'Mesh'**
Using Aspose.3D for Python via .NET, developers can convert any primitive object to a mesh. Primitives include many of the most basic and most used objects like box, sphere, plane, cylinder, and torus.

{{% alert color="primary" %}}

Bir arayüz imeshconvertible uygulayan herhangi bir sınıf herhangi bir 3D dosya formatına ihracat yaparken ağa dönüştürülebilir.

{{% /alert %}}
###  **Convert a 'Sphere' to 'eshesh'**
A sphere, spor toplarından uzaydaki gezegenlere kadar her yerde görünen üç boyutlu alanda mükemmel bir yuvarlak geometrik nesnedir. Let, bir örgü oluşturmak için Sphere İlkel kullanıyor.
To kod örneği aşağıda bir Sphere örgü dönüştürür.

{{< highlight "python" >}}
from aspose.threed.entities import Sphere

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Sphere class
convertible = Sphere()
#  Convert a Sphere to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Convert a 'Box' to 'eshesh'**
A Box, içeriğin taşınması için genellikle depolama olarak veya geçici kullanım için kalıcı kullanım için çeşitli kaplar ve prizler açıklar. Let, bir örgü oluşturmak için Box İlkel kullanıyor. The kod örneği aşağıda bir Box ağa dönüştürür.

{{< highlight "python" >}}
from aspose.threed.entities import Box

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Box class
convertible = Box()
#  Convert a Box to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Convert a 'Plane' to 'eshesh'**
A plane kalınlığı olmadan sonsuz uzanır. An bir uçağın örneği bir koordinat düzlemidir. Lets bir örgü oluşturmak için Plane İlkel kullanın. The kod örneği aşağıda bir Plane'i ağa dönüştürür.

{{< highlight "python" >}}
from aspose.threed.entities import Plane

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Plane class
convertible = Plane()
#  Convert a Plane to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Convert a 'Cylinder' to 'Mesh'**
A silindir, en temel eğrisel geometrik şekillerden biridir, verilen düz bir çizgiden, silindirin ekseninden sabit bir mesafede noktalar tarafından oluşturulan yüzey. It birçok yerde, örneğin bir evin önünde veya bir araba tahrik mili olarak bir sütun olarak kullanılabilir. Lets, bir örgü oluşturmak için Cylinder ilkelini kullanır. To kod örneği aşağıda bir Cylinder ağa dönüştürür.

{{< highlight "python" >}}
from aspose.threed.entities import Cylinder

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Cylinder class
convertible = Cylinder()
#  Convert a Cylinder to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
###  **Convert a 'Torus' to 'eshesh'**
A torus, daire ile bir eksen koplanar hakkında üç boyutlu bir alanda bir daire döndürerek oluşan bir devrim yüzeyidir. If devrimin ekseni çembere dokunmaz, yüzeyin halka şekli vardır ve devrim torusuna denir. Let, bir örgü oluşturmak için Torus ilkelini kullanıyor. The kod örneği aşağıda bir Torus'u ağa dönüştürür.

{{< highlight "python" >}}
from aspose.threed.entities import Torus

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize object by Torus class
convertible = Torus()
#  Convert a Torus to Mesh
mesh = convertible.to_mesh()

{{< /highlight >}}
