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
- [Fügt das Discreet3DS-Format hinzu.](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [Fügt die Eigenschaft FlipCoordinate System in der Klasse Aspose hinzu. ThreeD. Formates. Universal3DConfig](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

Dieses Dokument beschreibt Änderungen an Aspose.3D API von Version 1.4.0 bis 1.5.0, die für Modul-/Anwendungs entwickler von Interesse sein können. Es enthält nicht nur neue und aktualisierte öffentliche Methoden, sondern auch eine Beschreibung aller Änderungen im Verhalten hinter den Kulissen in Aspose.3D.

{{% /alert %}} 
###  **Konvertieren Sie das Primitive in ein Netz und erstellen Sie eine Szene aus primitiven 3D-Modellen**
**Verschiedene Klassen, Methoden und Eigenschaften werden hinzugefügt**

- **Fügt die Schnitts telle Aspose hinzu. ThreeD.Entities.IMesh Convertible.** 
-Jede Klasse, die diese Schnitts telle implementiert, kann beim Exportieren in beliebige 3D-Dateiformate in Mesh konvertiert werden.
- **Fügt die Klasse Aspose hinzu. ThreeD.Entities.Primitive.** 
-Es leitet sich aus der Entität klasse und auch der Basis klasse für alle primitiven Klassen ab.
- **Fügt die Klasse Aspose hinzu. ThreeD.Entities.Box/Zylinder/Flugzeug/Kugel/Torus.** 
-Diese können verwendet werden, um Szene mit einfachen Grundelementen zu definieren. Entwickler können sie auch automatisch in Mesh konvertieren.

Zu den Primitiven gehören viele der grundlegend sten und am häufigsten verwendeten Objekte wie Box, Kugel, Ebene, Zylinder und Torus. Entwickler können sie auch zu Änderungs zwecken in Mesh konvertieren. Diese Hilfe themen veranschaulichen, wie das geht: [Konvertieren Sie das Primitive in ein Netz](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models) und [Konvertieren Sie das Primitive in ein Netz](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
###  **Konvertieren Sie ein Mesh in Triangle Mesh mit benutzer definiertem Speicher layout des Vertex**
**Verschiedene Klassen, Methoden und Eigenschaften werden hinzugefügt**

- **Fügt die Klasse Aspose hinzu. ThreeD.Entities.TriMesh/TriMesh<T>** 
-TriMesh/TriMesh<T>Enthält die Definition für dreieck basierte Meshes mit benutzer definiertem Speicher layout. Dies ist nützlich, wenn der Entwickler die Szene in ihre eigenen proprietären Dateiformate oder beim Rendern konvertieren muss.
- **Fügt Struktur Aspose hinzu. ThreeD.Utilities.FVector2/FVector3/FVector4** 
-Diese Klassen präsentieren Vektor komponenten im Float. Nur wenige moderne GPU unterstützt doppelt präzise Vektor-, Single-Precision-Float-Typen sind in der Echtzeit-Rendering-Welt beliebter. Diese Ersetzungen werden mit dem ursprünglichen Vector2/Vector3/Vector4 koexistieren, da sie unterschied liche Rollen in Aspose.3D spielen. Doppelte Präzision wird haupt sächlich zum Speichern von Modelldaten verwendet, da weniger Fehler angesammelt wurden. Single-Precision wird haupt sächlich beim Rendern oder beim Konvertieren von proprietären Dateiformaten des Benutzers verwendet, da es eine bessere Akzeptanz und Leistung aufweist. Wir haben diesen Satz von Vektoren in Aspose eingeführt. 3D 1.5, weil wir Unterstützung für das benutzer definierte Vertex-Layout hinzugefügt haben, bei dem die Float-Vektoren häufig verwendet werden.
- **Fügt die Attribut klasse Aspose hinzu. ThreeD.Utilities.Semantic Attribute** 
-Der Entwickler kann die benutzer definierte Struktur für den Scheitel punkt definieren und dieses Attribut verwenden, um die Semantik der Felder zu markieren.
- **Fügt die Klasse Aspose hinzu. ThreeD.Utilities.Vertex Declaration** 
-Es beschreibt das Speicher layout des Scheitel punkts.
- **Addiert enum Aspose.ThreeD.Utilities.VertexFieldDataType/VertexField Semantic** 
-Diese Enum-Typen versehen den Datentyp bzw. die Semantik des Scheitel punkt feldes.
- **Fügt die Klasse Aspose hinzu. ThreeD.Utilities.Vertex Field** 
-Es beschreibt jedes Feld im benutzer definierten Speicher layout von Vertex.
- **Fügt die Klasse Aspose hinzu. ThreeD.Utilities.Vertex** 
-Es kann verwendet werden, um auf den rohen Scheitel punkt in TriMesh/TriMesh zuzugreifen<T>

Entwickler können jedes Mesh-Objekt mit dem benutzer definierten Speicher layout des Scheitel punkts in das Dreiecks netz konvertieren. Die Grafik software pakete und Hardware geräte arbeiten effizienter auf Dreiecken. Dieses Hilfe thema zeigt, wie das geht: [Konvertieren Sie ein Mesh in Triangle Mesh mit benutzer definiertem Speicher layout des Vertex](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
###  **Geteiltes Netz**
**Verschiedene Klassen, Methoden und Eigenschaften werden hinzugefügt**

- **Addiert enum Aspose.ThreeD.Entities.Split Mesh Policy** 
-Es gibt die Daten richtlinie an, die im Mesh-Splitting-Algorithmus verwendet wird. Wir unterstützen zwei Richtlinien, teilen Daten zwischen Sub-Meshes oder jedes Sub-Mesh hat seine eigenen Daten (Nur verwendete Daten).
- **Fügt 3 SplitMesh-Methoden zu Aspose hinzu. ThreeD.Entities.Polygon Modifier klasse** 
1. Teilen Sie Meshes auf einem angegebenen Knoten nach Material definition in Unter netze auf.
1. Teilen Sie das gesamte Netz in der gegebenen Szene nach Material definition in Unter netze auf.
1. Teilen Sie das angegebene Netz nach Material definition in Unter netze auf.
- **Fügt die Eigenschaft FlipCoordinate System in der Klasse Aspose hinzu. ThreeD. Formates. Universal3DConfig** 
-Benutzer können das Koordinaten system von U3D während des Imports oder Exports umdrehen.

Entwickler müssen möglicher weise ein Netz automatisch nach Material teilen, sodass für jedes Netz nur ein Material oder ein geteiltes Netz verwendet wird, indem das Material angegeben wird. Diese Hilfe themen veranschaulichen, wie das geht: [Teilen Sie ein Netz, indem Sie das Material angeben](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial) und [Alle Maschen einer Szene pro Material aufteilen](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
###  **Entfernung des Distreet3DS-Formats.**
Das Distreet3DS-Format ist aufgrund des falschen Zaubers als veraltet markiert.
###  **Fügt das Discreet3DS-Format hinzu.**
Das Discreet3DS-Format wurde eingeführt.
###  **Fügt die Eigenschaft FlipCoordinate System in der Klasse Aspose hinzu. ThreeD. Formates. Universal3DConfig**
Benutzer können das Koordinaten system von U3D während des Imports oder Exports umdrehen.
