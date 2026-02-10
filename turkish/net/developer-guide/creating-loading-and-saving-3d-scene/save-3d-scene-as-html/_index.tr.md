---
title: Save 3D Scene as HTML in C#
linktitle: Save 3D Scene as HTML
type: docs
weight: 90
url: /tr/net/save-3d-scene-as-html/
---
##  **Overview**

This article explains how you can convert 3D files to HTML after [loading them into Scene object](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/) using C# and covers wide range of topics (considering [supported file formats](https://docs.aspose.com/3d/net/supported-file-formats/)) e.g.

- Convert 3DS to HTML using C#
- Convert FBX to HTML in C#
- Convert STL to HTML in C#
- Convert U3D to HTML in C#
- Convert OBJ to HTML in C#


{{% alert color="primary" %}} 

This özelliği 19.9 veya daha büyük sürümle desteklenir.

{{% /alert %}} 
##  **Save 3D Scene as HTML**
Aspose.3D for .NET provides `Html5SaveOptions` class to save a save 3D scene as HTML. When you export the scene into HTML5 file, API will export three files, an `HTML` file, an Aspose3DWeb file(*.*a3dw**), and a rendered `JavaScript` file. In order to export a3dw file only, you can specify Aspose3DWeb as the export type, and reuse the JavaScript file within your own HTML page. The following C# code snippet shows how to save a 3D scene as HTML. 



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize 3D scene
var scene = new Scene();
// Create a child node
var node = scene.RootNode.CreateChildNode(new Cylinder());
// Set child node properites
node.Material = new LambertMaterial() { DiffuseColor = new Vector3(Color.Chartreuse) };
scene.RootNode.CreateChildNode(new Light() { LightType = LightType.Point }).Transform.Translation = new Vector3(10, 0, 10);
// Create a Html5SaveOptions
var opt = new Html5SaveOptions();
//Turn off the grid
opt.ShowGrid = false;
//Turn off the user interface
opt.ShowUI = false; 
// Save 3D to HTML5
scene.Save("HtmlSaveOption.html", opt);

{{< /highlight >}}

{{% alert color="primary" %}} 

Due to the browser's security limits, the exported HTML file cannot be opened directly, you need to open it through a web server, if you have python3 installed, you can start the web server in the command line in the exported directory

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Then aç<http://localhost:8000/test.html>. The web renderer WebGL2 kullanır, kullanabilirsiniz<https://get.webgl.org/webgl2/>Tarayıcınızın destekleyip desteklemediğini kontrol etmek için.


