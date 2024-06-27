---
title: 如何在Docker中运行 Aspose.3D for Java
type: docs
description: 在适用于Linux的Docker容器中运行 Aspose.3D for Java。
weight: 139
url: /zh/java/how-to-run-aspose-3d-in-docker/
---
微服务与容器化相结合，可以轻松地组合技术。Docker允许您轻松地将 Aspose.3D 功能集成到您的应用程序中，而不管您的开发堆栈中有什么技术。

如果您的目标是微服务，或者您的堆栈中的主要技术不是 .NET 、 C++ 或 Java，但您需要 Aspose.3D 功能，或者您已经在堆栈中使用了Docker，然后，您可能有兴趣在Docker容器中使用 Aspose.3D for Java。

## 先决条件

- Docker必须安装在您的系统上。

## 创建 Java 应用程序

在此示例中，您创建了一个 Java 应用程序，该应用程序生成一个简单的3d文件，保存并读取该文件。然后可以在Docker中建立和运行应用程序。

### 正在创建 Java 应用程序

使用以下代码在Eclipse中创建一个 Java 应用程序。在此示例中，我们使用 Aspose.3D for Java 在3d场景中创建一个平面，并设置向量，然后将其保存为obj格式。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-scene-ChangePlaneOrientation-ChangePlaneOrientation.java" >}}

### 将 Java 应用做成jar包

下图显示了在Eclipse中使用 “导出” 菜单制作jar包的方法。

**![使用eclipse制作Jar] (makejar.png)**

现在我们使用 Aspose.3D for Java 编写了一个 Java 程序，我们得到了一个jar包。接下来，我们将创建一个dockerfile。

### 配置Dockerfile

下一步是创建和配置Dockerfile。

1. 创建Dockerfile并将其放在jar包旁边。保留此文件名，不带扩展名 (默认)。
2.在Dockerfile中，指定:

{{< highlight "plain" >}}
   FROM williamyeh/java8:latest

   VOLUME /tmp

   ADD TestDocker.jar app.jar

   ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
{{< /highlight >}}

### 在Docker中构建和运行应用程序

现在可以在Docker中建立和运行应用程序。打开您喜欢的命令提示符，将目录更改为包含Dockerfile的文件夹，然后运行以下命令:

{{< highlight "plain" >}}
docker build -t java-app .
{{< /highlight >}}

执行上述命令后，您将获得 3D 文件的输出。此时，一个 Java 程序已在Linux Docker中成功运行。
