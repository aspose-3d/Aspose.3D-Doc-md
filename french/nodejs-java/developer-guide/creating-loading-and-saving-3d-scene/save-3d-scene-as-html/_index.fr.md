---
title: Enregistrer 3D Scène en HTML
type: docs
weight: 70
url: /fr/nodejs-java/save-3d-scene-as-html/
description: Aspose.3D for Node.js via Java fournit la classe ** HtmlSaveOptions ** pour enregistrer une scène de sauvegarde 3D en HTML.
---
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.9 ou supérieure.

{{% /alert %}} 
#  **Enregistrer 3D Scène en HTML**
Aspose.3D for Node.js via Java fournit la classe `HtmlSaveOptions` pour enregistrer une scène 3D en tant que HTML. Lorsque vous exportez la scène dans le fichier HTML5, API exportera trois fichiers, un fichier `HTML`, un fichier Aspose3DWeb (*.* a3dw **) et un fichier rendu `JavaScript`. Pour exporter uniquement le fichier a3dw, vous pouvez spécifier Aspose3DWeb comme type d'exportation et réutiliser le fichier JavaScript dans votre propre page HTML. L'extrait de code suivant montre comment enregistrer une scène 3D en HTML.

{{< highlight "java" >}}

// Initialize a scene
var scene = new aspose.threed.Scene();

scene.getRootNode().createChildNode(new aspose.threed.Cylinder());

var opt =new aspose.threed.Html5SaveOptions();
// Turn off the grid
opt.setShowGrid(false);
//Turn off the user interface
opt.setShowUI(false);

scene.save("html5SaveOption.html);

{{< /highlight >}}


{{% alert color="primary" %}} 

En raison des limites de sécurité du navigateur, le fichier HTML exporté ne peut pas être ouvert directement, vous devez l'ouvrir via un serveur Web, si vous avez installé python3, vous pouvez démarrer le serveur Web dans la ligne de commande dans le répertoire exporté

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Puis ouvrez-le<http://localhost:8000/test.html>. Le moteur de rendu Web utilise WebGL2, vous pouvez utiliser<https://get.webgl.org/webgl2/>Pour vérifier si votre navigateur le supporte ou non.


