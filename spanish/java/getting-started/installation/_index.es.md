---
title: Instalación
type: docs
weight: 50
url: /es/java/installation/
description: Aspose aloja todas las API de Java en el repositorio de Aspose. Puedes usar fácilmente Aspose.3D for Java API directamente en tus proyectos Maven con configuraciones simples.
---

## **Instalación de Aspose.3D para Java desde Aspose Repository**
Aspose aloja todas las API de Java en el [Aspose Repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). Puedes utilizar fácilmente la API Aspose.3D para Java directamente en tus proyectos Maven con configuraciones simples.

Primero debes especificar la configuración / ubicación del Aspose Repository en tu `pom.xml` de Maven como se muestra a continuación:

{{< highlight xml >}}
 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>
{{< /highlight >}}

Luego define la dependencia de la API Aspose.3D para Java en tu `pom.xml` de la siguiente manera:

{{< highlight xml >}}
 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>25.9.0</version>
    </dependency>
    <dependency>
      <groupId>org.bouncycastle</groupId>
      <artifactId>bc-fips</artifactId>
      <version>2.1.1</version>
    </dependency>


    <dependency>
      <groupId>org.lwjgl</groupId>
      <artifactId>lwjgl</artifactId>
      <version>${lwjgl.version}</version>
    </dependency>
      <artifactId>lwjgl-platform</artifactId>
      <version>${lwjgl.version}</version>
      <classifier>natives-windows</classifier>
    <dependency>
      <groupId>org.lwjgl</groupId>
      <artifactId>lwjgl-vulkan</artifactId>
      <version>${lwjgl.version}</version>
    </dependency>
</dependencies>
{{< /highlight >}}

Si estás usando JDK‑8, puedes usar la versión JDK‑8 de la siguiente forma:

{{< highlight xml >}}
 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>25.9.0</version>
        <classifier>jdk8</classifier>
    </dependency>
    <dependency>
      <groupId>org.bouncycastle</groupId>
      <artifactId>bc-fips</artifactId>
      <version>2.1.1</version>
    </dependency>
</dependencies>
{{< /highlight >}}

¡Felicidades! Has definido correctamente la dependencia Maven de Aspose.3D para Java en tu proyecto Maven.