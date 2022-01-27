---
title: Working with Watermark
type: docs
weight: 160
url: /net/working-with-watermark/
---

{{% alert color="primary" %}} 

Using the Aspose.3D for .NET API, developers can easily add blind watermarks to 3D files while saving in any supported output file format.

{{% /alert %}} 
# **Create a 3D Scene**
First you need to create a 3d scene from a 3d file.The following code snippet shows how to use this functionality:
```cs
string file = "template.3ds";
Scene scene = new Scene(file);
```

# **Encode Watermark**
Aspose.3D for .NET adds watermark text information and watermark password to 3d files through the EncodeWatermark method. The following code snippet shows how to use this functionality:
```cs
var numMeshes = 0;
scene.RootNode.Accept((Node node) =>
{
    var mesh = node.GetEntity<Mesh>();
    if (mesh != null)
    {
        numMeshes++;
        mesh = Watermark.EncodeWatermark(mesh, "HelloWorld", "1234");
        if (mesh != null)
        {
            node.Entity = mesh;
        }
    }
    return true;
});
```

# **Save Document**
You can save to any 3d file format you want.The following code snippet shows how to use this functionality:
```cs
string output =System.IO.Path.GetTempPath() + Guid.NewGuid().ToString() + ".fbx";
scene.Save(output, FileFormat.FBX7400ASCII);
```