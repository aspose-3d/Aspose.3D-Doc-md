---
title: Load text 3D files with custom encoding
type: docs
weight: 10
url: /net/load-text-3d-files-with-custom-encoding
description: Using Aspose.3D for .NET, developers can customize the text encoding for text-based 3D files.
---

{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), Sometimes, text-based 3D files exported by specialized tools may contain special characters that cannot be decoded using UTF-8. Aspose.3D provides a robust solution to handle such encoding issues, ensuring seamless import and processing of these files.

{{% /alert %}}



Here's how you can resolve this in Aspose.3D:

{{% highlight csharp %}}

var scene = Scene.FromFile(path, new ObjLoadOptions()
{
    Encoding = Encoding.GetEncoding("GBK")
});

{{% /highlight %}}

In this example:

1.   Create LoadOptions with Specific Encoding: A LoadOptions object is created, and the encoding is set to handle special characters (e.g., GBK).
1.   Load the 3D File: The 3D file containing special characters is loaded using the specified encoding.

By specifying the appropriate encoding during the loading process, Aspose.3D allows developers to manage and work with text-based 3D files containing special characters, thus overcoming potential issues with character decoding in UTF-8.
