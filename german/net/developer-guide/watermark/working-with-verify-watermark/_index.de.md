---
title: Arbeiten mit Verifiziermarken
type: docs
weight: 170
url: /de/net/working-with-verify-watermark/
---

{{% alert color="primary" %}}

Mit der Aspose.3D für .NET API können Entwickler problemlos eine blinde Wasserzeichenverifizierung zu 3D-Dateien hinzufügen, während sie in jedem unterstützten Ausgabedateiformat speichern.

{{% /alert %}}
# **Eine 3D-Szene erstellen**
Zuerst müssen Sie eine 3D-Szene aus einer 3D-Datei erstellen. Der folgende Codeausschnitt zeigt, wie Sie diese Funktionalität verwenden:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithWatermark-Create3DScene.cs" >}}

# **Wasserzeichen decodieren**
Aspose.3D für .NET verwendet die Methode `DecodeWatermark`, um das Wasserzeichen für die 3D-Datei zu bestätigen, nachdem das Passwort eingegeben wurde. Der folgende Codeausschnitt zeigt, wie Sie diese Funktionalität verwenden:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithVerifyWatermark-DecodeWatermark.cs" >}}

# **Dokumentbestätigung**
Für das zurückgegebene Ergebnis bedeutet, wenn das zurückgegebene Ergebnis null ist, dass dem 3D-Dokument kein Wasserzeichen hinzugefügt wurde. Wenn es Textinformationen zurückgibt, handelt es sich um das Wasserzeichen der 3D-Datei. Wenn das Passwort falsch eingegeben wird, wird eine Fehlermeldung zurückgegeben.