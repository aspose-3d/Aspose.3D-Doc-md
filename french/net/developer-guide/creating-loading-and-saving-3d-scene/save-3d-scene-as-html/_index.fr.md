---
title: Économisez 3D Scène comme HTML au C#
linktitle: Save 3D Scène comme HTML
type: docs
weight: 90
url: /fr/net/save-3d-scene-as-html/
---
## **Aperçu**

Cet article explique comment vous pouvez convertir les fichiers 3D en HTML après[Les charger dans l'objet Scène](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/)En utilisant C# et couvre un large éventail de sujets (en considérant[Formats de fichiers pris en charge](https://docs.aspose.com/3d/net/supported-file-formats/)) Par ex.

- Convertissez 3DS en HTML en utilisant C#
- Convertissez FBX en HTML
- Convertissez STL en HTML
- Convertissez U3D en HTML
- Convertissez OBJ en HTML


{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.9 ou supérieure.

{{% /alert %}} 
## **Save 3D Scène comme HTML**
Aspose.3D for .NET fournit la classe `Html5SaveOptions` pour enregistrer une scène de sauvegarde 3D comme HTML. Lorsque vous exportez la scène dans le fichier HTML5, le API exportera trois fichiers, un fichier `HTML`, un fichier DWeb Aspose3(*.**A3dw**), Et un fichier «JavaScript» rendu. Afin d'exporter le fichier a3dw seulement, vous pouvez spécifier Aspose3DWeb comme type d'exportation, et réutiliser le fichier JavaScript dans votre propre page HTML. L'extrait de code C# suivant montre comment enregistrer une scène 3D comme HTML.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-HtmlSaveOption.cs" >}}

{{% alert color="primary" %}} 

En raison des limites de sécurité du navigateur, le fichier HTML exporté ne peut pas être ouvert directement, vous devez l'ouvrir via un serveur Web, si vous avez python3 installé, vous pouvez démarrer le serveur Web dans la ligne de commande dans le répertoire exporté

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Puis ouvrez-le<http://localhost:8000/test.html>. Le moteur de rendu Web utilise WebGL2, vous pouvez utiliser<https://get.webgl.org/webgl2/>Pour vérifier si votre navigateur le supporte ou non.


