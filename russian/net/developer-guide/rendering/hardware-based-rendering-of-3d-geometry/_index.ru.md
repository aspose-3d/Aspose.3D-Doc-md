---
title: Аппаратный рендеринг геометрии 3D
type: docs
weight: 30
url: /ru/net/hardware-based-rendering-of-3d-geometry/
description: Используя Aspose.3D for .NET API, разработчики могут программировать GPU (графический процессор) и настраивать графическое оборудование для рендеринга геометрии 3D вместо фиксированного конвейера функций.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, разработчики могут программировать GPU (графический процессор) и настраивать графическое оборудование для рендеринга геометрии 3D вместо фиксированного конвейера функций. В этой статье мы сосредоточимся на аппаратном рендеринге с использованием [OpenGL 4,0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx) и [Вулкан](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
##  **Создание оборудования и рендеринг геометрии 3D**
Для рендеринга геометрии 3D требуются шейдер, буферы и состояние рендеринга. Никто из них не может работать друг без друга.

- **Буферы**-Треугольные списки-это отдельные треугольники, указанные в массиве, который иногда называют буфером. В списке треугольников каждый треугольник указан индивидуально. Точки треугольника можно совместно использовать с помощью индексов для уменьшения объема данных, которые необходимо передать графическому оборудованию.
- **Шейдеры**-Он определяет, как преобразовать треугольники из мирового пространства в пространство экрана и рассчитать окончательный цвет пикселя на стороне GPU
- **Государства-члены**-Он предоставляет параметры для GPU для растеризации треугольников в пиксели.

{{% alert color="primary" %}}

Мы подготовили демо-проект. См. [Этот URL-адрес загрузки](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

Язык затенения OpenGL (GLSL) является стандартным языком затенения высокого уровня для графики OpenGL API. Метод `InitRenderer` в файле `AssetBrowser/Controls/RenderView.cs` в демонстрационном приложении (имя: AssetBrowser) демонстрирует простое использование GLSL с помощью Aspose.3D API. Обычно используются три типа шейдеров: шейдеры вершин, шейдеры фрагмента и шейдеры геометрии.

Класс [`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) сообщает рендеру, что исходный код предназначен для языка затенения OpenGL, он может быть скомпилирован в класс [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram). Класс [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) определяет переменные, используемые в шейдере. Класс `VariableSemantic` используется для определения семантики переменной шейдера, Aspose.3D рендерер автоматически подготовит значения переменной шейдера в зависимости от семантики.
###  **Образец программирования для Shader**
Этот пример кода инициализирует рендерер и шейдер для сетки. Вы можете скачать полный рабочий проект этого примера из [Здесь](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "HardwareBasedRendering-Controls-RenderView-RenderView.cs" >}}
###  **Образец программирования для состояния буфера и Рендера**
Этот пример кода инициализирует буфер и состояние рендеринга для сетки.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "HardwareBasedRendering-Grid-ManualEntity.cs" >}}
