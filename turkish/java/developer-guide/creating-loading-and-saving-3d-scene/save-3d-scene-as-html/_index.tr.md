---
title: Save 3D Scene as HTML
type: docs
weight: 70
url: /tr/java/save-3d-scene-as-html/
description: Aspose.3D for Java ** htmlsaveoptions ** 3D sahneyi HTML olarak kaydetmek için sınıf sağlar.
---
{{% alert color="primary" %}} 

This özelliği 19.9 veya daha büyük sürümle desteklenir.

{{% /alert %}} 
#  **Save 3D Scene as HTML**
Aspose.3D for Java provides `HtmlSaveOptions` class to save a save 3D scene as HTML. When you export the scene into HTML5 file, API will export three files, an `HTML` file, an Aspose3DWeb file(*.*a3dw**), and a rendered `JavaScript` file. In order to export a3dw file only, you can specify Aspose3DWeb as the export type, and reuse the JavaScript file within your own HTML page. The following code snippet shows how to save a 3D scene as HTML. 



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

Due to the browser's security limits, the exported HTML file cannot be opened directly, you need to open it through a web server, if you have python3 installed, you can start the web-server in the command line in the exported directory

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Then aç<http://localhost:8000/test.html>. The web renderer WebGL2 kullanır, kullanabilirsiniz<https://get.webgl.org/webgl2/>Tarayıcınızın destekleyip desteklemediğini kontrol etmek için.


