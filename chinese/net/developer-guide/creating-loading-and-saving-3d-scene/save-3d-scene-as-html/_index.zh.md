---
title: 在 C# 中将 3D 场景另存为 HTML
linktitle: 将 3D 场景另存为 HTML
type: docs
weight: 90
url: /zh/net/save-3d-scene-as-html/
---
##  **概述**

本文介绍了如何使用 C# 在 [将它们加载到场景对象中](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/) 之后将 3D 文件转换为 HTML，并涵盖了广泛的主题 (考虑 [支持的文件格式](https://docs.aspose.com/3d/net/supported-file-formats/))。

- 使用 C# 将 3DS 转换为 HTML
- 在 C# 中将 FBX 转换为 HTML
- 在 C# 中将 STL 转换为 HTML
- 在 C# 中将 U3D 转换为 HTML
- 在 C# 中将 OBJ 转换为 HTML


{{% alert color="primary" %}} 

19.9或更高版本支持此功能。

{{% /alert %}} 
##  **将 3D 场景另存为 HTML**
Aspose。3D for .NET 提供 `Html5SaveOptions` 类将 3D 场景另存为 HTML。将场景导出到 HTML5 文件时，API 将导出三个文件: 一个 `HTML` 文件、一个 Aspose 3dweb文件 (*.* a3dw **) 和一个渲染的 `JavaScript` 文件。为了只导出a3dw文件，您可以指定 Aspose 3dweb作为导出类型，并在您自己的 HTML 页面中重用JavaScript文件。下面的 C# 代码片段显示了如何将 3D 场景保存为 HTML。



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-HtmlSaveOption.cs" >}}

{{% alert color="primary" %}} 

由于浏览器的安全限制，导出的 HTML 文件不能直接打开，您需要通过web服务器打开它，如果您安装了python3，您可以在导出目录中的命令行中启动web服务器

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

然后打开它<http://localhost:8000/test.html>。web渲染器使用WebGL2，您可以使用<https://get.webgl.org/webgl2/>检查您的浏览器是否支持它。


