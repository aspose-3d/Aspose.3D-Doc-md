---
title: 将 3D 场景另存为 HTML
type: docs
weight: 70
url: /zh/java/save-3d-scene-as-html/
description: Aspose.3D for Java 提供 ** HtmlSaveOptions ** 类，用于将 3D 场景另存为 HTML。
---
{{% alert color="primary" %}} 

19.9或更高版本支持此功能。

{{% /alert %}} 
#  **将 3D 场景另存为 HTML**
Aspose。3D for Java 提供 `HtmlSaveOptions` 类将 3D 场景另存为 HTML。将场景导出到 HTML5 文件时，API 将导出三个文件: 一个 `HTML` 文件、一个 Aspose 3dweb文件 (*.* a3dw **) 和一个渲染的 `JavaScript` 文件。为了只导出a3dw文件，您可以指定 Aspose 3dweb作为导出类型，并在您自己的 HTML 页面中重用JavaScript文件。下面的代码片段显示了如何将 3D 场景保存为 HTML。



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Initialize a scene
Scene scene = new Scene();
// Initialize a node
Node node = scene.getRootNode().createChildNode(new Cylinder());
// Set child node properites
LambertMaterial mat = new LambertMaterial();
mat.setDiffuseColor(new Vector3(0.34,0.59, 0.41));
node.setMaterial(mat);
Light light = new Light();
light.setLightType(LightType.POINT);
scene.getRootNode().createChildNode(light).getTransform().setTranslation(10, 0, 10);
// Initialize HTML5SaveOptions
HTML5SaveOptions opt = new HTML5SaveOptions();
// Turn off the grid
opt.setShowGrid(false);
//Turn off the user interface
opt.setShowUI(false);
scene.save(RunExamples.getDataDir() + "html5SaveOption.html", FileFormat.HTML5);

{{< /highlight >}}

{{% alert color="primary" %}} 

由于浏览器的安全限制，导出的 HTML 文件不能直接打开，您需要通过web服务器打开它，如果您安装了python3，您可以在导出目录中的命令行中启动web-server

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

然后打开它<http://localhost:8000/test.html>。web渲染器使用WebGL2，您可以使用<https://get.webgl.org/webgl2/>检查您的浏览器是否支持它。


