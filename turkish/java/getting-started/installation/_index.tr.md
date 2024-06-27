---
title: Installation
type: docs
weight: 50
url: /tr/java/installation/
description: Aspose hosts all Java APIs on Aspose Repository. You can easily use Aspose.3D for Java API directly in your Maven projects with simple configurations.
---
##  **Installing Aspose.3D for Java from Aspose Repository**
Aspose hosts all Java APIs on [Aspose Repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). You can easily use Aspose.3D for Java API directly in your Maven projects with simple configurations.

İlk olarak Maven `pom.xml` aşağıdaki gibi Aspose depo yapılandırması/konumunda belirtmeniz gerekir:

{{< highlight "xml" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Then define Aspose.3D for Java API dependency in your pom.xml as follows:

{{< highlight "xml" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>23.11.0</version>
    </dependency>

</dependencies>

{{< /highlight >}}


JDK-8 kullanıyorsanız, aşağıdaki gibi JDK-8 sürümünü kullanabilirsiniz:

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

Tebrikler! Aspose 'yı başarıyla tanımladınız. 3D for Java Maven Maven projenizde bağımlılık.
