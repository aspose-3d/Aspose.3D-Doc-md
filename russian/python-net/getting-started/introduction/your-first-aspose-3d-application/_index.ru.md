---
title: Ваше первое приложение Aspose.3D
type: docs
weight: 30
url: /ru/python-net/your-first-aspose-3d-application/
---

{{% alert color="primary" %}}

Этот учебник объясняет, как создать ваше первое приложение с использованием простого API Aspose.3D. Это простое приложение создает 3D-файл в указанной 3D-сцене.

{{% /alert %}}

## **Как создать приложение**

Следующие шаги позволяют создать приложение с использованием API Aspose.3D:

1. Создайте экземпляр класса [Scene](https://reference.aspose.com/3d/ru/python-net/aspose.threed/scene/).
1. Если у вас есть лицензия, то [примените ее](/3d/ru/python-net/licensing/).  
   Если вы используете ознакомительную версию, пропустите строки кода, связанные с лицензией.
1. Создайте новый 3D-файл или откройте существующий 3D-файл.
1. Получите доступ к содержимому сцены в 3D-файле.
1. Сформируйте измененный 3D-файл.

Реализация вышеуказанных шагов демонстрируется в примерах ниже.

### **Как создать новый документ сцены**

В следующем примере создается новый файл 3D-сцены с нуля. Сначала создается 3D-сцена, а затем файл сохраняется в формате FBX.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# The path to the documents directory.
# Create an object of the Scene class
scene = a3d.Scene()
# Save 3D scene document
scene.Save("document.fbx", a3d.FileFormat.FBX7500ASCII)

{{< /highlight >}}

### **Как открыть существующий файл**

В следующем примере открывается существующий 3D-файл шаблона с именем "document.fbx".

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# The path to the documents directory.

# Initialize a Scene class object
scene = Scene()
# Load an existing 3D document
scene.open("document.fbx")


{{< /highlight >}}
