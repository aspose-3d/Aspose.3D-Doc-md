---
title: Sparen Sie 3D Szene als HTML
type: docs
weight: 70
url: /de/java/save-3d-scene-as-html/
description: Aspose.3D for Java bietet die ** HtmlSave Options **-Klasse, um eine Save 3D-Szene als HTML zu speichern.
---
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.9 oder höher unterstützt.

{{% /alert %}} 
#  **Sparen Sie 3D Szene als HTML**
Aspose.3D for Java bietet `HtmlSaveOptions` Klasse, um eine Spar-3D-Szene als HTML zu sparen. Wenn Sie die Szene in HTML5-Datei exportieren, exportieren API drei Dateien, eine `HTML`-Datei, eine Aspose3DWeb-Datei (*.* a3dw **) und eine gerenderte `JavaScript`-Datei. Um nur a3dw-Datei zu exportieren, können Sie Aspose3DWeb als Export typ angeben und die JavaScript-Datei innerhalb Ihrer eigenen HTML-Seite wieder verwenden. Das folgende Code-Snippet zeigt, wie Sie eine 3D-Szene als HTML speichern.



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

Aufgrund der Sicherheits grenzen des Browsers kann die exportierte HTML-Datei nicht direkt geöffnet werden. Sie müssen sie über einen Webserver öffnen. Wenn Sie python3 installiert haben, können Sie den Webserver in der Befehlszeile im exportierten Verzeichnis starten

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Dann öffnen Sie es<http://localhost:8000/test.html>. Der Web-Renderer nutzt WebGL2, Sie können<https://get.webgl.org/webgl2/>Um zu überprüfen, ob Ihr Browser es unterstützt oder nicht.


