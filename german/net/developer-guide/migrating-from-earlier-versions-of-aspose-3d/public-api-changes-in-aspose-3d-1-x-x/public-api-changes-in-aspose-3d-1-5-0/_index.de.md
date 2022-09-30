---
title: Öffentliche API Änderungen in Aspose.3D 1.5.0
type: docs
weight: 20
url: /de/net/public-api-changes-in-aspose-3d-1-5-0/
---
**Inhalts übersicht**

- [Konvertieren Sie das Primitive in ein Netz und erstellen Sie eine Szene aus primitiven 3D-Modellen](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [Konvertieren Sie ein Mesh in Triangle Mesh mit benutzer definiertem Speicher layout des Vertex](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [Geteiltes Netz](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [Entfernung des Distreet3DS-Formats.](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [Fügt das Format Discreet3DS hinzu.](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [Fügt die Eigenschaft FlipCoordinate System in der Klasse Aspose.ThreeD hinzu. Formate. Universal3DConfig](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.3D API von Version 1.4.0 bis 1.5.0, die für Modul-/Anwendungs entwickler von Interesse sein können. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung etwaiger Änderungen im Verhalten hinter den Kulissen in Aspose.3D.

{{% /alert %}} 
### **Konvertieren Sie das Primitive in ein Netz und erstellen Sie eine Szene aus primitiven 3D-Modellen**
**Verschiedene Klassen, Methoden und Eigenschaften werden hinzugefügt**

- **Fügt Schnitts telle Aspose.ThreeD.Entities.IMesh Convertible hinzu.** 
-Jede Klasse, die diese Schnitts telle implementiert, kann beim Exportieren in beliebige 3D-Dateiformate in Mesh konvertiert werden.
- **Fügt Klasse Aspose.ThreeD. Entitäten hinzu. Primitiv.** 
-Es leitet sich aus der Entität klasse und auch der Basis klasse für alle primitiven Klassen ab.
- **Fügt Klasse Aspose.ThreeD. Entitäten. Box/Zylinder/Flugzeug/Kugel/Torus hinzu.** 
-Diese können verwendet werden, um Szene mit einfachen Grundelementen zu definieren. Entwickler können sie auch automatisch in Mesh konvertieren.

Zu den Primitiven gehören viele der grundlegend sten und am häufigsten verwendeten Objekte wie Box, Kugel, Ebene, Zylinder und Torus. Entwickler können sie auch zu Änderungs zwecken in Mesh konvertieren. Diese Hilfe themen veranschaulichen, wie dies zu tun ist:[Konvertieren Sie das Primitive in ein Netz](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models)Und[Konvertieren Sie das Primitive in ein Netz](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
### **Konvertieren Sie ein Mesh in Triangle Mesh mit benutzer definiertem Speicher layout des Vertex**
**Verschiedene Klassen, Methoden und Eigenschaften werden hinzugefügt**

- **Fügt Klasse Aspose.ThreeD. Entitäten. TriMesh/TriMesh<T> hinzu** 
-TriMesh/TriMesh<T>Enthält die Definition für dreieck basierte Meshes mit benutzer definiertem Speicher layout. Dies ist nützlich, wenn der Entwickler die Szene in ihre eigenen proprietären Dateiformate oder beim Rendern konvertieren muss.
- **Fügt Struktur Aspose.ThreeD.Utilities.FVector2/FVector3/FVector4 hinzu** 
-Diese Klassen präsentieren Vektor komponenten im Float. Nur wenige moderne GPU unterstützt Vektor-und Single-Precision-Float-Typen mit doppelter Genauigkeit, die in der Echtzeit-Rendering-Welt beliebter sind. Diese Ersetzungen existieren zusammen mit dem ursprünglichen Vector2/Vector3/Vector4, da sie in Aspose.3D unterschied liche Rollen spielen. Doppelte Präzision wird haupt sächlich zum Speichern von Modelldaten verwendet, da weniger Fehler angesammelt wurden. Single-Precision wird haupt sächlich beim Rendern oder beim Konvertieren von proprietären Dateiformaten des Benutzers verwendet, da es eine bessere Akzeptanz und Leistung aufweist. Wir haben diesen Satz von Vektoren in Aspose.3D 1.5 eingeführt, da wir Unterstützung für das benutzer definierte Scheitel punkt layout hinzugefügt haben, bei dem die Float-Vektoren häufig verwendet werden.
- **Fügt die Attribut klasse Aspose.ThreeD hinzu. Utilities.Semantic Attribute** 
-Der Entwickler kann die benutzer definierte Struktur für den Scheitel punkt definieren und dieses Attribut verwenden, um die Semantik der Felder zu markieren.
- **Fügt Klasse Aspose.ThreeD.Utilities.Vertex Declaration hinzu** 
-Es beschreibt das Speicher layout des Scheitel punkts.
- **Fügt enum Aspose.ThreeD.Utilities.VertexFieldDataType/Vertex Field Semantic hinzu** 
-Diese Enum-Typen versehen den Datentyp bzw. die Semantik des Scheitel punkt feldes.
- **Fügt die Klasse Aspose.ThreeD hinzu. Dienst programme. Vertex Field** 
-Es beschreibt jedes Feld im benutzer definierten Speicher layout von Vertex.
- **Fügt Klasse Aspose.ThreeD.Utilities.Vertex hinzu** 
-Es kann verwendet werden, um auf den rohen Scheitel punkt in TriMesh/TriMesh zuzugreifen<T>

Entwickler können jedes Mesh-Objekt mit dem benutzer definierten Speicher layout des Scheitel punkts in das Dreiecks netz konvertieren. Die Grafik software pakete und Hardware geräte arbeiten effizienter auf Dreiecken. Dieses Hilfe thema ver anschaulicht, wie dies zu tun ist:[Konvertieren Sie ein Mesh in Triangle Mesh mit benutzer definiertem Speicher layout des Vertex](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
### **Geteiltes Netz**
**Verschiedene Klassen, Methoden und Eigenschaften werden hinzugefügt**

- **Fügt enum Aspose.ThreeD. Entitäten. SplitMesh Policy hinzu** 
-Es gibt die Daten richtlinie an, die im Mesh-Splitting-Algorithmus verwendet wird. Wir unterstützen zwei Richtlinien, teilen Daten zwischen Sub-Meshes oder jedes Sub-Mesh hat seine eigenen Daten (Nur verwendete Daten).
- **Fügt Aspose.ThreeD. Entitäten 3 SplitMesh-Methoden hinzu. PolygonModifier-Klasse** 
1. Teilen Sie Meshes auf einem angegebenen Knoten nach Material definition in Unter netze auf.
1. Teilen Sie das gesamte Netz in der gegebenen Szene nach Material definition in Unter netze auf.
1. Teilen Sie das angegebene Netz nach Material definition in Unter netze auf.
- **Fügt die Eigenschaft FlipCoordinate System in der Klasse Aspose.ThreeD hinzu. Formate. Universal3DConfig** 
-Benutzer können das Koordinaten system von U3D während des Imports oder Exports umdrehen.

Entwickler müssen möglicher weise ein Netz automatisch nach Material teilen, sodass für jedes Netz nur ein Material oder ein geteiltes Netz verwendet wird, indem das Material angegeben wird. Diese Hilfe themen veranschaulichen, wie dies zu tun ist:[Teilen Sie ein Netz, indem Sie das Material angeben](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial)Und[Alle Maschen einer Szene pro Material aufteilen](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
### **Entfernung des Distreet3DS-Formats.**
Das Distreet3DS-Format ist aufgrund des falschen Zaubers als veraltet markiert.
### **Fügt das Format Discreet3DS hinzu.**
Das Format Discreet3DS wurde eingeführt.
### **Fügt die Eigenschaft FlipCoordinate System in der Klasse Aspose.ThreeD hinzu. Formate. Universal3DConfig**
Benutzer können das Koordinaten system von U3D während des Imports oder Exports umdrehen.
