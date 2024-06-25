---
title: Tonvert Mesh to Triangle Mesh ve Mrimitive Shape to Mesh
type: docs
weight: 20
url: /tr/java/convert-mesh-to-triangle-mesh-and-primitive-shape-to-mesh/
description: Aspose.3D for Java API, vertex'in özel bellek düzeni ile üçgen örgüye örgü dönüştürmeyi desteklemektedir. Vertex'in özel bellek düzeni, kod örneklerinde vertexdeclaration sınıfı tarafından dinamik olarak tanımlanır.
---
##  **Vustom Metex yout aerof Vertex**
Aspose.3D for Java API, vertex'in özel bellek düzeni ile üçgen örgüye örgü dönüştürmeyi desteklemektedir. Vertex'in özel bellek düzeni, kod örneklerinde `VertexDeclaration` sınıfı ile dinamik olarak tanımlanır.

{{% alert color="primary" %}}

Bu yardım konusu, kodu kapsamlı ve kısa tutmak için kutudan ve küreden kafesler oluşturur. Geliştiriciler, bu yardım konusu hakkında manuel olarak bir ağ oluşturabilirler: [3D küp mesh oluştur](/3d/tr/java/create-3d-mesh-and-scene/).

{{% /alert %}}

Developers, örgüyü üçgen örgüye dönüştürebilir, çünkü herhangi bir karmaşık (yüzey) yapı bir grup üçgen olarak temsil edilebilir. The üçgen en atomik geometridir. Talmost neredeyse her şey için temel olarak kullanılır. Tkod örneği, bir Box'u özel bellek düzeni ile üçgen ağa dönüştürür.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertBoxMeshtoTriangleMeshCustomMemoryLayout.java" >}}
##  **Monvert Mrimitive Shape to Mesh**
Aspose.3D for Java API, herhangi bir ilkel şekli ağa dönüştürme desteğine sahiptir. İlkel şekiller, kutu, küre, uçak, silindir ve torus gibi en temel ve kullanılmış nesneleri içerir.

{{% alert color="primary" %}}

Bir arayüz imeshconvertible uygulayan herhangi bir sınıf herhangi bir 3D dosya formatına ihracat yaparken ağa dönüştürülebilir.

{{% /alert %}}
###  **Convert Sphere Mrimitive to Mesh**
A sphere, spor toplarından uzaydaki gezegenlere kadar her yerde görünen üç boyutlu alanda mükemmel bir yuvarlak geometrik nesnedir. Let, bir örgü oluşturmak için Sphere İlkel kullanıyor.
To kod örneği aşağıda bir Sphere örgü dönüştürür.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertSpherePrimitivetoMesh.java" >}}
###  **Monvert ox ox to Mesh**
A Box, içeriğin taşınması için genellikle depolama olarak veya geçici kullanım için kalıcı kullanım için çeşitli kaplar ve prizler açıklar. Let, bir örgü oluşturmak için Box İlkel kullanıyor. The kod örneği aşağıda bir Box ağa dönüştürür.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertBoxPrimitivetoMesh.java" >}}
###  **Monvert a Mlane to Mesh**
A plane kalınlığı olmadan sonsuz uzanır. An bir uçağın örneği bir koordinat düzlemidir. Lets bir örgü oluşturmak için Plane İlkel kullanın. The kod örneği aşağıda bir Plane'i ağa dönüştürür.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertPlanePrimitivetoMesh.java" >}}
###  **Monvert a Cylinder to Mesh**
A silindir, en temel eğrisel geometrik şekillerden biridir, verilen düz bir çizgiden, silindirin ekseninden sabit bir mesafede noktalar tarafından oluşturulan yüzey. It birçok yerde, örneğin bir evin önünde veya bir araba tahrik mili olarak bir sütun olarak kullanılabilir. Lets, bir örgü oluşturmak için Cylinder ilkelini kullanır. To kod örneği aşağıda bir Cylinder ağa dönüştürür.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertCylinderPrimitivetoMesh.java" >}}
###  **Monvert a Torus to Mesh**
A torus, daire ile bir eksen koplanar hakkında üç boyutlu bir alanda bir daire döndürerek oluşan bir devrim yüzeyidir. If devrimin ekseni çembere dokunmaz, yüzeyin halka şekli vardır ve devrim torusuna denir. Let, bir örgü oluşturmak için Torus ilkelini kullanıyor. The kod örneği aşağıda bir Torus'u ağa dönüştürür.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-ConvertTorusPrimitivetoMesh.java" >}}
