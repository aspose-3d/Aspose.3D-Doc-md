---
title: Aspose.3D for Java 18.10-Oktober 2018
type: docs
weight: 30
url: /de/java/aspose-3d-for-java-18-10-october-2018/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versions hinweise für[Aspose.3D for Java 18.10](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.10/).

{{% /alert %}} 
## **Verbesserungen und Änderungen**


|**Zusammenfassung**|**Kategorie**|
|:- |:- |
|Unterstützung for .NET Core-Plattform|Neues Feature|
|Erlauben Sie dem Benutzer, die Kom primi erung zu deaktivieren, wenn Sie die Binär dateien FBX speichern|Neues Feature|
|Verbessern Sie die Import leistung FBX|Verbesserung|
|Verbessern Sie die binäre Schreib leistung FBX|Verbesserung|
|Import Exception beim Öffnen riesiger FBX-Dateien|Fehler|
|Problem mit UnitScaleFactor-Eigenschaft|Fehler|

## **Öffentliche API und rückwärts inkompatible Änderungen**

Bitte lesen Sie die Liste aller an der Öffentlichkeit vorgenommenen Änderungen API, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder sowie nicht abwärts kompatible Änderungen an Aspose.3D for Java API. Wenn Sie Bedenken hinsichtlich einer aufgeführten Änderung haben, geben Sie diese bitte auf der[Aspose.3D Unterstützung forum](https://forum.aspose.com/c/3d).

## **API ändert sich:**

**Mitglieder zur Klasse 'com. apose. threed.FBXSaveOptions' hinzugefügt:**

{{< highlight "java" >}}

     /**

     * Compression large binary data in the FBX file, default value is true.

     */

    public boolean com.aspose.threed.FBXSaveOptions.getEnableCompression();

    /**

     * Compression large binary data in the FBX file, default value is true.

     */

    public void com.aspose.threed.FBXSaveOptions.setEnableCompression(boolean val);

{{< /highlight >}}





**Beispiel code:**

{{< highlight "java" >}}

     Scene scene = new Scene("test.fbx");

    FBXSaveOptions opts = new FBXSaveOptions(FileFormat.FBX7500_BINARY);

    opts.setEnableCompression(false);

    scene.save("test.fbx", opts);

{{< /highlight >}}
