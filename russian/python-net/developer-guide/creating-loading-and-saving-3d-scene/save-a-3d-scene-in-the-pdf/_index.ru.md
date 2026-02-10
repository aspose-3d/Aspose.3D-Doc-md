---
title: Сохраните сцену 3D в PDF
type: docs
weight: 60
url: /ru/python-net/save-a-3d-scene-in-the-pdf/
description: Класс Сцена Aspose.3D API представляет собой сцену 3D. Разработчики могут построить сцену 3D, добавив камеру, свет, многоугольники и различные другие объекты. Теперь они также могут сохранить сцену 3D в формате PDF.
---
{{% alert color="primary" %}} 

Класс [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) из Aspose.3D API представляет сцену 3D. Разработчики могут построить сцену 3D, добавив камеру, свет, многоугольники и различные другие объекты. Теперь они также могут сохранить сцену 3D в формате PDF.

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for Python via .NET напрямую записывает информацию о API и номере версии в выходных документах. Например, при рендеринге чертежа в PDF Aspose.3D for Python via .NET заполняет поле `Application` значением 'Aspose.3D' и `PDF Producer` поля со значением e.g 'Aspose.3D 17,9'.

Обратите внимание, что вы не можете указать Aspose. Диаграмма для Python via .NET API изменить или удалить эту информацию из выходных документов.

{{% /alert %}} 
##  **Создать 3D PDF с цилиндром и отобразить в режиме затененной иллюстрации с оптимизированным освещением CAD**
Метод Save класса `Scene` позволяет сохранить сцену 3D в формате PDF. Разработчики могут загрузить любой поддерживаемый 3D файл или построить новую 3D сцену, они могут сохранить 3D сцену в формате PDF, как показано в этом примере кода:

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Cylinder
from aspose.threed.shading import PhongMaterial
from aspose.threed.formats import PdfSaveOptions, PdfLightingScheme, PdfRenderMode
# Create a new scene
scene = Scene()
# Create a cylinder child node
cylinder = scene.root_node.create_child_node("cylinder", Cylinder())
cylinder.material = PhongMaterial()
# Set rendering mode and lighting scheme
opt = PdfSaveOptions()
opt.lighting_scheme = PdfLightingScheme.CAD
opt.render_mode = PdfRenderMode.SHADED_ILLUSTRATION
# Save in the PDF format
scene.save("output_out.pdf", opt)

{{< /highlight >}}
