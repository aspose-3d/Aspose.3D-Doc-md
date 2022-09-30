---
title: Instalación
type: docs
weight: 50
url: /es/java/installation/
description: Aspose aloja todas las APIs Java en el repositorio Aspose. Usted puede utilizar fácilmente Aspose.3D for Java API directamente en sus proyectos Maven con configuraciones simples.
---
## **Instalación Aspose.3D for Java desde el repositorio Aspose**
Aspose aloja todas las APIs Java en[Aspose Repositorio](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d)... Usted puede utilizar fácilmente Aspose.3D for Java API directamente en sus proyectos Maven con configuraciones simples.

Primero debe especificar la configuración/ubicación del repositorio Aspose en su Maven `pom.xml` como se indica a continuación:

{{< highlight "java" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>http://repository.aspose.com/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

A continuación, defina la dependencia Aspose.3D 07613481 API en su pom.xml de la siguiente manera:

{{< highlight "java" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>21.4</version>
    </dependency>

</dependencies>

{{< /highlight >}}

¡Enhorabuena! Ha definido correctamente la dependencia Aspose.3D for Java Maven en su proyecto Maven.
