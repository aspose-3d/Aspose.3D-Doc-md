---
title: Sparen Sie 3D Szene als HTML in C#
linktitle: Sparen Sie 3D Szene als HTML
type: docs
weight: 90
url: /de/net/save-3d-scene-as-html/
---
##  **Übersicht**

Dieser Artikel erklärt, wie Sie 3D-Dateien nach [Laden sie in Szene Objekt](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/) mit C# in HTML konvertieren können, und deckt eine breite Palette von Themen ab (unter Berücksichtigung von [Unterstützte Dateiformate](https://docs.aspose.com/3d/net/supported-file-formats/)), z.

- Konvertieren Sie 3DS in HTML mit C#
- FBX zu HTML in C# umrechnen
- STL zu HTML in C# umrechnen
- U3D zu HTML in C# umrechnen
- OBJ zu HTML in C# umrechnen


{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.9 oder höher unterstützt.

{{% /alert %}} 
##  **Sparen Sie 3D Szene als HTML**
Aspose.3D for .NET bietet `Html5SaveOptions` Klasse, um eine Spar-3D-Szene als HTML zu sparen. Wenn Sie die Szene in HTML5-Datei exportieren, exportieren API drei Dateien, eine `HTML`-Datei, eine Aspose3DWeb-Datei (*.* a3dw **) und eine gerenderte `JavaScript`-Datei. Um nur a3dw-Datei zu exportieren, können Sie Aspose3DWeb als Export typ angeben und die JavaScript-Datei innerhalb Ihrer eigenen HTML-Seite wieder verwenden. Das folgende C#-Code-Snippet zeigt, wie Sie eine 3D-Szene als HTML speichern.



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

Aufgrund der Sicherheits grenzen des Browsers kann die exportierte HTML-Datei nicht direkt geöffnet werden. Sie müssen sie über einen Webserver öffnen. Wenn Sie python3 installiert haben, können Sie den Webserver in der Befehlszeile im exportierten Verzeichnis starten

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Dann öffnen Sie es<http://localhost:8000/test.html>. Der Web-Renderer nutzt WebGL2, Sie können<https://get.webgl.org/webgl2/>Um zu überprüfen, ob Ihr Browser es unterstützt oder nicht.


