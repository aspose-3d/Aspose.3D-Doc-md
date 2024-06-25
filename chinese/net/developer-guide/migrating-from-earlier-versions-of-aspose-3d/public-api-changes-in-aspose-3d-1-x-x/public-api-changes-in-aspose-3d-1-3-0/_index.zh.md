---
title: Aspose.3D 1.3.0中的公共 API 更改
type: docs
weight: 40
url: /zh/net/public-api-changes-in-aspose-3d-1-3-0/
---
**内容摘要**

- [命名空间和类名更改](#PublicAPIChangesinAspose.3D1.3.0-Namespaceandclassnamechanges)
- [通过分配引用和映射模式创建顶点](#PublicAPIChangesinAspose.3D1.3.0-CreateVertexbyAssigningtheReferenceandMappingModes)
- [在FileFormat中添加了 Universal 3D 保存选项](#PublicAPIChangesinAspose.3D1.3.0-Universal3DSavingOptionisaddedintheFileFormat)
- [将原始内容嵌入到 FBX 的纹理](#PublicAPIChangesinAspose.3D1.3.0-EmbedRawContenttotheTextureofFBX)
- [分解方法在Matrix4类中添加](#PublicAPIChangesinAspose.3D1.3.0-DecomposemethodisaddedintheMatrix4class)
- [在Vector4类中添加了一个新的构造函数来接收Vector3对象参数](#PublicAPIChangesinAspose.3D1.3.0-AnewconstructorinVector4classisaddedtoreceiveaVector3objectparameter)

{{% alert color="primary" %}} 

本文档介绍了对 Aspose.3D API 从版本1.2.0到1.3.0的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.3D 中幕后行为的任何更改的描述。

{{% /alert %}} 
###  **命名空间和类名更改**
- 命名空间 Aspose.ThreeD.Animations更改为 Aspose.ThreeD.Animation
- 类 Aspose.ThreeD.Animations.Animation更改为 Aspose.ThreeD.Animation.AnimationNode
- 命名空间 Aspose.ThreeD.IO更改为 Aspose.ThreeD.Formats
- 命名空间 Aspose.ThreeD.Utils更改为 Aspose.ThreeD.Utilities
###  **通过分配引用和映射模式创建顶点**
开发人员可以通过在单行代码中分配引用和映射模式来创建顶点。示例代码:

{{% alert color="primary" %}} 

代码中正在使用Mesh类对象。我们可以 [创建一个网格类对象，如在那里叙述](/pages/createpage.action?spaceKey=3dnet&title=Create+a+3D+Cube+Mesh&linkCreation=true&fromPageId=19923253)。

{{% /alert %}} 

**C#**

{{< highlight "csharp" >}}

 // call overloaded CreateElement method of the Mesh object

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;

{{< /highlight >}}

###  **在FileFormat中添加了 Universal 3D 保存选项**
Universal 3D 格式选项已添加到FileFormat枚举中。示例代码:

**C#**

{{< highlight "csharp" >}}

 // save scene in the Universal3D format

scene.Save("C:\\temp\\Output.fbx", FileFormat.Universal3D);

{{< /highlight >}}

###  **将原始内容嵌入到 FBX 的纹理**
的<tt>内容</tt>属性已添加到<tt>纹理</tt>类将原始内容嵌入 FBX 文档的纹理中。示例代码:

**C#**

{{< highlight "csharp" >}}

 // initialize Texture class object

Texture texture = new Texture();

// set file name

texture.FileName = "embedded-texture.png";

// set binary content

texture.Content = File.ReadAllBytes("c:\\test.png");

{{< /highlight >}}

###  **分解方法在Matrix4类中添加**
它是用于分解仿射变换矩阵的数学效用函数。
###  **在Vector4类中添加了一个新的构造函数来接收Vector3对象参数**
基于vector3构造Vector4更容易。向量4的第四个值表示平面w，其默认值为1。
