---
title: Installation
type: docs
weight: 50
url: /es/java/installation/
description: Aspose aloja todas las API Java en el repositorio Aspose. Puede usar fácilmente Aspose.3D for Java API directamente en sus proyectos Maven con configuraciones simples.
---
##  **Instalación de Aspose.3D for Java desde el repositorio Aspose**
Aspose aloja todas las APIs de Java en [Repositorio Aspose](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). Puede usar fácilmente Aspose.3D for Java API directamente en sus proyectos Maven con configuraciones simples.

Primero debe especificar la configuración/ubicación del repositorio Aspose en su Maven `pom.xml` de la siguiente manera:

{{< highlight "xml" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Luego defina Aspose.3D for Java API dependencia en su pom.xml de la siguiente manera:

{{< highlight "xml" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>23.11.0</version>
    </dependency>

</dependencies>

{{< /highlight >}}


Si está utilizando JDK-8, puede utilizar JDK-8 versión de la siguiente manera:

{{< highlight "xml" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>23.11.0</version>
        <classifier>jdk8</classifier>
    </dependency>

</dependencies>

{{< /highlight >}}

¡Felicitaciones! Ha definido con éxito la dependencia Aspose.3D for Java Maven en su proyecto Maven.
