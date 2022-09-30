---
title: Public API Changes Aspose.3D 1.3.0
type: docs
weight: 40
url: /tr/net/public-api-changes-in-aspose-3d-1-3-0/
---
**Contents Summary**

- [Namespace ve sınıf adı değişiklikleri](#PublicAPIChangesinAspose.3D1.3.0-Namespaceandclassnamechanges)
- [Ference reate Vertex ference eference ve pping apping des odes gning ssissitarafından](#PublicAPIChangesinAspose.3D1.3.0-CreateVertexbyAssigningtheReferenceandMappingModes)
- [FileFormat'ta Universal 3D ving aving ption ption eklenir](#PublicAPIChangesinAspose.3D1.3.0-Universal3DSavingOptionisaddedintheFileFormat)
- [Eaw aw aw tent FBX Texture için ontent](#PublicAPIChangesinAspose.3D1.3.0-EmbedRawContenttotheTextureofFBX)
- [Mecompose yöntemi Mx4 x4 sınıfında eklenir](#PublicAPIChangesinAspose.3D1.3.0-DecomposemethodisaddedintheMatrix4class)
- [Vector4 sınıfında yeni oluşturucu Vector3 nesne parametresi almak için eklenir](#PublicAPIChangesinAspose.3D1.3.0-AnewconstructorinVector4classisaddedtoreceiveaVector3objectparameter)

{{% alert color="primary" %}} 

This belgesi, 1.2.0 sürümünden 1.3.0 sürümüne Aspose.3D API değişikliklerini açıklar, bu modül/uygulama geliştiricilerine ilgi gösterebilir. It sadece yeni ve güncellenmiş kamu yöntemlerini değil, aynı zamanda Aspose.3D 'deki sahnelerin arkasındaki davranıştaki herhangi bir değişikliğin açıklamasını da içerir.

{{% /alert %}} 
### **Namespace ve sınıf adı değişiklikleri**
- Namespace Aspose.ThreeD.Animations Aspose.ThreeD olarak değiştirildi. Animation
- C07Aspose.ThreeD. Ani.. Animation Aspose.ThreeD olarak değiştirildi. Animationoode
- Namespace Aspose.ThreeD.481 O Aspose.ThreeD olarak değiştirildi. Formats
- Namespace Aspose.ThreeD.Utils Aspose.ThreeD olarak değiştirildi. Utilities
### **Ference reate Vertex ference eference ve pping apping des odes gning ssissitarafından**
Developers, tek bir kod satırında ference eference ve Mapping modlarını atayarak vertex oluşturabilir. Example kodu:

{{% alert color="primary" %}} 

The Mesh sınıfı nesne kodda kullanılıyor. We can[Orada anlatılan Mesh sınıfı bir nesne oluşturun](/pages/createpage.action?spaceKey=3dnet&title=Create+a+3D+Cube+Mesh&linkCreation=true&fromPageId=19923253).

{{% /alert %}} 

**C#**

{{< highlight "csharp" >}}

 // call overloaded CreateElement method of the Mesh object

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;

{{< /highlight >}}

### **FileFormat'ta Universal 3D ving aving ption ption eklenir**
Fhe Universal 3D format seçeneği FileFormat enum'a eklendi. Example kodu:

**C#**

{{< highlight "csharp" >}}

 // save scene in the Universal3D format

scene.Save("C:\\temp\\Output.fbx", FileFormat.Universal3D);

{{< /highlight >}}

### **Eaw aw aw tent FBX Texture için ontent**
The<tt>Content</tt>Özelliği eklendi<tt>Texture</tt>Ham içeriği FBX belgesinin dokusuna yerleştirmek için sınıf. Example kodu:

**C#**

{{< highlight "csharp" >}}

 // initialize Texture class object

Texture texture = new Texture();

// set file name

texture.FileName = "embedded-texture.png";

// set binary content

texture.Content = File.ReadAllBytes("c:\\test.png");

{{< /highlight >}}

### **Mecompose yöntemi Mx4 x4 sınıfında eklenir**
It, bir affine dönüşüm matrisini ayrıştırmak için kullanılan bir matematik yardımcı fonksiyonudur.
### **Vector4 sınıfında yeni oluşturucu Vector3 nesne parametresi almak için eklenir**
It, Vector3'e göre Vector4 oluşturmayı kolaylaştırır. Vector4'ün dördüncü değeri, düzlemi w sunar ve varsayılan değeri 1'dir.
