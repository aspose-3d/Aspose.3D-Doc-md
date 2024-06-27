---
title: Настройка системы осей для формата obj
linktitle: Настройка системы осей при экспорте сцены в формат OBJ
type: docs
weight: 70
url: /ru/net/customize-axis-system-for-obj-format
description: OBJ не имеют системы координат по умолчанию, мы можем вручную определить систему осей для нее.
---
{{% alert color="primary" %}} 

Файлы Wavefront OBJ не придерживаются стандартной системы координат; вместо этого интерпретация обычно обрабатывается импортером. Однако [Aspose.3D for .NET](https://products.aspose.com/3d/net/) предоставляет возможность вручную указать систему осей для файлов OBJ. Это включает в себя определение передней и передней осей, а также выбор между левой и правой системами координат. Aspose.3D автоматически обрабатывает преобразование системы координат, обеспечивая согласованность и точность ваших моделей 3D.


{{% /alert %}} 
##  **Указание системы осей для файлов OBJ в Aspose.3D**

Вот как вы можете вручную настроить систему осей при работе с файлами OBJ в Aspose.3D:

{{< highlight "csharp" >}}
//construct a right-handed axis system with +y as up and -z as front
Axis up = Axis.YAxis;
Axis front = Axis.NegativeZAxis;
AxisSystem axisSystem = new AxisSystem(CoordinateSystem.RightHanded, up, front);

ObjSaveOptions opt = new ObjSaveOptions();
//use the custom axis system to flip coordinate
opt.AxisSystem = axisSystem;
//set this to true, will convert mesh's position/normal from source axis system to custom axis system
//source axis system is defined by scene.AssetInfo.CoordinateSystem, scene.AssetInfo.UpVector, scene.AssetInfo.FrontVector
opt.FlipCoordinateSystem = true;

 // initialize a new 3D scene from existing file

var scene = Scene.FromFile("input.dae");

// Save the scene with customized axis system
s.Save("output.obj", opt);

{{< /highlight >}}

Используя системную конфигурацию оси Aspose.3D для файлов OBJ, можно добиться согласованных и точных результатов импорта независимо от исходной системы координат, используемой в файле OBJ. Эта функция повышает гибкость и контроль, упрощая интеграцию и работу с файлами OBJ в различных рабочих потоках 3D.

##  **Ресурсы**

1. [Онлайн учебник](https://products.aspose.com/3d/tutorial/)
2. [Аксис Систем](https://reference.aspose.com/3d/net/aspose.threed/axissystem/)