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

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
private void InitRenderer()
{
    // Create a default camera, because it's required during the viewport's creation.
    camera = new Camera();
    Scene.RootNode.CreateChildNode("camera", camera);
    // Create the renderer and render window from window's native handle
    renderer = Renderer.CreateRenderer();
    // Right now we only support native window handle from Microsoft Windows
    // We'll support more platform on user's demand.
    window = renderer.RenderFactory.CreateRenderWindow(new RenderParameters(), Handle);
    // Create 4 viewports, the viewport's area is meanless here because we'll change it to the right area in the SetViewports later
    viewports = new[]
    {
        window.CreateViewport(camera, Color.Gray, RelativeRectangle.FromScale(0, 0, 1, 1)),
        window.CreateViewport(camera, Color.Gray, RelativeRectangle.FromScale(0, 0, 1, 1)),
        window.CreateViewport(camera, Color.Gray, RelativeRectangle.FromScale(0, 0, 1, 1)),
        window.CreateViewport(camera, Color.Gray, RelativeRectangle.FromScale(0, 0, 1, 1))
    };
    SetViewports(1);


    //initialize shader for grid

    GLSLSource src = new GLSLSource();
    src.VertexShader = @"#version 330 core
    layout (location = 0) in vec3 position;
    uniform mat4 matWorldViewProj;
    void main()
    {
        gl_Position = matWorldViewProj * vec4(position, 1.0f);
    }";
                src.FragmentShader = @"#version 330 core
    out vec4 color;
    void main()
    {
        color = vec4(1, 1, 1, 1);
    }";
    // Define the input format used by GLSL vertex shader the format is struct ControlPoint { FVector3 Position;}
    VertexDeclaration fd = new VertexDeclaration();
    fd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Position);
    // Compile shader from GLSL source code and specify the vertex input format
    gridShader = renderer.RenderFactory.CreateShaderProgram(src, fd);
    // Connect GLSL uniform to renderer's internal variable
    gridShader.Variables = new ShaderVariable[]
    {
        new ShaderVariable("matWorldViewProj", VariableSemantic.MatrixWorldViewProj)
    };

    SceneUpdated("");
}

{{< /highlight >}}
###  **Образец программирования для состояния буфера и Рендера**
Этот пример кода инициализирует буфер и состояние рендеринга для сетки.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
class Grid : ManualEntity
{
    public Grid(Renderer renderer, ShaderProgram shader)
    {
        // Render state for grid
        RenderState = renderer.RenderFactory.CreateRenderState();
        RenderState.DepthTest = true;
        RenderState.DepthMask = true;
        this.Shader = shader;
        // Define the format of the control point to render the line
        VertexDeclaration vd = new VertexDeclaration();
        vd.AddField(VertexFieldDataType.FVector3, VertexFieldSemantic.Position);
        // and create a vertex buffer for storing this kind of data
        this.VertexBuffer = renderer.RenderFactory.CreateVertexBuffer(vd);
        // Draw the primitive as lines
        this.DrawOperation = DrawOperation.Lines;
        this.RenderGroup = RenderQueueGroupId.Geometries;

        List<FVector3> lines = new List<FVector3>();
        for (int i = -10; i <= 10; i++)
        {
            // Draw - line
            lines.Add(new FVector3(i, 0, -10));
            lines.Add(new FVector3(i,0, 10));


            // Draw | line
            lines.Add(new FVector3(-10, 0, i));
            lines.Add(new FVector3(10, 0, i));
        }
        // Put it to vertex buffer
        VertexBuffer.LoadData(lines.ToArray());
    }
}

{{< /highlight >}}
