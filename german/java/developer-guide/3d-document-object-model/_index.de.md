---
title: Aspose.3D Dokument objekt modell (DOM)
type: docs
weight: 20
url: /de/java/aspose-3d-document-object-model
description: Jede 3D Szene kann eine beliebige Anzahl von View ports umfassen. Mit Aspose.3D for Java API können Entwickler einen oder mehrere View ports in einem einzigen Screenshot erfassen. Sie können es in der GUI-basierten Java-Anwendung oder einem Bild rendern.
---
Das Aspose.3D Document Object Model (DOM) ist eine leistungs starke In-Memory-Darstellung einer 3D-Szene. Es bietet Entwicklern die Möglichkeit, den Inhalt und die Formatierung einer 3D-Szene programm gesteuert zu lesen, zu bearbeiten und zu ändern.

In diesem Abschnitt werden wir die Schlüssel klassen des Aspose.3D DOM und ihre Beziehungen untersuchen. Durch die Verwendung dieser Klassen können Sie programma tischen Zugriff auf verschiedene Elemente innerhalb einer 3D-Szene erhalten.

Lassen Sie uns in die Hauptklassen des Aspose.3D DOM eintauchen:

* **Szene**: Die Scene-Klasse repräsentiert die Wurzel der 3D-Szenen hierarchie. Es dient als Container für alle anderen Elemente und bietet Methoden zur Manipulation der Gesamt szene.
* **Knoten**: Knoten sind die Bausteine einer 3D Szene. Sie stellen einzelne Objekte oder Entitäten innerhalb der Szene dar, wie z. B. Maschen, Lichter, Kameras oder Gruppen. Knoten können transform iert, animiert und strukturiert werden.
* **Entitäten**: Die Entities-Klassen umfassen eine breite Palette von Objekten und Elementen, aus denen eine 3D-Szene besteht. Es umfasst Entitäten wie Maschen, Lichter, Kameras, Profile und mehr. Diese Entitäten dienen als Bausteine, sodass Sie komplexe Szenen erstellen können, indem Sie sie programma tisch kombinieren und manipulieren. Die Kategorie Entitäten bietet Zugriff und Kontrolle über diese grundlegenden Elemente einer 3D-Szene.
* **Materialien**: In den Material klassen geht es darum, die visuellen Eigenschaften von Objekten innerhalb einer 3D-Szene zu definieren. Es bietet Tools zum programma tischen Erstellen, Ändern und Steuern von Materialien, die bestimmen, wie Licht mit Oberflächen interagiert. Durch Anpassen von Eigenschaften wie Farbe, Textur, Transparenz und Reflexion können Sie verschiedene visuelle Effekte erzielen und das Erscheinung sbild Ihrer 3D-Modelle anpassen.
* **Animationen**: Die Animations klassen konzentrieren sich auf das Erstellen und Steuern von Bewegungen und Transformationen innerhalb einer 3D-Szene. Sie können Animationen programma tisch definieren und bearbeiten, sodass Objekte Eigenschaften im Laufe der Zeit verschieben, drehen, skalieren oder ändern können. Mit dieser Kategorie können Sie dynamische und interaktive Elemente in Ihre 3D Szenen einbringen.

Durch die Verwendung der oben genannten Aspose.3D DOM-Klassen können Sie programm gesteuert mit dem Inhalt und der Struktur einer 3D-Szene interagieren und diesen bearbeiten. Dies bietet Flexibilität und Kontrolle bei der Arbeit mit 3D-Modellen in Ihren Anwendungen.


## Szenen struktur

Wenn Aspose.3D eine 3D-Datei in den Speicher liest, werden Objekte verschiedener Typen generiert, um die verschiedenen Elemente innerhalb der 3D-Szene darzustellen.


Die Szenen struktur in Aspose.3D folgt dem zusammen gesetzten Design muster, das Flexibilität und Organisation bietet:

 * Knoten dienen als Container, die andere Knoten aufnehmen können, wodurch verschiedene Objekte innerhalb der Szene gruppiert werden können.
 * Jeder Knoten kann seine eigene Transformation haben, die auch für seine unter geordneten Knoten gilt.
 * Alle räumlichen Entität typen in Aspose.3D müssen unter einer Knoten instanz platziert werden. Dadurch wird sicher gestellt, dass Objekte wie Maschen, Lichter, Kameras und andere Elemente innerhalb der Szenen hierarchie organisiert sind.
 * Knoten können mehrere Materialien enthalten, und die Beziehung zwischen Polygonen und Materialien, die an einen Knoten angehängt sind, wird mithilfe des `VertexElementMaterial`-Konzepts innerhalb des Mesh-Objekts adressiert.


! [Szenen hierarchie](scene.png)


## Räumliche Entitäten
Alle räumlichen Entitäten innerhalb von Aspose.3D erben von der `Entity`-Klasse und dienen als grundlegende Bausteine für den Aufbau virtueller Umgebungen. Aspose.3D katego risiert diese Entitäten in mehrere Haupt kategorien, von denen jede ihren eigenen spezifischen Zweck und ihre eigene Funktional ität hat.

! [Entitäten](entity.png)

* **Primitiv**Die `Primitive`-Klasse dient als Basis klasse für alle prozedur alen 3D-Geometrien innerhalb von Aspose.3D, wie z. B. `Cylinder`, `Torus` und `Sphere`. Diese Geometrien können mit einem minimalen Satz von Parametern definiert werden, sodass Sie einfache 3D-Formen erstellen können.
* **Geometrie**: Geometrien in Aspose.3D bestehen normaler weise aus Eckpunkten, Kanten und Polygonen, die die Form und Struktur eines 3D-Objekts definieren. Diese Kategorie umfasst eine Vielzahl komplexer Geometrien, die zur Darstellung verschiedener Objekte innerhalb einer 3D-Szene verwendet werden.
* **Profil**: Profile, ähnlich wie Grundelemente, definieren geschlossene 2D-Konturen in der x-y-Ebene. Sie bieten eine Möglichkeit, 2D-Formen zu erstellen, die extrudiert werden können, um entsprechende 3D-Geometrien zu erzeugen. Profile werden häufig als Ausgangs punkt für die Erstellung von komplizierteren 3D-Objekten verwendet.
* **Kurve**: Im Gegensatz zu Profilen können Kurven offen oder nicht verbunden sein. Sie werden verwendet, um räumliche Pfade in 3D zu definieren. Kurven bieten die Möglichkeit, flexible und anpassbare Pfade zu erstellen, denen Objekte in einer 3D-Umgebung folgen können.
* **Extrusion**: Extrusionen sind eine Verfahrens technik, mit der 3D-Geometrien unter Verwendung von Profilen und Kurven erstellt werden. Durch Anwendung der Extrusion auf ein Profil oder eine Kurve kann eine 3D-Form erzeugt werden, indem das Profil oder die Kurve entlang einer bestimmten Richtung erweitert wird. Dieser Ansatz ermöglicht die Schaffung komplexerer und dynamischerer Geometrien.
* **Frustum**: Die Kategorie Frust um umfasst Objekte wie Lichter und Kameras. Frust ums definieren das Betrachtung volumen und die Perspektive in einer 3D-Szene. Kameras verwenden Frust ums, um den Teil der Szene zu bestimmen, der sichtbar sein wird, während Lichter Frust verwenden, um den Bereich zu definieren, in dem sie die Szene beleuchten.

Diese wichtigen Entität skate gorien in Aspose.3D umfassen eine Vielzahl von Entitäten, die beim Aufbau und der Darstellung virtueller Umgebungen eine wesentliche Rolle spielen, und bieten ein vielseitiges Toolkit zum Erstellen und Bearbeiten von 3D-Szenen.


### Geometrie typen

! [Geometrie typen](geometries.png)

Aspose.3D enthält viele Geometrie typen:


* `Mesh` Autoren werkzeug freundliches Polygon netz.
* `PointCloud` Punktwolke.
* `NurbsSurface` Nicht einheitliche rationale B-Spline-Oberflächen.
* `Patch` Oberfläche definiert durch eine Reihe von Kontroll punkten und Misch funktionen.
* `TriMesh` Rendern API-freundliches dreieck basiertes Mesh.


Die wichtigsten davon sind `Mesh` und `TriMesh`. Die Unterschiede sind in der Tabelle aufgeführt:

|Feature| `Mesh` | `TriMesh` |
| ---     |---     |---        |
|Nicht-Dreieck-Polygon|Ja|Nein|
|Leicht zu modifizieren|Ja|Nein|
|Daten index wieder verwendung|Ja|Nein|
|CPU Cache freundlich|Nein|Ja|
|Rendering API freundlich|Nein|Ja|
|Festes Speicher layout|Nein|Ja|

Von `Geometry` abgeleitete Klassen sind für Änderungen und die Erstellung von Inhalten konzipiert, während `TriMesh` für das Rendering konzipiert ist.

A `Geometry` besteht aus Kontroll punkten und `VertexElement`, die zusätzliche Daten für Kontroll punkt/Kante/Polygon/Polygon vertex definiert haben. `Geometry` kann null oder mehr `VertexElement` enthalten. konkrete `Geometry`-Unter klassen implementierten verschiedene Methoden zur Modellierung und Darstellung von 3D-Geometrien.


! [Geometrie typen](mesh.png)


Sie können ein Vertex element manuell erstellen und Daten dafür zuweisen. Das folgende Code beispiel zeigt, wie das geht:

{{< highlight "java" >}}
// Raw normal data
Vector4[] normals = new Vector4[]
{
    new Vector4(-0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258, 0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258, 0.577350258, 1.0),
    new Vector4(-0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258,-0.577350258,-0.577350258, 1.0),
    new Vector4( 0.577350258, 0.577350258,-0.577350258, 1.0),
    new Vector4(-0.577350258, 0.577350258,-0.577350258, 1.0)
};
// Call Common class create mesh using polygon builder method to set mesh instance
Mesh mesh = Common.createMeshUsingPolygonBuilder();
VertexElementNormal elementNormal = (VertexElementNormal)mesh.createElement(VertexElementType.NORMAL, MappingMode.CONTROL_POINT, ReferenceMode.DIRECT);
// Copy the data to the vertex element
elementNormal.setData(normals);
{{< /highlight >}}

### Primitive Geometrie typen


Aspose.3D bietet eine Reihe vordefinierter primitiver Geometrie typen, die bestimmten Regeln und Algorithmen folgen, um 3D-Modelle zu generieren. Diese primitiven Typen vereinfachen das Erstellen von 3D-Geometrien im Vergleich zur Verwendung komplexerer Geometrie typen.

Die verfügbaren vordefinierten primitiven Typen in Aspose.3D umfassen:

*  `Box`: Mit dem Box-Primitiv können Sie rechteckige Quader formen erstellen, die durch ihre Breite, Höhe und Tiefe definiert sind.
* Zylinder: Mit dem Zylinder primitiv können Sie zylindrische Formen erzeugen, indem Sie den Radius und die Höhe angeben. Dies ist nützlich, um Objekte wie Röhren oder Spalten zu erstellen.
*  `Dish`: Das Schalen primitiv ermöglicht die Schaffung schalen förmiger Geometrien, die üblicher weise zur Darstellung von Objekten wie Schalen oder Satelliten schüsseln verwendet werden.
*  `Plane`: Das Ebenen primitiv erzeugt flache Flächen, die durch ihre Breite und Länge definiert sind. Es wird häufig als Fundament oder Boden ebene in 3D-Szenen verwendet.
*  `Pyramid`: Mit dem Pyramiden primitiv können Sie pyramiden förmige Geometrien erstellen, die sich durch ihre Grund größe und-höhe auszeichnen. Dies ist nützlich für die Konstruktion von Objekten wie Gebäuden oder Pyramiden.
*  `Torus`: Mit dem Torus primitiv können Sie Donut-förmige Geometrien mit angegebenen Radien für die Haupt-und Neben kreise erzeugen. Es eignet sich zum Erstellen von Objekten, die Ringen oder Reifen ähneln.
*  `RectangularTorus`: Das rechteckige Torus-Primitiv erzeugt Torus-ähnliche Geometrien mit rechteckigen Querschnitten anstelle von kreisförmigen. Es bietet zusätzliche Flexibilität für die Schaffung einzigartiger Formen.
*  `Sphere`: Das Kugel primitiv erzeugt perfekt runde Geometrien basierend auf dem angegebenen Radius. Dies ist nützlich, um Objekte wie Planeten oder Bälle zu erstellen.

Wenn Sie diese vordefinierten primitiven Typen in Aspose.3D verwenden, können Sie ganz einfach eine breite Palette von grundlegenden 3D-Geometrien erstellen. Dies vereinfacht den Modellierung prozess und ermöglicht es Ihnen, Objekte innerhalb Ihrer 3D-Szenen schnell zu formen und zusammen zubauen.

! [Primitive Geometrie typen](primitives.png)

Das folgende Code beispiel zeigt, wie eine Kugel mit einem angegebenen Radius erstellt wird:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java

        // initialize a scene
        Scene scene = new Scene();
        // initialize a Sphere
        Sphere sphere = new Sphere();
        // set radius
        sphere.setRadius(10);
        // add sphere to the scene
        scene.getRootNode().createChildNode(sphere);
        // save scene
        scene.save("sphere.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}


### Extrusion typen

Extrusion kann verwendet werden, um eine Vielzahl von komplexen 3D-Objekten zu erstellen. Es ist eine grundlegende Methode für die 3D-Modellierung, bei der ein 2D-Profil entlang einer Kurve erweitert wird, um ein 3D-Objekt zu erstellen.

In Aspose.3D haben wir 3 Extrusion typen bereit gestellt:

* `LinearExtrusion` Lineare Extrusion nimmt ein 2D-Profil als Eingabe und erweitert die Form in der 3. Dimension.
* `RevolvedAreaSolid` Diese Klasse stellt ein festes Modell dar, indem ein Querschnitt, der von einem Profil bereit gestellt wird, um eine Achse gedreht wird.
* `SweptAreaSolid` Diese Klasse stellt ein solides Modell durch ein umfassendes Darstellung schema dar, mit dem ein 2D-Profilquerschnitt durch den Raum fegen kann.


! [Extrusionen](extrusions.png)

Das folgende Code beispiel zeigt, wie eine lineare Extrusion aus einem Text profil erstellt wird:

{{< highlight "java" >}}
    // Load font from bytes
    var font = FontFile.parse(Files.readAllBytes(Paths.get("test-font.otf")));
    // Create a Text profile
    var text = new Text();
    text.setFont(font);
    text.setContent("Hello World");
    text.setFontSize(10.0f);
    // Extrude the profile to give it a thickness.
    var linear = new LinearExtrusion(text, 10).toMesh();
    // create a scene from the mesh and save it to stl file
    var scene = new Scene(linear);
    scene.save("test.stl");


{{< /highlight >}}


### Kurven typen

In Aspose.3D repräsentiert eine Kurve einen oder mehrere räumliche Pfade, die verschiedene Formen annehmen können, z. B. Linien, NURBS-Kurven oder zusammen gesetzte Kurven, die aus mehreren Kurven segmenten bestehen. Kurven werden üblicher weise in Verbindung mit Extrusion typen verwendet, um dynamische und komplizierte 3D-Formen zu erstellen.

Kurven können verwendet werden, um komplexe Pfade zu definieren, denen Objekte in einer 3D-Umgebung folgen und sanfte und präzise Bewegungen ermöglichen. Durch die Verwendung verschiedener Kurven typen und deren Zusammenstellung können Sie vielseitige und anpassbare räumliche Pfade für Ihre 3D-Modelle erreichen.

Darüber hinaus bieten bestimmte Dateiformate, die von Aspose unterstützt werden. 3D, auch die Möglichkeit, Kurven daten zu importieren und zu exportieren. Auf diese Weise können Sie Kurven, die in externen Anwendungen erstellt wurden, nahtlos integrieren oder Kurven teilen, die innerhalb von Aspose.3D generiert wurden, mit anderer Software.


! [Kurven typen](curves.png)

## Profil typen

Aspose.3D bietet eine Reihe von 2D-Profilen, die verwendet werden können, um geschlossene Formen oder Konturen innerhalb einer 3D-Umgebung zu erstellen. Diese Profile ermöglichen die Erstellung komplizierter 2D-Strukturen, die weiter extrudiert oder in 3D-Geometrien manipuliert werden können. Hier sind einige bemerkens werte Profil implementie rungen in Aspose.3D:

* `ParameterizedProfile`: Aspose.3D bietet mehrere Implementie rungen, die Profile mit Standardformen anbieten. Diese vordefinierten Profile ermöglichen die schnelle Erstellung häufig verwendeter Formen wie Kreise, Rechtecke und Polygone.

* `MirroredProfile`: Mit diesem Profil typ können Sie ein vorhandenes Profil entlang der Y-Achse spiegeln und so eine symmetrische Form erzeugen. Es bietet eine bequeme Möglichkeit, ausgewogene und optisch ansprechende Profile zu generieren.

* `ArbitraryProfile`: Mit der beliebigen Profil implementierung können Sie eine beliebige Kurve zuordnen, um ein geschlossenes Profil zu erstellen. Dies bietet Flexibilität beim Entwerfen benutzer definierter Formen, indem eine Kurve definiert und zur weiteren Manipulation in ein geschlossenes Profil umgewandelt wird.

* `Text`: Aspose.3D beinhaltet die Möglichkeit, Profile aus Text mit einer bestimmten Schriftart zu generieren. Mit dieser Funktion können Sie Profile in Form von Buchstaben, Zahlen oder anderen Textinhalten erstellen und Ihren 3D-Modellen ein Element der Personal isierung oder des Brandings hinzufügen.

! [2D-Profiltypen](profiles.png)

### Kamera-und Licht typen

! [Kamera und Licht](frustums.png)

## Material typen

Aspose.3D bietet Unterstützung für verschiedene Arten von Materialien, einschl ießlich Lambert-Material, Phong-Material, PBR-Material, PBR-Spekularmaterial und Shader-Material (nur in FBX-Dateien verfügbar).

Jedes Material in Aspose.3D kann unterschied liche Attribute und Eigenschaften haben, die sein Aussehen und Verhalten innerhalb einer 3D Szene definieren. Diese Materialien können mit Textur instanzen verbunden werden, wodurch ihre visuellen Eigenschaften verbessert werden.

Texturen in Aspose.3D sind einem bestimmten Material attribut zugeordnet. Der Textur typ kombiniert die Parameter definitionen für die Bild quelle und den Textur-Sampler. Durch die Verwendung von Texturen können Sie detaillierte Muster, Farben und andere visuelle Effekte auf die Oberflächen Ihrer 3D-Modelle anwenden.

Mit der Unterstützung für eine Reihe von Material typen und der Möglichkeit, Texturen zu verbinden, bietet Aspose.3D Flexibilität bei der Erstellung optisch ansprechender und realistischer Materialien für Ihre 3D Szenen.

! [Material typen](materials.png)

Das folgende Code beispiel zeigt, wie ein PBR-Material auf eine Geometrie angewendet wird:

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// initialize a scene
Scene scene = new Scene();
// initialize PBR material object
PbrMaterial mat = new PbrMaterial();
// an almost metal material
mat.setMetallicFactor(0.9);
// material surface is very rough
mat.setRoughnessFactor(0.9);
// create a box to which the material will be applied
Node boxNode = scene.getRootNode().createChildNode("box", new Box());
boxNode.setMaterial(mat);
// save 3d scene into USDZ format
scene.save(MyDir + "PBR_Material_Box_Out.usdz");

{{< /highlight >}}

## Beziehung zu Animations objekten
Aspose.3D bietet Animations unterstützung auf Daten ebene, und die Berechnungs unterstützung wird derzeit entwickelt.

In Aspose.3D kann eine Szene mehrere AnimationClip-Objekte enthalten. Jeder Animations clip kann aus mehreren Animations knoten bestehen. Der Animations knoten folgt dem zusammen gesetzten Entwurfs muster und ermöglicht die Erstellung hierarchischer Strukturen mit Sub animations knoten.

Animations knoten können Bindungs punkten zugeordnet werden, die die Eigenschaften des zu animieren den Zielobjekts definieren. Vektoren sind häufig verwendete Datentypen in vielen Entität eigenschaften. Daher können Bindungs punkte unterschied liche Animations kanäle haben, um bestimmte Kanäle des Vektors unabhängig voneinander zu aktualisieren. Jeder Kanal enthält eine Keyframe-Sequenz, die definiert, wie der Wert im Laufe der Zeit animiert wird.

Dieses System bietet ein flexibles Framework für die Animation von Objekten innerhalb einer Szene. Durch Definieren von Animations clips, Knoten, Bindungs punkten und Kanälen können Sie komplexe und dynamische Animationen erstellen, die sich auf verschiedene Eigenschaften der Entitäten in Ihrer 3D-Szene auswirken.

Während Aspose.3D derzeit Animationen auf Daten ebene unterstützt, konzentriert sich die laufende Entwicklung auf die Erweiterung der Berechnungs unterstützung, wodurch die Funktionen zum Erstellen und Bearbeiten von Animationen innerhalb des Frameworks verbessert werden.

! [Animationen](animations.png)


Eine Szene mit Animationen kann diese Art von Struktur haben:


! [Beispiel für Animationen](animation_relations.png)