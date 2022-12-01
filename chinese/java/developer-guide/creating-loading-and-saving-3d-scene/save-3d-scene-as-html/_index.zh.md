---
title: 将3D场景保存为HTML
type: docs
weight: 70
url: /zh/java/save-3d-scene-as-html/
description: Aspose.3D for Java提供 ** HtmlSaveOptions ** 类，将保存3D场景保存为HTML。
---
{{% alert color="primary" %}} 

19.9或更高版本支持此功能。

{{% /alert %}} 
# **将3D场景保存为HTML**
Aspose.3D for Java提供了`HtmlSaveOptions`类来将保存3D场景保存为HTML。当您将场景导出到HTML5文件时，API将导出三个文件，一个`HTML`文件，一个Aspose3DWeb文件 (*。**a3dw**)，以及一个渲染的 “javascript” 文件。为了仅导出a3dw文件，您可以指定Aspose3DWeb作为导出类型，并在您自己的HTML页面中重用JavaScript文件。下面的代码片段显示了如何将3D场景保存为HTML。



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-html5SaveOption.java" >}}

{{% alert color="primary" %}} 

由于浏览器的安全限制，导出的HTML文件不能直接打开，您需要通过网络服务器打开它，如果您安装了python3，您可以在导出目录中的命令行中启动网络服务器

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

然后打开它<http://localhost:8000/test.html>。web渲染器使用WebGL2，您可以使用<https://get.webgl.org/webgl2/>检查您的浏览器是否支持它。


