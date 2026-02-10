---
title: Работа с Verify Watermark
type: docs
weight: 170
url: /ru/net/working-with-verify-watermark/
---

{{% alert color="primary" %}}

Используя API Aspose.3D для .NET, разработчики могут легко добавить проверку водяных знаков в 3D-файлы при сохранении в любой поддерживаемый формат выходного файла.

{{% /alert %}}
# **Создание 3D-сцены**
Сначала вам нужно создать 3D-сцену из 3D-файла. Следующий фрагмент кода показывает, как использовать эту функциональность:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string file = "template.3ds";
Scene scene = Scene.FromFile(file);
{{< /highlight >}}

# **Декодирование водяного знака**
Aspose.3D для .NET использует метод `DecodeWatermark` для подтверждения водяного знака для 3D-файла после ввода пароля. Следующий фрагмент кода показывает, как использовать эту функциональность:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string text = null;
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
{{< /highlight >}}

# **Подтверждение документа**
Для возвращенного результата, если возвращенный результат равен null, это означает, что к 3D-документу не добавлен водяной знак. Если он возвращает текстовую информацию, это водяной знак 3D-файла. Если пароль введен неправильно, будет возвращено сообщение об ошибке.