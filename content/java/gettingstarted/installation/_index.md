---
title : "Installation" 
description : "" 
weight : 8007 
toc : false
type: docs
url: /java/gettingstarted/installation/
---

# Aspose.3D for Java : Installation


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Installing Aspose.3D for Java from Aspose Repository](#installing-aspose.3d-for-java-from-aspose-repository)
{{< /panel >}}
 

 

## Installing Aspose.3D for Java from Aspose Repository

Aspose hosts all Java APIs on [Aspose Repository](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d). You can easily use Aspose.3D for Java API directly in your Maven projects with simple configurations.

First you need to specify Aspose Repository configuration / location in your Maven pom.xml as below:

{{< code lang="cs" >}}
<repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>http://repository.aspose.com/repo/</url>
    </repository>
</repositories>
{{< /code >}}

Then define Aspose.3D for Java API dependency in your pom.xml as follows:

{{< code lang="cs" >}}
<dependencies>
    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>19.6</version>
    </dependency>
</dependencies>
{{< /code >}}

Congratulations! You have successfully defined the Aspose.3D for Java Maven dependency in your Maven project.

