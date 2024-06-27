---
title: Installation
type: docs
weight: 50
url: /ar/java/installation/
description: Aspose hosts all Java APIs on Aspose Repository. You can easily use Aspose.3D for Java API directly in your Maven projects with simple configurations.
---
##  **تثبيت Aspose.3D for Java من مستودع Aspose**
Aspose hosts all Java APIs on [Aspose Repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). You can easily use Aspose.3D for Java API directly in your Maven projects with simple configurations.

أولاً تحتاج إلى تحديد تكوين/موقع مستودع Aspose في Maven `pom.xml` على النحو التالي:

{{< highlight "xml" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

ثم حدد اعتماد Aspose.3D for Java API في حسابك pom.xml على النحو التالي:

{{< highlight "xml" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>23.11.0</version>
    </dependency>

</dependencies>

{{< /highlight >}}


إذا كنت تستخدم our ، فيمكنك استخدام الإصدار على النحو التالي:

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

تهانينا! لقد نجحت في تحديد اعتماد Aspose.3D for Java Maven في مشروع Maven الخاص بك.
