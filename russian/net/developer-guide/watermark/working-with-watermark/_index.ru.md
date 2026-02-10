---
title: Работа с водяными знаками
type: docs
weight: 160
url: /ru/net/working-with-watermark/
---

{{% alert color="primary" %}} 

С помощью API Aspose.3D для .NET разработчики могут легко добавлять невидимые водяные знаки к 3D-файлам при сохранении в любой поддерживаемый формат выходного файла.

{{% /alert %}} 
# **Создание 3D-сцены**
Сначала вам нужно создать 3D-сцену из 3D-файла. Следующий фрагмент кода показывает, как использовать эту функциональность:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string file = "template.3ds";
Scene scene = Scene.FromFile(file);
{{< /highlight >}}

# **Кодирование водяного знака**
Aspose.3D для .NET добавляет информацию о водяном знаке и пароль водяного знака в 3D-файлы с помощью метода ``EncodeWatermark``. Следующий фрагмент кода показывает, как использовать эту функциональность:

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

# **Сохранение документа**
Вы можете сохранить в любой 3D-формат файла, который вам нужен. Следующий фрагмент кода показывает, как использовать эту функциональность:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string output = "output.fbx";
scene.Save(output, FileFormat.FBX7400ASCII);
{{< /highlight >}}