---
title: Kamu API Aspose içinde değişir. 3D 1.3.0
type: docs
weight: 40
url: /tr/net/public-api-changes-in-aspose-3d-1-3-0/
---
**Contents Summary**

- [Namespace ve sınıf adı değişiklikleri](#PublicAPIChangesinAspose.3D1.3.0-Namespaceandclassnamechanges)
- [Ference reate Vertex ference eference ve pping apping des odes gning ssissitarafından](#PublicAPIChangesinAspose.3D1.3.0-CreateVertexbyAssigningtheReferenceandMappingModes)
- [Dosya biçiminde Universal 3D kaydetme seçeneği eklenir](#PublicAPIChangesinAspose.3D1.3.0-Universal3DSavingOptionisaddedintheFileFormat)
- [Ham içeriği FBX dokusuna yerleştirin](#PublicAPIChangesinAspose.3D1.3.0-EmbedRawContenttotheTextureofFBX)
- [Mecompose yöntemi Mx4 x4 sınıfında eklenir](#PublicAPIChangesinAspose.3D1.3.0-DecomposemethodisaddedintheMatrix4class)
- [Vector4 sınıfında yeni oluşturucu Vector3 nesne parametresi almak için eklenir](#PublicAPIChangesinAspose.3D1.3.0-AnewconstructorinVector4classisaddedtoreceiveaVector3objectparameter)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 1.2.0 to 1.3.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **Namespace ve sınıf adı değişiklikleri**
- Namespace Aspose.ThreeD.Animations changed to Aspose.ThreeD.Animation
- Class Aspose.ThreeD.Animations.Animation changed to Aspose.ThreeD.Animation.AnimationNode
- {Space Aspose. threed. io Aspose olarak değiştirildi. threed. formats
- {Space Aspose. threed. utils Aspose olarak değiştirildi. threed. yardımcı programlar
###  **Ference reate Vertex ference eference ve pping apping des odes gning ssissitarafından**
Developers, tek bir kod satırında ference eference ve Mapping modlarını atayarak vertex oluşturabilir. Example kodu:

{{% alert color="primary" %}} 

The Mesh class object is being used in the code. We can [create a Mesh class object as narrated there](/pages/createpage.action?spaceKey=3dnet&title=Create+a+3D+Cube+Mesh&linkCreation=true&fromPageId=19923253).

{{% /alert %}} 

**C#**

{{< highlight "csharp" >}}

 // call overloaded CreateElement method of the Mesh object

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;

{{< /highlight >}}

###  **Dosya biçiminde Universal 3D kaydetme seçeneği eklenir**
Dosya formatı enum'a Universal 3D biçim seçeneği eklendi. Örnek kod:

**C#**

{{< highlight "csharp" >}}

 // save scene in the Universal3D format

scene.Save("C:\\temp\\Output.fbx", FileFormat.Universal3D);

{{< /highlight >}}

###  **Ham içeriği FBX dokusuna yerleştirin**
The<tt>Content</tt>Özelliği eklendi<tt>Texture</tt> class to embed the raw content in the texture of FBX document. Example code:

**C#**

{{< highlight "csharp" >}}

 // initialize Texture class object

Texture texture = new Texture();

// set file name

texture.FileName = "embedded-texture.png";

// set binary content

texture.Content = File.ReadAllBytes("c:\\test.png");

{{< /highlight >}}

###  **Mecompose yöntemi Mx4 x4 sınıfında eklenir**
It, bir affine dönüşüm matrisini ayrıştırmak için kullanılan bir matematik yardımcı fonksiyonudur.
###  **Vector4 sınıfında yeni oluşturucu Vector3 nesne parametresi almak için eklenir**
It, Vector3'e göre Vector4 oluşturmayı kolaylaştırır. Vector4'ün dördüncü değeri, düzlemi w sunar ve varsayılan değeri 1'dir.
