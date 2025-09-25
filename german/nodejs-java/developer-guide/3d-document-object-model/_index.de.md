---
title: Aspose.3D Dokumentobjektmodell (DOM)
type: docs
weight: 20
url: "/de/nodejs-java/aspose-3d-document-object-model"
description: "Jede 3D-Szene kann eine beliebige Anzahl von Ansichten enthalten. Mit Aspose.3D für Node.js-Java API können Entwickler eine oder mehrere Ansichten in einem einzigen Screenshot erfassen. Sie können es in einer GUI-basierten Node.js-Java-Anwendung oder einem Bild rendern."
---

Der Aspose.3D Document Object Model (DOM) ist eine leistungsstarke In-Memory-Darstellung einer 3D-Szene. Es bietet Entwicklern die Möglichkeit, den Inhalt und die Formatierung einer 3D-Szene programmgesteuert auszulesen, zu manipulieren und zu modifizieren.

In diesem Abschnitt werden wir die wichtigsten Klassen des Aspose.3D DOM und ihre Beziehungen untersuchen. Durch die Nutzung dieser Klassen können Sie programmatischen Zugriff auf verschiedene Elemente innerhalb einer 3D-Szene erhalten.

Lassen Sie uns die Hauptklassen des Aspose.3D DOM betrachten:

* **Scene**: Die Scene-Klasse stellt die Wurzel der 3D-Szenenhierarchie dar. Sie dient als Container für alle anderen Elemente und bietet Methoden zur Manipulation der gesamten Szene.
* **Node**: Nodes sind die Bausteine einer 3D-Szene. Sie stellen einzelne Objekte oder Entitäten innerhalb der Szene dar, wie z. B. Meshes, Lichter, Kameras oder Gruppen. Nodes können transformiert, animiert und texturiert werden.
* **Entities**: Die Entities-Klassen umfasst eine breite Palette von Objekten und Elementen, die eine 3D-Szene ausmachen. Dazu gehören Entitäten wie Meshes, Lichter, Kameras, Profile und mehr. Diese Entitäten dienen als Bausteine, mit denen Sie komplexe Szenen erstellen können, indem Sie sie programmgesteuert kombinieren und manipulieren. Die Entities-Kategorie bietet Zugriff und Kontrolle über diese grundlegenden Elemente einer 3D-Szene.
* **Materials**: Die Materials-Klassen befasst sich mit der Definition der visuellen Eigenschaften von Objekten innerhalb einer 3D-Szene. Es bietet Tools, um Materialien programmgesteuert zu erstellen, zu modifizieren und zu steuern, die bestimmen, wie Licht mit Oberflächen interagiert. Durch Anpassen von Eigenschaften wie Farbe, Textur, Transparenz und Reflexion können Sie verschiedene visuelle Effekte erzielen und das Erscheinungsbild Ihrer 3D-Modelle anpassen.
* **Animations**: Die Animation-Klassen konzentriert sich auf die Erstellung und Steuerung von Bewegung und Transformationen innerhalb einer 3D-Szene. Es ermöglicht Ihnen, Animationen programmgesteuert zu definieren und zu manipulieren, sodass Objekte sich im Laufe der Zeit bewegen, rotieren, skalieren oder Eigenschaften ändern können. Mit dieser Kategorie können Sie dynamische und interaktive Elemente zu Ihren 3D-Szenen hinzufügen.

Durch die Nutzung der oben genannten Aspose.3D DOM-Klassen können Sie programmgesteuert mit dem Inhalt und der Struktur einer 3D-Szene interagieren und diese manipulieren. Dies bietet Flexibilität und Kontrolle bei der Arbeit mit 3D-Modellen in Ihren Anwendungen.

## Szenenstruktur

Wenn Aspose.3D eine 3D-Datei in den Speicher lädt, werden Objekte verschiedener Typen generiert, um die verschiedenen Elemente innerhalb der 3D-Szene darzustellen.

Die Szenenstruktur in Aspose.3D folgt dem Composite-Designmuster, das Flexibilität und Organisation bietet:

* Nodes dienen als Container, die andere Nodes enthalten können, wodurch eine Gruppierung verschiedener Objekte innerhalb der Szene ermöglicht wird.
* Jeder Node kann seine eigene Transformation haben, die sich auch auf seine untergeordneten Nodes auswirkt.
* Alle räumlichen Entitätstypen in Aspose.3D müssen unter einer Node-Instanz platziert werden. Dies stellt sicher, dass Objekte wie Meshes, Lichter, Kameras und andere Elemente innerhalb der Szenenhierarchie organisiert sind.
* Nodes können mehrere Materialien enthalten, und die Beziehung zwischen Polygonen und Materialien, die an einen Node angehängt sind, wird mithilfe des Konzepts `VertexElementMaterial` innerhalb des Mesh-Objekts behandelt.

![Szenenhierarchie](scene.png)

## Räumliche Entitäten
Alle räumlichen Entitäten in Aspose.3D erben von der `Entity`-Klasse und dienen als grundlegende Bausteine für den Aufbau virtueller Umgebungen. Aspose.3D kategorisiert diese Entitäten in mehrere Hauptkategorien, die jeweils ihren eigenen spezifischen Zweck und ihre eigene Funktionalität haben.

![Entitäten](entity.png)

* **Primitive**: Die `Primitive`-Klasse dient als Basisklasse für alle prozeduralen 3D-Geometrien in Aspose.3D, wie z. B. `Zylinder`, `Torus` und `Kugel`. Diese Geometrien können mit einer minimalen Anzahl von Parametern definiert werden, was es bequem macht, grundlegende 3D-Formen zu erstellen.
* **Geometry**: Geometrien in Aspose.3D bestehen typischerweise aus Vertices, Edges und Polygonen, die die Form und Struktur eines 3D-Objekts definieren. Diese Kategorie umfasst eine breite Palette komplexer Geometrien, die in 3D-Modellen verwendet werden.
* **ArbitraryProfile**: Mit der `ArbitraryProfile`-Implementierung können Sie eine beliebige Kurve zu einem geschlossenen Profil abbilden. Dies bietet Flexibilität bei der Gestaltung benutzerdefinierter Formen durch Definition einer Kurve und Umwandlung dieser in ein geschlossenes Profil für weitere Manipulationen.
* **Text**: Aspose.3D bietet die Möglichkeit, Profile aus Text mit einer angegebenen Schriftart zu generieren. Diese Funktion ermöglicht es Ihnen, Profile in Form von Buchstaben, Zahlen oder anderen Textinhalten zu erstellen und fügt so Ihren 3D-Modellen ein Element der Personalisierung oder des Brandings hinzu.

![2D-Profiltypen](profiles.png)

## Kamera- und Lichttypen

![Kamera und Licht](frustums.png)

## Materialtypen

Aspose.3D unterstützt verschiedene Materialtypen, darunter Lambert-Material, Phong-Material, PBR-Material, PBR-Spiegelungs-Material und Shader-Material (nur in FBX-Dateien verfügbar).

Jedes Material in Aspose.3D kann unterschiedliche Attribute und Eigenschaften haben, die sein Aussehen und Verhalten innerhalb einer 3D-Szene definieren. Diese Materialien können Texturinstanzen zugeordnet werden, wodurch ihre visuellen Eigenschaften verbessert werden.

Texturen in Aspose.3D sind einer bestimmten Materialeigenschaft zugeordnet. Der Texturtyp kombiniert die Parameterdefinitionen für die Bildquelle und den Textursampler. Durch die Verwendung von Texturen können Sie detaillierte Muster, Farben und andere visuelle Effekte auf die Oberflächen Ihrer 3D-Modelle anwenden.

Mit der Unterstützung für eine Reihe von Materialtypen und der Möglichkeit, Texturen zu verbinden, bietet Aspose.3D Flexibilität bei der Erstellung optisch ansprechender und realistischer Materialien für Ihre 3D-Szenen.

![Materialtypen](materials.png)

## Animations-Objekt-Beziehungen
Aspose.3D bietet Animationsunterstützung auf Datenebene, und Berechnungssupport wird derzeit entwickelt.

In Aspose.3D kann eine Szene mehrere `AnimationClip`-Objekte enthalten. Jede Animationssequenz kann mehrere Animationsnodes enthalten. Der Animationsnode folgt dem Composite-Designmuster, das die Erstellung hierarchischer Strukturen mit Sub-Animationsnodes ermöglicht.

Animationsnodes können Bindepunkten zugeordnet werden, die die Eigenschaften des Zielobjekts definieren, die animiert werden sollen. Vektoren werden häufig als Datentypen in vielen Entitätseigenschaften verwendet. Daher können Bindepunkte unterschiedliche Animationskanäle haben, um bestimmte Kanäle des Vektors unabhängig zu aktualisieren. Jeder Kanal enthält eine Keyframe-Sequenz, die definiert, wie der Wert im Laufe der Zeit animiert wird.

Dieses System bietet einen flexiblen Rahmen für die Animation von Objekten in einer Szene. Durch die Definition von Animationssequenzen, Nodes, Bindepunkten und Kanälen können Sie komplexe und dynamische Animationen erstellen, die die Eigenschaften der Entitäten in Ihrer 3D-Szene beeinflussen.

Während Aspose.3D derzeit Animationsunterstützung auf Datenebene bietet, konzentriert sich die laufende Entwicklung auf die Erweiterung der Berechnungssupport, was die Möglichkeiten zur Erstellung und Manipulation von Animationen innerhalb des Frameworks verbessern wird.

![Animationen](animations.png)

Eine Szene mit Animationen kann diese Art von Struktur haben:

![Animationsbeispiel](animation_relations.png)