---
title: Aspose.3D for Java 18.8 - August 2018
type: docs
weight: 50
url: /de/java/aspose-3d-for-java-18-8-august-2018/
---
{{% alert color="primary" %}} 

Diese Seite enthält Versions hinweise für[Aspose.3D for Java 18.8](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.8/).

{{% /alert %}} 
## **Andere Verbesserungen und Änderungen**

|**Zusammenfassung**|**Kategorie**|
|:- |:- |
|Exportieren Sie glTF-Dateien mit Draco-Kompression|Neues Feature|
|Speicher verbrauch für Mesh-Indizes optimieren|Verbesserung|
|Verwenden Sie Aspose.3D mit Unity3D|Fehler|
|Lesen Sie COLLADA-Dateien, die im selben Ordner verweisen|Fehler|

## **Öffentliche API und rückwärts inkompatible Änderungen**

Bitte lesen Sie die Liste aller an der Öffentlichkeit vorgenommenen Änderungen API, z. B. hinzugefügte, umbenannte, entfernte oder veraltete Mitglieder sowie nicht abwärts kompatible Änderungen an Aspose.3D for Java API. Wenn Sie Bedenken hinsichtlich einer aufgeführten Änderung haben, geben Sie diese bitte auf der[Aspose.3D Unterstützung forum](https://forum.aspose.com/c/3d).

## **API ändert sich:**

**Ein neuer Getter/Setter wurde zu class com. apose. threed.GLTF SaveOptions hinzugefügt:**

{{< highlight "java" >}}

         public bool getDracoCompression();

        public void setDracoCompression(boolean value);

{{< /highlight >}}

Der Standardwert ist wahr. Wenn dies durch Einstellung auf true aktiviert wird, codiert der Exporteur glTF 2.0 das Mesh im Format Google Draco.
