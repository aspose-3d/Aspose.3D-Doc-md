---
title: Save 3D Scene as HTML
type: docs
weight: 90
url: /net/save-3d-scene-as-html/
---

{{% alert color="primary" %}} 

This feature is supported by version 19.9 or greater.

{{% /alert %}} 
# **Save 3D Scene as HTML**
Aspose.3D for .NET provides **HTMLSaveOptions** class to save a save 3D scene as HTML. When you export the scene into HTML5 file, API will export three files, an **HTML** file, an Aspose3DWeb file(*.**a3dw**), and a rendered **JavaScript** file. In order to export a3dw file only, you can specify Aspose3DWeb as the export type, and reuse the JavaScript file within your own HTML page. The following code snippet shows how to save a 3D scene as HTML. 



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-HtmlSaveOption.cs" >}}

{{% alert color="primary" %}} 

Due to the browser's security limits, the exported HTML file cannot be opened directly, you need to open it through a web server, if you have python3 installed, you can start the web server in the command line in the exported directory

{{% /alert %}} 

{{< highlight java >}}

 python3 -m http.server

{{< /highlight >}}

Then open it <http://localhost:8000/test.html>. The web renderer uses WebGL2, you can use <https://get.webgl.org/webgl2/> to check if your browser supports it or not.


