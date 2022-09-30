---
title: Save 3D Scène comme HTML
type: docs
weight: 90
url: /fr/python-net/save-3d-scene-as-html/
---
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.9 ou supérieure.

{{% /alert %}} 
# **Save 3D Scène comme HTML**
Aspose.3D pour Python via .NET fournit la classe `Html5SaveOptions` pour enregistrer une scène de sauvegarde 3D comme HTML. Lorsque vous exportez la scène dans le fichier HTML5, le API exportera trois fichiers, un fichier `HTML`, un fichier DWeb Aspose3(*.**A3dw**), Et un fichier «JavaScript» rendu. Afin d'exporter le fichier a3dw seulement, vous pouvez spécifier Aspose3DWeb comme type d'exportation, et réutiliser le fichier JavaScript dans votre propre page HTML. L'extrait de code suivant montre comment enregistrer une scène 3D comme HTML.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-HtmlSaveOption.py" >}}

{{% alert color="primary" %}} 

En raison des limites de sécurité du navigateur, le fichier HTML exporté ne peut pas être ouvert directement, vous devez l'ouvrir via un serveur Web, si vous avez python3 installé, vous pouvez démarrer le serveur Web dans la ligne de commande dans le répertoire exporté

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Puis ouvrez-le<http://localhost:8000/test.html>. Le moteur de rendu Web utilise WebGL2, vous pouvez utiliser<https://get.webgl.org/webgl2/>Pour vérifier si votre navigateur le supporte ou non.


