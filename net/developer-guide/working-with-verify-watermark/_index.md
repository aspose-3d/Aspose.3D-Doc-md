---
title: Working with Verify Watermark
type: docs
weight: 170
url: /net/working-with-verify-watermark/
---

{{% alert color="primary" %}} 

Using the Aspose.3D for .NET API, developers can easily add blind watermarks verification to 3D files while saving in any supported output file format.

{{% /alert %}} 
# **Create a 3D Scene**
First you need to create a 3d scene from a 3d file.The following code snippet shows how to use this functionality:
```cs
string file = "template.3ds";
Scene scene = new Scene(file);
```

# **Decode Watermark**
Aspose.3D for .NET uses the DecodeWatermark method to confirm the watermark for the 3d file after filling in the password.The following code snippet shows how to use this functionality:
```cs
string text =null;
try
{
    scene.RootNode.Accept((Node node) =>
    {
        var mesh = node.GetEntity<Mesh>();
        if (mesh != null)
        {
            text = Watermark.DecodeWatermark(mesh, "1234");
            if (text != null)
                return false;
        }
        return true;
    });
}
catch (UnauthorizedAccessException)
{
    return "Password error";
}
return text;
```

# **Document Confirmation**
For the returned result, if the returned result is null, it means that there is no watermark added to the 3d document. If it returns text information, it is the watermark of the 3d file. If the password is entered incorrectly, an error message will be returned.