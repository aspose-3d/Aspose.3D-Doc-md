---
title: Trabajando con la Marca de Agua
type: docs
weight: 160
url: /es/net/working-with-watermark/
---

{{% alert color="primary" %}}

Usando la API Aspose.3D para .NET, los desarrolladores pueden agregar fácilmente marcas de agua invisibles a archivos 3D mientras guardan en cualquier formato de archivo de salida compatible.

{{% /alert %}}
# **Crear una escena 3D**
Primero, necesita crear una escena 3D a partir de un archivo 3D. El siguiente fragmento de código muestra cómo usar esta funcionalidad:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string file = "template.3ds";
Scene scene = Scene.FromFile(file);
{{< /highlight >}}

# **Codificar Marca de Agua**
Aspose.3D para .NET agrega información de texto de la marca de agua y contraseña de la marca de agua a los archivos 3D a través del método ``EncodeWatermark``. El siguiente fragmento de código muestra cómo usar esta funcionalidad:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
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
{{< /highlight >}}

# **Guardar Documento**
Puede guardar en cualquier formato de archivo 3D que desee. El siguiente fragmento de código muestra cómo usar esta funcionalidad:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string output = "output.fbx";
scene.Save(output, FileFormat.FBX7400ASCII);
{{< /highlight >}}