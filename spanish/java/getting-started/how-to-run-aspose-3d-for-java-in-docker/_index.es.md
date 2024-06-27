---
title: Cómo ejecutar Aspose.3D for Java en Docker
type: docs
description: Ejecute Aspose.3D for Java en un contenedor Docker para Linux.
weight: 139
url: /es/java/how-to-run-aspose-3d-in-docker/
---
Los microservicios, junto con la contenedorización, permiten combinar fácilmente tecnologías. Docker le permite integrar fácilmente la funcionalidad Aspose.3D en su aplicación, independientemente de qué tecnología esté en su pila de desarrollo.

En caso de que esté apuntando a microservicios, o si la tecnología principal en su pila no es .NET, C++ o Java, pero necesita Aspose.3D, o si ya usa Docker en su pila, entonces puede estar interesado en utilizar Aspose.3D for Java en un contenedor Docker.

## Requisitos previos

- Docker debe estar instalado en su sistema.

## Crear una aplicación Java

En este ejemplo, crea una aplicación Java que crea un archivo 3D simple, lo guarda y lo lee. La aplicación se puede construir y ejecutar en Docker.

### Creación de la aplicación Java

Cree una aplicación Java en Eclipse usando el siguiente código. En este ejemplo, usamos Aspose.3D for Java para crear un plano en la escena 3d y establecer el vector y luego guardarlo en formato obj.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-scene-ChangePlaneOrientation-ChangePlaneOrientation.java" >}}

### Convertir la aplicación Java en un paquete jar

La siguiente figura muestra una forma de hacer un paquete jar usando el menú "Exportar" en Eclipse.

**¡! [Hacer Jar usando Eclipse] (MakeJar.png)**

Ahora que escribimos un programa Java usando Aspose.3D for Java, tenemos un paquete jar. A continuación, haremos un Dock File.

### Configuración de un Dockerfile

El siguiente paso es crear y configurar el Dockerfile.

1. Cree el Dockerfile y póngalo al lado del paquete jar. Mantenga este nombre de archivo sin extensión (predeterminado).
2. En Dockerfile, especifique:

{{< highlight "plain" >}}
   FROM williamyeh/java8:latest

   VOLUME /tmp

   ADD TestDocker.jar app.jar

   ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
{{< /highlight >}}

### Construir y ejecutar la aplicación en Docker

Ahora la aplicación se puede construir y ejecutar en Docker. Abra su símbolo del sistema favorito, cambie el directorio a la carpeta con el Dockerfile y ejecute el siguiente comando:

{{< highlight "plain" >}}
docker build -t java-app .
{{< /highlight >}}

Después de ejecutar el comando anterior, obtendrá la salida del archivo 3D. En este punto, un programa Java se ha ejecutado con éxito en Linux Docker.
