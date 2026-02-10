---
title: Enregistrer 3D Scène sous HTML dans C#
linktitle: Enregistrer 3D Scène en HTML
type: docs
weight: 90
url: /fr/net/save-3d-scene-as-html/
---
##  **Aperçu**

Cet article explique comment convertir des fichiers 3D en HTML après [Les charger dans l'objet Scène](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/) en utilisant C# et couvre un large éventail de sujets (en considérant [Formats de fichiers pris en charge](https://docs.aspose.com/3d/net/supported-file-formats/)) par ex.

- Convertir 3DS en HTML en utilisant C#
- Convertir FBX en HTML en C#
- Convertir STL en HTML en C#
- Convertir U3D en HTML en C#
- Convertir OBJ en HTML en C#


{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.9 ou supérieure.

{{% /alert %}} 
##  **Enregistrer 3D Scène en HTML**
Aspose.3D for .NET fournit la classe `Html5SaveOptions` pour enregistrer une scène 3D en HTML. Lorsque vous exportez la scène dans un fichier HTML5, API exportera trois fichiers, un fichier `HTML`, un fichier Aspose3DWeb (*.* a3dw **) et un fichier rendu `JavaScript`. Pour exporter uniquement le fichier a3dw, vous pouvez spécifier Aspose3DWeb comme type d'exportation et réutiliser le fichier JavaScript dans votre propre page HTML. L'extrait de code C# suivant montre comment enregistrer une scène 3D en HTML.



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

En raison des limites de sécurité du navigateur, le fichier HTML exporté ne peut pas être ouvert directement, vous devez l'ouvrir via un serveur Web, si vous avez installé python3, vous pouvez démarrer le serveur Web dans la ligne de commande dans le répertoire exporté

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Puis ouvrez-le<http://localhost:8000/test.html>. Le moteur de rendu Web utilise WebGL2, vous pouvez utiliser<https://get.webgl.org/webgl2/>Pour vérifier si votre navigateur le supporte ou non.


