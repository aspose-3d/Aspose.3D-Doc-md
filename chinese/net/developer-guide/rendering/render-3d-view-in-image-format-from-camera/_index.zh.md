---
title: 从相机以图像格式呈现3D视图
type: docs
weight: 50
url: /zh/net/render-3d-view-in-image-format-from-camera/
description: 使用Aspose.3D for .NET，开发人员可以渲染图像以查看具有或不具有增强背景，纹理，阴影的3D模型的逼真图像，并且还可以调整图像大小。
---
{{% alert color="primary" %}}

使用[Aspose.3D for .NET](https://products.aspose.com/3d/net/),开发人员可以渲染图像以查看3D模型的逼真图像，无论是否具有增强的背景，纹理，阴影，还可以调整图像大小。

{{% /alert %}}
## **从相机拍摄3D模型的照片**
[`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)类公开的`Render`方法可用于从活动相机拍摄照片。开发人员还可以使用几种不同的方式在场景中导航和定位相机。在这个代码示例中，我们在现有3D场景中的位置 (10,10，10) 创建一个摄像机，并查看用于渲染的原点。
### **编程示例**
此代码示例在3D场景中创建摄像机，设置其目标并渲染图像。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Rendering-Render3DModelImageFromCamera-Render3DModelImageFromCamera.cs" >}}
