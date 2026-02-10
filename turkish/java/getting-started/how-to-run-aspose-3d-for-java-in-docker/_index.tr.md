---
title: How to Run Aspose.3D for Java in Docker
type: docs
description: Linux için bir docker konteynerinde Aspose.3D for Java çalıştırın.
weight: 139
url: /tr/java/how-to-run-aspose-3d-in-docker/
---
Microservices, in conjunction with containerization make it possible to easily combine technologies. Docker allows you to easily integrate Aspose.3D functionality into your application, regardless of what technology is in your development stack.

In case you are targeting microservices, or if the main technology in your stack is not .NET, C++ or Java, but you need Aspose.3D functionality, or if you already use Docker in your stack, then you may be interested in utilizing Aspose.3D for Java in a Docker container.

## Önkoşullar

- Docker sisteminize kurulmalıdır.

## Java uygulaması oluşturun

Bu örnekte, basit bir 3d dosya oluşturan bir Java uygulaması oluşturursunuz, kaydeder ve okur. Uygulama daha sonra docker'da oluşturulabilir ve çalıştırılabilir.

### Java uygulamasını oluşturma

Create a Java application in Eclipse using the following code. In this example, we use Aspose.3D for Java to create a plane in the 3d scene and set the vector and then save it in obj format.

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

### Bir kavanoz paketine Java uygulamasını yapın

Aşağıdaki şekil, tutulmada "İhracat" menüsünü kullanarak bir kavanoz paketi yapmanın bir yolunu gösterir.

**! [Eclipse](makejar.png kullanarak kavanoz yap)**

Şimdi Aspose kullanarak Java programı yazdık. 3D for Java, bir kavanoz paketimiz var. Sonra bir dockerfile yapacağız.

### Bir dockerfile yapılandırması

Bir sonraki adım, dockerfile dosyasını oluşturmak ve yapılandırmaktır.

1. Dockerfile oluşturun ve kavanoz paketinin yanına yerleştirin. Bu dosya adını uzantısız tutun (varsayılan).
2. dockerfile, belirtin:

{{< highlight "plain" >}}
   FROM williamyeh/java8:latest

   VOLUME /tmp

   ADD TestDocker.jar app.jar

   ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
{{< /highlight >}}

### Uygulamayı docker'da oluşturma ve çalıştırma

Şimdi uygulama docker'da oluşturulabilir ve çalıştırılabilir. Favori komut isteminizi açın, dizini dockerfile ile klasöre değiştirin ve aşağıdaki komutu çalıştırın:

{{< highlight "plain" >}}
docker build -t java-app .
{{< /highlight >}}

After executing the above command, you will get the output of 3D file. At this point, a Java program has been successfully run in Linux Docker.
