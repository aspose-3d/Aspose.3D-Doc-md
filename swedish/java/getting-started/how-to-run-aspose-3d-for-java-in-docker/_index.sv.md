---
title: Hur man kör Aspose.3D for Java i dockar
type: docs
description: Kör Aspose.3D for Java i en Dockerbehållare för Linux.
weight: 139
url: /sv/java/how-to-run-aspose-3d-in-docker/
---
Mikrotjänster tillsammans med containerisering gör det möjligt att enkelt kombinera teknik. Dockaren låter dig enkelt integrera Aspose. 3D funktionalitet i din applikation, oavsett vilken teknik som finns i din utvecklingsstack.

Om du riktar på mikrotjänster, eller om huvudteknologin i din stack inte är .NET, C++ eller Java, men du behöver Aspose. 3D funktionalitet, eller om du redan använder Docker i din stack, då kan du vara intresserad av att använda Aspose. 3D for Java i en Dockerbehållare.

## Förutsättningar

- Dockaren måste vara installerad på ditt system.

## Skapa ett Java program

I det här exemplet skapar du ett Java-program som gör en enkel 3d-fil, sparar den och läser den. Programmet kan sedan byggas och köras i Docker.

### Skapa Java-program

Skapa ett Java-program i Eclipse med följande kod. I detta exempel använder vi Aspose. 3D for Java för att skapa ett plan i 3d-scenen och ställa in vektorn och sedan spara den i obj-format.

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

### Gör Java programmet till ett jarpaket

Följande figur visar ett sätt att göra ett burkpaket med "Export"-meny i Eclipse.

**! [Make Jar med Eclipse] (MakeJar.png)**

Nu när vi skrev ett Java-program med Aspose.3D for Java, fick vi ett bur-paket. Sen gör vi en hamnarfil.

### Anpassa en Dockerfil

Nästa steg är att skapa och konfigurera Dockerfilen.

1. Skapa Dockerfilen och placera den bredvid glaspaketet. Behåll filnamnet utan filändelse (standard).
2. Ange i Dockerfilen:

{{< highlight "plain" >}}
   FROM williamyeh/java8:latest

   VOLUME /tmp

   ADD TestDocker.jar app.jar

   ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
{{< /highlight >}}

### Bygga och köra applikationen i Dockern

Nu kan programmet byggas och köras i Docker. Öppna din favoritkommando, ändra katalog till mappen med Dockerfilen och kör följande kommando:

{{< highlight "plain" >}}
docker build -t java-app .
{{< /highlight >}}

Efter att ha kört ovanstående kommando, kommer du att få utdata för 3D-fil. Vid den här punkten har ett Java program körts med lyckat resultat i Linux Docker.
