---
title: Spara 3D Scene som HTML i C#
linktitle: Spara 3D Scene som HTML
type: docs
weight: 90
url: /sv/net/save-3d-scene-as-html/
---
##  **Översikt**

Den här artikeln förklarar hur du kan konvertera 3D-filer till HTML efter [Lasta in dem i sceneobjekt](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/) med C# och omfattar ett brett sortiment av ämnen (beakta [Stödda filformat](https://docs.aspose.com/3d/net/supported-file-formats/)) e. g.

- Konvertera 3DS till HTML med hjälp av C#
- Konvertera FBX till HTML i C#
- Konvertera STL till HTML i C#
- Konvertera U3D till HTML i C#
- Konvertera OBJ till HTML i C#


{{% alert color="primary" %}} 

Denna funktion stöds av version 19.9 eller större.

{{% /alert %}} 
##  **Spara 3D Scene som HTML**
Aspose.3D for .NET tillhandahåller klass `Html5SaveOptions` för att spara en 3D scen som HTML. När du exporterar scenen till filen HTML5, exporterar API tre filer, en `HTML` fil, en Aspose 3DWeb- fil(*. * a3dw**), och en uppvisad `JavaScript` fil. För att bara exportera a3dw-fil kan du ange Aspose 3DWeb som exporttyp, och återanvänd JavaScript-filen inom din egen HTML sida. Följande C# kodsnippet visar hur man sparar en 3D scen som HTML.



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

På grund av webbläsarens säkerhetsgränser kan den exporterade HTML-filen inte öppnas direkt. du måste öppna den via en webbserver, om du har python3 installerad, kan du starta webbservern i kommandoraden i den exporterade katalogen

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Öppna den då.<http://localhost:8000/test.html>. Webbens återgivning använder WebGL2, som du kan använda.<https://get.webgl.org/webgl2/>För att kontrollera om din webbläsare stöder det eller inte.


