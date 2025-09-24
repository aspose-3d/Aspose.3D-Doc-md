---
title: Installation
type: docs
weight: 50
url: /java/installation/
description: Aspose hosts all Java APIs on Aspose Repository. You can easily use Aspose.3D for Java API directly in your Maven projects with simple configurations.
---

## **Installing Aspose.3D for Java from Aspose Repository**
Aspose hosts all Java APIs on [Aspose Repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). You can easily use Aspose.3D for Java API directly in your Maven projects with simple configurations.

First you need to specify Aspose Repository configuration / location in your Maven `pom.xml` as below:

{{< highlight xml >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Then define Aspose.3D for Java API dependency in your pom.xml as follows:

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


If you're using JDK-8, you can use JDK-8 version as follows:

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

Congratulations! You have successfully defined the Aspose.3D for Java Maven dependency in your Maven project.
