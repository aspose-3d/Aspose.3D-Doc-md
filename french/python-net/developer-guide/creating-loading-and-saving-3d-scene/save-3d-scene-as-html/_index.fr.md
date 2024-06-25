---
title: Enregistrer 3D Scène en HTML
type: docs
weight: 90
url: /fr/python-net/save-3d-scene-as-html/
---
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.9 ou supérieure.

{{% /alert %}} 
#  **Enregistrer 3D Scène en HTML**
Aspose.3D for Python via .NET fournit la classe `Html5SaveOptions` pour enregistrer une scène 3D en tant que HTML. Lorsque vous exportez la scène dans le fichier HTML5, API exportera trois fichiers, un fichier `HTML`, un fichier Aspose3DWeb (*.* a3dw **) et un fichier rendu `JavaScript`. Pour exporter uniquement le fichier a3dw, vous pouvez spécifier Aspose3DWeb comme type d'exportation et réutiliser le fichier JavaScript dans votre propre page HTML. L'extrait de code suivant montre comment enregistrer une scène 3D en HTML.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-HtmlSaveOption.py" >}}

{{% alert color="primary" %}} 

En raison des limites de sécurité du navigateur, le fichier HTML exporté ne peut pas être ouvert directement, vous devez l'ouvrir via un serveur Web, si vous avez installé python3, vous pouvez démarrer le serveur Web dans la ligne de commande dans le répertoire exporté

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Puis ouvrez-le<http://localhost:8000/test.html>. Le moteur de rendu Web utilise WebGL2, vous pouvez utiliser<https://get.webgl.org/webgl2/>Pour vérifier si votre navigateur le supporte ou non.


