---
title: Installation
type: docs
weight: 50
url: /java/installation/
description: Aspose hosts all Java APIs on Aspose Repository. You can easily use Aspose.3D for Java API directly in your Maven projects with simple configurations.
---

## **Installing Aspose.3D for Java from Aspose Repository**
Aspose hosts all Java APIs on [Aspose Repository](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d). You can easily use Aspose.3D for Java API directly in your Maven projects with simple configurations.

First you need to specify Aspose Repository configuration / location in your Maven `pom.xml` as below:

{{< highlight java >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>http://repository.aspose.com/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Then define Aspose.3D for Java API dependency in your pom.xml as follows:

{{< highlight java >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>21.4</version>
    </dependency>

</dependencies>

{{< /highlight >}}

Congratulations! You have successfully defined the Aspose.3D for Java Maven dependency in your Maven project.
