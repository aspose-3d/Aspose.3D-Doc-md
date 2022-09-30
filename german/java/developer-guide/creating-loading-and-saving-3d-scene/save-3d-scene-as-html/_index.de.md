---
title: Sparen Sie 3D Szene als HTML
type: docs
weight: 70
url: /de/java/save-3d-scene-as-html/
description: Aspose.3D for Java bietet ** HtmlSave Options **-Klasse, um eine Save 3D-Szene als HTML zu speichern.
---
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.9 oder höher unterstützt.

{{% /alert %}} 
# **Sparen Sie 3D Szene als HTML**
Aspose.3D for Java bietet `HtmlSaveOptions` Klasse, um eine Save 3D Szene als HTML zu speichern. Wenn Sie die Szene in die Datei HTML5 exportieren, exportiert API drei Dateien, eine Datei `HTML`, eine Datei Aspose3DWeb (*.**A3dw**) Und eine gerenderte 'JavaScript'-Datei. Um nur a3dw-Datei zu exportieren, können Sie Aspose3DWeb als Export typ angeben und die JavaScript-Datei auf Ihrer eigenen HTML-Seite wieder verwenden. Das folgende Code-Snippet zeigt, wie Sie eine 3D-Szene als HTML speichern.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-html5SaveOption.java" >}}

{{% alert color="primary" %}} 

Aufgrund der Sicherheits grenzen des Browsers kann die exportierte Datei HTML nicht direkt geöffnet werden. Sie müssen sie über einen Webserver öffnen. Wenn Sie python3 installiert haben, können Sie den Webserver in der Befehlszeile im exportierten Verzeichnis starten

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Dann öffnen Sie es<http://localhost:8000/test.html>. Der Web-Renderer nutzt WebGL2, Sie können<https://get.webgl.org/webgl2/>Um zu überprüfen, ob Ihr Browser es unterstützt oder nicht.


