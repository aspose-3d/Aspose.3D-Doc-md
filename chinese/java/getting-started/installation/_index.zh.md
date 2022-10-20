---
title: 安装
type: docs
weight: 50
url: /zh/java/installation/
description: Aspose将所有Java api托管在Aspose存储库中。您可以通过简单的配置轻松地在Maven项目中直接使用Aspose.3D for Java API。
---
## **从Aspose存储库安装Aspose.3D for Java**
Aspose托管所有Java api[Aspose存储库](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/)。您可以通过简单的配置轻松地在Maven项目中直接使用Aspose.3D for Java API。

首先，您需要在Maven `pom.xml`中指定Aspose存储库配置/位置，如下所示:

{{< highlight "java" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

然后在您的pom.xml中定义Aspose.3D for Java API依赖关系，如下所示:

{{< highlight "java" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>21.4</version>
    </dependency>

</dependencies>

{{< /highlight >}}

恭喜你!您已在Maven项目中成功定义了Aspose.3D for Java Maven依赖关系。
