---
title: So führen Sie Aspose.3D for Java in Docker aus
type: docs
description: Führen Sie Aspose.3D for Java in einem Docker-Container für Linux aus.
weight: 139
url: /de/java/how-to-run-aspose-3d-in-docker/
---
Micros ervices in Verbindung mit Container isierung ermöglichen es, Technologien leicht zu kombinieren. Mit Docker können Sie auf einfache Weise Aspose.3D-Funktional ität in Ihre Anwendung integrieren, unabhängig davon, welche Technologie sich in Ihrem Entwicklungs stapel befindet.

Falls Sie auf Mikros ervices abzielen oder wenn die Haupt technologie in Ihrem Stack nicht .NET, C++ oder Java ist, sondern Sie Aspose benötigen. 3D Funktional ität, oder wenn Sie Docker bereits in Ihrem Stack verwenden, dann könnten Sie daran interessiert sein, Aspose zu verwenden. 3D for Java in einem Docker-Container.

## Voraussetzungen

- Docker muss auf Ihrem System installiert sein.

## Erstellen Sie eine Java-Anwendung

In diesem Beispiel erstellen Sie eine Java-Anwendung, die eine einfache 3D-Datei erstellt, speichert und liest sie. Die Anwendung kann dann in Docker erstellt und ausgeführt werden.

### Erstellen der Java-Anwendung

Erstellen Sie eine Java-Anwendung in Eclipse mit dem folgenden Code. In diesem Beispiel verwenden wir Aspose.3D for Java, um eine Ebene in der 3D-Szene zu erstellen und den Vektor festzulegen und dann im obj-Format zu speichern.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize Scene
Scene scene = new Scene();
// Initialize Plane
Plane plane = new Plane();
// Set Vector
plane.setUp(new Vector3(1, 1, 3));
scene.getRootNode().createChildNode(plane);
//This will generate a plane that has customized orientation
scene.save(MyDir+"ChangePlaneOrientation.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

### Machen Sie die Java-Anwendung zu einem Glas paket

Die folgende Abbildung zeigt eine Möglichkeit, ein Glas paket mithilfe des Menüs "Exportieren" in Eclipse zu erstellen.

**! [Machen Sie Jar mit Eclipse](MakeJar.png)**

Nachdem wir nun ein Java-Programm mit Aspose.3D for Java geschrieben haben, haben wir ein Glas paket erhalten. Als nächstes machen wir eine Docker file.

### Eine Docker file konfigurieren

Der nächste Schritt besteht darin, die Docker file zu erstellen und zu konfigurieren.

1. Erstellen Sie die Docker file und platzieren Sie sie neben dem JAR-Paket. Behalten Sie diesen Dateinamen ohne Erweiterung bei (Standard).
2. Geben Sie im Docker file Folgendes an:

{{< highlight "plain" >}}
   FROM williamyeh/java8:latest

   VOLUME /tmp

   ADD TestDocker.jar app.jar

   ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
{{< /highlight >}}

### Erstellen und Ausführen der Anwendung in Docker

Jetzt kann die Anwendung in Docker erstellt und ausgeführt werden. Öffnen Sie Ihre bevorzugte Eingabe aufforderung, ändern Sie das Verzeichnis in den Ordner mit der Docker file und führen Sie den folgenden Befehl aus:

{{< highlight "plain" >}}
docker build -t java-app .
{{< /highlight >}}

Nachdem Sie den obigen Befehl ausgeführt haben, erhalten Sie die Ausgabe der 3D-Datei. Zu diesem Zeitpunkt wurde ein Java-Programm erfolgreich in Linux Docker ausgeführt.
